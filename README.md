# SonIA Company Website

Astro corporate website for SonIA, an AI platform for high-volume recruiting workflows.

## Development

```sh
npm install
npm run dev
npm run build
```

## LinkedIn short links

GitHub Pages serves the static files in `public/`. Each LinkedIn post gets a short link at `/li<n>` that redirects to the homepage with its own UTM campaign.

To create `/li3`, copy `public/li2/index.html` to `public/li3/index.html` and replace **all three** occurrences of the destination URL with `https://sonia-hr.com/?utm_source=linkedin&utm_medium=social&utm_campaign=<campaign>`, using the campaign defined for post 3 in `_Contexto/linkedin.md` (channel rule 5). In HTML attributes, write `&amp;` instead of `&`; in the JavaScript string, keep `&`. Keep the `noindex` tag and the social preview metadata. Do not add the short link to `src/pages/` (which generates sitemap routes).

After merging to `main`, the GitHub Actions workflow builds and publishes the site to GitHub Pages. Open `https://sonia-hr.com/li3` in a private browser window and check that the address bar shows the tagged homepage URL. Then confirm the campaign in Analytics Realtime. The short-link HTML itself does not load Analytics; the destination homepage does.
