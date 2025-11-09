# Quick Start Guide - 15 Minutes to Live Portfolio

## 🚀 Fast Track Deployment

### Step 1: Setup (5 minutes)

```bash
# Create project folder
mkdir anish-portfolio
cd anish-portfolio

# Create file structure
mkdir -p css js assets/images assets/files

# Copy all files from the artifacts:
# - index.html (root)
# - css/style.css
# - js/main.js
# - .gitignore
# - README.md

# Add your photo (name it profile.jpg)
# Copy to: assets/images/profile.jpg

# Add your CV (name it Anish_Sam_Paul_Resume.pdf)
# Copy to: assets/files/Anish_Sam_Paul_Resume.pdf
```

### Step 2: Test Locally (2 minutes)

```bash
# Using Python
python -m http.server 8000

# Visit: http://localhost:8000
# Verify everything looks good
```

### Step 3: Deploy to GitHub (5 minutes)

```bash
# Initialize Git
git init
git add .
git commit -m "Initial commit"

# Create repo on GitHub (via web interface):
# Name: anish-sam-paul.github.io

# Push to GitHub
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/anish-sam-paul.github.io.git
git push -u origin main

# Enable GitHub Pages:
# GitHub → Settings → Pages → Source: main branch → Save
```

**Your site is now live at:**
`https://YOUR-USERNAME.github.io/`

### Step 4: Custom Domain (3 minutes)

**On Namecheap:**
1. Buy domain: `anishsampaul.com`
2. Advanced DNS → Add A Records:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
3. Add CNAME: `www` → `YOUR-USERNAME.github.io.`

**On GitHub:**
1. Settings → Pages → Custom domain: `anishsampaul.com`
2. Save
3. Wait 30-60 minutes
4. Enable HTTPS

**Done! Your portfolio is live at your custom domain! 🎉**

---

## 📋 Pre-Deployment Checklist

- [ ] Install Git
- [ ] Create GitHub account
- [ ] Have profile photo ready (JPG/PNG)
- [ ] Have CV PDF ready
- [ ] Choose domain name
- [ ] Have credit card ready for domain purchase

---

## 🔥 Common Commands

**Local testing:**
```bash
python -m http.server 8000
```

**Update website:**
```bash
git add .
git commit -m "Update content"
git push
```

**Check Git status:**
```bash
git status
```

---

## 💡 Tips

1. **Test Everything Locally First**
   - All links work
   - Images load
   - Mobile responsive
   - No console errors (F12)

2. **Commit Often**
   - Make small, frequent commits
   - Write clear commit messages
   - Push after each major change

3. **Use Meaningful Commit Messages**
   - ✅ "Update work experience with current role"
   - ❌ "Update stuff"

4. **Keep it Updated**
   - Update every 3-6 months
   - Add new projects
   - Refresh content

---

## 🆘 Emergency Fixes

**Site is broken after update:**
```bash
# Revert to last working version
git log  # Find last good commit hash
git reset --hard <commit-hash>
git push --force
```

**Wrong file committed:**
```bash
git rm <filename>
git commit -m "Remove incorrect file"
git push
```

**Need to start over:**
```bash
# Delete everything and re-clone
rm -rf .git
git init
# Start fresh
```

---

## 📱 Mobile Testing

Test on multiple screen sizes:
- iPhone (375px)
- iPad (768px)
- Desktop (1200px+)

Use Chrome DevTools (F12) → Toggle Device Toolbar

---

## 🎯 Next Steps After Launch

1. **Share your portfolio:**
   - Add to LinkedIn
   - Add to email signature
   - Share on social media

2. **Monitor performance:**
   - Google PageSpeed Insights
   - Check mobile responsiveness
   - Test all links monthly

3. **Enhance over time:**
   - Add blog section
   - Add project gallery
   - Integrate contact form
   - Add testimonials

4. **Keep learning:**
   - Experiment with new features
   - Stay updated with web trends
   - Gather feedback and improve

---

**Need Help?**
- Check DEPLOYMENT_GUIDE.md for detailed instructions
- Check README.md for customization tips
- Search on Stack Overflow for specific issues