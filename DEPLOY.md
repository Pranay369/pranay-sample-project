# Deploying your portfolio ($0 hosting)

This site is **static** (HTML, CSS, JS). You can host it for free on **GitHub Pages** or **Cloudflare Pages**.

## Before you publish

1. In [`index.html`](index.html), replace every `https://YOUR_SITE_URL` with your real URL (including trailing path if the site lives in a project repo, e.g. `https://username.github.io/repo-name`).
2. Add an Open Graph image (optional but recommended for LinkedIn): save as `assets/images/og-preview.png` (about **1200×630** pixels). Update `og:image` if your filename or path differs.
3. Replace placeholder copy, links (`mailto:`, LinkedIn, GitHub), and project URLs.

## Option A: GitHub Pages

1. Create a new repository on GitHub and push this folder (e.g. `main` branch).
2. In the repo: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Select branch **main** and folder **/ (root)**, then save.
5. After a minute or two, the site is live at:
   - **Project site:** `https://<username>.github.io/<repository>/`
   - **User site (optional):** name the repo `<username>.github.io` and use the root of that repo for the same files → `https://<username>.github.io/`

**Note:** Free GitHub Pages for **personal accounts** typically uses a **public** repository. If the site loads without styles, check that `styles.css` and `script.js` are committed and that you used the correct base URL for any absolute links.

## Option B: Cloudflare Pages

1. Push the project to GitHub (or GitLab).
2. In [Cloudflare Dashboard](https://dash.cloudflare.com/) go to **Workers & Pages → Create → Pages → Connect to Git**.
3. Select the repository. For this plain static site:
   - **Build command:** leave empty (or `exit 0`).
   - **Build output directory:** `/` (root) — or set the project root to this folder if the repo contains other projects.
4. Deploy. You get a `*.pages.dev` URL; you can add a custom domain later in **Custom domains**.

If you later add a build step (e.g. Vite), set **Build command** to `npm run build` and **Output directory** to `dist`.

## Custom domain (optional, paid)

Buy a domain from any registrar (~$10–15/year). Then:

- **GitHub Pages:** add a `CNAME` file or configure the custom domain in **Pages** settings; follow GitHub’s DNS instructions.
- **Cloudflare:** add the domain to your account and follow **Custom domains** on the Pages project.

## LinkedIn

Add your live site under **Contact info → Website** or **Featured** on your profile. Open the link in an incognito window and on your phone to confirm everything loads.
