# GitHub Desktop Setup Guide - Meter Analyzer

## Step 1: Copy Files to Your Local Repo

1. **Download these 3 files** from the links provided:
   - `index.html` - Landing page
   - `meter_half_hourly_chart.html` - Meter analyzer app
   - `README.md` - Documentation

2. **Paste all 3 files** into your repo folder:
   ```
   C:\Users\willi\OneDrive\Documents\GitHub\meteranalizer
   ```

3. **Confirm** the files are there alongside existing files (README.md, meter_half_hourly_chart.html)

---

## Step 2: Open GitHub Desktop

1. Open **GitHub Desktop**
2. Make sure **meteranalyzer** repo is selected (top-left dropdown)

---

## Step 3: Stage & Commit Changes

GitHub Desktop should automatically detect the new/updated files:

1. **Left panel** will show:
   - ✅ index.html (new)
   - ✅ meter_half_hourly_chart.html (modified)
   - ✅ README.md (new or modified)

2. All should be **checked/selected** by default

3. **Bottom-left**, enter commit message:
   ```
   Add web app with landing page and documentation
   ```

4. Click **"Commit to main"**

---

## Step 4: Push to GitHub

1. Click **"Push origin"** button (top-right area)
2. Wait for it to complete (should take 5-10 seconds)
3. You should see a confirmation message

---

## Step 5: Enable GitHub Pages (Manual Step Required)

**YOU MUST DO THIS MANUALLY - Cannot be automated:**

1. **Go to GitHub website**: https://github.com/williamgagiano-droid/meteranalyzer

2. Click **Settings** tab

3. Scroll down left sidebar to **"Pages"**

4. Under "Build and deployment":
   - Source: Select **"Deploy from a branch"** (if not already selected)
   - Branch: Select **"main"** 
   - Folder: Select **"/ (root)"**

5. Click **Save**

6. Wait 1-2 minutes for GitHub to process

7. You'll see a green box with:
   ```
   ✅ Your site is published at:
   https://williamgagiano-droid.github.io/meteranalyzer/
   ```

---

## Step 6: Test Your Live App

1. Open your browser
2. Visit: **https://williamgagiano-droid.github.io/meteranalyzer/**
3. You should see the beautiful landing page
4. Click "Open Analyzer →" to test the meter tool
5. Upload your CSV and verify it works!

---

## Done! 🎉

Your meter analyzer is now live on the web!

**Summary of what you did:**
- ✅ Added 3 files to your local repo
- ✅ Committed changes in GitHub Desktop
- ✅ Pushed to GitHub
- ✅ Enabled GitHub Pages (manual)
- ✅ Meter analyzer is now a live web app!

**Your app URL**: https://williamgagiano-droid.github.io/meteranalyzer/

---

## Troubleshooting

**If you get "404 - Page not found":**
- Wait a few more minutes (GitHub needs time to deploy)
- Hard refresh (Ctrl+Shift+R on Windows)
- Check that Pages is enabled in Settings

**If changes don't appear:**
- Hard refresh your browser (Ctrl+Shift+R)
- Clear browser cache
- Wait 2-3 minutes for GitHub Pages to rebuild

**If GitHub Desktop shows "Please pull from origin":**
- Click "Pull origin" first before pushing

---

**Next time you update the app:**
1. Edit files locally
2. GitHub Desktop will detect changes
3. Commit & Push (no Pages setup needed again!)
4. Changes live in 1-2 minutes
