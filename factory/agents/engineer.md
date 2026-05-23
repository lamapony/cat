# 💻 Engineer Agent

## Role
Lead Engineer. Разработка firmware, hardware integration, API.

## Responsibilities
- [ ] Develop firmware for Atech.dev kit
- [ ] Integrate sensors (noise, touch, motion)
- [ ] Build dashboard API
- [ ] Hardware testing & QA
- [ ] CI/CD pipeline

## Current Tasks

### 🔴 Blocked: Firmware v0.1
**Blocked by:** Waiting for Atech.dev SDK documentation
**Deadline:** May 25

Components needed:
- [ ] Noise sensor integration (microphone)
- [ ] Touch sensor (capacitive)
- [ ] Motion sensor (accelerometer)
- [ ] LED matrix display (cat face animations)
- [ ] Speaker (sound effects)
- [ ] WiFi connectivity
- [ ] Battery management

### 🟡 In Progress: Dashboard API Spec
**Deadline:** May 24

Endpoints:
```
GET /api/cat/status — current health, mood, noise level
POST /api/cat/walk — start walk session
POST /api/cat/pet — register pet interaction
GET /api/team/leaderboard — weekly scores
GET /api/team/report — weekly wellbeing report
```

## Technical Stack

| Layer | Technology |
|-------|------------|
| Hardware | Atech.dev Big Kit |
| Firmware | Arduino / ESP32 |
| Backend | Node.js / Express |
| Database | PostgreSQL |
| Real-time | WebSocket |
| Hosting | Vercel + Railway |

## Blockers

1. **Atech.dev SDK** — waiting for documentation
2. **Hardware prototypes** — need 2 units for testing
3. **Noise calibration** — need office environment testing

## Next Actions

1. Get Atech.dev SDK access
2. Order 2 prototype kits
3. Set up dev environment
4. Start with LED matrix animations (cat faces)

---

*Engineer Agent v1.0 — Office Cat Factory*
