# Andrei-Theodor Ginavar — Personal Site

A single-page static site (Home / About / Timeline / Research / Publications / Activities / Contact). plain HTML/CSS/JS, ready for GitHub Pages.

## Files

```
index.html          the whole site
files/CV_ATG.pdf     downloadable CV (linked from the nav and footer)
```

## Deploy to GitHub Pages

1. Create a new repository on GitHub, e.g. `theodor-ginavar.github.io` (use exactly `<your-username>.github.io` for a root domain) or any name like `personal-site`.
2. Push these files to the repo root:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Pick **Branch: main**, folder **/ (root)**, then **Save**.
6. Wait ~1 minute — GitHub will give you a URL like:
   - `https://<your-username>.github.io/` (if the repo is named `<your-username>.github.io`), or
   - `https://<your-username>.github.io/<repo-name>/` (any other repo name).

## Updating content later

Everything lives in `index.html` — sections are clearly commented (`<!-- ================= ABOUT ================= -->` etc.). To update your CV file, replace `files/CV_ATG.pdf` with the new PDF (keep the same filename, or update the `href="files/CV_ATG.pdf"` links in `index.html`).

## Notes

- Fonts (Fraunces / Inter / IBM Plex Mono) are loaded from Google Fonts via CDN — no local font files needed.
- The hero chart and section reveals are pure CSS/SVG animation plus a small vanilla-JS `IntersectionObserver` — no framework or build tool required.
- LinkedIn URL is pulled from your previous Google Sites page: update it in the footer if it changes.
