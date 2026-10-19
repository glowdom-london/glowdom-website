# Connect glowdom.co.uk from IONOS to GitHub Pages

The static homepage is `index.html`; `Glowdom-preview.html` contains the same design for existing links. GitHub Pages publishes from `design/gentle-refinements`, root folder. `main` is unchanged.

IONOS supplies DNS management with the domain. No additional DNS subscription is needed. Domain changes must be made by the domain/account owner; this workspace has no IONOS account access.

## Connect www.glowdom.co.uk

1. In the GitHub repository, open **Settings → Pages**. Under **Custom domain**, enter **www.glowdom.co.uk** and save. Keep the publishing branch `design/gentle-refinements` and `/ (root)`. GitHub creates/updates a `CNAME` file on that branch when the custom domain is saved.
2. Sign in to IONOS. Open **Domains & SSL**, select **glowdom.co.uk**, and open **DNS**.
3. Add or edit the record for the **www** host:

   | Type | Host/name | Target/value |
   | --- | --- | --- |
   | CNAME | www | glowdom-london.github.io |

   The target is just the hostname, without `https://`, the repository name or a file path. If `www` already has a conflicting A, AAAA or CNAME record, replace only that conflicting `www` record. Do not remove MX, email-related TXT or unrelated subdomain records. Leave TTL at the default unless IONOS requires another choice.
4. Wait for DNS validation and the HTTPS certificate to finish, then enable **Enforce HTTPS** in GitHub Pages when available. DNS and certificate provisioning may take time; an immediate failure is not proof that the settings are wrong.

GitHub recommends configuring the custom domain in the repository before pointing DNS at GitHub Pages. The assistant has not activated a custom-domain redirect; the account owner completes these settings together.

## Optional: connect the bare glowdom.co.uk as well

If the bare domain should also reach GitHub Pages, configure these apex A records at IONOS (host `@`, or the root-domain name shown by IONOS):

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

Replace conflicting web-hosting A records for the apex while preserving unrelated records, particularly email records. Remove an old apex AAAA record only if it belongs to a previous web host; otherwise check the current GitHub Pages IPv6 instructions before changing it. IONOS may offer equivalent domain/root record controls instead of an `@` field.

Official reference: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Current verification limits

The original GitHub Pages deployment was verified as successful through the public GitHub Actions page. The updated deployment is checked separately after pushing. This workspace's egress proxy currently blocks direct requests to `glowdom-london.github.io`, `glowdom.co.uk`, `www.glowdom.co.uk`, and the DNS-over-HTTPS endpoint, so direct live HTTP/DNS validation cannot be claimed from those blocked requests. Local page tests and remote source verification are separate from custom-domain readiness. No IONOS records or custom-domain setting have been changed by the assistant.
