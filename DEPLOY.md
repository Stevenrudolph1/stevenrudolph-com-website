# DigitalOcean Deployment Guide

## Quick Start

Your website is ready to deploy! Follow these steps:

### 1. Create GitHub Repository

1. Go to https://github.com/new
2. Create a new repository (e.g., `stevenrudolph-com`)
3. Don't initialize with README (we already have one)

### 2. Push to GitHub

Run these commands from the SR Website folder:

```bash
cd "/Users/stevenrudolph/Desktop/SR Website"
git remote add origin https://github.com/YOUR-USERNAME/stevenrudolph-com.git
git branch -M main
git push -u origin main
```

### 3. Deploy on DigitalOcean

1. Go to https://cloud.digitalocean.com/apps
2. Click "Create App"
3. Choose "GitHub" as source
4. Authorize DigitalOcean to access your repos
5. Select your `stevenrudolph-com` repository
6. DigitalOcean will auto-detect it as a **Static Site**
7. Configure:
   - **Name**: stevenrudolph-com
   - **Branch**: main
   - **Output Directory**: leave blank (root directory)
8. Click "Next" → "Next" → "Create Resources"

### 4. Custom Domain (Optional)

Once deployed, to use stevenrudolph.com:

1. In your app settings, go to "Domains"
2. Click "Add Domain"
3. Enter `stevenrudolph.com` and `www.stevenrudolph.com`
4. Update your domain's DNS settings:
   - Add CNAME record: `www` → `your-app.ondigitalocean.app`
   - Add A record: `@` → DigitalOcean's IP

### 5. Free Tier Info

DigitalOcean App Platform free tier includes:
- 3 static sites
- Free SSL certificates
- Automatic deployments from GitHub
- Custom domains supported

## Customizing Your Site

### Update Content

Edit `index.html`:
- Change the "About Me" section
- Update project descriptions
- Add your real contact links (email, GitHub, LinkedIn)

### Change Colors

Edit `style.css` and modify the `:root` variables:

```css
:root {
    --primary-color: #2563eb;  /* Your brand color */
    --secondary-color: #1e40af; /* Darker shade */
}
```

### Add Images

1. Create an `images` folder
2. Add your photos/screenshots
3. Reference them in HTML: `<img src="images/yourimage.jpg">`

## Updating Your Site

After making changes:

```bash
git add .
git commit -m "Update content"
git push
```

DigitalOcean will automatically rebuild and redeploy!

## Support

- DigitalOcean Docs: https://docs.digitalocean.com/products/app-platform/
- Community: https://www.digitalocean.com/community/

---

**Your site is ready! 🚀**


