# bilalkah.github.io

The root address redirects to
[Last Signal from Karakale](https://bilalkah.github.io/karakale/). Project
repositories publish their own sites below this address:

- `/karakale/` is published from the
  [karakale](https://github.com/bilalkah/karakale) repository.
- `/jsonb_slice/` is published from the
  [jsonb_slice](https://github.com/bilalkah/jsonb_slice) repository. Its root
  is a release index. Each tag owns a stable documentation path such as
  `/jsonb_slice/0.1.0/`.

- `index.html` sends `/` to `/karakale/`.
- `404.html` does the same for every other path, such as the old blog's
  pages. Links to `/wolfenstein/...`, the game's address before the
  repository was renamed, go to the same page under `/karakale/`, with
  their query and anchor. Paths under an active project site belong to that
  project's repository and never reach this one.
- `.nojekyll` makes GitHub Pages serve the files as they are.

GitHub Pages serves this repository from the root of its default branch
(Settings → Pages → Deploy from a branch). Each project repository uses its
own Pages workflow. GitHub serves that artifact below the repository name.

The earlier Jekyll site is kept on the `archive/old-site` branch. To bring
it back, point Pages at that branch or restore its files from it.
