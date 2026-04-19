---
id: doc-database
title: Lingo.jpg — Database
type: doc
subtype: database
status: published
sequence: 4
createdAt: "2026-04-19T21:04:06.519Z"
updatedAt: "2026-04-19T21:04:06.519Z"
---

# Database

The universe of Lingo.jpg revolves around the `Meme`. A Meme isn't just an image; it's a puzzle. It contains the raw image, the original text, the obscured text (the part the user has to guess), and the literal translation. 

Attached to every Meme is a `Breakdown`. This is the AI-generated or human-curated cultural context. It contains the explanation of the joke, definitions of specific slang terms used, and a tone indicator.

Users interact with Memes by creating `Attempts`. An Attempt records whether they guessed the translation correctly, how long it took, and how many hints they used. This data feeds into the spaced repetition algorithm for their `Deck`.

The economy runs on `Points` and `Unlocks`. Users earn points through Attempts. They spend points on `Emojis`. An Emoji is a digital asset (a GIF or PNG) with a localized meaning. When a user buys one, an `Unlock` record is created, linking the User to the Emoji, allowing them to use it in the `Comments` section of any Meme.

<flex_block type="data-model">
{
  "collections": [
    {
      "name": "Users",
      "icon": "lucide:user",
      "description": "Learners and memelords. Tracks points, streaks, and target languages.",
      "keyFields": ["username", "pointsBalance", "currentStreak", "targetLanguages", "avatarUrl"],
      "relationships": ["unlocks → Unlocks", "attempts → Attempts", "deck → Saves"]
    },
    {
      "name": "Memes",
      "icon": "lucide:image",
      "description": "The core curriculum. The image, the text, and the puzzle configuration.",
      "keyFields": ["imageUrl", "language", "originalText", "hiddenPhrase", "difficulty", "tags"],
      "relationships": ["breakdown → Breakdowns", "comments → Comments", "creator → Users (if UGC)"]
    },
    {
      "name": "Breakdowns",
      "icon": "lucide:book-open",
      "description": "The cultural context. Explains the joke, the slang, and the literal vs actual meaning.",
      "keyFields": ["memeId", "literalTranslation", "actualMeaning", "slangDictionary", "culturalContext", "tone"],
      "relationships": ["meme → Memes"]
    },
    {
      "name": "Attempts",
      "icon": "lucide:gamepad-2",
      "description": "A user's attempt to solve a meme. Drives the points economy and spaced repetition.",
      "keyFields": ["userId", "memeId", "isCorrect", "pointsEarned", "timestamp"],
      "relationships": ["user → Users", "meme → Memes"]
    },
    {
      "name": "Emojis",
      "icon": "lucide:smile",
      "description": "The digital assets in The Vault. The ultimate flex.",
      "keyFields": ["name", "assetUrl", "cost", "rarity", "languageContext"],
      "relationships": ["unlocks → Unlocks"]
    },
    {
      "name": "Unlocks",
      "icon": "lucide:key",
      "description": "The ledger of which user owns which emoji.",
      "keyFields": ["userId", "emojiId", "unlockedAt"],
      "relationships": ["user → Users", "emoji → Emojis"]
    }
  ]
}
</flex_block>

---

<flex_block type="data-model" id="blk-001" name="Data Model">
{
  "collections": [
    {
      "name": "Users",
      "icon": "lucide:user",
      "description": "Learners and memelords. Tracks points, streaks, and target languages.",
      "keyFields": [
        "username",
        "pointsBalance",
        "currentStreak",
        "targetLanguages",
        "avatarUrl"
      ],
      "relationships": [
        "unlocks → Unlocks",
        "attempts → Attempts",
        "deck → Saves"
      ]
    },
    {
      "name": "Memes",
      "icon": "lucide:image",
      "description": "The core curriculum. The image, the text, and the puzzle configuration.",
      "keyFields": [
        "imageUrl",
        "language",
        "originalText",
        "hiddenPhrase",
        "difficulty",
        "tags"
      ],
      "relationships": [
        "breakdown → Breakdowns",
        "comments → Comments",
        "creator → Users (if UGC)"
      ]
    },
    {
      "name": "Breakdowns",
      "icon": "lucide:book-open",
      "description": "The cultural context. Explains the joke, the slang, and the literal vs actual meaning.",
      "keyFields": [
        "memeId",
        "literalTranslation",
        "actualMeaning",
        "slangDictionary",
        "culturalContext",
        "tone"
      ],
      "relationships": [
        "meme → Memes"
      ]
    },
    {
      "name": "Attempts",
      "icon": "lucide:gamepad-2",
      "description": "A user's attempt to solve a meme. Drives the points economy and spaced repetition.",
      "keyFields": [
        "userId",
        "memeId",
        "isCorrect",
        "pointsEarned",
        "timestamp"
      ],
      "relationships": [
        "user → Users",
        "meme → Memes"
      ]
    },
    {
      "name": "Emojis",
      "icon": "lucide:smile",
      "description": "The digital assets in The Vault. The ultimate flex.",
      "keyFields": [
        "name",
        "assetUrl",
        "cost",
        "rarity",
        "languageContext"
      ],
      "relationships": [
        "unlocks → Unlocks"
      ]
    },
    {
      "name": "Unlocks",
      "icon": "lucide:key",
      "description": "The ledger of which user owns which emoji.",
      "keyFields": [
        "userId",
        "emojiId",
        "unlockedAt"
      ],
      "relationships": [
        "user → Users",
        "emoji → Emojis"
      ]
    }
  ]
}
</flex_block>
