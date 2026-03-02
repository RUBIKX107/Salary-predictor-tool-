# Salary-predictor-tool-

AI-powered salary prediction using Claude (Anthropic API). Single HTML file, no frameworks, no build tools.

---

## Project Structure

```
salary-predictor/
├── index.html      ← Full app (HTML + CSS + JS)
└── README.md       ← This file
```

---

## Run Locally

**Step 1 — Clone**
```bash
git clone https://github.com/YOUR_USERNAME/salary-predictor.git
cd salary-predictor
```

**Step 2 — Add your API Key**

Open `index.html` in any text editor. Find this block (around line 205):

```js
headers: { "Content-Type": "application/json" },
```

Replace it with:

```js
headers: {
  "Content-Type": "application/json",
  "x-api-key": "sk-ant-YOUR_KEY_HERE",
  "anthropic-version": "2023-06-01",
  "anthropic-dangerous-direct-browser-access": "true"
},
```

Get your key at: https://console.anthropic.com/

**Step 3 — Open in browser**
```bash
# Just double-click index.html  OR run a local server:
python -m http.server 8080
# then visit http://localhost:8080
```

---

## How It Works

1. Fill in: Role, Industry, Location, Experience, Education, Skills
2. Hits Claude API with your profile
3. Claude returns JSON: salary range + market analysis + factor tags
4. App renders animated results

---

## Tech Stack

- Vanilla HTML / CSS / JS (zero dependencies, zero build step)
- Anthropic Claude claude-sonnet-4-20250514
- Google Fonts (Syne + DM Mono)
