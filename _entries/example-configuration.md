---
sectionid: example-config
parent-id: config
sectionclass: h2
title: Example Configuration
number: 3600
---

A example configuration using `mod_authn_yubikey` is looking as follows (configured on a mac):    

    # These are global parameters, libcurl needs to be loaded from
    # wherever it is installed on your system    

    LoadFile /opt/local/lib/libcurl.dylib
    LoadModule authn_yubikey_module modules/mod_authn_yubikey.so
    ErrorDocument 406 http://coffeecrew.org/index.html    

    # This tells apache that you really do not want any security in the
    # first place and that you will protect your login location or directory
    # by responsibly setting up an SSL connection to that location. If you
    # just use OneFactor authentication (just the key, no password) this is
    # of course unneccessary, since a stolen password (the token output)
    # cannot be reused.    

    AuthYubiKeyRequireSecure Off    

    # Global configuration end    

    AuthType Basic
    AuthBasicProvider yubikey
    AuthName "Please Log In using your YubiKey"
    AuthYubiKeyTimeout 30
    AuthYubiKeyTmpFile conf/ykTmpDb
    AuthYubiKeyUserFile conf/ykUserDb
    AuthYubiKeyRequireSecure On
    AuthYubiKeyExternalErrorPage Off
    Require valid-user
