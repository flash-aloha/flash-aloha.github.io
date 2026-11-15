# flash-aloha.github.io

Project page for **Flash ALOHA: Learning Fast and Precise Manipulation**,
served at https://flash-aloha.github.io.

- `/` — the project page (`index.html`, `style.css`, `cad.js`, `sections.js`).
- `/static/files/flash-aloha.pdf` — the current paper; replace this file to update it.
- `/robots.txt` and `/sitemap.xml` — crawler discovery files for the page and PDF.

## Preview locally

No build or dependency installation is required. From the repository root, run:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000. Use an HTTP server so the graph data and 3D models
can load correctly.

## Upload to GitHub Pages

Upload the repository contents to the root of the Pages publishing branch,
including `.nojekyll`, `index.html`, the CSS and JavaScript files, `robots.txt`,
`sitemap.xml`, and the entire `static/` directory. Keep the directory structure
intact. Configure GitHub Pages to deploy from that branch and `/ (root)`.

Use Git to upload the full repository: the hero GIF exceeds GitHub's browser
upload limit. No individual site asset exceeds GitHub's 100 MiB Git file limit.
Exclude `.git/`, macOS metadata, and temporary drafts from any upload archive.

## Search and sharing metadata

`index.html` contains a canonical URL, Open Graph and Twitter image metadata,
paper citation metadata, and Schema.org `ScholarlyArticle` JSON-LD. The preview
image uses the existing static ball-catching image.

The sitemap lists the home page and paper PDF. After deployment, submit
https://flash-aloha.github.io/sitemap.xml in Google Search Console. If the site
moves to a custom domain, update the absolute URLs in `index.html`,
`robots.txt`, and `sitemap.xml` together. Update the citation and structured
metadata when the paper title or authors change; add a publication date only
when it is confirmed.

References: [Google sitemap guidance](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap),
[Google Scholar metadata guidance](https://scholar.google.com/intl/en/scholar/inclusion.html),
[GitHub file size limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github).

## Assets

The full-platform CAD file (`static/models/flash-aloha.glb`) is optional: when
absent, `cad.js` constructs the rig and loads the included `rs-arm.glb` models.
The scissor-handle model is included separately.

Videos in `static/videos/flash-aloha/` have their captions burned in; the
script that makes them lives in the johnyao93.github.io repo at
`tools/captions/caption.sh`.
