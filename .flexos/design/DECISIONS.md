# Design Decisions

## What I Found
- A strong directive for "dark mode only" in the core specs.
- A TikTok-style vertical feed UI.
- Cyber-neon aesthetic (toxic green, electric purple) over a deep purple-black background.
- "Discord custom emoji" culture for gamification (The Vault).
- An existing prototype (`home-v1.html`) that successfully captures the impact-font meme card and bottom drawer reveal.

## What I Chose
- **Light Mode Re-imagined:** The core specs insisted on dark mode only. To satisfy the hard constraints of the design system, I designed a "Light Hacker / Whiteboard" theme. It uses a stark white background with high-contrast borders, retaining the toxic green and electric purple accents but adjusting their lightness for accessibility.
- **Typography:** Space Grotesk for display (gives that slightly chaotic, techy vibe), Inter for high legibility in the UI, and Impact specifically scoped for meme image overlays.
- **Shape Language:** Generous border radii (`1rem` to `1.5rem`) to feel like a modern mobile app, combined with thick `1px` borders to give a tactile, slightly brutalist edge.
- **Motion:** Emphasized the "bottom sheet" (drawer) pattern for the Culture Breakdown, as it keeps the user in the context of the feed.
- **App Shell Constraint:** The entire app is constrained to a `420px` max-width container, even on desktop. This preserves the vertical TikTok-style feed experience across all devices.

## What I Rejected
- **Sterile Gamification:** Rejected the flat, friendly, rounded look of traditional language apps (like Duolingo). The UI needs to feel like a native internet platform.
- **Card-based Feed:** Rejected separating the meme from the background. The meme *is* the card in the feed.

## Aesthetic Direction
"A chaotic-good, internet-native learning feed where dark mode is king, blending TikTok's immersive vertical scroll with Discord's custom emoji culture, accented by cyber-neon toxic green and electric purple."