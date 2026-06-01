# ⚡ GANESH R — GitHub Profile Setup Guide
## NexusGrid Labs · Cyberpunk Founder OS v2.0

---

## 📁 Repository Structure

```
GaneshRamesh2004/          ← Your special profile repo (username matches GitHub)
├── README.md              ← Main profile page (THE cyberpunk dashboard)
├── .last-updated          ← Auto-generated heartbeat file
├── .github/
│   └── workflows/
│       ├── snake.yml          ← Contribution snake animation
│       ├── metrics.yml        ← GitHub metrics generation
│       └── update-profile.yml ← Auto-update heartbeat
└── SETUP.md               ← This file
```

---

## 🚀 Step-by-Step Setup

### STEP 1 — Create the Special Profile Repository

1. Go to **github.com/new**
2. Set repository name to exactly: **`GaneshRamesh2004`** (must match your GitHub username)
3. Set to **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

> ⚡ GitHub automatically detects this as your profile repo and displays README.md on your profile.

---

### STEP 2 — Upload Files

**Option A — GitHub Web UI (Easiest):**
1. Go to your new `GaneshRamesh2004` repository
2. Click **"Add file"** → **"Upload files"**
3. Upload the entire `.github/` folder and `README.md`
4. Commit to `main` branch

**Option B — Git CLI:**
```bash
# Clone your new profile repo
git clone https://github.com/GaneshRamesh2004/GaneshRamesh2004.git
cd GaneshRamesh2004

# Copy all files from this package into it
cp -r /path/to/this/package/. .

# Push
git add .
git commit -m "⚡ init: cyberpunk founder profile v2.0"
git push origin main
```

---

### STEP 3 — Set Up GitHub Secrets (Required for Metrics)

Go to your profile repo → **Settings** → **Secrets and variables** → **Actions** → **New repository secret**

| Secret Name | Value | Required For |
|---|---|---|
| `GITHUB_TOKEN` | Auto-provided by GitHub | Snake, Auto-update |
| `METRICS_TOKEN` | Personal Access Token (see below) | Metrics workflow |

**To create `METRICS_TOKEN`:**
1. Go to **github.com/settings/tokens**
2. Click **"Generate new token (classic)"**
3. Name it: `METRICS_TOKEN`
4. Select scopes: `read:user`, `repo`, `read:org`
5. Generate and copy the token
6. Paste as the secret value

---

### STEP 4 — Enable GitHub Actions

1. Go to your repo → **Actions** tab
2. If prompted, click **"I understand my workflows, go ahead and enable them"**
3. Manually trigger each workflow once:
   - Click **🐍 Generate Contribution Snake** → **Run workflow**
   - Click **📊 Update GitHub Metrics** → **Run workflow**
   - Click **⚡ Auto Update Profile** → **Run workflow**

---

### STEP 5 — Create the `output` Branch (for Snake)

The snake workflow pushes SVGs to an `output` branch. After the first snake run:
1. The `output` branch is auto-created
2. The README already references:
   ```
   https://raw.githubusercontent.com/GaneshRamesh2004/GaneshRamesh2004/output/github-snake-dark.svg
   ```
3. This will auto-populate once the workflow runs ✅

---

### STEP 6 — Verify Everything Works

After running all workflows, your profile should show:

- ✅ **Animated hero banner** (capsule-render)
- ✅ **Typing SVG** animation
- ✅ **GitHub stats** cards (dark theme)
- ✅ **Streak stats** widget
- ✅ **Activity graph** with neon styling
- ✅ **Trophy wall** (darkhub theme)
- ✅ **Contribution snake** (animated SVG)
- ✅ **Summary cards** (4 cards)
- ✅ **Profile view counter** (komarev)

---

## 🔧 Customization

### Update Colors
The profile uses this cyberpunk palette:
```
Primary Green  : #00ff41  (Matrix green)
Electric Blue  : #00b4d8  (Neon cyan)
Deep Purple    : #7b2ff7  (Neon violet)
Burning Orange : #FF6B35  (Startup orange)
Dark Base      : #0d0d0d  (Near black)
```

### Change Themes
- Stats cards: change `theme=chartreuse-dark` to any [supported theme](https://github.com/anuraghazra/github-readme-stats/blob/master/themes/README.md)
- Streak: change `theme=dark` to match
- Activity graph: customize `bg_color`, `color`, `line`, `point`

### Add Real Project Links
In the **FEATURED DEPLOYMENTS** section, replace:
```markdown
[![NexusGrid](https://img.shields.io/badge/...)](https://github.com/GaneshRamesh2004)
```
With actual repo links:
```markdown
[![NexusGrid](https://img.shields.io/badge/...)](https://github.com/GaneshRamesh2004/your-repo-name)
```

---

## 🛠️ Troubleshooting

| Issue | Fix |
|---|---|
| Snake SVG not showing | Wait for workflow to run, check `output` branch exists |
| Stats showing "Not Found" | Check username is exactly `GaneshRamesh2004` |
| Metrics workflow failing | Verify `METRICS_TOKEN` secret is set correctly |
| Images not loading | Some services may be temporarily down; try again in 1-2 hours |
| Actions not running | Go to Settings → Actions → Allow all actions |

---

## 📡 External Services Used

| Service | URL | Purpose |
|---|---|---|
| capsule-render | capsule-render.vercel.app | Animated banners |
| readme-typing-svg | readme-typing-svg.demolab.com | Typing animation |
| github-readme-stats | github-readme-stats.vercel.app | Stats cards |
| github-readme-streak-stats | github-readme-streak-stats.herokuapp.com | Streak widget |
| github-readme-activity-graph | github-readme-activity-graph.vercel.app | Activity graph |
| github-profile-trophy | github-profile-trophy.vercel.app | Trophy wall |
| github-profile-summary-cards | github-profile-summary-cards.vercel.app | Summary cards |
| komarev profile views | komarev.com/ghpvc | View counter |
| shields.io | shields.io | All badges |

---

## ⚡ Made by Ganesh R — NexusGrid Labs
**github.com/GaneshRamesh2004 · ganeshr2004231@gmail.com**
