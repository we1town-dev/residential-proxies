# Residential Proxies

[![WeProxy — Residential proxies](./assets/banner.png)](https://weproxy.io/en/proxies/rotating-ipv4-residential?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)

[![Website](https://img.shields.io/badge/Website-weproxy.io-111111?style=for-the-badge)](https://weproxy.io/?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies) [![Pricing](https://img.shields.io/badge/Pricing-Plans-2563eb?style=for-the-badge)](https://weproxy.io/en/pricing?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)

**Residential proxies** route traffic through IP addresses assigned by consumer ISPs. They are commonly used when datacenter exits are blocked or when you need geo-realistic egress for scraping, ads QA, and research.

Maintained by [WeProxy](https://weproxy.io) — residential, mobile, datacenter, and ISP proxy products.

## What are residential proxies?

A residential proxy uses an IP that looks like a normal home or broadband connection. Compared with classic datacenter proxies:

| | Residential | Datacenter |
| --- | --- | --- |
| IP reputation | ISP / consumer-like | Hosting / cloud ASN |
| Typical cost | Higher per GB | Lower per GB |
| Best for | Harder targets, geo checks | Volume, cheaper hops |
| WeProxy | [Rotating residential](https://weproxy.io/en/proxies/rotating-ipv4-residential), [Static residential](https://weproxy.io/en/proxies/static-ipv4-residential) | [Rotating datacenter](https://weproxy.io/en/proxies/rotating-ipv4-datacenter) |

See also [Premium rotating residential](https://weproxy.io/en/proxies/premium-rotating-residential) and full [Pricing](https://weproxy.io/en/pricing).

## Why teams use residential proxies

- Fewer blocks on sites that fingerprint hosting ASNs
- Country / city targeting for localization and ads verification
- Sticky sessions for logged-in flows (when the product supports sticky)
- Complementary line next to mobile and ISP products

Always follow the target site’s terms and WeProxy’s acceptable use policy.

## How to connect (WeProxy gateway)

```text
Host: gw.weproxy.com.tr
Port: 8989
URL:  http://USER:PASSWORD@gw.weproxy.com.tr:8989
```

Credentials are issued in the [customer panel](https://my.we1.town). Use the package username for your residential product — do not invent undocumented username formats.

HTTP(S) is the default path for most clients. SOCKS5 may be available depending on the package settings in the panel.

### cURL

```bash
curl -x http://USER:PASSWORD@gw.weproxy.com.tr:8989 https://api.ipify.org
```

### Language examples

- Node.js — see the `nodejs-proxy` companion repo
- PHP — see `php-proxy`
- Python — see `python-proxy`

Site docs: [Integrations](https://weproxy.io/en/integrations).

## Rotating vs static residential

- **Rotating:** exit IP changes on a schedule or per request — good for crawling and broad coverage ([rotating IPv4 residential](https://weproxy.io/en/proxies/rotating-ipv4-residential)).
- **Static / sticky:** keep a fixed or long-lived residential IP — good for sessions that need identity continuity ([static IPv4 residential](https://weproxy.io/en/proxies/static-ipv4-residential)).

## Use cases

- Web scraping and price intelligence
- Ad verification and creative QA by geo
- SEO and SERP monitoring
- Market research and localization testing
- Social / multi-profile tooling (comply with platform rules)

## FAQ

### Residential vs mobile?

Mobile proxies use carrier / LTE exits. Residential uses ISP broadband-style IPs. Pick based on the target’s filtering — compare on [weproxy.io](https://weproxy.io).

### Do I need SOCKS5?

Only if your application requires SOCKS. Most HTTP libraries work with an HTTP proxy URL to the WeProxy gateway.

### How do I verify the exit IP?

Request an echo service through the proxy, e.g. `https://api.ipify.org`, and confirm the returned address matches expectations.

## Get started

1. Read product pages on [weproxy.io](https://weproxy.io)
2. Choose a plan on [Pricing](https://weproxy.io/en/pricing)
3. Create credentials at [my.we1.town](https://my.we1.town)
4. Run the cURL check above

## Suggested GitHub topics

`residential-proxy` · `residential-proxies` · `proxy` · `proxies` · `web-scraping` · `socks5` · `http-proxy` · `geo-targeting`

## License

MIT — see [LICENSE](./LICENSE).
