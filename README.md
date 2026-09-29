# bilalkah.github.io

This site only redirects to the
[Wolfenstein engine's site](https://bilalkah.github.io/wolfenstein/), which
is published from the [wolfenstein](https://github.com/bilalkah/wolfenstein)
repository by its GitHub Actions workflow.

- `index.html` sends `/` to `/wolfenstein/`.
- `404.html` does the same for every other path, such as the old blog's
  pages. Paths under `/wolfenstein/` belong to the wolfenstein repository's
  site and never reach this one.
- `.nojekyll` makes GitHub Pages serve the files as they are.

GitHub Pages serves this repository from the root of its default branch
(Settings → Pages → Deploy from a branch).

The earlier Jekyll site is kept on the `archive/old-site` branch. To bring
it back, point Pages at that branch or restore its files from it.
