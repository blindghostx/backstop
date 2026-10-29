# backstop

Home, privacy policy and support pages for Backstop for iPhone, served by GitHub Pages at
https://blindghostx.github.io/backstop/.

| File | URL |
|---|---|
| `index.html` | https://blindghostx.github.io/backstop/ |
| `privacy.html` | https://blindghostx.github.io/backstop/privacy.html |
| `support.html` | https://blindghostx.github.io/backstop/support.html |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are, without Jekyll. |

Each page is a single HTML file with its styles inside and no JavaScript. They use system fonts and make no
outside requests, so a visit sends nothing to anyone but GitHub Pages.

## Publish

1. Create the public repository `blindghostx/backstop` on GitHub.
2. Copy everything in this folder to the root of its `main` branch, `.nojekyll` included. Leave out the `._*`
   and `.DS_Store` files macOS adds on non-Mac drives, for example with
   `rsync -a --exclude '._*' --exclude '.DS_Store' <this folder>/ <the repository>/`.
3. Commit and push to `main`.
4. In the repository's Settings › Pages, set Source to Deploy from a branch, branch `main`, folder `/ (root)`.
5. After the first deploy finishes, open the three URLs above and check that each one loads.

## Where the URLs are used

- **The app:** Settings › About Backstop opens `privacy.html` (Privacy policy) and `support.html` (Help and
  support). Both URLs are set in `AppLinks` in `Backstop/Backstop/SettingsView.swift`, so renaming or moving a
  page needs a new app build.
- **App Store Connect:** Privacy Policy URL is `privacy.html` and Support URL is `support.html`. The home page
  can be the Marketing URL.

When the privacy policy changes, update the effective date under its title and the "Last updated" line at the
end of `privacy.html`.
