# Salah Eddine Karim — Portfolio

Personal portfolio site. Community Manager & Content Strategist, Casablanca.

Plain static site: one `index.html`, two small scripts, and an `assets/` folder.
No build step, no dependencies to install.

---

## Put it online for free (GitHub Pages)

### 1. Create the repository

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `portfolio` (or `USERNAME.github.io` if you want the short URL — replace `USERNAME` with your GitHub username)
3. Set it to **Public**
4. Click **Create repository**

### 2. Upload the files

On the new repo page, click **uploading an existing file**, then drag in **everything** from the downloaded folder:

```
index.html
support.js
image-slot.js
robots.txt
.nojekyll
assets/          <- the whole folder
```

Click **Commit changes**.

> Every file is under 25 MB, so browser upload works. If the `assets` folder does not
> drag in as a folder, open it and drag its files in after creating the folder.

### 3. Turn on Pages

1. In the repo: **Settings** → **Pages** (left sidebar)
2. Under *Build and deployment* → *Source*: **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)** → **Save**
4. Wait about a minute, then reload. Your URL appears at the top:

```
https://USERNAME.github.io/portfolio/
```

That is your live website. Done.

---

## Updating the site later

Open the file on GitHub → pencil icon → edit → **Commit changes**.
To add or replace an image or video: **Add file** → **Upload files** into `assets/`.
Changes go live in under a minute.

---

## Custom domain (optional)

Buy a domain, then in **Settings → Pages → Custom domain** enter it and save.
At your registrar, point the domain at GitHub:

| Type  | Name | Value                 |
|-------|------|-----------------------|
| CNAME | www  | `USERNAME.github.io`  |
| A     | @    | `185.199.108.153`     |
| A     | @    | `185.199.109.153`     |
| A     | @    | `185.199.110.153`     |
| A     | @    | `185.199.111.153`     |

Then tick **Enforce HTTPS**.

---

## Two SEO touches once you know your URL

**1. Social preview image** — in `index.html`, inside `<helmet>`, add:

```html
<meta property="og:url" content="https://USERNAME.github.io/portfolio/">
<meta property="og:image" content="https://USERNAME.github.io/portfolio/assets/portrait.jpg">
```

**2. Sitemap** — create `sitemap.xml` at the repo root:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url><loc>https://USERNAME.github.io/portfolio/</loc></url>
</urlset>
```

Then uncomment the `Sitemap:` line in `robots.txt` with the same URL.

---

## Alternative: Vercel (also free)

1. [vercel.com/new](https://vercel.com/new) → import the GitHub repo
2. Framework preset: **Other**, leave build settings empty
3. **Deploy**

Vercel gives you `your-project.vercel.app` and redeploys on every commit.

---

## Still to fill in

- LinkedIn URL and email address (contact buttons currently point nowhere)
- Two full podcast episodes (reserved slots inside the Clinique du Droit case study)
- Real testimonials (the three cards say "coming soon" on purpose)
