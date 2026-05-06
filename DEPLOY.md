# DEPLOY &mdash; Step-by-step

This walks you through getting the portfolio from your laptop to a live URL at **https://poojakannanv.github.io/**.

Time required: about 5 minutes.

## Prerequisites

You need:

1. A free **GitHub** account using the username `poojakannanv`. If your username is different, see "Different username?" at the bottom.
2. **Git** installed on your machine. Check by opening a terminal / PowerShell and running:
   ```
   git --version
   ```
   If you see a version number, you're good. If not, download from https://git-scm.com/download/win.

## Step 1 &mdash; Create the GitHub repo

1. Go to https://github.com/new
2. Fill in:
   - **Repository name**: `poojakannanv.github.io` (this exact name is required for the root URL to work)
   - **Description**: `Personal portfolio site` (optional)
   - **Public** (must be Public for free GitHub Pages)
   - Do NOT tick "Add a README", "Add .gitignore", or "Choose a license" &mdash; we already have those locally
3. Click **Create repository**
4. On the next page, copy the HTTPS URL it shows (it will look like `https://github.com/poojakannanv/poojakannanv.github.io.git`)

## Step 2 &mdash; Push your local files

Open a terminal / PowerShell **inside this folder**:

```
C:\Users\pooja.kannan\OneDrive - Waymade Group\Documents\MyWorkSpace\MyProjects\poojakannanv.github.io
```

Tip: in File Explorer, navigate into the folder, then type `cmd` or `powershell` in the address bar and hit Enter &mdash; that opens a terminal already pointed here.

Run these commands one at a time:

```bash
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/poojakannanv/poojakannanv.github.io.git
git push -u origin main
```

GitHub will prompt you to authenticate. If you've never done this before, the easiest path is:

- It will open a browser window asking you to sign in with your GitHub account.
- After signing in, it stores credentials so you don't have to re-enter them.

If browser auth doesn't open, you can use a **Personal Access Token**:
1. https://github.com/settings/tokens > Generate new token (classic)
2. Tick the `repo` scope, generate, copy the token
3. When git asks for a password, paste the token (not your GitHub password)

## Step 3 &mdash; Enable GitHub Pages

1. Go to your repo: https://github.com/poojakannanv/poojakannanv.github.io
2. Click **Settings** (top tab)
3. In the left sidebar, click **Pages**
4. Under **Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` and folder `/ (root)`
   - Click **Save**
5. Wait 1&mdash;2 minutes. Refresh the page. At the top you'll see:
   > Your site is live at https://poojakannanv.github.io/

That's it. Your portfolio is live.

## Step 4 &mdash; Verify

Open https://poojakannanv.github.io/ in a fresh tab. The whole page should load. Click around the nav, try the email button, check the GitHub link.

Then test the link preview:

- Paste the URL into a LinkedIn post draft &mdash; it should pull in the OG image and description.
- Same on WhatsApp, Slack, X.

## Step 5 &mdash; Add the URL to your resume / LinkedIn

**LinkedIn**:
- Profile > Edit intro > Contact info > Website > add `https://poojakannanv.github.io/` as type "Portfolio"
- Profile > Add featured > Add a link > paste the URL with title "Portfolio site"

**Resume / CV**:
- Header line, alongside email and phone:
  `Portfolio: poojakannanv.github.io`

**Email signature**:
- `Pooja Kannan · Full-Stack Developer · poojakannanv.github.io`

## Updating the site later

Anytime you want to update the content:

```bash
# edit index.html
git add index.html
git commit -m "Update About section"
git push
```

GitHub Pages auto-deploys within ~1 minute of every push.

## Different username?

If your GitHub username is **not** `poojakannanv`:

1. Replace every occurrence of `poojakannanv` in the repo name with your actual username.
2. Update the `og:url` and `canonical` URLs in `index.html` to match your new live URL.
3. The repo must still be named `<your-username>.github.io` for the clean root URL.

## Troubleshooting

**"Page not found" after enabling Pages**
Wait 2-3 more minutes. First-time deploys can take up to 10 minutes.

**Old version still showing**
Hard-refresh: Ctrl+F5 (Windows) or Cmd+Shift+R (Mac). GitHub's CDN caches aggressively.

**Want a custom domain like `poojakannan.dev`**
Buy the domain (Namecheap, Cloudflare Registrar are cheap), then in repo Settings > Pages > Custom domain, add it. GitHub gives you the DNS records to point at your registrar. Free, takes ~30 minutes.
