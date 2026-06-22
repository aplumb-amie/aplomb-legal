# Aplomb Legal Site

Privacy policy and terms of use for **Aplomb Technique** and **Aplomb Fit**.

Hosted at: `https://aplombtechnique.app`

## App Store URLs to use

| App | Field | URL |
|-----|-------|-----|
| Aplomb Technique | Privacy Policy URL | `https://aplombtechnique.app/privacy` |
| Aplomb Technique | Terms of Use URL | `https://aplombtechnique.app/terms` |
| Aplomb Fit | Privacy Policy URL | `https://aplombtechnique.app/privacy` |
| Aplomb Fit | Terms of Use URL | `https://aplombtechnique.app/terms` |

---

## Deploy to GitHub Pages (one-time setup)

### Step 1 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository**
3. Name it `aplomb-legal` (or any name you like)
4. Set it to **Public** (required for GitHub Pages)
5. Click **Create repository**

### Step 2 — Upload these files

Option A — drag and drop in the browser:
1. On the repo page, click **Add file → Upload files**
2. Drag all files from this folder into the upload area
3. Click **Commit changes**

Option B — using Git:
```bash
cd aplomb-legal-site
git init
git add .
git commit -m "Add legal site"
git remote add origin https://github.com/YOUR-USERNAME/aplomb-legal.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`
4. Click **Save**

GitHub will show a URL like `https://your-username.github.io/aplomb-legal` — ignore this for now.

### Step 4 — Connect your custom domain

1. Still in Settings → Pages, find the **Custom domain** field
2. Enter `aplombtechnique.app` and click **Save**
3. GitHub will create a `CNAME` file automatically (or use the one in this folder)

### Step 5 — Point your domain to GitHub Pages

Log into your domain registrar (where you bought `aplombtechnique.app`) and add these DNS records:

| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | YOUR-USERNAME.github.io |

DNS changes can take up to 48 hours to propagate, but usually take under an hour.

### Step 6 — Enable HTTPS

Once the domain is connected:
1. Settings → Pages → tick **Enforce HTTPS**
2. Wait a few minutes for the certificate to generate

### Done!

Your policy pages will be live at:
- `https://aplombtechnique.app` — home page
- `https://aplombtechnique.app/privacy` — privacy policy
- `https://aplombtechnique.app/terms` — terms of use

---

## For aplombfit.app

The same policy covers both apps (it explicitly names Aplomb Fit). For the App Store submission, simply point both apps to the same URLs above.

If you later want `aplombfit.app` to also display the pages directly, create a second GitHub Pages repo and repeat the same process pointing to the `aplombfit.app` domain — the HTML files are identical.

---

## Updating the policies

1. Edit the relevant `.html` file
2. Update the "Last updated" date near the top of the file
3. Commit and push — GitHub Pages redeploys automatically within a few minutes
4. Send an email to your users if the change is material (required by GDPR)
