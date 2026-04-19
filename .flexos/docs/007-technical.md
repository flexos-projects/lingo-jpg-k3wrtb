---
id: doc-technical
title: Lingo.jpg — Technical
type: doc
subtype: technical
status: published
sequence: 7
createdAt: "2026-04-19T21:04:06.519Z"
updatedAt: "2026-04-19T21:04:06.519Z"
---

# Technical

The app needs to feel snappy, native, and highly visual. Because it relies heavily on images and real-time interactions, performance is paramount. It doesn't need to be a native app immediately; a highly optimized PWA (Progressive Web App) solves the distribution problem and allows for rapid iteration, which is crucial when your content is based on fast-moving internet trends.

The AI layer is the secret weapon. Standard translation APIs (like Google Translate) fail spectacularly at slang and memes. The app requires an LLM (like Anthropic's Claude 3.5 Sonnet or OpenAI's GPT-4o) with a highly specific system prompt to parse the cultural nuance of the uploaded memes and generate the "Culture Breakdown." 

<flex_block type="stack">
{
  "framework": { "name": "Nuxt 4", "why": "Fast, modern, builds a beautiful PWA that feels like a native app without App Store approval delays." },
  "database": { "name": "Supabase", "why": "PostgreSQL for complex relational data (users, memes, unlocks) + instant real-time sync for the points economy." },
  "auth": { "name": "Supabase Auth", "why": "Frictionless social login (Google/Apple) to ensure users don't drop off before their first meme." },
  "ai": { "name": "Anthropic Claude 3.5", "why": "Superior at parsing cultural context, nuance, and humor compared to standard translation models." },
  "hosting": { "name": "Vercel", "why": "Edge network delivery ensures images and API routes load instantly globally." },
  "storage": { "name": "Vercel Blob", "why": "Handles the massive volume of user-uploaded meme images (UGC) with on-the-fly optimization." }
}
</flex_block>

---

<flex_block type="stack" id="blk-001" name="Tech Stack">
{
  "framework": {
    "name": "Nuxt 4",
    "why": "Fast, modern, builds a beautiful PWA that feels like a native app without App Store approval delays."
  },
  "database": {
    "name": "Supabase",
    "why": "PostgreSQL for complex relational data (users, memes, unlocks) + instant real-time sync for the points economy."
  },
  "auth": {
    "name": "Supabase Auth",
    "why": "Frictionless social login (Google/Apple) to ensure users don't drop off before their first meme."
  },
  "ai": {
    "name": "Anthropic Claude 3.5",
    "why": "Superior at parsing cultural context, nuance, and humor compared to standard translation models."
  },
  "hosting": {
    "name": "Vercel",
    "why": "Edge network delivery ensures images and API routes load instantly globally."
  },
  "storage": {
    "name": "Vercel Blob",
    "why": "Handles the massive volume of user-uploaded meme images (UGC) with on-the-fly optimization."
  }
}
</flex_block>
