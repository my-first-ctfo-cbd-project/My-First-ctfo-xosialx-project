# Developer Guide

## Project overview

This repository contains a static marketing landing page for CTFO-XOSIALX. The site is designed to deploy directly to Cloudflare Pages without a framework build step.

## Repository structure

- `index.html` — main landing page
- `README.md` — deployment summary and quick-start instructions
- `LICENSE` — project license

## Local development

Open the project folder and serve it locally:

```bash
cd My-First-ctfo-xosialx-project-
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Cloudflare Pages deployment setup

1. Log in to Cloudflare.
2. Open Workers & Pages.
3. Click Create application.
4. Select Pages.
5. Choose Connect to Git.
6. Select this repository: `myctfoxosialx-crypto/My-First-ctfo-xosialx-project-`.
7. Set the build configuration:
   - Framework preset: `None`
   - Build command: leave empty
   - Build output directory: `/`
   - Production branch: `main`
8. Click Save and Deploy.

## Notes about the current setup

This project is a static HTML site, so Cloudflare Pages can serve it directly. There is no React, Vite, Next.js, or Node build process required.

## Custom domain setup

After deployment:

1. Open the Cloudflare Pages project.
2. Select Custom domains.
3. Add your domain or subdomain.
4. Update DNS records as Cloudflare instructs.
5. Wait for DNS propagation and SSL certificate issuance.

## Deployment troubleshooting

### Blank page after deployment

- Confirm `index.html` exists in the repository root.
- Ensure the Pages output directory is set to `/`.
- Check the deployment logs for any file path issues.

### CSS or layout not loading

- Verify the browser is loading the deployed `index.html` correctly.
- Ensure no file paths were broken during upload.
- Rebuild or redeploy after any changes.

### Missing fonts or images

- Use relative paths from the repository root.
- Avoid absolute local file paths.

## Recommended next improvements

- Add a product catalog section.
- Add a contact/order form.
- Add metadata and Open Graph tags for social sharing.
- Add an FAQ section and testimonials.
- Set up a custom domain and SSL.

## Git workflow

Use a clean branch for each feature or deployment-related update.

```bash
git checkout -b feature/cloudflare-pages-update
git add .
git commit -m "Update Cloudflare Pages setup"
git push origin feature/cloudflare-pages-update
```

Then open a pull request in GitHub and merge after review.
