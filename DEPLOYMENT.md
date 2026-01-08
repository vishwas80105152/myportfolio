# Netlify Deployment Guide

## Quick Deploy Steps

### 1. Push Changes to GitHub
The project is now configured for Netlify. Commit and push the changes:

```bash
git add .
git commit -m "Configure for Netlify deployment"
git push origin main
```

### 2. Deploy on Netlify

1. Go to [Netlify](https://app.netlify.com)
2. Click **"Add new site"** → **"Import an existing project"**
3. Connect to GitHub and select your repository: `vishwas80105152/myportfolio`
4. Netlify will auto-detect the build settings from `netlify.toml`:
   - Build command: `npm run build`
   - Publish directory: `build`
5. Click **"Show advanced"** and add environment variables:
   - `REACT_APP_GITHUB_TOKEN` = Your GitHub personal access token
   - `GITHUB_USERNAME` = `vishwas80105152` (or your GitHub username)
   - `USE_GITHUB_DATA` = `true`
   - `MEDIUM_USERNAME` = Your Medium username (optional)
6. Click **"Deploy site"**

### 3. Get Your GitHub Token (if needed)

1. Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate new token (classic)
3. No scopes needed - just generate a simple token
4. Copy and paste it into Netlify environment variables

### 4. Your Site Will Be Live!

Netlify will provide you with a URL like: `https://your-site-name.netlify.app`

Every time you push to GitHub, Netlify will automatically rebuild and deploy your site!
