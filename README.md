# leancpms.com

The website for LeanCPMS, the open-source charge point management system,
and LeanCPMS Cloud, the hosted service from Forsslund Systems AB.

It is a few static pages: no build step, no framework, no JavaScript, no
trackers and no cookies.

| File | What |
|---|---|
| `index.html` | the home page |
| `configuration.html` | the YAML configuration, with example files |
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

The example YAML files on `configuration.html` are coloured by hand with
`<span class="k|s|c">` (key, string, comment). They must stay valid
manifests: after changing one, copy it out and run `cpms manifest validate`
on it.

## Publishing

The site is served by GitHub Pages from the `main` branch, repository root.
A push to `main` publishes it within a minute or two. The domain is set by
the `CNAME` file and in the repository's Pages settings; DNS for
leancpms.com points to GitHub Pages.
