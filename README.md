# App Pages

A small static site for project information and OAuth application pages.

Current project:
- **web-ingest-drive** — homepage, privacy policy, and terms for the personal Baidu Netdisk → Google Drive tool.

## Deployment (Cloudflare Pages)

- Repository: `teddyli18000/app-pages`
- Production branch: `main`
- Framework preset: **None**
- Build command: **leave blank**
- Build output directory: `public`
- No environment variables, functions, Workers, database, paid plan or GitHub Actions needed.

Cloudflare gives a temporary `*.pages.dev` URL. For Google OAuth production branding, connect a subdomain of a **domain you own** and verify that domain in Google Search Console. A Pages subdomain alone should not be treated as proof of domain ownership.

Public links after custom domain connection:
- `https://<host>/web-ingest/`
- `https://<host>/web-ingest/privacy/`
- `https://<host>/web-ingest/terms/`

## Security & budget

The site is static HTML/CSS, contains no third-party scripts, API tokens, forms or backend endpoints. Cloudflare's `_headers` supplies CSP and browser hardening headers for static responses. Never commit credentials or personal data. Hosting does **not** need access to Google, GitHub Secrets, or Baidu credentials.

Cloudflare Pages Free currently includes a monthly build quota. Deploys use the selected Git repository; do not add automated workflows or functions just to serve these pages.

## Adding a project

Add a separate directory under `public/` containing an actual project description and a project-specific privacy policy. Update the home page index. Keep the site purely static.
