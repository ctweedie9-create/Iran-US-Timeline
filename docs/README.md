# 🔴 Iran–US Conflict Intelligence Timeline

Live-updating, multi-source conflict intelligence tracker covering the 2025–2026 Iran–US war.
Auto-refreshes every 3 minutes from 12 RSS feeds across Global, Australian and NSW sources.

---

## ⚡ Quick Deploy (GitHub Pages — Free)

### Step 1 — Create your GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Name it `iran-timeline` (or any name you prefer)
3. Set it to **Public** (required for free GitHub Pages)
4. Click **Create repository**

---

### Step 2 — Upload the files

**Option A — GitHub web interface (easiest, no Git required)**

1. In your new repo, click **Add file → Upload files**
2. Upload this entire folder structure:
   ```
   docs/
     index.html
   .github/
     workflows/
       deploy.yml
   README.md
   ```
3. Commit directly to `main`

**Option B — Git command line**

```bash
git clone https://github.com/YOUR_USERNAME/iran-timeline.git
cd iran-timeline
# Copy all files from this package into the folder
git add .
git commit -m "Initial deploy: Iran-US conflict timeline"
git push origin main
```

---

### Step 3 — Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **GitHub Actions**
3. Click **Save**

The GitHub Action will run automatically on every push. First deploy takes ~60 seconds.

---

### Step 4 — Access your live URL

Your site will be live at:
```
https://YOUR_USERNAME.github.io/iran-timeline/
```

Share this URL with any team, agency, or organisation — no login required.

---

## 🔒 Multi-Agency Access Control (Optional)

For restricted access per agency, add **Cloudflare Access** (free tier) in front:

1. Add your GitHub Pages domain to Cloudflare (free)
2. Go to **Zero Trust → Access → Applications**
3. Add an application, set the domain, and create policies by email domain:
   - e.g. `@agency1.gov.au` → full access
   - e.g. `@partner.org` → read access
4. Each agency can be given a separate subdomain with its own policy

This is completely free under Cloudflare's free tier.

---

## 📡 RSS Feed Sources

| Feed | Region | Type |
|------|--------|------|
| Reuters World | Global | Wire |
| BBC World | Global | Broadcast |
| Al Jazeera | Global | Broadcast |
| The Guardian World | Global | Press |
| AP News | Global | Wire |
| CFR Global Conflict | Global | Think Tank |
| ABC Australia | Australia | Broadcast |
| Sydney Morning Herald | Australia | Press |
| The Australian | Australia | Press |
| ABC NSW | NSW | Broadcast |
| SMH NSW | NSW | Press |
| Daily Telegraph NSW | NSW | Press |

---

## 🔄 Update Frequency

- **Auto-refresh**: Every 3 minutes (configurable — change `REFRESH_INTERVAL` in `index.html`)
- **CORS Proxy**: Uses `allorigins.win` — free, no API key required
- **Relevance filter**: Only Iran/Hormuz/nuclear/conflict-related articles surface

---

## 📋 Event Types

Historical events are pre-seeded (2018–present) covering:
`Military` · `Diplomatic` · `Nuclear` · `Political` · `Economic` · `Civil Unrest` · `Human Rights` · `Government`

---

## 🛠 Customisation

All configuration is at the top of `docs/index.html`:

- `RSS_FEEDS` — add/remove/change feeds
- `HISTORICAL_EVENTS` — add new archived events
- `REFRESH_INTERVAL` — change auto-refresh timing (milliseconds)
- `RELEVANCE_PATTERN` — adjust the keyword filter for live feed items

No build tools, no npm, no dependencies to install. Edit and push — that's it.

---

## 📄 Licence

For internal intelligence and situational awareness use. All news content sourced from respective publishers via RSS.
