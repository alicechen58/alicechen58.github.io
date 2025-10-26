# 🔧 Fix URL and Styling Issues

## The Problem

Your site is currently showing at:
- ❌ `https://alicechen58.github.io/YuekunChen.github.io/` (with broken styling)

It should be:
- ✅ `https://alicechen58.github.io/` (with proper styling)

## The Cause

Your GitHub username is **alicechen58**, but your repository is named **YuekunChen.github.io**. This mismatch makes it a "project site" instead of a "user site", which:
1. Creates the long URL with the repo name in the path
2. Breaks CSS/asset loading because paths are incorrect

## The Fix (5 Minutes)

### Step 1: Rename Your Repository on GitHub

1. Go to: `https://github.com/alicechen58/YuekunChen.github.io`
2. Click **Settings** (top tabs)
3. Scroll to "Repository name"
4. Change from: `YuekunChen.github.io`
5. Change to: `alicechen58.github.io` ⚠️ **Must match your GitHub username exactly**
6. Click **Rename**
7. ⚠️ You'll be warned that your site URL will change - that's what we want!

### Step 2: Update Your Local Repository Remote

After renaming on GitHub, update your local git remote:

```bash
cd /Users/qiantaichen/Documents/GitHub/YuekunChen.github.io

# Update the remote URL
git remote set-url origin https://github.com/alicechen58/alicechen58.github.io.git

# Verify it worked
git remote -v
```

You should see:
```
origin  https://github.com/alicechen58/alicechen58.github.io.git (fetch)
origin  https://github.com/alicechen58/alicechen58.github.io.git (push)
```

### Step 3: Enable GitHub Actions Deployment

1. Go to: `https://github.com/alicechen58/alicechen58.github.io/settings/pages`
2. Under "Build and deployment" → **Source**
3. Select: **GitHub Actions** (not "Deploy from a branch")
4. Save

### Step 4: Push Your Changes

I've already updated the configuration files. Now push them:

```bash
git add .
git commit -m "Fix URL configuration and enable auto-deploy"
git push origin master
```

### Step 5: Wait for Deployment

1. Go to: `https://github.com/alicechen58/alicechen58.github.io/actions`
2. Watch the "Build and Deploy to GitHub Pages" workflow run (2-3 minutes)
3. Once it shows a green checkmark ✓, visit:
   - ✅ `https://alicechen58.github.io/`

## What I've Already Fixed

✅ Updated `_config.yml` with:
- Correct URL: `https://alicechen58.github.io`
- Correct baseurl: `""` (empty for user sites)
- Correct repository: `alicechen58/alicechen58.github.io`
- Correct GitHub username: `alicechen58`

✅ Updated all deployment documentation with correct URLs

✅ GitHub Actions workflow is ready to deploy

## After the Fix

Your site will be:
- ✅ Short, clean URL: `https://alicechen58.github.io/`
- ✅ Properly styled with all CSS and assets loading
- ✅ Auto-deploying on every push to master
- ✅ Looking like the Academic Pages template (image 2 you showed)

## Troubleshooting

**If styling still doesn't show after deployment:**

1. Hard refresh your browser (Ctrl+F5 or Cmd+Shift+R)
2. Clear browser cache
3. Check Actions tab for any errors in the build
4. Wait 5 minutes for CDN propagation

**If you prefer a different username in the URL:**

You'd need to either:
- Change your GitHub username to match, OR
- Create a GitHub organization with the desired name and transfer the repo there

---

**Questions?** Check if the workflow succeeded in the Actions tab first!

