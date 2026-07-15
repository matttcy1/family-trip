# Perth Family Itinerary

Static single-page itinerary site (30 Aug – 6 Sep 2026).

## Deploy to GitHub + Cloudflare Pages

1. Create a new GitHub repo (e.g. `perth-itinerary`) and push this folder:
   ```
   git init
   git add .
   git commit -m "Initial itinerary site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/perth-itinerary.git
   git push -u origin main
   ```
2. In Cloudflare dashboard: Workers & Pages → Create → Pages → Connect to Git → select the repo.
3. Build settings: no build command needed, no framework preset — set **Build output directory** to `/` (root), leave build command blank.
4. Deploy. Cloudflare will give you a `*.pages.dev` URL; add a custom domain later if you want.

No dependencies, no build step — it's a single static `index.html`.
