# Eigen website

A static company website for **eigenroot.com**, built with HTML and CSS. The site has no framework, build step, runtime dependencies, forms, analytics or external font requests.

## Deploy to Vercel

From this project directory, run:

```sh
npx vercel@latest --prod
```

Sign in if requested, create a new project and follow the prompts. The included `vercel.json` sets the output directory to `public` and disables build and install commands. No environment variables are required.

If importing a Git repository through the Vercel dashboard instead, choose **Other** as the framework preset, use `public` as the output directory, and leave the build and install commands empty. The repository root must contain `vercel.json` and the `public` folder.

Official reference: [Deploying from the Vercel CLI](https://vercel.com/docs/projects/deploy-from-cli).

## Connect eigenroot.com

1. In your Vercel project, open **Settings → Domains** and add `eigenroot.com` and `www.eigenroot.com`.
2. Copy the exact DNS values Vercel displays. The apex normally uses an A record and `www` a CNAME; use the project-specific values, not an IP copied from an old tutorial.
3. In Namecheap, open **Domain List → Manage → Advanced DNS**. The domain's nameservers were checked on 13 October 2026 and are `dns1.registrar-servers.com` and `dns2.registrar-servers.com`.
4. Update only conflicting website/parking records for `@` and `www`, then add any ownership-verification records Vercel requests. Preserve the existing MX email-forwarding records and email-related TXT records. Keep the current nameservers.
5. Wait for Vercel to report a valid configuration and issue the HTTPS certificate. Keep `www.eigenroot.com` as the primary production domain and configure `eigenroot.com` to redirect to it in Vercel’s Domains settings. Redirects are managed there; `vercel.json` intentionally has no host redirect to avoid conflicting rules.
6. Open both domains in a private/incognito browser window and confirm the website is visible without signing in. If authentication appears, review the project's Deployment Protection settings.

Official references: [Vercel custom domains](https://vercel.com/docs/domains/set-up-custom-domain) and [Namecheap DNS records](https://www.namecheap.com/support/knowledgebase/article.aspx/434/2237/how-do-i-set-up-host-records-for-a-domain/).

The domain is not connected merely by downloading or deploying this source package. DNS and certificate validation must complete before the custom domain is live.

## Preview locally

From the project root:

```sh
python3 -m http.server 3000 --directory public
```

Open `http://localhost:3000`. Use a local web server rather than opening the HTML directly, because asset URLs start at `/`.

## Edit the website

- Page copy, services, company details and email links: `public/index.html`.
- Colours, spacing, layout and typography: `public/styles.css`.
- Images, icons and the locally hosted Manrope font: `public/assets/`.
- Hosting configuration: `vercel.json`. Hostname redirects are managed in Vercel’s Domains settings.
- Search and link previews: metadata in `public/index.html`, plus `public/sitemap.xml`, `public/robots.txt` and `public/assets/social-preview.png`.

To change the email address, replace every occurrence of `info@eigenroot.com` in `public/index.html`, including all three `mailto:` links. Keep the URL-encoded subject `Enquiry%20for%20Eigen` or update it deliberately.

The footer's copyright year is static. Update it when appropriate. If the primary domain changes, also update canonical/social URLs, the sitemap, robots file and the domain redirect in Vercel’s Domains settings.

## Assets and licensing

The Eigen wordmark and symbol come from the supplied brand assets. Only empty canvas was trimmed and web formats prepared; the design has not been redrawn. The decorative hero treatment uses static CSS layers of the existing symbol.

Manrope is self-hosted under the SIL Open Font License. Its license is included at `public/assets/fonts/OFL.txt`. Source: [Google Fonts Manrope](https://github.com/google/fonts/tree/main/ofl/manrope).

## Public information

The website displays the Eigen brand, the legal name EIGEN ROOT TECH LTD, Accra, Ghana, and the confirmed email address. GRID is listed as an upcoming home services product for Ghana, starting with home cleaning and laundry. Other private products, phone numbers, the premises address and registration documents are not included.
