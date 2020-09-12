---
sectionid: config-option-AuthnYubiKeyTmpFile
parent-id: config
sectionclass: h2
title: AuthnYubiKeyTmpFile
number: 3200
---

**Parameter Name:** `AuthnYubiKeyTmpFile`

**Default Value:** `$SERVER_ROOT/conf/ykTmpDb`

**Description:** The `AuthYubiKeyTmpFile` directive specifies the temporary file
which is used to store authenticated users. If a user successfully
authenticates, the authentication time is stored within this file.
It is used to determine when the user logged in last.

**Remember**, if you specify the location of the file, that if you
configure it to `/tmp` on UNIX systems, that possibly everyone can view
that file.
