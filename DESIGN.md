---
version: alpha
name: Office-Cat-design-analysis
description: "Office Cat design language — a social catalyst for teams. Near-black canvas (#0a0a0f) with warm terracotta accent (#ff6b35) inspired by playful interaction and emotional warmth. The system reads as friendly yet precise: a digital pet that lives in your office. Display type is set in a custom geometric sans (Inter fallback) at 500–700 with measured negative tracking. Cards live as dark panels (#12121a) with subtle borders. The accent terracotta appears on CTAs, health bars, and cat states — never decoratively. Page rhythm leans on animated cat visual in hero, feature cards with emoji icons, and a live factory status grid."

colors:
  primary: "#ff6b35"
  primary-soft: "#ff8c5a"
  primary-deep: "#e55a2b"
  on-primary: "#0a0a0f"
  ink: "#f0f0f5"
  ink-strong: "#ffffff"
  ink-muted: "#a0a0b0"
  ink-subtle: "#606070"
  body: "#d0d0d8"
  mute: "#8a8a95"
  hairline: "#2a2a35"
  hairline-strong: "#3a3a45"
  canvas: "#0a0a0f"
  canvas-soft: "#12121a"
  canvas-soft-2: "#1a1a25"
  health: "#22d3ee"
  health-soft: "#67e8f9"
  success: "#4ade80"
  warning: "#fbbf24"
  danger: "#ef4444"
  inverse-canvas: "#ffffff"
  inverse-surface: "#f5f5f5"
  inverse-ink: "#0a0a0f"

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
    backgroundColor: "{colors.canvas}"
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
    hoverShadow: "0 10px 40px rgba(255, 107, 53, 0.3)"
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
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.primary-soft}"
    typography: "{typography.body}"
    fontWeight: 600
    rounded: "{rounded.sm}"
    padding: "{spacing.md} {spacing.xl}"
  card-feature:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.ink}"
    borderColor: "{colors.hairline}"
    typography: "{typography.body}"
    rounded: "{rounded.lg}"
    padding: "{spacing.2xl}"
    hoverBorderColor: "{colors.primary}"
    hoverTransform: "translateY(-5px)"
    hoverShadow: "0 20px 60px rgba(0, 0, 0, 0.3)"
    topAccent: "3px solid linear-gradient(90deg, {colors.primary}, {colors.primary-soft})"
  card-pricing:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.ink}"
    borderColor: "{colors.hairline}"
    typography: "{typography.body}"
    rounded: "{rounded.xl}"
    padding: "{spacing.2xl}"
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
    gradientGlow: "radial-gradient(circle, rgba(255, 107, 53, 0.3) 0%, transparent 60%)"
  factory-badge:
    backgroundColor: "{colors.canvas-soft}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.lg}"
    padding: "{spacing.lg} {spacing.xl}"
  factory-agent-card:
    backgroundColor: "{colors.canvas-soft}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.md}"
    padding: "{spacing.xl}"
    textAlign: "center"
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
  Use the Office Cat design system for any UI related to team social tools,
  companion robots, or workplace wellbeing. Key rules:
  
  1. Canvas is always near-black (#0a0a0f), never pure white
  2. Primary accent is terracotta (#ff6b35) — warm, playful, energetic
  3. Health/cyan (#22d3ee) for status indicators and health bars
  4. Cards have subtle borders (#2a2a35) and hover to primary accent
  5. Typography is Inter, bold headlines with negative tracking
  6. Cat animations: gentle breathe (scale pulse), health bar gradient
  7. Factory sections use monospace accents and agent status grids
  8. Always include a "Factory at Work" section showing active agents
  9. CTA buttons glow with accent shadow on hover
  10. Footer links to Atech.dev hardware and Factory AI agents

---
