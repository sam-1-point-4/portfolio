# Complete Deployment Guide

## Step 2: Deploy to GitHub Pages (FREE)

### Prerequisites
- GitHub account (free)
- Git installed on your computer
- Your website tested locally and working

### Part A: Push to GitHub

1. **Create a new repository on GitHub**
   - Go to https://github.com
   - Click the "+" icon → "New repository"
   - Name it: `anish-sam-paul.github.io` (or any name you prefer)
   - Make it **Public**
   - Do NOT initialize with README (we already have one)
   - Click "Create repository"

2. **Initialize Git in your project folder**
   ```bash
   cd anish-portfolio
   git init
   git add .
   git commit -m "Initial commit: Portfolio website"
   ```

3. **Connect to GitHub and push**
   ```bash
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/anish-sam-paul.github.io.git
   git push -u origin main
   ```
   
   Replace `YOUR-USERNAME` with your actual GitHub username.

### Part B: Enable GitHub Pages

1. **Go to your repository on GitHub**
   - Navigate to your repository page

2. **Configure GitHub Pages**
   - Click "Settings" tab
   - Scroll down to "Pages" in the left sidebar
   - Under "Source", select:
     - Branch: `main`
     - Folder: `/ (root)`
   - Click "Save"

3. **Wait for deployment**
   - GitHub will show: "Your site is ready to be published at..."
   - Wait 1-3 minutes
   - Your site will be live at: `https://YOUR-USERNAME.github.io/repository-name/`
   - If you named it `anish-sam-paul.github.io`, it will be at: `https://YOUR-USERNAME.github.io/`

4. **Verify deployment**
   - Click the provided URL
   - Your portfolio should now be live!

---

## Step 3: Connect Custom Domain from Namecheap

### Part A: Buy Domain on Namecheap

1. Go to Namecheap.com
2. Search for your desired domain (e.g., `anishsampaul.com`)
3. Purchase the domain (usually $8-15/year)

### Part B: Configure DNS on Namecheap

1. **Log in to Namecheap**
   - Go to Dashboard → Domain List
   - Click "Manage" next to your domain

2. **Update DNS Settings**
   - Go to "Advanced DNS" tab
   - Add the following records:

   **A Records** (Add 4 records):
   ```
   Type: A Record
   Host: @
   Value: 185.199.108.153
   TTL: Automatic

   Type: A Record
   Host: @
   Value: 185.199.109.153
   TTL: Automatic

   Type: A Record
   Host: @
   Value: 185.199.110.153
   TTL: Automatic

   Type: A Record
   Host: @
   Value: 185.199.111.153
   TTL: Automatic
   ```

   **CNAME Record** (for www):
   ```
   Type: CNAME Record
   Host: www
   Value: YOUR-USERNAME.github.io.
   TTL: Automatic
   ```

3. **Save all records**
   - Click "Save All Changes"
   - DNS changes can take 5-48 hours to propagate (usually 1-2 hours)

### Part C: Configure Custom Domain on GitHub

1. **Go to your GitHub repository**
   - Click "Settings" → "Pages"

2. **Add custom domain**
   - Under "Custom domain", enter your domain: `anishsampaul.com`
   - Click "Save"

3. **Create CNAME file**
   - GitHub should automatically create a CNAME file in your repository
   - Or create it manually:
     ```bash
     echo "anishsampaul.com" > CNAME
     git add CNAME
     git commit -m "Add custom domain"
     git push
     ```

4. **Enable HTTPS** (wait 10-20 minutes after DNS propagates)
   - Go back to Settings → Pages
   - Check "Enforce HTTPS" (this might take some time to become available)
   - Wait for the SSL certificate to be issued (automatic and free)

5. **Verify your website**
   - Visit `https://anishsampaul.com`
   - Visit `https://www.anishsampaul.com`
   - Both should work and redirect to HTTPS

---

## Alternative: Deploy to Netlify (Also FREE)

If you prefer Netlify over GitHub Pages:

### Option 1: Deploy via Drag & Drop

1. Go to https://app.netlify.com/drop
2. Drag your entire `anish-portfolio` folder
3. Netlify will give you a URL: `random-name.netlify.app`
4. Go to "Domain settings" → Add custom domain
5. Follow DNS instructions (similar to above, but different IP addresses)

### Option 2: Deploy via Git

1. Push your code to GitHub (as above)
2. Sign up at Netlify.com
3. Click "New site from Git"
4. Connect to GitHub
5. Select your repository
6. Deploy settings:
   - Build command: (leave empty)
   - Publish directory: `/`
7. Click "Deploy site"

---

## Step 4: Updating Your Website

Whenever you want to update your portfolio:

1. **Make changes locally**
   - Edit your HTML, CSS, or JS files
   - Test locally to make sure everything works

2. **Push changes to GitHub**
   ```bash
   git add .
   git commit -m "Update: describe your changes"
   git push
   ```

3. **Automatic deployment**
   - GitHub Pages will automatically rebuild your site
   - Changes will be live in 1-2 minutes
   - Visit your website to see the updates

---

## Maintenance & Monitoring

### Keep Your Site Running

1. **Regular Updates**
   - Update your work experience as you progress
   - Add new projects and skills
   - Keep your CV updated

2. **Monitor Uptime**
   - GitHub Pages has 99.9% uptime
   - No action needed from you

3. **Analytics (Optional)**
   - Add Google Analytics for free
   - Track visitors and page views
   - Insert tracking code in `<head>` of index.html

4. **Backups**
   - Your code is already backed up on GitHub
   - Download a local copy periodically

### Costs Summary

- **GitHub Pages**: FREE forever
- **Custom Domain**: $8-15/year (Namecheap)
- **SSL Certificate**: FREE (automatically provided)
- **Total Annual Cost**: Just the domain ($8-15)

---

## Troubleshooting

### Common Issues

**Site not loading after deployment**
- Wait 1-3 minutes after deploying
- Clear your browser cache
- Try incognito/private mode

**Custom domain not working**
- Check DNS propagation: https://dnschecker.org
- Wait 24-48 hours for DNS to fully propagate
- Verify DNS records are correct on Namecheap

**Images not showing**
- Check file paths are correct and case-sensitive
- Make sure images exist in `assets/images/`
- Check browser console for errors (F12)

**Mobile layout broken**
- Test on different screen sizes
- Check CSS media queries
- Use browser dev tools (F12) → Toggle device toolbar

### Getting Help

- GitHub Pages Status: https://www.githubstatus.com
- GitHub Pages Docs: https://docs.github.com/pages
- Namecheap Support: https://www.namecheap.com/support/

---

## Adding to LinkedIn

Once your site is live:

1. **Update LinkedIn Profile**
   - Go to your LinkedIn profile
   - Click "Add profile section"
   - Select "Contact info"
   - Add your website URL
   - Save changes

2. **Share on LinkedIn**
   - Create a post announcing your new portfolio
   - Include the link
   - Add relevant hashtags: #DataAnalyst #Portfolio #BI

3. **Add to Email Signature**
   - Include your portfolio URL
   - Example: "View my portfolio: https://anishsampaul.com"

---

## Success Checklist

- [ ] Code tested locally
- [ ] Repository created on GitHub
- [ ] Code pushed to GitHub
- [ ] GitHub Pages enabled
- [ ] Site accessible via GitHub URL
- [ ] Domain purchased on Namecheap
- [ ] DNS records configured
- [ ] Custom domain added to GitHub
- [ ] HTTPS enabled
- [ ] Site accessible via custom domain
- [ ] Both www and non-www work
- [ ] Profile photo added
- [ ] CV PDF added and downloadable
- [ ] All links work correctly
- [ ] Mobile responsive verified
- [ ] Added to LinkedIn profile

**Congratulations! Your portfolio is now live! 🎉**