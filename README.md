# leancpms.com

The website for LeanCPMS, the open-source charge point management system,
and LeanCPMS Cloud, the hosted service from Forsslund Systems AB.

It is a single static page: no build step, no framework, no JavaScript, no
trackers and no cookies.

| File | What |
|---|---|
| `index.html` | the page |
| `style.css` | all styles; light and dark mode follow `prefers-color-scheme` |
| `favicon.svg` | the icon |
| `404.html` | shown by GitHub Pages for unknown paths |
| `CNAME` | the custom domain, `leancpms.com` |

## Editing

Edit the HTML or CSS directly. To preview locally:

```bash
python3 -m http.server 8000
# open http://localhost:8000/
```

## Publishing

The site is served by GitHub Pages from the `main` branch, repository root.
A push to `main` publishes it within a minute or two. The domain is set by
the `CNAME` file and in the repository's Pages settings; DNS for
leancpms.com points to GitHub Pages.
