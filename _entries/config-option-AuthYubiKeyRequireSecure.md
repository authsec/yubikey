---
sectionid: config-option-AuthnYubiKeyRequireSecure
parent-id: config
sectionclass: h2
title: AuthnYubiKeyRequireSecure
number: 3400
---

**Parameter Name:** `AuthnYubiKeyRequireSecure`

**Default Value:** `On` (secure connection required)

**Description:** The `AuthYubiKeyRequireSecure` directive takes care of users
using `https` with your selected target. This is especially useful if you are
authenticating users with two factors (password AND yubikey), since the
password and the token itself are just Base64 encoded when they are sent back
to the server authenticating the user.
