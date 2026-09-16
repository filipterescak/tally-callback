# tally-callback

Static redirect endpoints for Tally's Enable Banking flow.

Enable Banking only whitelists `http`/`https` redirect URLs, so the app cannot
register its own `tally://` scheme directly. These two pages sit on GitHub
Pages, receive the bank's redirect, and forward the query string onward.

## Publish

    git init
    git add -A
    git commit -m "Tally callback endpoints"
    git branch -M main
    git remote add origin https://github.com/filipterescak/tally-callback.git
    git push -u origin main

Then: repo Settings -> Pages -> Source "Deploy from a branch" -> main / (root).

## Register these in the Enable Banking control panel

    https://filipterescak.github.io/tally-callback/native/
    https://filipterescak.github.io/tally-callback/web/

Trailing slashes included — matching is exact.
