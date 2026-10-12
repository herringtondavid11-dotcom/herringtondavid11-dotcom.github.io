# Davey web files (GitHub Pages)

Hosts the universal link Plaid uses to return users to Davey after they log in at an OAuth bank
(Chase, Wells Fargo, Bank of America, ...).

- `.well-known/apple-app-site-association`: tells iOS that `/plaid/oauth*` links open Davey
  (app ID `D2Z4ABFHAB.com.davidherrington.Davey`). No file extension, served without redirects.
- `plaid/oauth/index.html`: fallback page shown if the link opens in a browser instead of the app.
- `.nojekyll`: makes GitHub Pages publish the `.well-known` folder.

Publish these files at the root of `https://<github-username>.github.io` (a repo named `<github-username>.github.io`).
Check with: `curl -i https://<github-username>.github.io/.well-known/apple-app-site-association`
