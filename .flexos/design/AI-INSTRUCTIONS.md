# Design System — AI Build Instructions

> A chaotic-good, internet-native learning feed where dark mode is king, blending TikTok's immersive vertical scroll with Discord's custom emoji culture, accented by cyber-neon toxic green and electric purple.

## The Rules

These are non-negotiable. Every screen, every component, every interaction.

### 1. Always Use the Token Vocabulary
- NEVER hardcode colours, spacing, font sizes, radii, or shadows.
- ALWAYS use `var(--token-name)` from tokens.css.
- Colour: `--color-primary`, `--color-surface`, `--color-text-muted`, etc.
- Spacing: `--space-1` through `--space-16`.
- Type: `--font-size-sm`, `--font-display`, `--font-weight-bold`, etc.

### 2. Always Use the Component Classes
- NEVER assemble styles from scratch. Use `.btn-primary`, `.card`, `.input`, `.badge-primary`.
- The full class vocabulary is in `components.css`. Do not invent new base classes.
- For page-specific layout, use scoped `<style>` with semantic class names that consume tokens.

### 3. Both Themes, Always
- Every screen must work in both light and dark mode.
- Light mode is a stark, high-contrast "whiteboard" theme. Dark mode is a deep purple-black cyber theme.
- The system handles the token swap via `data-theme="light"` on `<html>`.

### 4. App Shell Constraint (Mobile First)
- **CRITICAL:** The entire app UI must be constrained to a `max-width: var(--container-mobile)` (420px) container, centered on the screen.
- Lingo.jpg is a vertical, TikTok-style feed. It does not expand to fill desktop monitors. On desktop, it looks like a mobile phone frame in the center of the screen.
- Use `dvh` for full height to avoid iOS Safari bottom bar issues.
- Bottom navigation `.bottom-nav` is fixed at the bottom of the container.

### 5. Typography Rules
- Page titles & Numbers: `--font-display` (Space Grotesk).
- UI Text & Culture Breakdown: `--font-body` (Inter).
- Meme Image Overlays ONLY: `--font-meme` (Impact).
- Headings use `--letter-spacing-tight`.

### 6. Interaction & Motion Rules
- Correct answers should trigger a state change to `.btn-primary` and `.meme-blank.revealed`.
- The Culture Breakdown uses `.drawer`. It starts at `transform: translateY(100%)` and transitions to `transform: translateY(0)` via `.drawer.open`.
- Use `--transition-drawer` for the bottom sheet (it uses a snappy cubic-bezier).

### 7. Composition Patterns

When building **The Feed (`/feed`)**, compose:
1. `.c-header` at the top with `.c-logo` and `.badge-primary` (streak).
2. Main area `.c-feed` containing a full-height `.card`.
3. Inside the card: `.meme-image-container` (top 55%) and `.c-interaction` (bottom 45%).
4. Hidden `.drawer` waiting to slide up.
5. `.bottom-nav` at the bottom.

When building **The Vault (`/vault`)**, compose:
1. `.c-vault-header` showing current Glot Points in `--font-display`.
2. `.c-vault-grid` (3 columns).
3. Populate with `.vault-item` (add `.locked` class to unpurchased items).

## Component Quick Reference

| Need this? | Use this class | Notes |
|---|---|---|
| Action Button | `.btn .btn-primary` | Glows neon green on hover. |
| Vault Button | `.btn .btn-accent` | Glows electric purple on hover. |
| Secondary Button| `.btn .btn-surface` | Outlined, standard interaction. |
| Streak Counter | `.badge .badge-primary` | Pill shape, display font. |
| Meme Card | `.card` | Wrap the meme image and interaction in this. |
| The Blank | `.meme-blank` | Add `.revealed` when solved. |
| Image Overlay | `.meme-text-overlay` | Uses Impact font, white with black stroke. |
| Bottom Sheet | `.drawer` | Add `.open` via JS to slide up. |
| Nav Bar | `.bottom-nav` | Contains `.nav-item` links. |
| Store Item | `.vault-item` | Add `.locked` for unowned emojis. |
