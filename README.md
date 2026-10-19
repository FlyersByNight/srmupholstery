# SRM Upholstery website

Plain HTML/CSS, no build step. Hosts free on Cloudflare Pages.

## Files
- `index.html` – the whole site (one page)
- `styles.css` – styling
- `images/` – logo files; put project photos in `images/gallery/`
- `_headers` – Cloudflare caching/security headers

## Deploy to Cloudflare Pages (free)
1. Sign in at dash.cloudflare.com (free account).
2. Workers & Pages → Create → Pages → **Upload assets**.
3. Name the project `srm-upholstery`, drag in the contents of this folder, Deploy.
   The site is live at `https://srm-upholstery.pages.dev`.
4. Custom domain: in the Pages project → Custom domains → add e.g. `www.srmupholstery.co.uk`.
   Easiest if the domain is registered at (or its nameservers moved to) Cloudflare;
   Cloudflare Registrar sells `.co.uk` at cost (roughly £5–6/year), so total running cost is just the domain.
5. To update the site later, open the project → Create new deployment → upload the folder again.

## Adding photos
Resize to about 1200px wide and save as .webp or .jpg, put them in `images/gallery/`, then in
`index.html` replace a placeholder tile with:

    <figure class="tile"><img src="images/gallery/sofa.webp" alt="Re-upholstered sofa" loading="lazy"><figcaption>Chesterfield sofa</figcaption></figure>
