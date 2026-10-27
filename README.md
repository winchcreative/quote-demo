# Demo quote

A read-only demo of an interactive flip-book quote for a trades business, built for showing to prospects.

Visitors flip through a made-up bathroom quote for "Mr & Mrs Taylor" from "Your Company Here", zoom in on any page, then either
sign (full-screen signature dialog, then a signed confirmation page) or decline. Nothing is saved or sent anywhere: reload the page
and the demo starts again.

It is a static site: `index.html`, `404.html` and the `vendor/` folder. No build step, no backend, no keys. The only things it loads
from outside are Google Fonts and the `signature_pad` script from cdnjs.

## Deploy to GitHub Pages

1. Merge the pull request into `main` (never push to `main` directly).
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder,
   then **Save**.
4. After a minute or so the site is live at `https://<owner>.github.io/<repo>/`.

Do not add a `CNAME` file; the demo uses the default `github.io` address.

## Run it locally

```
python3 -m http.server 8000
```

then open <http://localhost:8000/>.

See `CLAUDE.md` for the rules for working on this repo.
