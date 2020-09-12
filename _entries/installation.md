---
sectionid: installation
sectionclass: h1
is-parent: yes
title: Installation From Source
number: 2000
---

For `mod_authn_yubikey` to work you first need `libcurl`. You have to install libcurl according to the installation instructions valid for your distribution and/or platform.

On a Debian system you would typically do a simple

    aptitude install libcurl3

As a next step you need to download the source from the module
[here](source/authn_yubikey.tar.bz2). After extracting the module you need to
adopt the Makefile to point to an apache source tree, so the module is able to
compile (of course for compiling you might want to have `libcurl-dev` too).

If you are not installing the module into a custom built apache, you might want
to use the apache server already installed on your system. If you are running
debian you need to have the `apxs` tool for building the module. You can get
this tool by typing

    aptitude install apache-threaded-dev

After you installed that, you can build and install the module with the
following command (after changing into the directory you unpacked the module
source of course):

    apxs2 \
    -DYK_PACKAGE=\\\"mod_authn_yubikey\\\" \
    -DYK_PACKAGE_VERSION=\\\"0.1\\\" -I. -Wc -c -lcurl \
    mod_authn_yubikey.c libykclient.c libykclient.slo mod_authn_yubikey.slo \
    && su -c "apxs2 -i mod_authn_yubikey.la"

After your finished installing `libcurl` and coping/compiling/installing the module, you now can go on configuring `mod_authn_yubikey`.
