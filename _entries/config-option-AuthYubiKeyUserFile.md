---
sectionid: config-option-AuthnYubiKeyUserFile
parent-id: config
sectionclass: h2
title: AuthnYubiKeyUserFile
number: 3300
---

**Parameter Name:** `AuthnYubiKeyUserFile`

**Default Value:** `$SERVER_ROOT/conf/ykUserDb`

**Description:** The `AuthYubiKeyUserFile` directive is the file which is
responsible for the tokenid/username mapping. Additionally it is required for
users to be present with their Yubikey id within this file to access the site
protected by `mod_authn_yubikey`.
