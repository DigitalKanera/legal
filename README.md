# Kanera Apps — legal & support site

Static privacy and support pages for all apps. Free hosting via **GitHub Pages**.

## Recommended: dedicated repo

1. Create a new GitHub repo: **`DigitalKanera/legal`** (name can be anything; `legal` keeps URLs short).
2. Copy the **contents** of this folder (`index.html`, `assets/`, `tipforge/`, `.nojekyll`) to the **root** of that repo.
3. Push to `main`.
4. GitHub → **Settings → Pages** → Build from **main** branch, folder **`/ (root)`**.
5. Wait ~1 minute. Your site is live at:

   ```
   https://digitalkanera.github.io/legal/
   ```

### App Store Connect URLs (TipForge)

| Field | URL |
|-------|-----|
| **Privacy Policy** | `https://digitalkanera.github.io/legal/tipforge/privacy.html` |
| **Support URL** | `https://digitalkanera.github.io/legal/tipforge/support.html` |

Replace `digitalkanera` with your GitHub username if different.

## Custom domain (optional)

In the `legal` repo: **Settings → Pages → Custom domain** → e.g. `legal.kanerachad.com`.

Then URLs become:

- `https://legal.kanerachad.com/tipforge/privacy.html`
- `https://legal.kanerachad.com/tipforge/support.html`

Cloudflare DNS (free) or your registrar’s DNS works fine.

## Add another app

1. Create `other-app/privacy.html` and `other-app/support.html` (copy TipForge as a template).
2. Add a row to `index.html` under **Apps**.
3. Push — GitHub Pages redeploys automatically.

## Edit contact email

Search/replace `support@kanerachad.com` in HTML files with your real support address.

## Local preview

```bash
cd legal
python3 -m http.server 8080
# Open http://localhost:8080/tipforge/privacy.html
```

Note: root-absolute paths (`/assets/style.css`) need the server rooted at `legal/`.

## Why this folder lives in TipForge

Source of truth stays with the app repo for agents and developers. Deploy by copying to the **`DigitalKanera/legal`** publishing repo (or symlink/subtree if you prefer automation later).
