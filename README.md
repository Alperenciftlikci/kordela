# Kordela website

Public website for **Kordela: Connect the Dots Game**, the iOS puzzle game
(connect dots of the same color, fill the board, never cross). It is plain
static HTML with inline CSS: no build step, no frameworks, and no external
fonts, scripts, trackers or analytics.

Served with GitHub Pages from the `main` branch, root folder.

| Page | URL | Used for |
|---|---|---|
| `index.html` | https://alperenciftlikci.github.io/kordela/ | App Store marketing URL |
| `privacy-policy.html` | https://alperenciftlikci.github.io/kordela/privacy-policy.html | App Store privacy policy URL, in-app Privacy Policy link |
| `support.html` | https://alperenciftlikci.github.io/kordela/support.html | App Store support URL, in-app support link |

`icon.png` is the app icon at 512 px, made with
`sips -z 512 512 AppIcon-light.png --out icon.png` from the game's
`App/Resources/Assets.xcassets/AppIcon.appiconset/`.

## Publish

1. Create a public GitHub repository named `kordela` on the `Alperenciftlikci`
   account. The repository name becomes the `/kordela/` part of the URL.
2. Push this folder:

   ```sh
   git remote add origin https://github.com/Alperenciftlikci/kordela.git
   git push -u origin main
   ```

3. On GitHub, open **Settings → Pages**. Under **Build and deployment**, set
   **Source** to *Deploy from a branch*, then **Branch** to `main` and the folder
   to `/ (root)`, and save.
4. After a minute or two, the three URLs above are live. The empty `.nojekyll`
   file tells Pages to serve the files as they are.

## When the app goes live

- In `index.html`, replace the "Coming soon to the App Store" badge with Apple's
  official "Download on the App Store" badge, linked to the app's App Store page.
- Optionally add `<meta name="apple-itunes-app" content="app-id=…">` to each
  page's `<head>` for Safari's Smart App Banner.

## Keep it in sync with the app

The privacy policy describes what the app actually does: progress on the device;
Firebase anonymous sign-in, an online backup of progress and the Sequins wallet,
Crashlytics (on by default, can be turned off), App Check and opt-in game
statistics (Google Analytics); RevenueCat for purchases. If the app starts
collecting something new, update `privacy-policy.html` and its effective date,
along with the App Store privacy labels.

Contact: kordela.app@gmail.com
