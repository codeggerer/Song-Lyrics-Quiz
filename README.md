# 🎤 Song Lyrics Quiz

A modern, fast-paced web game designed to test and sharpen your music knowledge. Guess song lyrics word-by-word or in freestyle mode, challenge yourself against the clock, unlock leveling rewards and cosmetic themes, and track your all-time lyrical vocabulary.

Built as an entirely self-contained single-page web app with zero dependencies, featuring deep integration with the **LRCLIB** music database.

---

## 🌟 Key Features

### 1. Song Sourcing & Lyrics Engine
- **Online Database Search:** Instantly fetch lyrics from millions of tracks via the integrated [LRCLIB](https://lrclib.net) API.
- **Custom Lyrics Input:** Paste your own lyrics to create custom quizzes on the fly.
- **Smart Text Normalizer:**
  - Tolerant German umlaut matching (e.g., inputting `ä` matches `ae`, and vice versa).
  - Punctuation, smart quotes, and symbol stripping for seamless typing flow.
  - Automatic homoglyph and Cyrillic look-alike resolution to prevent scraper/encoding mismatch errors.
  - Optional **Auto-Reveal Filler Words** toggle to automatically uncover interjections like *yeah*, *uh*, *mmh*, and *woah*.

---

### 2. Diverse Game Modes

| Mode | Unlock | Description |
| :--- | :---: | :--- |
| **Classic** | Level 1 | Guess all words in any order before the timer expires. |
| **Chorus Hunter** | Level 5 | Automatically detects recurring choruses and refrains; focus solely on uncovering the song's core hook while verse lines remain readable. |
| **Sudden Death** | Level 10 | Start with a harsh 30-second clock. Each uniquely discovered word grants a configurable time bonus (default `+3.0s`, customizable up to `+5.0s`, capped at max 1:00–3:00 min). |
| **Word for Word (Flow)** | Level 15 | Strict sequential guessing. Move through the song in exact chronological order, with arrow-key word jumping and box focusing. |
| **Artist Roulette** | Level 20 | Pick an artist, spin a casino-style visual prize wheel with spoiler blur protection, and try to guess both the hidden song title (+50 XP bonus) and its lyrics. |

---

### 3. Progression, XP & Progression System
- **Dynamic XP Formula:** Earn experience points based on word completion percentage, unique vocabulary ratio, speed bonuses, and 100% perfect runs.
- **Player Ranks:** Climb from *Radio Listener* up to *Lyric Legend*.
- **Daily Quests:** Complete 3 procedural daily challenges every 24 hours (volume, accuracy, mode-specific tasks) for an extra `+30 XP` completion bounty.
- **End-Game Visuals & Tiered Celebrations:**
  - Classic multicolored confetti for starter levels.
  - Golden particle cascades for intermediate milestones.
  - Full-screen high-performance canvas **Supernova Shockwave Explosions** with chromatic shimmers for mastery tiers (Level 20+).

---

### 4. Cosmetics & Visual Engine
- **Dark & Light Mode:** Tailored contrast themes, with system-default dark styling.
- **Custom Accent Colors:** Choose from curated color dots, use the Apple-style native color wheel picker, or unlock the continuous **Rainbow Accent Mode** at Level 30.
- **Ambient Animated Backgrounds:** Hardware-accelerated dynamic canvas ribbons and drifting glowing orbs (*Aurora, Sunset, Amethyst, Emerald, Gold*).
- **Word Box Skins:** Unlock distinct styling for uncovered words (*Classic, Neon Glow, Crystal Glass / Acrylic, Golden Frame*).
- **Web Audio FX:** Synthesized procedural sound effects for hits, buzzer errors, wheel ticks, and tiered victory fanfares via the Web Audio API.

---

### 5. Statistics, Highscores & Vocabulary Tracker
- **Personal Vocabulary Codex:** Inspect every unique word you have ever guessed, complete with total frequencies and distinct song appearance counts. Filterable and sortable (A–Z, Frequency, Song Count).
- **Advanced Player Analytics:** Monitor total games played, average accuracy, 100% perfect songs, top 5 most-played artists, and top 10 most common lyrical words.
- **Local Song Library:** Auto-saved high scores, editable song titles, best times, and page-by-page table navigation.
- **Data Portability:** Full JSON export and import backups to migrate your saved library across devices.

---

## 🚀 Getting Started

Because the application is packaged entirely within a single standalone file, you do not need Node.js, npm, or any build tools to run it.

### Running Locally
1. Clone or download the repository:
   ```bash
   git clone https://github.com/codeggerer/Song-Lyrics-Quiz.git
   ```
2. Open `index.html` directly in any modern desktop or mobile web browser (Google Chrome, Firefox, Safari, Edge, Brave).

### Running on a Local Server (Optional)
To test across multiple devices on the same Wi-Fi network:
```bash
# Using Python 3
python3 -m http.server 8000

# Or using Node.js npx
npx serve .
```

---

## 📱 Mobile & PWA Usage

The app is fully responsive and supports touch devices, notched screens, and fullscreen displays.

1. Open your live hosted URL in Safari (iOS) or Chrome (Android).
2. Tap the browser share/menu icon $\rightarrow$ **"Add to Home Screen"**.
3. Launch the app directly from your home screen to enjoy a borderless, native app-like experience without navigation bars.

---

## 🛠️ Tech Stack & Architecture

- **Markup & Styling:** Vanilla HTML5, semantic tags, pure CSS3 (CSS Variables, Flexbox, CSS Grid, `@property` hardware-accelerated animations).
- **Logic:** Vanilla JavaScript (ES6+), async/await, Canvas 2D API for fluid 60/120fps effects.
- **Sound:** Synthesized Web Audio API oscillators (no external `.mp3` or `.wav` dependencies).
- **Typography:** Google Fonts ([Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans)).
- **API:** [LRCLIB REST API](https://lrclib.net) for song search and synchronization.
- **Storage:** Client-side persistent storage via `localStorage`.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).