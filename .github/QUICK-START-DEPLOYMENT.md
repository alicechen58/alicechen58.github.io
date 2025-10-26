# Quick Start: GitHub Pages Auto-Deploy

## ⚡ 3-Step Setup

### 1. Enable GitHub Actions for Pages

Go to: `https://github.com/YuekunChen/YuekunChen.github.io/settings/pages`

Change **Source** to: **GitHub Actions** (instead of "Deploy from a branch")

![GitHub Pages Settings](https://docs.github.com/assets/cb-47267/mw-1440/images/help/pages/publishing-source-drop-down.webp)

### 2. Push Your Changes

```bash
git add .
git commit -m "Enable auto-deploy with GitHub Actions"
git push origin master
```

### 3. Watch It Deploy

1. Go to: `https://github.com/YuekunChen/YuekunChen.github.io/actions`
2. See "Build and Deploy to GitHub Pages" running
3. Wait ~3-5 minutes
4. Visit: `https://YuekunChen.github.io` ✨

## 🎯 That's It!

From now on, every push to `master` will automatically rebuild and deploy your site.

---

**Having issues?** See the full guide: [DEPLOYMENT.md](DEPLOYMENT.md)

