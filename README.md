# AI Researcher — public legal documents

This folder is **not part of the mobile app**. Publish it as a **separate public GitHub repository** (e.g. `airesearcher-legal`) so Privacy Policy and Terms stay public while the main app repo stays private.

## One-time setup

1. Create a **new public** repo on GitHub, e.g. `airesearcher-legal` (empty, no README).
2. Publish from the private app repo:

```bash
bash scripts/publish-legal-docs.sh
```

3. **Enable GitHub Pages** (required — without this, `github.io` returns 404; the blob URL on github.com is not enough):

   **Option A — GitHub Actions (recommended)**

   - Repo → **Settings → Pages**
   - **Build and deployment → Source:** `GitHub Actions`
   - Push again or re-run the **Deploy GitHub Pages** workflow
   - Wait 1–3 minutes

   **Option B — Branch `/docs`**

   - **Settings → Pages → Source:** Deploy from branch
   - Branch: `main`, folder: **`/docs`** → Save

4. Verify in browser:

   - `https://<github-user>.github.io/airesearcher-legal/`
   - `https://<github-user>.github.io/airesearcher-legal/privacy/`
   - `https://<github-user>.github.io/airesearcher-legal/terms/`

   Example: [Dimon70007/airesearcher-legal](https://github.com/Dimon70007/airesearcher-legal) →  
   `https://dimon70007.github.io/airesearcher-legal/privacy/`

5. In the **private** app `.env`:

```env
LEGAL_PUBLIC_REPO=git@github.com:<github-user>/airesearcher-legal.git
LEGAL_PRIVACY_URL=https://<github-user>.github.io/airesearcher-legal/privacy/
LEGAL_TERMS_URL=https://<github-user>.github.io/airesearcher-legal/terms/
LEGAL_SUPPORT_EMAIL=your-real-email@example.com
```

6. Rebuild the app.

## Troubleshooting 404 on github.io

| Symptom | Cause | Fix |
|---------|--------|-----|
| `github.io/.../privacy` → 404 | Pages **not enabled** | Settings → Pages → enable (see above) |
| `github.com/.../blob/.../privacy.md` works | Normal — that's the repo viewer, not Pages | Enable Pages |
| Old URL without trailing `/` | Static layout uses folders | Use `/privacy/` in app `.env` |

Source markdown (`.md`) stays in `docs/` for editing; browsers get static HTML from `docs/privacy/index.html` and `docs/terms/index.html`.

## Update workflow

Edit `docs/privacy.md` / `docs/terms.md` (and matching `privacy/index.html` / `terms/index.html` if content changed), then:

```bash
bash scripts/publish-legal-docs.sh
```

## Custom domain (optional)

Point DNS to GitHub Pages and set **Custom domain** in the public repo’s Pages settings. Update `LEGAL_*_URL` in the app `.env`.

## Engineering compliance tracker

Sign-off checklist for ads/billing (private app repo):  
[`docs/monetization-legal-checklist.md`](../docs/monetization-legal-checklist.md) in **AIResearcher** (TASK-080). Update `privacy.md` / `terms.md` here when that checklist calls for 80.D1–D2.
