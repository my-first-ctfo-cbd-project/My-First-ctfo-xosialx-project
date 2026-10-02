# My-First-ctfo-xosialx-project-

A simple static landing page for the CTFO-XOSIALX brand, ready to deploy on Cloudflare Pages.

## Project status

- Static HTML site
- No build step required
- Cloudflare Pages compatible

## Cloudflare Pages deployment

This project can be deployed directly as a static site.

### Deployment steps

1. Sign in to your Cloudflare account.
2. Open Workers & Pages.
3. Select Create application > Pages.
4. Choose Connect to Git.
5. Select the repository: `myctfoxosialx-crypto/My-First-ctfo-xosialx-project-`.
6. Use the following settings:
   - Framework preset: `None`
   - Build command: leave blank
   - Build output directory: `/`
   - Production branch: `main`
7. Click Save and Deploy.

### Important notes

- The site entry point is `index.html`.
- Cloudflare Pages will serve the repository root as a static site.
- No additional build step is required for the current project structure.

## Local preview

Open the project root in a browser, or use a simple local static server if you want to preview it before deployment:

```bash
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Developer guide

See `DEVELOPERS_GUIDE.md` for extended deployment and maintenance instructions.
