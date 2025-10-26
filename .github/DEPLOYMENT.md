# GitHub Pages Deployment Setup

This repository is configured for automatic deployment to GitHub Pages using GitHub Actions.

## How It Works

Every time you push commits to the `master` branch, GitHub Actions will:
1. Check out your repository
2. Set up Ruby and install Jekyll dependencies
3. Build your Jekyll site
4. Deploy the built site to GitHub Pages

## Initial Setup (One-Time Configuration)

To enable automatic deployments, you need to configure GitHub Pages in your repository settings:

### Step 1: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/alicechen58/alicechen58.github.io`
2. Click on **Settings** (top navigation)
3. Click on **Pages** (left sidebar under "Code and automation")
4. Under **Build and deployment**:
   - **Source**: Select **GitHub Actions** (not "Deploy from a branch")
5. Save the changes

### Step 2: Push Your Changes

Once GitHub Pages is configured to use GitHub Actions:

```bash
git add .
git commit -m "Add GitHub Actions deployment workflow"
git push origin master
```

### Step 3: Monitor Deployment

1. Go to the **Actions** tab in your GitHub repository
2. You'll see a workflow run called "Build and Deploy to GitHub Pages"
3. Click on it to see the build progress
4. Once complete (green checkmark ✓), your site will be live at:
   - `https://alicechen58.github.io`

## Workflow File

The deployment workflow is defined in:
```
.github/workflows/pages-deploy.yml
```

### What the Workflow Does

- **Triggers**: Runs automatically on every push to `master` branch
- **Build**: Compiles your Jekyll site with all plugins and content
- **Deploy**: Publishes the built site to GitHub Pages
- **Manual Run**: Can also be triggered manually from the Actions tab

### Build Environment

- **Ruby Version**: 3.1
- **Jekyll Plugins**: Automatically installs all gems from your `Gemfile`
- **GitHub Pages Gem**: Ensures compatibility with GitHub's environment

## Troubleshooting

### Site Not Updating After Push

1. Check the **Actions** tab for any failed workflow runs
2. Click on the failed run to see error logs
3. Common issues:
   - Missing dependencies in `Gemfile`
   - Syntax errors in markdown or YAML front matter
   - Broken links or missing files

### Build Fails

- Check that all files referenced in your markdown exist
- Verify YAML front matter syntax in all `.md` files
- Ensure all images and PDFs are committed to the repository

### Permission Errors

If you see permission errors in the Actions tab:
1. Go to **Settings** → **Actions** → **General**
2. Under "Workflow permissions", select **Read and write permissions**
3. Save and re-run the workflow

## Local Development

To test your site locally before pushing:

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve -l -H localhost

# View at http://localhost:4000
```

## Deployment Timeline

- **Commit → Push**: Instant
- **Build Time**: ~2-3 minutes
- **Propagation**: ~1-2 minutes
- **Total**: Your changes will be live in about 5 minutes after pushing

## Custom Domain (Optional)

To use a custom domain like `alicechen.com`:

1. Add a `CNAME` file to the repository root with your domain name
2. Configure DNS with your domain registrar
3. GitHub Pages will automatically use your custom domain

---

**Note**: The first deployment may take slightly longer as GitHub Pages sets up your environment. Subsequent deployments will be faster due to caching.

