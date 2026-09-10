# Akent portfolio site

Static site — no build step, no framework. Edit `index.html` / `styles.css` directly and
re-deploy (see below).

## Placeholder content to replace before going live

Search for `PLACEHOLDER` comments in `index.html`:
- Hero tagline/pitch
- Bio text + headshot photo (currently a gradient placeholder box)
- Client cards — real client names are already filled in from context; **confirm each client is
  OK being publicly featured** before this goes live
- Video links (currently `href="#"`) + thumbnails (currently a solid placeholder box)
- Testimonial quotes + attribution (currently fake placeholder quotes)
- Contact email

## Local preview

```
python3 -m http.server 8000
```
then open http://localhost:8000

## Deploy (GitHub Pages)

1. Push this repo to GitHub (public repo, since Pages on a free plan needs public).
2. Repo Settings → Pages → Source: deploy from branch `main`, folder `/ (root)`.
3. Custom domain: add a `CNAME` file here containing your domain, then point DNS at GoDaddy:
   - `A` records (root domain) → GitHub Pages IPs, or
   - `CNAME` record (`www`) → `<username>.github.io`
4. Tick "Enforce HTTPS" in Pages settings once DNS resolves.
