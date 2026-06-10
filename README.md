# Kanera Apps — legal & support site

Static privacy and support pages for all apps. Free hosting via **GitHub Pages**.

## Publish (one-time setup)

The site is pushed to **[github.com/DigitalKanera/legal](https://github.com/DigitalKanera/legal)**.

### Enable GitHub Pages (required once)

1. Open **[github.com/DigitalKanera/legal/settings/pages](https://github.com/DigitalKanera/legal/settings/pages)**
2. Under **Build and deployment → Source**, choose **Deploy from a branch**
3. Branch: **`main`**, folder: **`/ (root)`**
4. Click **Save**
5. Wait 1–2 minutes. Site URL:

   ```
   https://digitalkanera.github.io/legal/
   ```

### App Store Connect URLs (TipForge)

| Field | URL |
|-------|-----|
| **Privacy Policy** | `https://digitalkanera.github.io/legal/tipforge/privacy.html` |
| **Support URL** | `https://digitalkanera.github.io/legal/tipforge/support.html` |

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

## Sync changes from TipForge

After editing files in `TipForge/legal/`, publish to the live repo:

```bash
cd legal
git add .
git commit -m "Update legal pages"
git push origin main
```

The `legal/` folder contains its own git remote pointing at `DigitalKanera/legal`.
