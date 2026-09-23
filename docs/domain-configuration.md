# BetterHalf Labs domain configuration

Verified September 23, 2026: all three domains show Valid Configuration in Vercel. Both websites load over HTTPS and www redirects to the root domain.

DNS provider: Hostinger. Nameservers: ns1.dns-parking.com and ns2.dns-parking.com.

| Type | Host | Value | TTL |
| --- | --- | --- | --- |
| A | @ | 216.198.79.1 | 300 |
| CNAME | www | 2454dbdd1b7f83a7.vercel-dns-017.com | 300 |
| CNAME | incentives | eb81e0a2365b9577.vercel-dns-017.com | 300 |

The root and www domains belong to Vercel project betterhalf-labs-portfolio. www redirects to https://betterhalflabs.com with HTTP 308. The incentives subdomain belongs to canada-incentives-explorer. Both projects are in team simranscarborough-9150s-projects.

## Preventing recurrence

Do not reset the Hostinger DNS zone or reconnect these hostnames to another hosting provider unless intentionally migrating the websites. The former root/www address 185.158.133.1 conflicts with Vercel hosting. Avoid competing A/AAAA records and do not place an A record alongside a CNAME at the same hostname.

Preserve existing Titan email MX, SPF, DKIM, and unrelated records. Verification TXT records do not route website traffic.

After changes, check both Vercel domain dashboards for Valid Configuration and open all three HTTPS URLs. Allow time for DNS propagation and certificate issuance. If Vercel changes its recommended values, use the live dashboard values and update this document.

- https://vercel.com/simranscarborough-9150s-projects/betterhalf-labs-portfolio/settings/domains
- https://vercel.com/simranscarborough-9150s-projects/canada-incentives-explorer/settings/domains

## Deployment source

DNS changes are saved in Hostinger; GitHub files do not apply them automatically. At inspection, the portfolio production deployment showed a manual `vercel deploy` source, and this repository contained only a README. This document records infrastructure configuration; it does not connect this repository to Vercel or replace deployed application source.
