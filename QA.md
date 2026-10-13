# Website verification

Checked on 13 October 2026 using an isolated Chrome browser and a local HTTP server serving this project's public directory.

- Desktop 1440px, tablet 768px and mobile 320px/360px: rendered and visually reviewed; no horizontal overflow.
- Existing wordmark and the CSS-layered Eigen symbol render correctly at all checked widths.
- Refined navigation, service dividers, rounded email buttons and dark About panel were visually reviewed.
- The self-hosted Manrope font loads successfully.
- Main navigation and the back-to-top link point to existing sections.
- All three email links use info@eigenroot.com and subject Enquiry for Eigen. The visible contact email is info@eigenroot.com.
- The keyboard skip link works and visible focus is provided.
- Foreground/background contrast: dark text on white 17.77:1; muted text on white 5.79:1; muted text on the grey surface 5.30:1; button text on blue 5.46:1.
- No browser runtime errors or failed asset requests occurred during the checks.
- The custom 404 page links back to the homepage.
- GRID is explicitly marked Coming soon, with home cleaning and laundry described as its initial planned services. No booking, download or waitlist action implies it is already available.
- No public phone number, premises address, other private product details, customer claims, forms or analytics scripts are included.
- Vercel configuration fields were reviewed against Vercel's current configuration schema. No framework or build is required.
- DNS checks confirm Namecheap nameservers and existing registrar-servers.com email-forwarding MX records.

## Launch checks still required

Production domain routing and certificate issuance were not checked in this local verification pass. After deployment, verify both custom domains, the apex-to-www redirect and HTTPS in an anonymous browser. Local preview does not validate Vercel's production routing or certificate issuance.

## Custom domain fix

Diagnosed a loop between Vercel’s apex-to-www domain redirect and the opposite www-to-apex redirect formerly in vercel.json. Removed the source redirect so Vercel’s Domains settings are the only authority. Canonical, Open Graph, Twitter image, robots and sitemap URLs now use https://www.eigenroot.com. The website design and hero were not changed.
