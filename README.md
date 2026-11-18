# leancpms.com

The website for LeanCPMS, the open-source charge point management system,
and LeanCPMS Cloud, the hosted service from Forsslund Systems AB.

It is a few static pages: no build step, no framework, no JavaScript, no
trackers and no cookies.
The exception is `docs/`, the documentation site, which is generated
elsewhere and uses JavaScript for its search (below).

| File | What |
|---|---|
| `index.html` | the home page |
| `configuration.html` | the YAML configuration, with example files |
| `style.css` | all styles; light and dark mode follow `prefers-color-scheme` |
| `favicon.svg` | the icon |
| `404.html` | shown by GitHub Pages for unknown paths |
| `docs/` | the documentation site, **generated**: do not edit it here (below) |
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

## The documentation, `docs/`

`docs/` is built from the Markdown in the LeanCPMS repository
(`forsslund/leancpms`, `docs-site/`) and pushed here by its workflow
`docs-site.yml` on every change to the docs on its `main`, as a commit
"Docs: built from leancpms <commit>". Each push replaces the whole
directory, so a change made here by hand is lost: change the Markdown
there instead. The push uses a deploy key of this repository titled
"leancpms docs-site", with write access; its private half is the secret
`LEANCPMS_COM_DEPLOY_KEY` in the LeanCPMS repository.
