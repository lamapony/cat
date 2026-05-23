# RoboCat — Product Requirements Document

## Document Information

| Field | Value |
|-------|-------|
| **Product Name** | RoboCat |
| **Version** | 1.0 MVP |
| **Status** | Hackathon / Proof of Concept |
| **Date** | 2026-05-23 |
| **Author** | Labdo Products |
| **Classification** | Internal — Commercial in Confidence |
| **Prompt Version** | 1.0 (AI-Ready) |
| **Prompt Target** | LLM Code Generation / Design / Content |

---

## 1. Executive Summary

### 1.1 Product Vision
RoboCat is an ambient emotional intelligence device for physical workspaces. It transforms environmental stressors (acoustic noise, social isolation) into actionable emotional feedback loops, creating measurable improvements in workplace wellbeing and social cohesion.

### 1.2 Value Proposition
**For Workspace Operators:** Differentiation in a commoditized coworking market through proprietary emotional intelligence infrastructure. First-mover advantage in ambient workplace robotics.

**For End Users:** Passive stress reduction through biofeedback-style environmental awareness. Active social bonding through asynchronous voice messaging without digital friction.

### 1.3 Target Market Segment
- **Primary:** Coworking spaces, serviced offices, creative studios (B2B)
- **Secondary:** Open-plan corporate offices, startup hubs (Enterprise B2B)
- **Tertiary:** Educational institutions, healthcare waiting areas (Public sector)

### 1.4 Business Model
- **Revenue Stream:** Hardware sales with one-time purchase
- **Pricing Strategy:** Cost-plus 20% margin at pilot scale; target 40% margin at 500+ unit volume
- **Unit Economics:** 400 DKK COGS → 500 DKK MSRP (pilot); 280 DKK COGS → 500 DKK MSRP (scale)
- **Go-to-Market:** Direct sales to workspace operators; channel partnerships with facility management firms

---

## 2. Market Analysis

### 2.1 Total Addressable Market (TAM)
**Nordic coworking market:** 2,500+ active coworking spaces (2025 data)
- Denmark: ~400 spaces
- Sweden: ~800 spaces
- Norway: ~500 spaces
- Finland: ~450 spaces
- Iceland: ~100 spaces

**TAM at 500 DKK/unit:** 1,250,000 DKK (~167,000 EUR)

### 2.2 Serviceable Addressable Market (SAM)
Spaces with 50+ desks, premium positioning, wellness-focused branding:
- Denmark: ~120 spaces
- Nordics: ~600 spaces

**SAM:** 300,000 DKK (~40,000 EUR)

### 2.3 Serviceable Obtainable Market (SOM)
Year 1 target: 50 units across Copenhagen + Aarhus
**SOM:** 25,000 DKK (~3,350 EUR)

### 2.4 Competitive Landscape

| Competitor | Category | Approach | Weakness vs RoboCat |
|------------|----------|----------|---------------------|
| **Nokia/Withings** | Environmental sensors | Pure data, no emotion | No behavioral feedback loop |
| **Muse Headband** | Personal biofeedback | Individual only | Not ambient/shared |
| **Amazon Astro** | Office robot | Surveillance-focused | Privacy concerns, high cost |
| **Petcube** | Remote pet interaction | Home use, app-dependent | Not workplace-appropriate |
| **Moodbeam** | Mood tracking | Wearable, manual input | Requires user action |

**RoboCat Differentiation:** Only ambient, emotional, privacy-first device requiring zero user onboarding or app installation.

### 2.5 Market Trends
- **Wellness economy growth:** 9.9% CAGR (Global Wellness Institute)
- **Coworking differentiation crisis:** 73% of operators cite "commoditization" as top threat (Coworking Insights 2025)
- **Acoustic comfort standards:** ISO 3382-3 gaining traction in office design
- **Privacy-first tech:** Post-GDPR demand for local-processing devices

---

## 3. Product Definition

### 3.1 Product Classification
- **Category:** Ambient Workplace Robotics (AWR)
- **Subcategory:** Emotional Intelligence Interface (EII)
- **Form Factor:** Desktop ambient device
- **Interaction Model:** Zero-UI (touch + environmental sensing)
- **Processing Architecture:** Edge-only (no cloud dependency)

### 3.2 Core Value Drivers

| Priority | Value Driver | Metric | Target |
|----------|-------------|--------|--------|
| P0 | Noise awareness | Time above 70dB | -30% within 2 weeks |
| P0 | Stress relief | Self-reported stress | -20% (qualitative) |
| P1 | Social connection | Inter-coworker interactions | +25% voice gift usage |
| P1 | Space differentiation | Visitor memorability | "Would recommend" +15% |
| P2 | Content virality | Social media mentions | 5+ organic posts/month |

### 3.3 User Personas

#### Persona A: The Workspace Operator (Buyer)
- **Name:** Lena, Office Manager
- **Age:** 34
- **Role:** Facilities & Experience Manager at 150-desk coworking space
- **Pain Points:** Member churn, noise complaints, inability to differentiate from competitors
- **Success Metrics:** Retention rate, NPS, occupancy rate
- **Buying Criteria:** ROI within 6 months, minimal maintenance, visible impact

#### Persona B: The Stressed Developer (End User)
- **Name:** Jakob
- **Age:** 28
- **Role:** Full-stack developer, hot-desking 3x/week
- **Pain Points:** Open office noise, lack of personal space, superficial colleague relationships
- **Success Metrics:** Ability to focus, feeling of belonging, casual social connections
- **Usage Pattern:** Passive ambient presence; occasional voice gift exchange

#### Persona C: The Community Manager (Champion)
- **Name:** Maria
- **Age:** 31
- **Role:** Community Manager, responsible for member engagement
- **Pain Points:** Organizing events is time-consuming; organic community building is hard
- **Success Metrics:** Member engagement scores, event attendance, community sentiment
- **Usage Pattern:** Active promoter; uses RoboCat as conversation starter

### 3.4 User Stories

#### US-001: Noise Awareness
> As a coworking member, I want the environment to gently signal when it's too loud, so that I and others naturally moderate our volume without confrontation.

**Acceptance Criteria:**
- Device detects sustained noise >70dB for >5 seconds
- Visual indicator (LED + screen) transitions to "stressed" state within 2 seconds
- No audible alarm — purely emotional/visual signal
- State persists until noise drops below 60dB for >10 seconds

#### US-002: Stress Relief
> As a stressed worker, I want to physically interact with a responsive object, so that I get immediate tactile and auditory feedback that reduces my anxiety.

**Acceptance Criteria:**
- Capacitive touch detection on 3 zones (head, back, belly)
- Response latency <500ms from touch to audio/visual feedback
- Audio feedback: synthesized purring (20-50Hz fundamental)
- Visual feedback: warm amber glow, relaxed eye expression
- Interaction duration: minimum 2 seconds to trigger full response

#### US-003: Asynchronous Social Connection
> As a coworker, I want to leave a voice message for a colleague without scheduling or apps, so that we maintain human connection despite asynchronous schedules.

**Acceptance Criteria:**
- Voice recording triggered by 2-second hold on head sensor
- Recording duration: 3-10 seconds
- Storage: local only, FIFO buffer (max 5 messages)
- Playback triggered by any coworker's touch interaction
- Visual indication of pending message (slow pulse)
- Message auto-deletes after playback

#### US-004: Zero-Friction Deployment
> As a workspace operator, I want to place the device and have it work immediately, so that I don't need IT support, onboarding, or user training.

**Acceptance Criteria:**
- No app installation required
- No user accounts or registration
- No WiFi configuration for core functionality
- Battery-powered (8+ hours) with USB-C charging
- Operational within 30 seconds of power-on

---

## 4. Functional Requirements

### 4.1 System Architecture

```
┌─────────────────────────────────────────┐
│           RoboCat Device                │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐ │
│  │  Noise  │  │  Touch  │  │  Voice  │ │
│  │ Sensor  │  │ Sensors │  │  (Mic)  │ │
│  └────┬────┘  └────┬────┘  └────┬────┘ │
│       └─────────────┴─────────────┘    │
│                   │                      │
│            ┌──────┴──────┐               │
│            │   ESP32     │               │
│            │  Processor  │               │
│            │  (240MHz)   │               │
│            └──────┬──────┘               │
│       ┌───────────┼───────────┐        │
│  ┌────┴────┐ ┌────┴────┐ ┌────┴────┐   │
│  │  TFT   │  │ Speaker│  │  LEDs   │   │
│  │ Display│  │  (DAC) │  │ WS2812B│   │
│  └────────┘  └────────┘  └────────┘   │
└─────────────────────────────────────────┘
```

### 4.2 Hardware Specifications

| Component | Spec | Rationale |
|-----------|------|-----------|
| **MCU** | ESP32-WROOM-32 | Dual-core, WiFi/BT, ample GPIO, low cost |
| **Audio Input** | MAX9814 + MEMS mic | 60dB gain, AGC, low power |
| **Audio Output** | ESP32 DAC + 1W amp | Direct drive, no external codec |
| **Display** | ST7735 1.8" TFT 128×160 | Sufficient for eyes animation, SPI interface |
| **Touch** | TTP223 × 3 | Capacitive, low power, no calibration |
| **LEDs** | WS2812B × 8 | Addressable, rich color, single wire |
| **Battery** | 2000mAh Li-Po | 8h active, 48h standby |
| **Enclosure** | 3D printed PLA | 150×100×80mm, cat-like form factor |

### 4.3 Software Stack

| Layer | Technology | Purpose |
|-------|------------|---------|
| **Firmware** | MicroPython v1.22 | Rapid iteration, REPL debugging |
| **RTOS** | uasyncio | Cooperative multitasking for sensors + UI |
| **Audio** | Custom PWM + WAV playback | Purring synthesis, voice recording |
| **Display** | framebuf + ST7735 driver | Eye animations, state indicators |
| **LEDs** | neopixel | Mood lighting, state visualization |
| **Storage** | Internal flash (FIFO) | Voice message buffer |

### 4.4 Emotion State Machine

```
                    ┌─────────────┐
         ┌─────────│   HAPPY     │◄────────┐
         │         │  (default)  │         │
         │         └──────┬──────┘         │
         │                │                │
    noise ▼           touch ▼         no interaction
         │                │                │
    ┌────┴────┐    ┌────┴────┐      (10 min)
    │ STRESSED│    │ PLAYFUL │         │
    │  (>70dB)│    │(2-30sec)│         ▼
    └────┬────┘    └────┬────┘    ┌────┴────┐
         │              │         │  LONELY │
    noise ▼         time ▼         │ (>10min)│
   drops │         passes         └────┬────┘
         │         (30sec)             │
         └────────────►◄─────────────┘
                          touch
```

### 4.5 Feature Priority Matrix

| Feature | Priority | Effort | Impact | Status |
|---------|----------|--------|--------|--------|
| Noise detection + Stressed state | P0 | Low | High | MVP |
| Touch response + Happy state | P0 | Low | High | MVP |
| Voice Gift (record/play) | P0 | Medium | High | MVP |
| LED ambient lighting | P1 | Low | Medium | MVP |
| TFT eye animations | P1 | Medium | Medium | MVP |
| Battery power management | P1 | Medium | Medium | Post-MVP |
| WiFi OTA updates | P2 | Medium | Low | Post-MVP |
| Mobile app (optional) | P3 | High | Low | Future |
| Cloud dashboard | P3 | High | Low | Future |

---

## 5. Non-Functional Requirements

### 5.1 Performance
- **Sensor polling rate:** 10Hz (100ms intervals)
- **Display refresh rate:** 30fps for animations
- **Audio latency:** <100ms (touch to sound output)
- **State transition latency:** <500ms (sensor trigger to full state change)
- **Boot time:** <5 seconds from power-on to operational

### 5.2 Reliability
- **MTBF:** >2,000 hours (target for production)
- **Battery life:** 8 hours active, 48 hours standby
- **Storage durability:** >100,000 write cycles (flash memory)
- **Environmental range:** 0-40°C, 20-80% humidity

### 5.3 Security & Privacy
- **Data residency:** 100% local processing, zero cloud transmission
- **Voice data:** Stored only in RAM + flash, no encryption required (no network)
- **Physical security:** No camera, no biometric sensors
- **GDPR compliance:** Not applicable (no personal data processing)

### 5.4 Accessibility
- **Visual:** High contrast display, color-blind friendly state indicators (shape + color)
- **Auditory:** Visual alternatives for all audio feedback
- **Motor:** No fine motor skills required (large touch zones)
- **Cognitive:** Zero learning curve, intuitive emotional metaphors

### 5.5 Regulatory
- **CE marking:** Required for EU sale (EMC, LVD, RoHS)
- **Radio:** WiFi module pre-certified (ESP32)
- **Battery:** UN38.3 for shipping (Li-Po)

---

## 6. Go-to-Market Strategy

### 6.1 Phase 1: Hackathon Proof (May 2026)
- **Objective:** Validate concept, secure first customer
- **Target:** The Union Workspaces (pilot customer)
- **Deliverable:** 1 working prototype + pitch deck
- **Success Metric:** Letter of intent or purchase order

### 6.2 Phase 2: Copenhagen Pilot (Jun-Aug 2026)
- **Objective:** Deploy 6-12 units, gather qualitative feedback
- **Target:** 3 coworking spaces in Copenhagen
- **Deliverable:** Refined hardware + firmware v1.1
- **Success Metric:** NPS >50, 80% daily interaction rate

### 6.3 Phase 3: Nordic Expansion (Sep-Dec 2026)
- **Objective:** Scale to 50+ units, establish channel partnerships
- **Target:** Denmark + Sweden coworking networks
- **Deliverable:** Production-ready hardware + packaging
- **Success Metric:** 50 units sold, 2 channel partners

### 6.4 Phase 4: Product-Market Fit (2027)
- **Objective:** Achieve sustainable unit economics
- **Target:** 300+ units, breakeven on COGS reduction
- **Deliverable:** Firmware v2.0 with community behaviors
- **Success Metric:** 40% gross margin, <5% return rate

### 6.5 Pricing Strategy

| Segment | Units | Price/Unit | Total | Terms |
|---------|-------|------------|-------|-------|
| Pilot (hackathon) | 6 | 500 DKK | 3,000 DKK | 50% upfront |
| Early adopter | 12 | 500 DKK | 6,000 DKK | Net 30 |
| Volume (50+) | 50 | 450 DKK | 22,500 DKK | Net 30 |
| Channel (100+) | 100 | 400 DKK | 40,000 DKK | Net 60 |

---

## 7. Success Metrics & KPIs

### 7.1 Product Metrics

| Metric | Definition | Target | Measurement |
|--------|-----------|--------|-------------|
| **Interaction Rate** | % of workdays with >1 touch interaction | >70% | Device telemetry |
| **Noise Reduction** | % decrease in time above 70dB | >30% | Sensor logs |
| **Voice Gift Usage** | Messages sent per device per week | >3 | Device telemetry |
| **Uptime** | % of work hours device is operational | >95% | Heartbeat |
| **Battery Life** | Hours between charges | >8h | Power monitoring |

### 7.2 Business Metrics

| Metric | Definition | Target | Measurement |
|--------|-----------|--------|-------------|
| **CAC** | Customer acquisition cost | <200 DKK | Sales spend / customers |
| **LTV** | Lifetime value per customer | >2,000 DKK | Revenue × retention |
| **Gross Margin** | (Revenue - COGS) / Revenue | >35% | Financial tracking |
| **NPS** | Net Promoter Score | >50 | Quarterly survey |
| **Churn** | % customers not reordering | <10%/year | CRM data |

### 7.3 Hackathon Success Criteria

| Criteria | Weight | Target |
|----------|--------|--------|
| Working prototype | 30% | Device responds to noise + touch |
| Pitch quality | 25% | Clear value prop, compelling demo |
| Business viability | 25% | Identified customer + pricing |
| Technical feasibility | 20% | BOM defined, architecture sound |

---

## 8. Risk Assessment

### 8.1 Technical Risks

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| ESP32 audio quality insufficient | Medium | High | External codec fallback |
| Capacitive touch false triggers | Medium | Medium | Software debounce + threshold tuning |
| Battery life below target | Low | High | Power profiling + sleep modes |
| 3D print quality inconsistent | Medium | Medium | JLCPCB injection molding at scale |

### 8.2 Market Risks

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Coworking spaces see no value | Low | High | Pilot with The Union for validation |
| Privacy concerns (despite local-only) | Medium | Medium | Clear messaging, open source firmware |
| Competitor launches similar product | Medium | High | Speed to market, community moat |
| Price sensitivity at 500 DKK | Medium | Medium | Volume discounts, lease model option |

### 8.3 Operational Risks

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Supply chain delays (ESP32) | Low | Medium | Dual-source (Espressif + AI-Thinker) |
| Assembly quality issues | Medium | Medium | QC checklist, batch testing |
| Founder bandwidth constraints | High | High | Agent-based development (Paperclip) |

---

## 9. Appendix

### 9.1 Glossary

| Term | Definition |
|------|-----------|
| **AWR** | Ambient Workplace Robotics |
| **EII** | Emotional Intelligence Interface |
| **Voice Gift** | Asynchronous voice message left via device touch interaction |
| **Zero-UI** | Interaction model requiring no screen, app, or explicit interface |
| **Edge-only** | Processing entirely on-device, no cloud connectivity |

### 9.2 Reference Documents

- `PITCH.md` — Executive summary for investors/customers
- `ECONOMICS.md` — Detailed unit economics and financial projections
- `PROJECT.md` — Hackathon sprint plan and technical architecture
- `src/main.py` — MVP firmware source code
- `HACKATHON.md` — Quick reference for hackathon execution

### 9.3 Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-05-23 | Labdo Products | Initial PRD for The Boring Hackathon |

---

## 10. AI Prompt Engineering Toolkit

### 10.1 Document Purpose

This PRD is designed as a **self-contained prompt source** for AI agents and LLMs. Each section can be extracted, combined, or referenced to generate code, designs, marketing copy, or business analysis without additional context.

### 10.2 Prompt Patterns

#### Pattern A: Code Generation from Architecture

```
CONTEXT: You are an embedded systems developer.
TASK: Implement the firmware module described below.
CONSTRAINTS: MicroPython, ESP32, no external dependencies beyond standard library.

ARCHITECTURE:
{paste 4.1 System Architecture diagram}

HARDWARE:
{paste 4.2 Hardware Specifications table}

SOFTWARE STACK:
{paste 4.3 Software Stack table}

OUTPUT: Complete .py file with class structure, method stubs, and TODO comments for unimplemented logic.
```

#### Pattern B: Design Generation from Requirements

```
CONTEXT: You are a product designer creating a promotional landing page.
TASK: Design a single-page website for the product described below.
CONSTRAINTS: Dark theme (anthracite #1a1a1a, charcoal #2d2d2d, accent #f5a623), responsive, no external images.

PRODUCT:
{paste 1.1 Product Vision + 1.2 Value Proposition}

FEATURES:
{paste 3.4 User Stories (US-001 through US-004)}

TARGET AUDIENCE:
{paste 3.3 User Personas}

OUTPUT: Complete HTML/CSS/JS file with all sections, animations, and responsive breakpoints.
```

#### Pattern C: Marketing Copy from Value Props

```
CONTEXT: You are a copywriter for a B2B hardware startup.
TASK: Write {format} for the product described below.
TONE: Professional but warm, data-driven but emotional, Scandinavian minimalism.

VALUE PROPOSITION:
{paste 1.2 Value Proposition}

TARGET MARKET:
{paste 1.3 Target Market Segment}

KEY DIFFERENTIATORS:
{paste 2.4 Competitive Landscape}

OUTPUT: {specify format — e.g., "LinkedIn post", "email drip campaign", "pitch deck script", "product one-pager"}
```

#### Pattern D: Business Analysis from Metrics

```
CONTEXT: You are a business analyst evaluating a hardware startup.
TASK: Analyze the unit economics and provide recommendations.

UNIT ECONOMICS:
{paste 1.4 Business Model + 6.5 Pricing Strategy}

MARKET DATA:
{paste 2.1 TAM + 2.2 SAM + 2.3 SOM}

KPIs:
{paste 7.1 Product Metrics + 7.2 Business Metrics}

OUTPUT: SWOT analysis, 3 strategic recommendations, and a sensitivity analysis on pricing.
```

#### Pattern E: Risk Assessment from Register

```
CONTEXT: You are a technical program manager.
TASK: Create a mitigation plan for the risks identified below.

RISKS:
{paste 8.1 Technical Risks + 8.2 Market Risks + 8.3 Operational Risks}

CONSTRAINTS: Budget 50,000 DKK, timeline 6 months, team of 3 people.

OUTPUT: Prioritized risk matrix, mitigation actions with owners and deadlines, and contingency triggers.
```

### 10.3 Prompt Variables

| Variable | Source Section | Use Case |
|----------|---------------|----------|
| `{PRODUCT_VISION}` | 1.1 | Any generative task |
| `{VALUE_PROP_B2B}` | 1.2 (first paragraph) | Sales copy, pitch decks |
| `{VALUE_PROP_B2C}` | 1.2 (second paragraph) | User-facing content |
| `{TAM}` | 2.1 | Investor materials |
| `{PERSONA_OPERATOR}` | 3.3 (Persona A) | Buyer-focused content |
| `{PERSONA_DEVELOPER}` | 3.3 (Persona B) | End-user content |
| `{US_NOISE}` | US-001 | Feature documentation |
| `{US_TOUCH}` | US-002 | UX design briefs |
| `{US_VOICE}` | US-003 | Technical specs |
| `{US_ZERO}` | US-004 | Deployment guides |
| `{BOM}` | 4.2 | Procurement, manufacturing |
| `{STATE_MACHINE}` | 4.4 | Firmware implementation |
| `{KPI_INTERACTION}` | 7.1 (first row) | Dashboard metrics |
| `{PRICE_PILOT}` | 6.5 (first row) | Sales quotes |
| `{RISK_TECH}` | 8.1 | Project planning |
| `{RISK_MARKET}` | 8.2 | Strategy sessions |

### 10.4 Multi-Agent Prompt Chains

#### Chain 1: Full Product Build

```
AGENT_1 (Architect):
  INPUT: Sections 4.1, 4.2, 4.3, 4.4
  OUTPUT: Technical architecture document with component diagram

AGENT_2 (Developer):
  INPUT: AGENT_1 output + Sections 4.3, 4.4, 4.5
  OUTPUT: Complete firmware source code

AGENT_3 (Designer):
  INPUT: Sections 1.1, 1.2, 3.3, 3.4
  OUTPUT: Landing page HTML/CSS/JS

AGENT_4 (Copywriter):
  INPUT: Sections 1.2, 1.3, 2.4, 6.5
  OUTPUT: Marketing copy package (email, social, pitch)

AGENT_5 (Analyst):
  INPUT: Sections 2.1-2.3, 7.1-7.2, 8.1-8.3
  OUTPUT: Investor deck + risk mitigation plan
```

#### Chain 2: Hackathon Sprint

```
AGENT_1 (PM):
  INPUT: Sections 1.1, 3.4, 4.5
  OUTPUT: Prioritized task list with time estimates

AGENT_2 (Hardware):
  INPUT: Sections 4.2, 4.3, 8.1
  OUTPUT: Wiring diagram + component checklist

AGENT_3 (Software):
  INPUT: Sections 4.3, 4.4, US-001 to US-004
  OUTPUT: main.py with all sensor integrations

AGENT_4 (Business):
  INPUT: Sections 1.4, 6.5, 7.3
  OUTPUT: Pitch script + pricing sheet
```

### 10.5 Context Window Optimization

For LLMs with limited context windows, use these compressed prompt formats:

#### Ultra-Compressed (500 tokens)

```
PRODUCT: RoboCat — ambient emotional robot for offices. Senses noise, reacts with feelings, connects coworkers via voice gifts. ESP32, MicroPython, local-only, no cloud. 500 DKK, no subscription.

TASK: {specify}
OUTPUT: {specify format}
```

#### Compressed (2000 tokens)

```
PRODUCT: RoboCat — ambient emotional intelligence device for workspaces. Hardware: ESP32 + mic + touch sensors + TFT + speaker + LEDs. Software: MicroPython, uasyncio, local processing. Features: noise detection → stressed state; touch → happy/purring; voice gift (record 10s, playback on touch). Target: coworking spaces, 500 DKK/unit, no subscription. Market: 400 spaces Denmark, 2,500 Nordics. Differentiation: only ambient emotional robot, privacy-first, zero-UI.

PERSONAS: Workspace Operator (buyer, cares about retention), Stressed Developer (user, cares about focus), Community Manager (champion, cares about engagement).

TASK: {specify}
OUTPUT: {specify format}
```

#### Full Context (8000+ tokens)

Use entire sections as documented, with explicit references:

```
REFERENCE: PRD.md Sections 1.1, 1.2, 3.3, 3.4, 4.2, 4.4, 6.5
TASK: {specify}
OUTPUT: {specify format}
```

### 10.6 Quality Gates for AI Output

When using this PRD to prompt AI agents, verify output against:

| Gate | Check | Source |
|------|-------|--------|
| **Accuracy** | Technical specs match BOM (4.2) | Cross-reference hardware table |
| **Consistency** | User stories align with state machine (4.4) | Trace US-001 to US-004 through states |
| **Completeness** | All P0 features covered | Check against 4.5 Feature Priority Matrix |
| **Tone** | Content matches brand voice | Reference 1.1 (vision) and 3.3 (personas) |
| **Feasibility** | Timeline and budget realistic | Validate against 8.3 Operational Risks |

---

*Document Classification: Internal — Commercial in Confidence*
*© 2026 Labdo Products. All rights reserved.*
