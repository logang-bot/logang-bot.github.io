# logang-bot.github.io

The developer website for every app published under this Play developer account. GitHub Pages
serves it at <https://logang-bot.github.io/>.

## What lives here

| Path | Purpose |
|---|---|
| `index.html` | Developer page: who publishes the apps, the list of apps, a contact address |
| `app-ads.txt` | Authorised ad sellers. Ad networks only read it from the **root** of the website listed on the Play store listing, so it can only live in this repo. One file covers every app on the account |
| `<app-name>/privacy-policy.html` | Each new app's privacy policy |
| `google1e30460a0ee048b1.html` | Google Search Console ownership proof, which Play Console uses to verify the developer website. Google re-checks it periodically, so **never delete or rename it** |

## Adding an app

1. Write its policy at `<app-name>/privacy-policy.html`. Describe that app's own data use; don't
   point several apps at one generic policy.
2. Add an `<article class="app">` to `index.html` with its store link and policy link.
3. In Play Console, set the app's **Website** to `https://logang-bot.github.io` and its
   **Privacy policy** to the new page's URL.
4. If it shows ads, add any new network's lines to `app-ads.txt`. Don't duplicate lines already
   there.

## Existing exceptions

- **PartyPuzl**: the policy lives in the `partypuzl-legal` repo, served at
  `/partypuzl-legal/privacy-policy.html`. That URL is registered in Play Console, so it stays.
- **PartyPuzl premium packs**: `partypuzl-packs` serves the pack bank JSON at
  `/partypuzl-packs/`. Don't create a folder with either name here; a project repo's Pages site
  takes over that path.
