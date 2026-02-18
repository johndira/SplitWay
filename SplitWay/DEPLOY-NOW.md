# 🚀 Deploy SplitWay to GitHub Pages

## Files Ready to Deploy

All files in this folder are ready to upload to GitHub:

- `index.html` — The complete app (with API key embedded)
- `README.md` — Project documentation
- `LICENSE` — MIT license
- `.gitignore` — Git ignore rules
- `DEPLOYMENT.md` — Detailed deployment guide

## Quick Deploy (5 Minutes)

### Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `splitway`
3. Make it **Public**
4. **DO NOT** initialize with README (we have one)
5. Click "Create repository"

### Step 2: Upload Files

**Option A: Upload via Web (Easiest)**

1. On your new repo page, click "uploading an existing file"
2. Drag ALL files from this folder into the upload area
3. Commit message: "Initial commit"
4. Click "Commit changes"

**Option B: Git Command Line**

```bash
cd /path/to/this/folder
git init
git add .
git commit -m "Initial commit: SplitWay with API key"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/splitway.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repo Settings
2. Click "Pages" in the left sidebar
3. Under "Source":
   - Branch: `main`
   - Folder: `/ (root)`
4. Click "Save"
5. Wait 1-2 minutes

### Step 4: Your App is Live!

Your app will be at:
```
https://YOUR-USERNAME.github.io/splitway/
```

## ✅ What Works

- ✅ Camera access (HTTPS from GitHub Pages)
- ✅ Receipt scanning with AI (your API key is embedded)
- ✅ All assignment features
- ✅ Tip calculator
- ✅ SMS payment requests
- ✅ Mobile optimized

## ⚠️ Important Warnings

### API Key is Public

Your API key is embedded in `index.html` and will be visible to anyone who:
- Views the page source (Right-click → View Page Source)
- Opens browser dev tools (F12 → Network tab)
- Downloads the HTML file

### What This Means

✅ **Good news:** You have no credit card, so no surprise charges
❌ **Bad news:** People can copy your key and use your free credits
⏱️ **Timeline:** Your free credits will probably drain in days/weeks

### When Credits Run Out

The app will show an error:
```
Unable to read receipt automatically
Error: API error 429: Rate limit exceeded
```

Users can still use "+ Add Item" to enter items manually.

## 🔄 When to Rotate Your Key

You should delete this key and create a new one when:
1. Your credits run low
2. You want to use the app yourself
3. You add a credit card to your Anthropic account

To rotate:
1. Go to https://console.anthropic.com/settings/keys
2. Delete key: `sk-ant-api03-dIiEFUv...`
3. Create new key
4. Replace in `index.html` line ~1640
5. Re-upload to GitHub

## 📱 Testing on Mobile

After deployment:
1. Visit your GitHub Pages URL on your phone
2. Allow camera access when prompted
3. Take a photo of a receipt
4. Watch it process and extract items automatically

## 🆘 Troubleshooting

**Receipt scanning doesn't work:**
- Check browser console (F12) for errors
- Verify you're on HTTPS (GitHub Pages URL)
- Try "+ Add Item" as fallback

**Camera doesn't work:**
- Grant camera permissions in browser
- Ensure you're using HTTPS
- Try a different browser

**App shows API error:**
- Free credits may be exhausted
- Check https://console.anthropic.com/settings/usage
- Use "+ Add Item" for manual entry

## 🎯 For Your Resume

Update your README with the live link after deployment:
```markdown
**[Live Demo](https://your-username.github.io/splitway/)**
```

Good luck! 🚀
