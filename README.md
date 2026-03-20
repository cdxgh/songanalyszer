# 🎬 CineMood — Bollywood & Hollywood Song Analyzer

Upload a photo and let AI analyze your **facial expression + background** to suggest matching **Bollywood and Hollywood songs**.

## ✨ Features

- 📸 Upload any photo (selfie, landscape, group shot)
- 🤖 Claude Vision AI analyzes: expression, background, lighting & mood
- 🎵 Get 3 Bollywood song recommendations with reasons
- 🎬 Get 3 Hollywood song recommendations with reasons
- 🎭 Full scene analysis + cinematic mood title
- 💅 Beautiful vintage cinema-themed UI

## 🚀 How to Run

### Option 1 — Direct (no setup needed)
Just open `index.html` in your browser. That's it!

> ⚠️ **Note:** The Anthropic API is called directly from the browser. This works when hosted via Claude.ai artifacts or a platform that injects the API key. For self-hosting, see Option 2.

### Option 2 — Self Host with your own API Key

1. Get your Anthropic API key from [console.anthropic.com](https://console.anthropic.com)
2. Open `index.html` and find this line in the `<script>` section:

```js
const response = await fetch('https://api.anthropic.com/v1/messages', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
```

3. Add your API key to the headers:

```js
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'YOUR_ANTHROPIC_API_KEY_HERE',
  'anthropic-version': '2023-06-01'
},
```

> ⚠️ **Security Warning:** Never expose your API key in public GitHub repos. Use a backend proxy or environment variables for production.

### Option 3 — GitHub Pages

1. Fork this repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Your site will be live at `https://yourusername.github.io/cinemood`

## 📁 File Structure

```
cinemood/
├── index.html   ← The entire app (single file)
└── README.md    ← This file
```

## 🛠️ Tech Stack

- Pure HTML + CSS + JavaScript (no frameworks, no build step)
- [Claude claude-sonnet-4-20250514 Vision API](https://docs.anthropic.com/en/docs/vision) for image analysis
- Google Fonts: Playfair Display, Libre Baskerville, Space Mono

## 📸 How It Works

1. You upload a photo
2. It's converted to base64 and sent to Claude's Vision API
3. Claude analyzes the facial expression, background, lighting, and overall vibe
4. Returns a JSON with mood, scene analysis, and 6 song recommendations
5. Results are rendered with a cinematic Bollywood/Hollywood split UI

## 🎨 Design

Vintage cinema aesthetic — dark background, gold typography, film strip borders, Bollywood pink vs Hollywood blue color split.

---

Made with ❤️ using Claude AI
