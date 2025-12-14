# 🐾 Sunnymead Animal Hospital Website - Owner's Guide

Welcome! This guide will help you set up and maintain your new website. Don't worry if you're new to this - we'll go step by step.

---

## Table of Contents

1. [Getting Your Website Online](#1-getting-your-website-online)
2. [Connecting Your Domain](#2-connecting-your-domain)
3. [Making Changes to Your Website](#3-making-changes-to-your-website)
4. [Common Updates](#4-common-updates)
5. [File Structure](#5-file-structure)
6. [Getting Help](#6-getting-help)

---

## 1. Getting Your Website Online

### Step 1: Create a GitHub Account

1. Go to [github.com](https://github.com)
2. Click **"Sign up"**
3. Follow the prompts to create your free account
4. Verify your email address

### Step 2: Copy (Fork) This Website to Your Account

1. Go to the original repository (the link you were given)
2. Click the **"Fork"** button in the top-right corner
3. Click **"Create fork"**
4. You now have your own copy of the website!

### Step 3: Turn on GitHub Pages

1. In your new repository, click **"Settings"** (the gear icon tab)
2. In the left sidebar, click **"Pages"**
3. Under "Source", select **"Deploy from a branch"**
4. Under "Branch", select **"main"** and **"/ (root)"**
5. Click **"Save"**
6. Wait 2-3 minutes, then refresh the page
7. You'll see a green box with your website URL!

### Step 4: Enable HTTPS (Secure Connection)

1. On the same Pages settings page, find **"Enforce HTTPS"**
2. Check the box ✅
3. Your site is now secure!

---

## 2. Connecting Your Domain

If you want to use your own domain (like `www.sunnymeadanimal.com`):

### Step 1: Add Your Domain in GitHub

1. Go to **Settings** → **Pages**
2. Under "Custom domain", type your domain (e.g., `www.sunnymeadanimal.com`)
3. Click **"Save"**

### Step 2: Update Your Domain's DNS Settings

You'll need to log into wherever you bought your domain (GoDaddy, Namecheap, Google Domains, etc.) and add these settings:

**For www.yourdomain.com:**
- Add a **CNAME record**:
  - Name/Host: `www`
  - Value/Points to: `YOUR-GITHUB-USERNAME.github.io`

**For yourdomain.com (without www):**
- Add these **A records**:
  - Name/Host: `@`
  - Value: `185.199.108.153`
  - Value: `185.199.109.153`
  - Value: `185.199.110.153`
  - Value: `185.199.111.153`

### Step 3: Wait

DNS changes can take anywhere from 10 minutes to 48 hours to take effect. Be patient!

### Step 4: Enable HTTPS Again

Once your domain is connected, go back to **Settings** → **Pages** and check **"Enforce HTTPS"** again.

---

## 3. Making Changes to Your Website

### Option A: Edit Directly on GitHub (Easiest)

1. Go to your repository on GitHub
2. Navigate to the file you want to edit (e.g., `index.html`)
3. Click the **pencil icon** ✏️ to edit
4. Make your changes
5. Scroll down and click **"Commit changes"**
6. Add a brief description of what you changed
7. Click **"Commit changes"** again
8. Wait 1-2 minutes for your site to update

### Option B: Download and Edit on Your Computer

1. Click the green **"Code"** button
2. Click **"Download ZIP"**
3. Extract the files on your computer
4. Edit with any text editor (Notepad++, VS Code, or even regular Notepad)
5. To upload changes:
   - On GitHub, navigate to the file
   - Click the pencil icon
   - Delete all content
   - Paste your new content
   - Commit the changes

---

## 4. Common Updates

### Changing Business Hours

Edit `index.html` and search for "8am" or "Mon-Fri". You'll find the hours in several places:
- Hero section stats
- Footer

Also update in: `location.html`, `contact.html`, `cats.html`, `employment.html`

### Changing Phone Number

Search for `951-242-3118` and replace with your new number. This appears in:
- Navigation
- Hero section
- Contact section
- Footer
- All service pages

### Updating the Address

Search for `24537 Sunnymead` and update. Found in:
- Contact section
- Footer
- Location page

### Adding a New Team Member

In `index.html`, find the "Team Section" (search for `team-card-full`). Copy an existing team card and modify the name, photo, and bio.

### Changing a Service Description

Go to the `services/` folder and open the relevant file (e.g., `wellness.html`). The main content is in the `<section class="service-detail">` area.

### Updating Employment Listings

Edit `employment.html`. Each job is in a `<div class="job-listing">` section. You can:
- Modify existing listings
- Copy a listing to add a new job
- Delete a listing to remove a job

### Changing the Online Pharmacy Link

Search for `sunnymeadanimalhospital.securevetsource.com` in `index.html` and update the URL.

---

## 5. File Structure

Here's what each file does:

```
sunnymead-vet/
│
├── index.html          ← Homepage (most important!)
├── location.html       ← Location page with map
├── contact.html        ← Contact information page
├── cats.html           ← Cat-friendly amenities page
├── employment.html     ← Job listings page
│
├── services/           ← Individual service pages
│   ├── wellness.html
│   ├── vaccinations.html
│   ├── surgery.html
│   └── ... (14 total)
│
├── css/
│   └── style.css       ← All the styling (colors, fonts, layout)
│
├── js/
│   └── main.js         ← Interactive features (menus, animations)
│
├── images/             ← All photos and the logo
│   ├── uAulYoN4UcwQ.png  ← Your logo
│   ├── dr-ontiveros.jpg
│   ├── dr-lauro.jpg
│   └── ...
│
└── CNAME               ← Your custom domain (if using one)
```

---

## 6. Getting Help

### If Something Breaks

1. **Don't panic!** GitHub keeps a history of all changes
2. Go to your repository → click **"commits"**
3. Find a commit from before the problem
4. Click on it, then click **"Browse files"**
5. You can see what the files looked like before

### Common Problems

**"My changes aren't showing up"**
- Wait 2-3 minutes - GitHub needs time to rebuild the site
- Try a hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Clear your browser cache

**"My images aren't showing"**
- Make sure the image filename matches exactly (including capitals)
- Images should be in the `images/` folder
- In your HTML, the path should be `images/filename.jpg`

**"The site looks weird/broken"**
- Check that you didn't accidentally delete any HTML tags
- Every `<div>` needs a closing `</div>`
- Every `<p>` needs a closing `</p>`

### Learning Resources

- [HTML Basics](https://www.w3schools.com/html/) - W3Schools is beginner-friendly
- [GitHub Docs](https://docs.github.com/en/pages) - Official GitHub Pages help

---

## Quick Reference Card

| To do this... | Do this... |
|--------------|------------|
| Edit a page | GitHub → find file → click ✏️ pencil |
| See your site | Go to Settings → Pages → click the URL |
| Update hours | Search for "8am" in index.html |
| Update phone | Search for "242-3118" |
| Add an image | Upload to images/ folder, reference as `images/filename.jpg` |
| Undo a mistake | Go to Commits, find earlier version |

---

**You've got this! 🐕 🐈**

The best way to learn is to try making small changes and seeing what happens. Start with something simple like updating the hours or phone number.

---

*Last updated: December 2024*

