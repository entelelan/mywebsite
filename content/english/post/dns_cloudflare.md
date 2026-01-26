+++
author = "EnteleLAN"
title = "Cloudflare - helping build a better Internet"
date = "2025-09-18"
description = "Cloudflare DNS"
+++

Cloudflare's goal is to help build a better Internet&mdash;an ambitious goal indeed. Their commitment to protecting and building a better Internet for every user is reflected in their DNS service, which blocks malware and adult content. In 2018, Cloudflare announced <a href="https://blog.cloudflare.com/announcing-1111/" target="_blank">1.1.1.1</a>, a privacy-first consumer DNS service. In 2020, Cloudflare announced <a href="https://blog.cloudflare.com/introducing-1-1-1-1-for-families/" target="_blank">1.1.1.1 for Families</a>, a security and adult content filter.

Cloudflare's **core privacy resolver** is **1.1.1.1** designed for speed and privacy. Their **security resolver** is **1.1.1.2**, includes all the benefits of 1.1.1.1 while also protecting users from sites containing malware, spam, botnet command-and-control attacks, or phishing threats. Additionally, their **family resolver** **1.1.1.3**, offers all the benefits of 1.1.1.2, with the added feature of blocking unwanted adult content from both direct site navigation and search engines locked to Safe Search mode.

For more information regarding Cloudflare's commitment to building a better Internet and delivering a safer browsing experience, checkout this <a href="https://blog.cloudflare.com/safer-resolver/" target="_blank">article</a> from <a href="https://blog.cloudflare.com/" target="_blank">The Cloudflare Blog</a>. And don't forget to explore their free app that makes your Internet experience safer: <a href="https://one.one.one.one/" target="_blank">1.1.1.1</a>.

<br>

## DNS Resolver Options

---

**Malware Blocking Only**  
Primary DNS: 1.1.1.2  
Secondary DNS: 1.0.0.2

**Malware and Adult Content**  
Primary DNS: 1.1.1.3  
Secondary DNS: 1.0.0.3

<br>

### For IPv6 use:
**Malware Blocking Only**  
Primary DNS: 2606:4700:4700::1112  
Secondary DNS: 2606:4700:4700::1002

**Malware and Adult Content**  
Primary DNS: 2606:4700:4700::1113  
Secondary DNS: 2606:4700:4700::1003

<div class="commentbox"></div>

<script src="https://unpkg.com/commentbox.io/dist/commentBox.min.js"></script>
<script>
  commentBox('5668915749322752-proj', {
    backgroundColor: 'transparent',
    textColor: '#ffffff',
    subtextColor: '#ffffff',
    sortOrder: 'newest'
  });
</script>