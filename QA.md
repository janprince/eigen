# Website verification

Checked on 13 October 2026 using an isolated Chrome browser and a local HTTP server serving this project's public directory.

- Desktop 1440px, tablet 768px and mobile 360px: rendered and visually reviewed; no horizontal overflow.
- Existing wordmark and symbol load correctly at all checked widths.
- The self-hosted Manrope font loads successfully.
- Main navigation and the back-to-top link point to existing sections.
- All three email links use the confirmed address and subject Enquiry for Eigen.
- The keyboard skip link works and visible focus is provided.
- Foreground/background contrast: dark text on white 17.77:1; muted text on white 5.79:1; muted text on the grey surface 5.30:1; button text on blue 5.46:1.
- No browser runtime errors or failed asset requests occurred during the checks.
- The custom 404 page links back to the homepage.
- No public phone number, premises address, private product details, customer claims, forms or analytics scripts are included.
- Vercel configuration fields were reviewed against Vercel's current configuration schema. No framework or build is required.
- DNS checks confirm Namecheap nameservers and existing registrar-servers.com email-forwarding MX records.

## Launch checks still required

No Vercel production deployment or DNS changes were made. After deploying, verify the public production URL, both custom domains, the www redirect and HTTPS in an anonymous browser. Local preview does not validate Vercel's production routing or certificate issuance.
