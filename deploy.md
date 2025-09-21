# Netlify Deployment Guide

## Quick Deploy to Netlify

### Option 1: Connect GitHub Repository (Recommended)
1. Go to [Netlify](https://netlify.com)
2. Click "New site from Git"
3. Connect your GitHub account
4. Select your repository
5. Netlify will automatically detect Vite settings:
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
6. Click "Deploy site"

### Option 2: Drag & Drop Deploy
1. Run `npm run build` locally
2. Go to [Netlify](https://netlify.com)
3. Drag the `dist` folder to the deploy area

### Option 3: Netlify CLI
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login to Netlify
netlify login

# Deploy
netlify deploy --prod --dir=dist
```

## Environment Variables (if needed)
If you need environment variables:
1. Go to Site settings > Environment variables
2. Add your variables (e.g., `VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY`)

## Custom Domain
1. Go to Site settings > Domain management
2. Add your custom domain
3. Configure DNS settings as instructed

## Build Settings
The `netlify.toml` file is already configured with:
- ✅ Build command: `npm run build`
- ✅ Publish directory: `dist`
- ✅ Node.js version: 20
- ✅ SPA redirects
- ✅ Security headers
- ✅ Cache optimization

## Automatic Deploys
Once connected to GitHub:
- ✅ Every push to main branch = automatic deploy
- ✅ Pull requests = preview deploys
- ✅ Branch deploys for testing

## Performance Optimizations
- ✅ Static assets cached for 1 year
- ✅ Gzip compression enabled
- ✅ CDN distribution worldwide
- ✅ HTTP/2 support
