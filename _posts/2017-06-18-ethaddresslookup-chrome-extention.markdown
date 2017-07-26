---
layout: post
title: "EthAddressLookup Chrome Extension (Initial Release)"
date: 2017-06-18 23:48:00 +0100
permalink: /ethaddresslookup-chrome-extension/
categories: ethereum, extension
is_blog_post: false
comments: true
---

**GITHUB:** [https://github.com/409H/EtherAddressLookup](https://github.com/409H/EtherAddressLookup)


I was getting a little tired of copy/pasting Ethereum addresses into Etherscan, so I made a Chrome Extension to search the
DOM and put links for all non-linked Ethereum Addresses (well, strings that looks like an Ethereum address.)

It is my first Chrome Extension, the first release, and I am expecting to push a few updates out.

Effectively, it injects an JavaScript file on the active tab and runs the following;

```js
document.body.innerHTML = document.body.innerHTML.replace(
    new RegExp("(?!.*\")(0[xX][0-9a-fA-F]{40})(?!\")(!?<\s|\<|$)", "g"), 
    `<a href="https://etherscan.io/address/$1" class="ext-etheraddresslookup-link">$1</a>$2`
);
```

And that's it. Nothing special, but I needed it, so I made it &mdash; I hope it comes in use for you also.

### Notes
* I plan to code up the following;
  * Add the ability to disable the extension styles for the link
  * Add the option to show a popup on-hover of the address to show basic information (balance, transaction count)
* I haven't got a Chrome Developer account *yet*, so it's not an official release, but it will be soon.

### Preview

Here's a GIF of it in action on a random Reddit thread.

![/assets/images/blog-ethereumaddresslookup.gif](/assets/images/blog-ethereumaddresslookup.gif)

### Installation

* Clone/download [the repo](https://github.com/409H/EtherAddressLookup).
* Go to [chrome://extensions](chrome://extensions) in Chrome.
* Turn on developer mode.
* Load the `manifest.json` file by dragging and dropping.
