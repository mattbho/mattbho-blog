+++
title = "GitHub Pages Custom Domain Setup"
author = ["Matt Ho"]
date = 2026-07-04
draft = false
+++

Notes for next time I set up a custom domain on GitHub Pages.
_It's actually been years since I set up my personal web-site. I've owned this domain for years but have never deployed anything on it... lol. So here's what I discovered and learned. Mainly for my own reference as I'm sure I'll need to do this again but its for anyone who wants to set up their own website and assign a domain._


## DNS records {#dns-records}

**Apex domain** _(Fancy word for root domain, nothing in front of it like www. or any subdomain)_ - four **A records**:

Set this on Squarespace to point to Github's Pages servers (Because I am deploying on gh pages)

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**www subdomain** - one **CNAME** record pointing to `mattbho.github.io`.


## After saving DNS {#after-saving-dns}

1.  Set the custom domain in repo **Settings &gt; Pages**
2.  Wait 10-30 minutes - GitHub provisions a **Let's Encrypt cert** automatically, but it needs DNS to propagate first _(took a whole day for me don't be surprised lol)_
3.  Once **Enforce HTTPS** is clickable, enable it
