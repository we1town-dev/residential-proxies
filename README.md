# Residential Proxies

[![WeProxy — Residential proxies](./assets/banner.png)](https://weproxy.io/en/proxies/rotating-ipv4-residential?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)

[![Website](https://img.shields.io/badge/Website-weproxy.io-111111?style=for-the-badge)](https://weproxy.io/?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)
[![Residential](https://img.shields.io/badge/Product-Residential-16a34a?style=for-the-badge)](https://weproxy.io/en/proxies/rotating-ipv4-residential?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)
[![Pricing](https://img.shields.io/badge/Pricing-Plans-2563eb?style=for-the-badge)](https://weproxy.io/en/pricing?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)

**Residential proxies** exit through IP addresses associated with consumer ISPs — useful when datacenter ASNs are filtered and you need geo-realistic browsing, scraping, or ads QA.

This guide covers how residential differs from datacenter/mobile, rotating vs static, and how to connect via the [WeProxy](https://weproxy.io) gateway.

---

## Residential vs other IP types

| | Residential | Datacenter | Mobile |
| --- | --- | --- | --- |
| Look & feel | Home / broadband ISP | Hosting / cloud ASN | Carrier / LTE |
| Typical cost | Higher per GB | Lower per GB | Premium |
| Strength | Harder targets, geo trust | Raw speed & volume | Carrier reputation |
| WeProxy | [Rotating](https://weproxy.io/en/proxies/rotating-ipv4-residential) · [Static](https://weproxy.io/en/proxies/static-ipv4-residential) · [Premium rotating](https://weproxy.io/en/proxies/premium-rotating-residential) | [DC rotating](https://weproxy.io/en/proxies/rotating-ipv4-datacenter) | [Mobile](https://weproxy.io/en/proxies/mobile-proxy) |

Also see [ISP proxy](https://weproxy.io/en/proxies/isp-proxy) when you want sticky ISP-sourced identity without classic “hosting DC” fingerprints.

## Rotating vs static residential

**Rotating residential**  
Exit IP changes on an interval or per request. Good for crawling, SERP checks, and broad coverage.

→ [Rotating IPv4 residential](https://weproxy.io/en/proxies/rotating-ipv4-residential?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)

**Static / sticky residential**  
Keep a fixed or long-lived residential IP for sessions that need continuity (logins, carts, multi-step flows).

→ [Static IPv4 residential](https://weproxy.io/en/proxies/static-ipv4-residential?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)

Pick the model from [Pricing](https://weproxy.io/en/pricing) based on workflow — not “quality myths.” Always follow destination terms and WeProxy acceptable use.

## Why teams choose residential

- Fewer blocks on sites that fingerprint hosting networks  
- Country / city style targeting for localization and ads verification  
- Complementary line next to mobile and ISP products  
- Same WeProxy gateway pattern as other packages  

Coverage overview: [Locations](https://weproxy.io/en/locations?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)

## Connect with WeProxy

```text
Host: gw.weproxy.com.tr
Port: 8989
URL:  http://USER:PASSWORD@gw.weproxy.com.tr:8989
```

Use the residential package username from [my.we1.town](https://my.we1.town). HTTP(S) is the default path; SOCKS5 only if enabled for your package.

### Verify exit IP

```bash
curl -x http://USER:PASSWORD@gw.weproxy.com.tr:8989 https://api.ipify.org
```

### Code samples

- [Node.js](https://github.com/weproxy-io/nodejs-proxy)  
- [PHP](https://github.com/weproxy-io/php-proxy)  
- [Python](https://github.com/weproxy-io/python-proxy)  
- Site docs: [Integrations](https://weproxy.io/en/integrations)

## Use cases that fit residential well

1. **Harder scrape targets** where DC pools burn quickly  
2. **Ad verification** by market / creative geo  
3. **SEO monitoring** that should look like real-user egress  
4. **Localization QA** for language and currency pages  
5. **Sticky sessions** for multi-step authenticated flows (static/sticky products)

## Operational tips

- Re-check exit IP after credential or package changes  
- Separate “discovery crawl” (rotating) from “logged-in” (sticky) pipelines  
- Pair with [Proxy Checker](https://weproxy.io/en/tools/proxy-checker) when validating formats  
- Free lists are not residential substitutes — see [free-proxy-list](https://github.com/weproxy-io/free-proxy-list)

## FAQ

**Residential vs mobile?**  
Mobile uses carrier exits; residential uses ISP broadband-style IPs. Choose based on how the target filters traffic — compare on [weproxy.io](https://weproxy.io).

**Do I need SOCKS5 for residential?**  
Only if your app requires SOCKS. Most HTTP libraries work with the HTTP proxy URL above.

**Can I share one IP across tools?**  
Static/sticky packages are built for identity continuity. Rotating packages intentionally change exits.

## Get started

1. Read [Rotating residential](https://weproxy.io/en/proxies/rotating-ipv4-residential?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)  
2. Compare plans on [Pricing](https://weproxy.io/en/pricing?utm_source=github&utm_medium=referral&utm_campaign=residential-proxies)  
3. Issue credentials at [my.we1.town](https://my.we1.town)  
4. Smoke-test with cURL  

## Related

- [Paid proxy servers overview](https://github.com/weproxy-io/paid-proxy-servers)  
- [WeProxy homepage](https://weproxy.io)  
- [support@weproxy.io](mailto:support@weproxy.io)  

## License

MIT — see [LICENSE](./LICENSE).
