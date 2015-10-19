---
layout: default
---

## What?

### IPFS

The InterPlanetary File System (IPFS) is a new hypermedia distribution protocol,
addressed by content and identities. IPFS enables the creation of completely
distributed applications. It aims to make the web faster, safer, and more open.

### BitShares 2.0

BitShares in version 2.0 offers a decentralized exchange for digital goods. It
offers stable crypto currencies like bitUSD and bitEUR and other assets. Due to
its blockchain nature, it is censorship resistant, open and cryptographically
secured.

## Where?

<ul>
{% for v in site.version %}
 <li>{{ v.date }} - <a href="http://ipfs.io/ipfs/{{ v.hash }}">IPFS</a></li>
{% endfor %}
</ul>
