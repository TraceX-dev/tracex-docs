# TraceX Docs

Documentation for the TraceX platform, covering quality management, product development and team collaboration. Visit [tracex.co](https://tracex.co/) to learn more.

## Local development

To verify and preview documentation locally:

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Run the development server:**
   ```bash
   npm run dev
   ```
   The documentation will be available at `http://localhost:4321` (or the next available port).

3. **Build and preview the production build:**
   ```bash
   npm run build
   npm run preview
   ```
   This will run type checking (`astro check`) and build the documentation, then serve a preview of the production build.

## GitHub Pages deployment

The workflow in `.github/workflows/deploy.yml` builds the Astro site with
`npm run build` and deploys the generated `dist/` directory on pushes to `main`.
It can also be run manually from the repository's Actions tab.

In the repository's **Settings → Pages → Build and deployment**, set **Source**
to **GitHub Actions**. The branch-based Jekyll builder cannot process Astro
components and reports invalid YAML front matter when it reads their JavaScript
front matter.

Keep the custom domain set to `docs.tracex.co` in the Pages settings.
`astro.config.mjs` uses this URL as the site origin, and `public/CNAME` is copied
into the build output. No repository path prefix is needed for this custom domain.

## Submitting requests and feedback

Join the [TraceX Community](https://app.tracex.co/login/join?workspace=tracex-ws) to ask questions, suggest documentation topics and share feedback with our team.

You can also submit documentation issues in the [TraceX Docs repository](https://github.com/TraceX-dev/tracex-docs).
