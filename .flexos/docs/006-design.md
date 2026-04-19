---
id: doc-design
title: Lingo.jpg — Design
type: doc
subtype: design
status: published
sequence: 6
createdAt: "2026-04-19T21:04:06.519Z"
updatedAt: "2026-04-19T21:04:06.519Z"
---

# Design

Lingo.jpg does not look like a classroom. It looks like the internet. 

The aesthetic is heavily inspired by late-night scrolling. Dark mode is not an option; it is the default and only mode. The background is a deep, bruised purple-black, allowing the memes (which are often bright, low-res, or colorful) to pop off the screen. 

The accents are pure cyber-neon. A toxic, radioactive green serves as the primary action color—it's the color of correct answers, high scores, and active streaks. A vibrant electric purple serves as the secondary accent for The Vault and premium interactions. 

Typography is split between a bold, hyper-legible sans-serif for UI elements, and a slightly chaotic, marker-style display font for streak counters and point callouts. The text needs to feel digital but slightly raw, like a Discord server run by hackers who love linguistics.

Components are designed to get out of the way of the content. Cards have no borders, only subtle ambient shadows that glow in the accent colors. Buttons are chunky, pill-shaped, and feature aggressive haptic feedback. When you get a translation right, the button doesn't just change color; the phone buzzes, the points physically fly up the screen, and the UI reacts. 

The Empty States are snarky. If you have no saved memes, the app tells you: "Your deck is as empty as a textbook. Go scroll." 

<flex_block type="tokens">
{
  "category": "colors",
  "mode": "dark",
  "tokens": {
    "--color-primary": "oklch(80% 0.25 145)",
    "--color-primary-hover": "oklch(85% 0.25 145)",
    "--color-primary-subtle": "oklch(80% 0.25 145 / 0.15)",
    "--color-accent": "oklch(65% 0.25 300)",
    "--color-accent-hover": "oklch(70% 0.25 300)",
    "--color-bg": "oklch(15% 0.03 285)",
    "--color-surface": "oklch(20% 0.04 285)",
    "--color-surface-raised": "oklch(25% 0.05 285)",
    "--color-border": "oklch(30% 0.05 285)",
    "--color-text": "oklch(95% 0.01 285)",
    "--color-text-muted": "oklch(70% 0.03 285)",
    "--color-success": "oklch(80% 0.25 145)",
    "--color-warning": "oklch(75% 0.20 50)",
    "--color-error": "oklch(65% 0.25 20)"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "colors",
  "mode": "light",
  "tokens": {
    "--color-primary": "oklch(60% 0.20 145)",
    "--color-primary-hover": "oklch(55% 0.20 145)",
    "--color-primary-subtle": "oklch(60% 0.20 145 / 0.15)",
    "--color-accent": "oklch(55% 0.25 300)",
    "--color-accent-hover": "oklch(50% 0.25 300)",
    "--color-bg": "oklch(98% 0.01 285)",
    "--color-surface": "oklch(100% 0 0)",
    "--color-surface-raised": "oklch(95% 0.02 285)",
    "--color-border": "oklch(90% 0.03 285)",
    "--color-text": "oklch(20% 0.04 285)",
    "--color-text-muted": "oklch(50% 0.05 285)",
    "--color-success": "oklch(60% 0.20 145)",
    "--color-warning": "oklch(70% 0.20 50)",
    "--color-error": "oklch(60% 0.25 20)"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "typography",
  "tokens": {
    "--font-display": "'Space Grotesk', system-ui, sans-serif",
    "--font-body": "'Inter', system-ui, sans-serif",
    "--font-mono": "'JetBrains Mono', monospace",
    "--font-size-xs": "0.75rem",
    "--font-size-sm": "0.875rem",
    "--font-size-base": "1rem",
    "--font-size-lg": "1.125rem",
    "--font-size-xl": "1.25rem",
    "--font-size-2xl": "1.5rem",
    "--font-size-3xl": "2rem",
    "--font-size-4xl": "2.5rem",
    "--font-weight-normal": "400",
    "--font-weight-medium": "500",
    "--font-weight-bold": "700",
    "--font-weight-black": "900"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "spacing",
  "tokens": {
    "--space-1": "0.25rem",
    "--space-2": "0.5rem",
    "--space-3": "0.75rem",
    "--space-4": "1rem",
    "--space-6": "1.5rem",
    "--space-8": "2rem",
    "--space-12": "3rem",
    "--space-16": "4rem"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "radii",
  "tokens": {
    "--radius-sm": "0.5rem",
    "--radius-md": "1rem",
    "--radius-lg": "1.5rem",
    "--radius-full": "9999px"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "shadows",
  "tokens": {
    "--shadow-glow-primary": "0 0 20px oklch(80% 0.25 145 / 0.2)",
    "--shadow-glow-accent": "0 0 20px oklch(65% 0.25 300 / 0.2)",
    "--shadow-card": "0 10px 30px oklch(0% 0 0 / 0.5)"
  }
}
</flex_block>

<flex_block type="mockup-html" id="landing-preview">
<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lingo.jpg</title>
<style>
  :root {
    --color-primary: oklch(80% 0.25 145);
    --color-accent: oklch(65% 0.25 300);
    --color-bg: oklch(15% 0.03 285);
    --color-surface: oklch(20% 0.04 285);
    --color-surface-raised: oklch(25% 0.05 285);
    --color-border: oklch(30% 0.05 285);
    --color-text: oklch(95% 0.01 285);
    --color-text-muted: oklch(70% 0.03 285);
    --font-display: 'Space Grotesk', system-ui, sans-serif;
    --font-body: 'Inter', system-ui, sans-serif;
    --radius-md: 1rem;
    --radius-lg: 1.5rem;
    --radius-full: 9999px;
    --space-2: 0.5rem;
    --space-4: 1rem;
    --space-6: 1.5rem;
    --shadow-glow-primary: 0 0 20px oklch(80% 0.25 145 / 0.2);
  }

  [data-theme="light"] {
    --color-primary: oklch(60% 0.20 145);
    --color-accent: oklch(55% 0.25 300);
    --color-bg: oklch(98% 0.01 285);
    --color-surface: oklch(100% 0 0);
    --color-surface-raised: oklch(95% 0.02 285);
    --color-border: oklch(90% 0.03 285);
    --color-text: oklch(20% 0.04 285);
    --color-text-muted: oklch(50% 0.05 285);
    --shadow-glow-primary: 0 4px 12px oklch(60% 0.20 145 / 0.2);
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }
  
  body {
    background-color: var(--color-bg);
    color: var(--color-text);
    font-family: var(--font-body);
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    overflow: hidden;
  }

  .app-container {
    width: 100%;
    max-width: 420px;
    height: 100vh;
    max-height: 850px;
    background-color: var(--color-bg);
    position: relative;
    display: flex;
    flex-direction: column;
    box-shadow: 0 0 40px rgba(0,0,0,0.5);
  }

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: var(--space-4);
    z-index: 10;
  }

  .logo {
    font-family: var(--font-display);
    font-weight: 900;
    font-size: 1.5rem;
    letter-spacing: -0.05em;
  }

  .streak {
    display: flex;
    align-items: center;
    gap: var(--space-2);
    background: var(--color-surface);
    padding: 0.25rem 0.75rem;
    border-radius: var(--radius-full);
    font-weight: 700;
    color: var(--color-primary);
    border: 1px solid var(--color-border);
  }

  .feed {
    flex: 1;
    display: flex;
    flex-direction: column;
    padding: var(--space-4);
    overflow: hidden;
    position: relative;
  }

  .meme-card {
    background: var(--color-surface);
    border-radius: var(--radius-lg);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    height: 100%;
    border: 1px solid var(--color-border);
    position: relative;
    transition: transform 0.3s ease;
  }

  .meme-image-container {
    height: 55%;
    position: relative;
    background: #000;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }

  .meme-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: 0.8;
  }

  .meme-text-overlay {
    position: absolute;
    top: 10%;
    width: 90%;
    text-align: center;
    font-family: impact, sans-serif;
    color: white;
    font-size: 1.8rem;
    text-transform: uppercase;
    -webkit-text-stroke: 1px black;
    text-shadow: 2px 2px 0 #000;
  }

  .interaction-area {
    padding: var(--space-6) var(--space-4);
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .prompt {
    font-size: 0.875rem;
    color: var(--color-text-muted);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: var(--space-2);
  }

  .challenge-text {
    font-size: 1.25rem;
    font-weight: 500;
    line-height: 1.4;
    margin-bottom: var(--space-6);
  }

  .blank {
    display: inline-block;
    background: var(--color-surface-raised);
    border-bottom: 2px solid var(--color-text-muted);
    color: transparent;
    padding: 0 1rem;
    border-radius: 4px;
    min-width: 100px;
    cursor: pointer;
    transition: all 0.2s ease;
  }

  .blank.revealed {
    background: transparent;
    border-bottom: 2px solid var(--color-primary);
    color: var(--color-primary);
    text-shadow: var(--shadow-glow-primary);
  }

  .options {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: var(--space-2);
  }

  .btn-option {
    background: var(--color-surface-raised);
    border: 1px solid var(--color-border);
    color: var(--color-text);
    padding: var(--space-4);
    border-radius: var(--radius-md);
    font-family: var(--font-body);
    font-size: 1rem;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.2s ease;
  }

  .btn-option:active {
    transform: scale(0.98);
  }

  .btn-option.correct {
    background: var(--color-primary);
    color: #000;
    border-color: var(--color-primary);
    box-shadow: var(--shadow-glow-primary);
  }

  .context-drawer {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: var(--color-surface-raised);
    border-top: 1px solid var(--color-primary);
    padding: var(--space-6) var(--space-4);
    border-radius: var(--radius-lg) var(--radius-lg) 0 0;
    transform: translateY(100%);
    transition: transform 0.4s cubic-bezier(0.16, 1, 0.3, 1);
    box-shadow: 0 -10px 40px rgba(0,0,0,0.5);
  }

  .context-drawer.open {
    transform: translateY(0);
  }

  .drawer-title {
    font-family: var(--font-display);
    color: var(--color-primary);
    font-size: 1.25rem;
    margin-bottom: var(--space-2);
    display: flex;
    justify-content: space-between;
  }

  .drawer-text {
    color: var(--color-text-muted);
    line-height: 1.6;
    font-size: 0.95rem;
  }

  .bottom-nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: var(--space-4);
    background: var(--color-bg);
    border-top: 1px solid var(--color-border);
    padding-bottom: calc(var(--space-4) + env(safe-area-inset-bottom, 0px));
  }

  .nav-item {
    color: var(--color-text-muted);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 4px;
    font-size: 0.75rem;
    cursor: pointer;
  }

  .nav-item.active {
    color: var(--color-text);
  }

  .nav-item.vault {
    color: var(--color-accent);
  }

  .nav-icon {
    width: 24px;
    height: 24px;
    background: currentColor;
    mask-size: contain;
    mask-repeat: no-repeat;
    mask-position: center;
    -webkit-mask-size: contain;
    -webkit-mask-repeat: no-repeat;
    -webkit-mask-position: center;
  }

  .icon-home { -webkit-mask-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path><polyline points="9 22 9 12 15 12 15 22"></polyline></svg>'); }
  .icon-vault { -webkit-mask-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"></rect><path d="M7 11V7a5 5 0 0 1 10 0v4"></path></svg>'); }
  .icon-user { -webkit-mask-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"></path><circle cx="12" cy="7" r="4"></circle></svg>'); }
  
  .theme-toggle {
    position: absolute;
    top: 1rem;
    right: 1rem;
    background: transparent;
    border: 1px solid var(--color-border);
    color: var(--color-text);
    padding: 0.5rem;
    border-radius: var(--radius-full);
    cursor: pointer;
    z-index: 100;
  }

  @media (min-width: 421px) {
    .app-container {
      border-radius: var(--radius-lg);
      border: 1px solid var(--color-border);
    }
    .theme-toggle {
      right: -3rem;
    }
  }
</style>
</head>
<body>

<button class="theme-toggle" onclick="document.documentElement.setAttribute('data-theme', document.documentElement.getAttribute('data-theme') === 'dark' ? 'light' : 'dark')">🌓</button>

<div class="app-container">
  <div class="header">
    <div class="logo">Lingo.jpg</div>
    <div class="streak">🔥 12</div>
  </div>

  <div class="feed">
    <div class="meme-card">
      <div class="meme-image-container">
        <!-- Using a placeholder image that looks like a classic dramatic reaction -->
        <img src="https://images.unsplash.com/photo-1518020382113-a7e8fc38eac9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Funny pug" class="meme-image">
        <div class="meme-text-overlay">
          Yo después de decir<br>"no mames" 50 veces<br>en una hora
        </div>
      </div>
      
      <div class="interaction-area">
        <div>
          <div class="prompt">Translate the slang</div>
          <div class="challenge-text">
            Me after saying "<span class="blank" id="blank-target">_______</span>" 50 times in an hour.
          </div>
        </div>

        <div class="options">
          <button class="btn-option" onclick="handleWrong(this)">"I don't suck"</button>
          <button class="btn-option" onclick="handleWrong(this)">"No way"</button>
          <button class="btn-option" onclick="handleCorrect(this)">"You've gotta be kidding me"</button>
          <button class="btn-option" onclick="handleWrong(this)">"I am tired"</button>
        </div>
      </div>

      <div class="context-drawer" id="drawer">
        <div class="drawer-title">
          <span>Culture Breakdown</span>
          <span>+50 Pts</span>
        </div>
        <div class="drawer-text">
          <strong>"No mames"</strong> literally translates to something vulgar ("don't suck"), but in Mexico, it's the ultimate punctuation mark for disbelief, shock, or frustration. It translates best to "You've gotta be kidding me" or "No fucking way."
        </div>
      </div>
    </div>
  </div>

  <div class="bottom-nav">
    <div class="nav-item active">
      <div class="nav-icon icon-home"></div>
      Feed
    </div>
    <div class="nav-item vault">
      <div class="nav-icon icon-vault"></div>
      Vault
    </div>
    <div class="nav-item">
      <div class="nav-icon icon-user"></div>
      Profile
    </div>
  </div>
</div>

<script>
  function handleCorrect(btn) {
    // Visual feedback for the button
    document.querySelectorAll('.btn-option').forEach(b => b.style.opacity = '0.5');
    btn.style.opacity = '1';
    btn.classList.add('correct');
    
    // Fill in the blank
    const blank = document.getElementById('blank-target');
    blank.textContent = "you've gotta be kidding me";
    blank.classList.add('revealed');

    // Show the context drawer
    setTimeout(() => {
      document.getElementById('drawer').classList.add('open');
    }, 400);
  }

  function handleWrong(btn) {
    btn.style.opacity = '0.3';
    btn.style.transform = 'translateX(5px)';
    setTimeout(() => btn.style.transform = 'translateX(-5px)', 100);
    setTimeout(() => btn.style.transform = 'translateX(0)', 200);
  }
</script>
</body>
</html>
</flex_block>

---

<flex_block type="tokens" id="blk-001" name="colors">
{
  "category": "colors",
  "mode": "dark",
  "tokens": {
    "--color-primary": "oklch(80% 0.25 145)",
    "--color-primary-hover": "oklch(85% 0.25 145)",
    "--color-primary-subtle": "oklch(80% 0.25 145 / 0.15)",
    "--color-accent": "oklch(65% 0.25 300)",
    "--color-accent-hover": "oklch(70% 0.25 300)",
    "--color-bg": "oklch(15% 0.03 285)",
    "--color-surface": "oklch(20% 0.04 285)",
    "--color-surface-raised": "oklch(25% 0.05 285)",
    "--color-border": "oklch(30% 0.05 285)",
    "--color-text": "oklch(95% 0.01 285)",
    "--color-text-muted": "oklch(70% 0.03 285)",
    "--color-success": "oklch(80% 0.25 145)",
    "--color-warning": "oklch(75% 0.20 50)",
    "--color-error": "oklch(65% 0.25 20)"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-002" name="colors">
{
  "category": "colors",
  "mode": "light",
  "tokens": {
    "--color-primary": "oklch(60% 0.20 145)",
    "--color-primary-hover": "oklch(55% 0.20 145)",
    "--color-primary-subtle": "oklch(60% 0.20 145 / 0.15)",
    "--color-accent": "oklch(55% 0.25 300)",
    "--color-accent-hover": "oklch(50% 0.25 300)",
    "--color-bg": "oklch(98% 0.01 285)",
    "--color-surface": "oklch(100% 0 0)",
    "--color-surface-raised": "oklch(95% 0.02 285)",
    "--color-border": "oklch(90% 0.03 285)",
    "--color-text": "oklch(20% 0.04 285)",
    "--color-text-muted": "oklch(50% 0.05 285)",
    "--color-success": "oklch(60% 0.20 145)",
    "--color-warning": "oklch(70% 0.20 50)",
    "--color-error": "oklch(60% 0.25 20)"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-003" name="typography">
{
  "category": "typography",
  "tokens": {
    "--font-display": "'Space Grotesk', system-ui, sans-serif",
    "--font-body": "'Inter', system-ui, sans-serif",
    "--font-mono": "'JetBrains Mono', monospace",
    "--font-size-xs": "0.75rem",
    "--font-size-sm": "0.875rem",
    "--font-size-base": "1rem",
    "--font-size-lg": "1.125rem",
    "--font-size-xl": "1.25rem",
    "--font-size-2xl": "1.5rem",
    "--font-size-3xl": "2rem",
    "--font-size-4xl": "2.5rem",
    "--font-weight-normal": "400",
    "--font-weight-medium": "500",
    "--font-weight-bold": "700",
    "--font-weight-black": "900"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-004" name="spacing">
{
  "category": "spacing",
  "tokens": {
    "--space-1": "0.25rem",
    "--space-2": "0.5rem",
    "--space-3": "0.75rem",
    "--space-4": "1rem",
    "--space-6": "1.5rem",
    "--space-8": "2rem",
    "--space-12": "3rem",
    "--space-16": "4rem"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-005" name="radii">
{
  "category": "radii",
  "tokens": {
    "--radius-sm": "0.5rem",
    "--radius-md": "1rem",
    "--radius-lg": "1.5rem",
    "--radius-full": "9999px"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-006" name="shadows">
{
  "category": "shadows",
  "tokens": {
    "--shadow-glow-primary": "0 0 20px oklch(80% 0.25 145 / 0.2)",
    "--shadow-glow-accent": "0 0 20px oklch(65% 0.25 300 / 0.2)",
    "--shadow-card": "0 10px 30px oklch(0% 0 0 / 0.5)"
  }
}
</flex_block>
