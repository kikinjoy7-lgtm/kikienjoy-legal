# Kiki enJoy — Legal Documents

Static HTML hosting for the app's legal pages on Cloudflare Pages.

## 🌐 Pages

| URL | File | Description |
|---|---|---|
| `/` | `index.html` | Landing page with links to the three documents |
| `/terms` | `terms.html` | Terms of Service (תנאי שימוש) |
| `/privacy` | `privacy.html` | Privacy Policy (מדיניות פרטיות) |
| `/accessibility` | `accessibility.html` | Accessibility Statement (הצהרת נגישות) |

Pretty URLs (`/terms` rather than `/terms.html`) are served natively by
Cloudflare Pages — when a request comes in for `/terms`, Pages
automatically looks for a matching `terms.html` and serves it. No
`_redirects` file is needed for this pattern; we previously had one
and it caused a redirect loop, so it was removed.

## 🚀 Deploy

Cloudflare Pages picks up commits to `main` automatically.

1. Edit the HTML file you want to change.
2. `git commit && git push origin main`
3. Cloudflare deploys within ~30 seconds.

No build step — pages are pure static HTML/CSS.

## 📱 Used by

The Kiki enJoy mobile app (`kiki-n-joy` repo) opens these URLs from the
Profile → "תנאים ותקנונים" submenu via `Linking.openURL(...)`.

## ⚖️ Status

All three documents currently carry a yellow "טיוטה" (draft) banner —
this is intentional and stays until they are reviewed by a lawyer.
Remove the banners by editing the corresponding HTML files and pushing
the change.
