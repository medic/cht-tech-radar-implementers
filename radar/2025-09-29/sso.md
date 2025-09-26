---
title:      "Single Sign-On (SSO)"
ring:       adopt
quadrant:   tools
tags:       [integration, authentication]
---

The [CHT supports Single Sign-On (SSO)](https://docs.communityhealthtoolkit.org/hosting/sso/) via integration with an external authentication server. Users connecting to a CHT instance authenticate with their SSO credentials instead of needing a CHT-specific username and password.

SSO authentication is implemented with the industry standard [OpenID](https://openid.net/) Connect (OIDC) protocol. Any OIDC-compliant authentication server can be integrated with the CHT.
