# AI Researcher — public legal documents

This folder is **not part of the mobile app**. Publish it as a **separate public GitHub repository** (e.g. `airesearcher-legal`) so Privacy Policy and Terms stay public while the main app repo stays private.

## One-time setup

1. Create a **new public** repo on GitHub, e.g. `airesearcher-legal` (empty, no README).
2. Copy this folder’s contents into that repo (only `docs/`, `_config.yml`, and this README).
3. GitHub → **Settings → Pages** → Source: **Deploy from branch** → Branch: `main` → Folder: **`/docs`** → Save.
4. After 1–2 minutes, documents are live at:
   - `https://<github-user>.github.io/airesearcher-legal/`
   - `https://<github-user>.github.io/airesearcher-legal/privacy`
   - `https://<github-user>.github.io/airesearcher-legal/terms`

5. In the **private** app repo, set `.env`:

```env
LEGAL_PUBLIC_REPO=git@github.com:<github-user>/airesearcher-legal.git
LEGAL_PRIVACY_URL=https://<github-user>.github.io/airesearcher-legal/privacy
LEGAL_TERMS_URL=https://<github-user>.github.io/airesearcher-legal/terms
LEGAL_SUPPORT_EMAIL=your-real-email@example.com
```

6. Rebuild the app (Metro cache reset if needed).

## Update workflow

Edit `docs/privacy.md` or `docs/terms.md` in the private repo, then sync to the public repo:

```bash
bash scripts/publish-legal-docs.sh
```

Or manually copy `legal-public/docs/*` and push to the public repo.

## Custom domain (optional)

If you later register a domain, point DNS to GitHub Pages and set **Custom domain** in the public repo’s Pages settings. Then update `LEGAL_*_URL` in the app `.env`.
