---
version: alpha
name: Office-Cat-Light-Theme
description: "Office Cat light theme design system — warm, friendly, and approachable. Built for teams who want social connection without corporate stiffness. Cream canvas (#faf9f6) with terracotta accent (#e85d2b) and soft shadows. The system reads as welcoming yet precise: a digital pet that lives in your office. Display type is set in Inter with measured negative tracking. Cards live as white panels with subtle borders and warm shadows."

colors:
  primary: "#e85d2b"
  primary-soft: "#f07040"
  primary-deep: "#c44a1a"
  on-primary: "#ffffff"
  ink: "#1a1a1a"
  ink-strong: "#000000"
  ink-muted: "#6b6b6b"
  ink-subtle: "#9a9a9a"
  body: "#4a4a4a"
  mute: "#8a8a8a"
  hairline: "#e5e5e5"
  hairline-strong: "#d0d0d0"
  canvas: "#faf9f6"
  canvas-soft: "#ffffff"
  canvas-soft-2: "#f5f4f0"
  health: "#0ea5e9"
  health-soft: "#38bdf8"
  success: "#22c55e"
  warning: "#f59e0b"
  danger: "#ef4444"
  inverse-canvas: "#0a0a0f"
  inverse-surface: "#12121a"
  inverse-ink: "#f0f0f5"

typography:
  display-xl:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 72px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -3.0px
  display-lg:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 48px
    fontWeight: 700
    lineHeight: 1.10
    letterSpacing: -1.8px
  display-md:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: -1.0px
  headline:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.20
    letterSpacing: -0.6px
  card-title:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: -0.4px
  subhead:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.40
    letterSpacing: -0.2px
  body-lg:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: -0.1px
  body:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: -0.05px
  body-sm:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: 0px
  caption:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.40
    letterSpacing: 0.5px
  eyebrow:
    fontFamily: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif
    fontSize: 14px
    fontWeight: 600
    lineHeight: 1.40
    letterSpacing: 2.0px
    textTransform: uppercase

rounded:
  none: 0px
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 24px
  pill: 9999px
  full: 9999px

spacing:
  xxs: 2px
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 20px
  2xl: 24px
  3xl: 32px
  4xl: 40px
  5xl: 48px
  6xl: 64px

components:
  nav-bar:
    backgroundColor: "rgba(250, 249, 246, 0.9)"
    backdropFilter: "blur(20px)"
    textColor: "{colors.ink}"
    typography: "{typography.body-sm}"
    padding: "{spacing.md} {spacing.3xl}"
    borderBottom: "1px solid {colors.hairline}"
  nav-link:
    textColor: "{colors.ink-muted}"
    hoverColor: "{colors.primary}"
    typography: "{typography.body-sm}"
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body}"
    fontWeight: 600
    rounded: "{rounded.sm}"
    padding: "{spacing.md} {spacing.xl}"
    hoverBackground: "{colors.primary-soft}"
    hoverTransform: "translateY(-2px)"
    hoverShadow: "0 10px 40px rgba(232, 93, 43, 0.25)"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    borderColor: "{colors.hairline}"
    typography: "{typography.body}"
    fontWeight: 600
    rounded: "{rounded.sm}"
    padding: "{spacing.md} {spacing.xl}"
    hoverBorderColor: "{colors.primary}"
    hoverTextColor: "{colors.primary}"
  card-feature:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.ink}"
    borderColor: "{colors.hairline}"
    typography: "{typography.body}"
    rounded: "{rounded.lg}"
    padding: "{spacing.2xl}"
    shadow: "0 2px 8px rgba(0, 0, 0, 0.04)"
    hoverBorderColor: "{colors.primary}"
    hoverTransform: "translateY(-5px)"
    hoverShadow: "0 20px 40px rgba(0, 0, 0, 0.08)"
    topAccent: "3px solid linear-gradient(90deg, {colors.primary}, {colors.primary-soft})"
  card-pricing:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.ink}"
    borderColor: "{colors.hairline}"
    typography: "{typography.body}"
    rounded: "{rounded.xl}"
    padding: "{spacing.2xl}"
    shadow: "0 2px 8px rgba(0, 0, 0, 0.04)"
    hoverBorderColor: "{colors.primary}"
  card-pricing-popular:
    borderColor: "{colors.primary}"
    transform: "scale(1.05)"
    badge: "MOST POPULAR"
    badgeBackground: "{colors.primary}"
    badgeTextColor: "{colors.on-primary}"
  text-input:
    backgroundColor: "{colors.canvas-soft-2}"
    textColor: "{colors.ink}"
    borderColor: "{colors.hairline}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sm}"
    padding: "{spacing.md} {spacing.lg}"
  hero-section:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    gradientGlow: "radial-gradient(circle, rgba(232, 93, 43, 0.12) 0%, transparent 60%)"
  factory-badge:
    backgroundColor: "{colors.canvas-soft}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.lg}"
    padding: "{spacing.lg} {spacing.xl}"
    shadow: "0 2px 8px rgba(0, 0, 0, 0.04)"
  factory-agent-card:
    backgroundColor: "{colors.canvas-soft}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.md}"
    padding: "{spacing.xl}"
    textAlign: "center"
    shadow: "0 2px 8px rgba(0, 0, 0, 0.04)"
  status-indicator:
    activeColor: "{colors.success}"
    idleColor: "{colors.warning}"
    errorColor: "{colors.danger}"
  health-bar:
    backgroundColor: "{colors.canvas-soft-2}"
    fillGradient: "linear-gradient(90deg, {colors.danger}, {colors.warning}, {colors.success})"
    height: "8px"
    rounded: "{rounded.pill}"
  cat-face:
    fontSize: "8rem"
    animation: "breathe 3s ease-in-out infinite"
    scale: "1.0 → 1.05 → 1.0"

layout:
  maxWidth: "1200px"
  gridColumns: "repeat(auto-fit, minmax(300px, 1fr))"
  gap: "{spacing.lg}"
  sectionPadding: "{spacing.6xl} {spacing.2xl}"
  heroPadding: "8rem {spacing.2xl} 4rem"

responsive:
  breakpoints:
    mobile: "768px"
    tablet: "1024px"
    desktop: "1200px"
  mobile:
    display-xl: "48px"
    display-lg: "32px"
    heroGrid: "1fr"
    navLinks: "hidden"
    pricingPopular: "scale(1.0)"

agent-prompt-guide: |
  Use the Office Cat light theme for any UI related to team social tools,
  companion robots, or workplace wellbeing. Key rules:
  
  1. Canvas is always warm cream (#faf9f6), never pure white
  2. Primary accent is terracotta (#e85d2b) — warm, playful, energetic
  3. Health/cyan (#0ea5e9) for status indicators and health bars
  4. Cards have subtle borders (#e5e5e5) and soft shadows
  5. Typography is Inter, bold headlines with negative tracking
  6. Cat animations: gentle breathe (scale pulse), health bar gradient
  7. Factory sections use monospace accents and agent status grids
  8. Always include a "Factory at Work" section showing active agents
  9. CTA buttons glow with accent shadow on hover
  10. Footer links to Atech.dev hardware and Factory AI agents

---
