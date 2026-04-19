---
id: doc-pages
title: Lingo.jpg — Pages
type: doc
subtype: pages
status: published
sequence: 3
createdAt: "2026-04-19T21:04:06.519Z"
updatedAt: "2026-04-19T21:04:06.519Z"
---

# Pages

You open the app and bypass the boring stuff. The landing page is a live, interactive meme challenge. "Translate this to enter." It proves the value immediately. Once you create an account, you land directly in **The Feed**. It’s a dark, immersive interface. A meme takes up the center of the screen. Below it, a scrambled sentence or a fill-in-the-blank input. You make your guess, the screen flashes neon green for correct, and the **Culture Breakdown** drawer slides up to explain the joke. You swipe up to go to the next one. 

In the bottom navigation, the center tab is a glowing padlock icon: **The Vault**. Tapping it takes you to a neon-lit storefront. Here, you see silhouettes of locked emojis. A counter at the top shows your Glot Points. You tap a locked "Crying Cat (Spanish Edition)" sticker, spend 500 points, and the unlock animation plays. 

The **Deck** page is your library. It looks like a photo gallery, but tapping any meme flips it over to reveal the vocabulary, the slang definitions, and your mastery level of those specific words. 

The **Profile** page is your gamer tag. It shows your current streak, your total points, your top three unlocked emojis displayed proudly next to your avatar, and a heat map of your learning activity over the last year. 

<flex_block type="page-inventory">
{
  "pages": [
    { "route": "/", "name": "Landing", "type": "marketing", "description": "Interactive meme challenge that acts as the hook and signup flow." },
    { "route": "/feed", "name": "The Feed", "type": "app", "description": "Vertical scroll of meme translation challenges. The core loop." },
    { "route": "/breakdown/:id", "name": "Culture Breakdown", "type": "app", "description": "Bottom sheet overlay explaining the joke, slang, and context of a solved meme." },
    { "route": "/vault", "name": "The Vault", "type": "app", "description": "The gamification store. Spend points on custom emojis and stickers." },
    { "route": "/deck", "name": "The Deck", "type": "app", "description": "Saved memes gallery. Contextual flashcards for spaced repetition." },
    { "route": "/upload", "name": "Field Notes", "type": "app", "description": "Upload a screenshot from the wild for AI explanation and community sharing." },
    { "route": "/profile", "name": "Profile", "type": "app", "description": "Your stats, streaks, and flexed emoji unlocks." },
    { "route": "/login", "name": "Auth", "type": "auth", "description": "Quick social login to save your streak." }
  ]
}
</flex_block>

---

<flex_block type="page-inventory" id="blk-001" name="Page Inventory">
{
  "pages": [
    {
      "route": "/",
      "name": "Landing",
      "type": "marketing",
      "description": "Interactive meme challenge that acts as the hook and signup flow."
    },
    {
      "route": "/feed",
      "name": "The Feed",
      "type": "app",
      "description": "Vertical scroll of meme translation challenges. The core loop."
    },
    {
      "route": "/breakdown/:id",
      "name": "Culture Breakdown",
      "type": "app",
      "description": "Bottom sheet overlay explaining the joke, slang, and context of a solved meme."
    },
    {
      "route": "/vault",
      "name": "The Vault",
      "type": "app",
      "description": "The gamification store. Spend points on custom emojis and stickers."
    },
    {
      "route": "/deck",
      "name": "The Deck",
      "type": "app",
      "description": "Saved memes gallery. Contextual flashcards for spaced repetition."
    },
    {
      "route": "/upload",
      "name": "Field Notes",
      "type": "app",
      "description": "Upload a screenshot from the wild for AI explanation and community sharing."
    },
    {
      "route": "/profile",
      "name": "Profile",
      "type": "app",
      "description": "Your stats, streaks, and flexed emoji unlocks."
    },
    {
      "route": "/login",
      "name": "Auth",
      "type": "auth",
      "description": "Quick social login to save your streak."
    }
  ]
}
</flex_block>
