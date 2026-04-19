---
id: doc-006
title: "Design"
type: doc
subtype: design
status: published
sequence: 6
createdAt: "2026-04-19"
updatedAt: "2026-04-19"
---

# Design

## Aesthetic Direction
A chaotic-good, internet-native learning feed where dark mode is king, blending TikTok's immersive vertical scroll with Discord's custom emoji culture, accented by cyber-neon toxic green and electric purple.

Reference products: TikTok (feed UX), Discord (emoji culture), BeReal (raw aesthetic).

## Colour System
- **Primary (Toxic Green):** Used for correct answers, active streaks, and primary actions. It glows.
- **Accent (Electric Purple):** Used for The Vault, premium features, and rare items.
- **Surface:** Deep purple-black in dark mode, stark white in light mode. High contrast borders separate elements.

## Typography
- **Display:** Space Grotesk. Used for headers, point counters, and the logo.
- **Body:** Inter. Used for all UI text and the culture breakdown. Highly legible.
- **Meme Overlay:** Impact. Used exclusively for text overlaid on meme images.

## Shape Language
- **Radii:** Friendly but substantial (`16px` for cards, `24px` for drawers, `9999px` for pills).
- **Shadows:** Ambient neon glows rather than drop shadows. Correct answers cast a green glow; the vault casts a purple glow.
- **Spacing:** Tight in the feed to maximize image size, generous in the drawer for reading.

## Component Inventory
- **Buttons:** Chunky, tactile. `.btn-primary` glows green on hover/active.
- **The Blank:** `.meme-blank` is a glowing underline that fills with text when solved.
- **Meme Card:** Edge-to-edge container with impact text overlay.
- **Culture Drawer:** Bottom sheet that slides up smoothly.
- **Vault Item:** Grid square with a silhouette (locked) or full color (unlocked).

## Composition Patterns
- **The Feed (`C-FEED-VIEW`):** Full viewport height minus the bottom nav. The meme takes up the top 60%, the interaction area (prompt, blank, options) takes the bottom 40%. The Culture Drawer slides over the interaction area.
- **The Vault (`C-VAULT-VIEW`):** Header with current points, followed by a grid of vault items.
- **The Deck (`C-DECK-VIEW`):** A grid of square meme thumbnails.
- **Field Notes (`C-UPLOAD-VIEW`):** Camera/upload interface with AI scanning effects.

## Motion & Interaction
- Fast, punchy animations.
- The Culture Drawer slides up with a cubic-bezier easing (`cubic-bezier(0.16, 1, 0.3, 1)`).
- Incorrect guesses trigger a horizontal shake.
- Correct guesses trigger a neon flash and scale bump.

## Responsive Strategy
- **Mobile-First:** The app is designed primarily as a mobile experience with a bottom navigation bar.
- **Desktop:** Constrained to a `420px` max-width container centered on the screen to preserve the vertical feed UX.
