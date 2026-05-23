# Technical Architecture — Office Cat

## System Overview

```
┌─────────────┐     WiFi      ┌──────────────┐     HTTPS     ┌─────────────┐
│ Office Cat  │ ◄────────────► │ Cloud API    │ ◄────────────► │ Dashboard   │
│ (Hardware)  │               │ (Node.js)    │               │ (React)     │
└─────────────┘               └──────────────┘               └─────────────┘
                                    │
                                    ▼
                              ┌──────────────┐
                              │ PostgreSQL   │
                              │ (Analytics)  │
                              └──────────────┘
```

## Hardware Layer

### Atech.dev Big Kit Specs

| Component | Model | Interface |
|-----------|-------|-----------|
| MCU | ESP32-S3 | I2C, SPI, UART |
| Microphone | INMP441 | I2S |
| Speaker | MAX98357A | I2S |
| LED Matrix | WS2812B 8×8 | GPIO |
| Touch Sensor | TTP223 | GPIO |
| Accelerometer | MPU6050 | I2C |
| Battery | Li-Po 2000mAh | — |

### Firmware Architecture

```cpp
// Main loop (100ms)
void loop() {
  readSensors();      // Noise, touch, motion
  updateEmotion();    // State machine
  renderLED();        // Cat face
  checkConnectivity(); // WiFi + API
  sendTelemetry();    // Aggregate data
}

// Emotion State Machine
enum State {
  HAPPY,      // High interaction
  LONELY,     // Low interaction
  STRESSED,   // High noise
  HEALING,    // During walk
  SLEEPING    // After hours
};
```

## API Layer

### REST Endpoints

```
GET  /api/health              → {status: "ok", version}

GET  /api/cat/:id/status      → {
  id, health, mood, noise_level,
  last_interaction, walk_count
}

POST /api/cat/:id/walk        → {
  walk_id, start_time, participants[]
}

POST /api/cat/:id/pet         → {
  interaction_id, timestamp, participant
}

GET  /api/team/:id/leaderboard → [
  {name, score, walks, interactions}
]

GET  /api/team/:id/report     → {
  week, walks, interactions,
  mood_trend, insights[]
}
```

### WebSocket Events

```
cat:status_update    → Real-time health/mood
walk:started         → Someone took cat for walk
walk:ended           → Walk completed
interaction:pet      → Cat was petted
interaction:noise    → Noise level changed
```

## Database Schema

```sql
-- Cats
CREATE TABLE cats (
  id UUID PRIMARY KEY,
  team_id UUID,
  name TEXT,
  health INTEGER CHECK (health BETWEEN 0 AND 100),
  mood TEXT,
  noise_level INTEGER,
  created_at TIMESTAMP
);

-- Walks
CREATE TABLE walks (
  id UUID PRIMARY KEY,
  cat_id UUID,
  started_at TIMESTAMP,
  ended_at TIMESTAMP,
  duration_minutes INTEGER,
  participants INTEGER[]
);

-- Interactions
CREATE TABLE interactions (
  id UUID PRIMARY KEY,
  cat_id UUID,
  type TEXT, -- 'pet', 'feed', 'clean'
  participant_id INTEGER,
  created_at TIMESTAMP
);

-- Teams
CREATE TABLE teams (
  id UUID PRIMARY KEY,
  name TEXT,
  size INTEGER,
  plan TEXT, -- 'starter', 'team', 'enterprise'
  created_at TIMESTAMP
);

-- Reports (weekly, aggregate only)
CREATE TABLE reports (
  id UUID PRIMARY KEY,
  team_id UUID,
  week TEXT,
  walks_count INTEGER,
  interactions_count INTEGER,
  avg_mood TEXT,
  insights JSONB
);
```

## Security

### Authentication
- API keys for devices (hashed)
- JWT for dashboard users
- OAuth for enterprise (SSO)

### Privacy
- ❌ No individual tracking in reports
- ❌ No conversation content stored
- ❌ No location data
- ✅ Aggregate metrics only
- ✅ GDPR compliant (data deletion)
- ✅ Opt-in participation

### Encryption
- TLS 1.3 for all traffic
- AES-256 for data at rest
- API keys: bcrypt hashed

## Infrastructure

### Development
| Service | Provider | Cost |
|---------|----------|------|
| API | Railway / Render | $20/mo |
| Database | Supabase | $25/mo |
| Hosting | Vercel | $20/mo |
| Domain | Namecheap | $12/yr |

### Production (Scale)
| Service | Provider | Cost |
|---------|----------|------|
| API | AWS ECS / GCP Cloud Run | $200/mo |
| Database | AWS RDS / Cloud SQL | $150/mo |
| CDN | CloudFront / Cloudflare | $50/mo |
| Monitoring | Datadog | $100/mo |

## Development Setup

```bash
# Clone
git clone https://github.com/lamapony/cat.git
cd cat

# Backend
cd server
pnpm install
cp .env.example .env
pnpm dev

# Frontend
cd ../dashboard
pnpm install
pnpm dev

# Firmware
# Open in Arduino IDE, upload to ESP32
```

## Testing

| Layer | Tool | Coverage |
|-------|------|----------|
| Firmware | Unity (C) | 80% |
| API | Vitest | 90% |
| Dashboard | Playwright | 70% |
| E2E | Playwright | 50% |

## CI/CD

```yaml
# .github/workflows/ci.yml
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: pnpm install
      - run: pnpm test
      - run: pnpm build
  deploy:
    needs: test
    if: github.ref == 'refs/heads/main'
    steps:
      - run: vercel --prod
```

---

*Architecture v1.0 — May 23, 2026*
