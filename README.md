# bilalkah.github.io

This site only redirects to the site of
[Last Signal from Karakale](https://bilalkah.github.io/karakale/), which is
published from the [karakale](https://github.com/bilalkah/karakale)
repository by its GitHub Actions workflow.

- `index.html` sends `/` to `/karakale/`.
- `404.html` does the same for every other path, such as the old blog's
  pages. Links to `/wolfenstein/...`, the game's address before the
  repository was renamed, go to the same page under `/karakale/`, with
  their query and anchor. Paths under `/karakale/` belong to the karakale
  repository's site and never reach this one.
- `.nojekyll` makes GitHub Pages serve the files as they are.

GitHub Pages serves this repository from the root of its default branch
(Settings → Pages → Deploy from a branch).

The earlier Jekyll site is kept on the `archive/old-site` branch. To bring
it back, point Pages at that branch or restore its files from it.
