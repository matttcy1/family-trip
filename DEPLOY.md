# Deploy setup

- GitHub repo: `matttcy1/family-trip` (branch `main`), root contains `index.html` + `README.md`.
- Cloudflare Pages is connected to this repo/branch and auto-deploys on every push — no action needed there.
- A fine-grained GitHub token (Contents: Read/write, scoped to this repo only) is stored locally in `.deploy-token` in this folder. It's git-ignored and never committed.
- To push an update: clone the repo fresh into a scratch directory using the token, overwrite `index.html`, commit, and push to `main`. This avoids relying on the `.git` folder inside this synced Desktop folder, which doesn't reliably support git operations in the Cowork sandbox.
- The token expires roughly 90 days from creation (~mid-Oct 2026, unless set otherwise) — check GitHub if pushes start failing with an auth error, and regenerate + replace `.deploy-token` if so.
