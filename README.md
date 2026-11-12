# pratikshakamat

Portfolio site for **Pratiksha Kamat**, a researcher, writer and storyteller working in TV, editorial and community media in Ireland.

It's a plain static site (HTML + CSS, no build step), hosted on GitHub Pages.

```
index.html          the whole site (one page)
assets/css/site.css styles
assets/img/         web-sized photos
favicon.svg
.nojekyll           tells GitHub Pages to serve files as-is
```

## Preview locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Publish on GitHub Pages

1. Repo **Settings → Pages**
2. Source: **Deploy from a branch**, branch `main`, folder `/ (root)`
3. The site appears at https://salilwalavalkar.github.io/pratikshakamat/

### Custom domain (pratikshakamat.com)

When you're ready to switch the domain over from its current host:

1. In **Settings → Pages → Custom domain**, enter `pratikshakamat.com` (GitHub adds a `CNAME` file).
2. At the domain registrar, point DNS at GitHub Pages:
   - `A` records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www`: `salilwalavalkar.github.io`
3. Tick **Enforce HTTPS** once the certificate is issued.

## Adding new work

- **New TV credit:** copy an `<article class="card">` block in the `#screen` section.
- **New article:** copy an `<a><article>…</article></a>` block in `#words`.
- Resize photos before adding them (about 1400px wide), e.g. `sips -Z 1400 photo.jpg --out assets/img/name.jpg`.

## Still to do

- [ ] A downloadable CV (`assets/cv.pdf`)
- [ ] Optional: stills from each show to sit alongside the credit screenshots
