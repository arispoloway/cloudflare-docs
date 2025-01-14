---
pcx_content_type: concept
title: Authenticated Origin Pulls (mTLS)
weight: 4
layout: single
meta:
    description: Authenticated Origin Pulls helps ensure requests to your origin server come from the Cloudflare network.
---

# Authenticated Origin Pulls (mTLS)

Authenticated Origin Pulls helps ensure requests to your origin server come from the Cloudflare network, which provides an additional layer of security on top of [Full](/ssl/origin-configuration/ssl-modes/full/) or [Full (strict)](/ssl/origin-configuration/ssl-modes/full-strict/) encryption modes.

This authentication becomes particularly important with the [Cloudflare Web Application Firewall (WAF)](/waf/). Together with the WAF, you can make sure that **all traffic** is evaluated before receiving a response from your origin server.

Although Cloudflare provides you a certificate to easily configure zone-level authentication, if you want more strict security, you should upload your own certificate. Using a custom certificate is possible with both [zone-level](/ssl/origin-configuration/authenticated-origin-pull/set-up/zone-level/) and [per-hostname](/ssl/origin-configuration/authenticated-origin-pull/set-up/per-hostname/) authenticated origin pulls and is required if you need your domain to be [FIPS](https://en.wikipedia.org/wiki/Federal_Information_Processing_Standards) compliant.

## Availability

{{<feature-table id="ssl.authenticated_origin_pulls">}}

## More information

{{<directory-listing>}}

## Related topics

- [SSL/TLS Encryption Modes](/ssl/origin-configuration/ssl-modes/)
- [Cloudflare Tunnel](/cloudflare-one/connections/connect-networks/)

## Limitations

Authenticated Origin Pulls is not compatible with [Railgun](/railgun/) (deprecated) and does not apply when your [SSL/TLS encryption mode](/ssl/origin-configuration/ssl-modes/) is set to **Off** or **Flexible**.
