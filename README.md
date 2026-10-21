# bilalkah.github.io

The root address is Bilal Kahraman's project index. It introduces the work
and links to the source and project pages. Project repositories publish their
own sites below this address:

- `/karakale/` is published from the
  [karakale](https://github.com/bilalkah/karakale) repository.
- `/jsonb_slice/` is published from the
  [jsonb_slice](https://github.com/bilalkah/jsonb_slice) repository. Its root
  is a release index. Each tag owns a stable documentation path such as
  `/jsonb_slice/0.1.0/`.

- `index.html` and `styles.css` provide the root project index.
- `404.html` redirects only the old `/wolfenstein/...` paths to `/karakale/`.
  Other missing paths show a normal error page. Paths under an active project
  site belong to that project's repository and never reach this one.
- `.nojekyll` makes GitHub Pages serve the files as they are.

GitHub Pages serves this repository from the root of its default branch
(Settings → Pages → Deploy from a branch). Each project repository uses its
own Pages workflow. GitHub serves that artifact below the repository name.

The earlier Jekyll site is kept on the `archive/old-site` branch. To bring
it back, point Pages at that branch or restore its files from it.
