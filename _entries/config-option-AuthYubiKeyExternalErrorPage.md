---
sectionid: config-option-AuthnYubiKeyExternalErrorPage
parent-id: config
sectionclass: h2
title: AuthnYubiKeyExternalErrorPage
number: 3500
---

**Parameter Name:** `AuthnYubiKeyExternalErrorPage`

**Default Value:** `Off` (built in error page used)

**Description:** The `AuthYubiKeyExternalErrorPage` directive let’s you specify
an error page different from the built in error page, so that you are able to
design your own. By using the `ErrorDocument` directive within your
configuration you can even redirect the user to a site not residing on you
machine.
