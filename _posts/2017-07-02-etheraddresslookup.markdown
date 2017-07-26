---
layout: post
title: "EthAddressLookup Chrome Extension (Packaged Chrome Extension)"
date: 2017-07-02 02:07:00 +0100
permalink: /ethaddresslookup-chrome-extension-release/
categories: ethereum, extension
is_blog_post: true
comments: true
---

**Chrome Extension:** [https://chrome.google.com/webstore/detail/etheraddresslookup/pdknmigbbbhmllnmgdfalmedcmcefdfn](https://chrome.google.com/webstore/detail/etheraddresslookup/pdknmigbbbhmllnmgdfalmedcmcefdfn)

**Note:** If you wish to manually install, go to [this GitHub repository for installation instructions (https://github.com/409H/EtherAddressLookup)](https://github.com/409H/EtherAddressLookup).

### v1.3

* Due to the recent phishing campaigns going on, we have decided to start a [domain blacklist](https://github.com/409H/EtherAddressLookup/blob/master/blacklists/domains.json), and 
the extension will try to help you from being phished by removing the ability for you to interact with the blacklisted 
domain by wiping the DOM and displaying a notice. This functionality is toggleable, but it's best to keep it on.
  * If you find a domain that look suspicious and/or confirmed stealing private keys/being malicious, send 
a [pull request](https://github.com/409H/EtherAddressLookup/compare) or [open an issue](https://github.com/409H/EtherAddressLookup/issues/new).

### v1.2

* You can now select your favourite blockchain explorer for links to direct you to.

### v1.0

* This extension will search the DOM for any Ether address (a hexidecimal string) and add a link to it to your favourite
blockchain explorer. It will give you the option to add a highlight option so you can easily find addresses.