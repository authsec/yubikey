---
sectionid: intro
sectionclass: h1
title: Introduction
number: 1000
---

With `mod_authn_yubikey` you can protect your website with a basic auth mechanism (the username password popup box), just more secure 😉

The `mod_authn_yubikey` module is an authentication provider for the apache 2.2 platform. It leverages the YubiKey which is a small token that acts as an authentication device. By enabling your apache installation with this module you can use your YubiKey for authentication with your website.

The `mod_authn_yubikey` module provides one and two factor authentication for your website and is completely independend from the technlogy that implements your website (like CGI, JSP or PHP).

In your backend application you can read the `HTTP_X_YUBI_AUTH_TYPE` header, which is either `OneFactor` or `TwoFactor` stating that the user authenticated using either just the Yubikey itself or in conjunction with an additional password, where TwoFactor would be sent instead.
