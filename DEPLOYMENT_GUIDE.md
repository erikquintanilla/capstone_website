# Capstone Website — GitHub Deployment Guide
## How to Replace Your Old Site and Go Live with the New One

---

## What This Guide Covers

1. Replacing your old ZIP with the new one on your computer
2. Pushing all the new files to GitHub
3. Enabling GitHub Pages so your site is live on the internet
4. Making future edits and updating the live site

---

## PART 1 — Set Up Your Computer

### Step 1 — Install Git (if you haven't already)

Go to https://git-scm.com/downloads and download Git for your operating system.

- **Windows:** Run the installer, click Next on everything, keep all defaults.
- **Mac:** Open Terminal and type `git --version`. If Git isn't installed, it will prompt you to install it automatically.

To confirm Git is installed, open a terminal (or Command Prompt on Windows) and type:

```
git --version
```

You should see something like `git version 2.x.x`.

---

### Step 2 — Unzip the New Website Files

1. Find the file you downloaded: **CAPSTONE_WEBSITE_UPDATED.zip**
2. Right-click it → **Extract All** (Windows) or double-click (Mac)
3. You'll get a folder called `capstone_site_updated/`
4. Rename that folder to whatever your project is called, for example: `capstone-website`

Your folder structure should look like this:

```
capstone-website/
├── index.html
├── css/
│   └── style.css
├── assets/
│   ├── hero-bg.png
│   └── capstone_paper.docx
└── pages/
    ├── essay.html
    ├── findings.html
    ├── resources.html
    ├── works-cited.html
    └── about.html
```

---

## PART 2 — Connect to GitHub

### Step 3 — Create a GitHub Account (if you don't have one)

Go to https://github.com and sign up for a free account.
Use a professional username — this will appear in your website URL.

---

### Step 4 — Create a New Repository on GitHub

1. Log in to GitHub
2. Click the **+** icon in the top-right corner → **New repository**
3. Fill in the form:
   - **Repository name:** `capstone-website` (or any name you like — no spaces)
   - **Description:** My high school capstone research website
   - **Visibility:** Public ← this is required for the free GitHub Pages hosting
   - **Do NOT** check "Initialize this repository with a README"
4. Click **Create repository**
5. GitHub will show you a page with setup instructions — **keep this page open**, you'll need the repository URL in Step 6

Your repository URL will look like:
```
https://github.com/YOUR-USERNAME/capstone-website.git
```

---

### Step 5 — Open a Terminal in Your Website Folder

**Windows:**
1. Open File Explorer and navigate to your `capstone-website` folder
2. Click the address bar at the top, type `cmd`, and press Enter
3. A Command Prompt window opens already inside that folder

**Mac:**
1. Open Terminal (search "Terminal" in Spotlight)
2. Type `cd ` (with a space after), then drag your `capstone-website` folder into the Terminal window
3. Press Enter

To confirm you're in the right place, type:
```
ls
```
You should see `index.html` listed in the output.

---

### Step 6 — Initialize Git and Push to GitHub

Type these commands one at a time, pressing Enter after each one.

```bash
git init
```
This sets up Git tracking in your folder.

```bash
git add .
```
This stages all your files to be uploaded. The dot means "everything."

```bash
git commit -m "Initial capstone website upload"
```
This saves a snapshot of your files with a message describing what changed.

```bash
git branch -M main
```
This names your main branch "main" (GitHub's standard).

```bash
git remote add origin https://github.com/YOUR-USERNAME/capstone-website.git
```
⚠️ Replace `YOUR-USERNAME` and `capstone-website` with your actual GitHub username and repository name from Step 4.

```bash
git push -u origin main
```
This uploads all your files to GitHub.

GitHub may ask you to log in. Enter your GitHub username and password.
> **Note:** If GitHub asks for a password and rejects it, you need a Personal Access Token instead. Go to GitHub → Settings → Developer Settings → Personal Access Tokens → Generate new token. Use that token as your password.

---

## PART 3 — Enable GitHub Pages (Free Hosting)

### Step 7 — Turn On GitHub Pages

1. Go to your repository on GitHub: `https://github.com/YOUR-USERNAME/capstone-website`
2. Click the **Settings** tab (near the top of the page)
3. In the left sidebar, click **Pages**
4. Under **Source**, click the dropdown that says "None" and select **Deploy from a branch**
5. Under **Branch**, select **main** and make sure the folder is set to **/ (root)**
6. Click **Save**

GitHub will take about 1–2 minutes to build your site.

---

### Step 8 — Find Your Live Website URL

After saving, refresh the Pages settings page. GitHub will show you a green banner with your live URL:

```
Your site is live at https://YOUR-USERNAME.github.io/capstone-website/
```

Open that URL in any browser — your capstone website is now publicly live on the internet.

---

## PART 4 — Making Future Edits and Updating the Live Site

### Every time you make changes to your website files, do this:

Open your terminal in the `capstone-website` folder and run:

```bash
git add .
git commit -m "Describe what you changed here"
git push
```

GitHub Pages will automatically rebuild and update your live website within 1–2 minutes.

**Example commit messages:**
```bash
git commit -m "Updated essay with new section on sustainability"
git commit -m "Fixed typo in works cited page"
git commit -m "Added new hero background image"
```

---

## PART 5 — Replacing the Old ZIP (If You Had a Previous Version)

If you had an older version of the site already on GitHub, here's how to fully replace it:

1. Delete all the old files from your local folder (keep the hidden `.git` folder — do not delete that)
2. Copy all the new files from `capstone_site_updated/` into that same folder
3. Open terminal in the folder and run:

```bash
git add .
git commit -m "Updated site with new capstone content and works cited page"
git push
```

GitHub Pages will automatically update within 1–2 minutes.

---

## Quick Reference — The 3 Commands You'll Use Every Time

```bash
git add .
git commit -m "Your message here"
git push
```

That's it. Every time you edit a file, run those three commands and your live site updates automatically.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| `git: command not found` | Git isn't installed. Go to git-scm.com and install it. |
| `Permission denied` | Use a Personal Access Token as your password (see Step 6 note) |
| `failed to push` error | Run `git pull origin main` first, then try `git push` again |
| Site shows old content | Wait 2 minutes and hard-refresh the browser (Ctrl+Shift+R or Cmd+Shift+R) |
| 404 error on your URL | Make sure Pages is set to deploy from `main` branch, root folder |

---

## Your Final Checklist

- [ ] Git installed on your computer
- [ ] New ZIP unzipped and folder renamed
- [ ] GitHub account created
- [ ] New repository created (Public)
- [ ] `git init`, `add`, `commit`, `push` completed
- [ ] GitHub Pages enabled on `main` branch, root folder
- [ ] Live site URL confirmed working
- [ ] Capstone paper downloads correctly from the Resources page
- [ ] All navigation links working (Essay, Findings, Resources, Works Cited, About)

---

*Erik Quintanilla Cruz · Oakland Technical High School · Capstone 2025–2026*
