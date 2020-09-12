---
sectionid: using
sectionclass: h1
title: Using mod_authn_yubikey
number: 4000
---

Now that you have configured the `mod_authn_yubikey` module, you’ll probably
want to use it. For this to happen, you have to add the tokenId/user mapping
into the file configured with `AuthYubiKeyUserFile` which defaults to
`conf/ykUserDb` if not specified otherwise.

To add the user `jensfrey` with the password `test123` and the token id
`abcdefghijkl` you would do:

    htpasswd -csb conf/ykUserDb abcdefghijkl jensfrey:test123

Which lets the user `jensfrey` access the site when he:

1. Enters his username (`jensfrey`) in the username field.
2. Enters his password (`test123`) in the password field.
3. And the presses the button on the YubiKey (while having the cursor still
set on the password field)

**Note:** Remember to put the `-s` option into the command, since UNIX
platforms use `crypt()` by default. The `-s` switch forces SHA hashing of the password (you can also use `-m` which is for MD5 hashing). [Thanks to Fredrik Soderblom for pointing that out].
