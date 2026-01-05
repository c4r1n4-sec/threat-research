# Setup Guide 🚀

## Step 1: Add Your Images

The markdown files reference images from your PDFs. Extract them and place them in the appropriate `/images` folders:

**RedLine-Stealer/images/**
- Network captures from Wireshark
- Hollows Hunter screenshots  
- dnSpy decompiled code
- etc.

**LockBit-3.0/images/**
- PowerShell dropper screenshots
- Ghidra analysis images
- CAPA/FLOSS outputs
- etc.

Check the `README.md` in each images folder for the full list.

## Step 2: Create GitHub Repo

1. Go to github.com/c4r1n4-sec
2. Click "New repository"
3. Name: `threat-research`
4. Make it **Public**
5. Do **NOT** initialize with README (you already have one)
6. Click "Create repository"

## Step 3: Push to GitHub via VS Code

1. Open VS Code
2. File → Open Folder → select the `threat-research` folder
3. Open Terminal (Terminal → New Terminal)
4. Run these commands:

```bash
git init
git add .
git commit -m "Initial commit: RedLine and LockBit analyses"
git branch -M main
git remote add origin https://github.com/c4r1n4-sec/threat-research.git
git push -u origin main
```

5. Sign in to GitHub when prompted

## Step 4: Verify

Go to https://github.com/c4r1n4-sec/threat-research

Your analyses should display directly on GitHub - people can read them without downloading anything.

## Adding New Analyses

When you finish Lumma Stealer or any other analysis:

1. Create a new folder: `mkdir Lumma-Stealer`
2. Create `Lumma-Stealer/README.md` with your analysis
3. Add images to `Lumma-Stealer/images/`
4. Update the main README.md to include the new analysis
5. Commit and push:

```bash
git add .
git commit -m "Added Lumma Stealer analysis"
git push
```

---

Your repo will be live at:
**https://github.com/c4r1n4-sec/threat-research**

This is what you'll share when Ian boosts your LinkedIn post.
