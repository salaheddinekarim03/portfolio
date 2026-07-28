# Salah Eddine Karim — Portfolio

Live portfolio site. All media (images, videos, PDFs) is served from Supabase
Storage, so this repo holds only 5 small files — no large-file upload problems.

```
index.html        the whole site
support.js        runtime
image-slot.js     image placeholder component
robots.txt
.nojekyll         tells GitHub Pages not to run Jekyll
```

## Publish it (GitHub Pages)

1. [github.com/new](https://github.com/new) → name it `portfolio` → **Public** → create
2. **Add file → Upload files** → drag in all 5 files above → **Commit changes**
3. **Settings → Pages** → Source: *Deploy from a branch* → branch **main**, folder **/ (root)** → **Save**

A minute later your URL appears:

```
https://USERNAME.github.io/portfolio/
```

Naming the repo `USERNAME.github.io` instead gives you the shorter `username.github.io`.

## Updating later

Edit `index.html` on GitHub (pencil icon) → **Commit changes**. Live in under a minute.

To swap a photo or video: upload the new file to the Supabase `assets` bucket using
the **same filename**. No code change, no redeploy.

## Media

Served from:

```
https://aqzbwqmqzlomvrvxhzsl.supabase.co/storage/v1/object/public/assets/
```

The bucket must stay **public**. Filenames are referenced exactly as uploaded.

## Custom domain (optional)

**Settings → Pages → Custom domain** → enter your domain → Save. At your registrar:

| Type  | Name | Value                 |
|-------|------|-----------------------|
| CNAME | www  | `USERNAME.github.io`  |
| A     | @    | `185.199.108.153`     |
| A     | @    | `185.199.109.153`     |
| A     | @    | `185.199.110.153`     |
| A     | @    | `185.199.111.153`     |

Then tick **Enforce HTTPS**.

## Two SEO touches once the URL exists

**1.** In `index.html`, inside `<helmet>`, add:

```html
<meta property="og:url" content="https://USERNAME.github.io/portfolio/">
<meta property="og:image" content="https://aqzbwqmqzlomvrvxhzsl.supabase.co/storage/v1/object/public/assets/portrait.jpg">
```

**2.** Create `sitemap.xml` at the repo root:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url><loc>https://USERNAME.github.io/portfolio/</loc></url>
</urlset>
```

Then uncomment the `Sitemap:` line in `robots.txt` with that URL.

## Alternative: Vercel

[vercel.com/new](https://vercel.com/new) → import the repo → Framework preset **Other**,
build settings empty → **Deploy**.

## Still open

- Real testimonials (three cards say "coming soon" on purpose)
- PFE report title/topic in the Experience section is generic
