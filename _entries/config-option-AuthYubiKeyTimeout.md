---
sectionid: config-option-AuthnYubiKeyTimeout
parent-id: config
sectionclass: h2
title: AuthnYubiKeyTimeout
number: 3100
---

**Parameter Name:** `AuthnYubiKeyTimeout`

**Default Value:** `43200` seconds (12h)

**Description:** The `AuthYubiKeyTimeout` directive specifies an absolute
timeout since the user last logged in. This means, that if the timeout is set
to 120 seconds, the user has to log in again after 120 seconds of using the
page. This is a hard timeout which is not renewed as the user is working with
the page.
