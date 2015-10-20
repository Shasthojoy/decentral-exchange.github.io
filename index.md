---
layout: default
---

## What?

<tt>decentral.exchange</tt> offers a peer-2-peer entry to the <a
href="http://bitshares.org">BitShares 2</a> decentralized exchange. There,
people can trade digital goods freely and without counter-party risk.

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
<div class="text-center">
{% assign versions = (site.version | sort: 'build' | reverse) %}
{% for v in versions limit:1%}
<a class="btn btn-lg btn-success" href="ipfs://{{ v.hash }}">
  <i class="fa fa-users fa-3x pull-left"></i> Peer-2-Peer<br/>
                                          <small>v: <tt>{{v.commit}}</tt></small><br/>
                                          <small>(requires IPFS)</small></a>
<a class="btn btn-lg btn-danger" href="http://ipfs.io/ipfs/{{ v.hash }}">
  <i class="fa fa-user fa-3x pull-left"></i> via Gateway<br/>
                                          <small>v: <tt>{{v.commit}}</tt></small><br/>
                                          <small>(via ipfs.io)</small></a>
{% endfor %}
</div>


#### All Versions
<ul>
{% for v in versions %}
 <li><tt>{{ v.date }}</tt>
  - <a href="http://ipfs.io/ipfs/{{ v.hash }}">IPFS</a> 
  / <a href="https://github.com/decentral-exchange/wallet/archive/{{ v.commit }}.zip"><i class="fa fa-file-archive-o"></i></a>
  / <a href="https://github.com/decentral-exchange/wallet/tree/{{ v.commit }}"><i class="fa fa-github-alt"></i></a>
 </li>
{% endfor %}
</ul>

## How?
* **Github** <a aria-label="Star decentral-exchange/wallet on GitHub"
           data-count-aria-label="# stargazers on GitHub"
           data-count-api="/repos/decentral-exchange/wallet#stargazers_count"
           data-count-href="/decentral-exchange/wallet/stargazers" data-icon="octicon-star"
           href="https://github.com/decentral-exchange/wallet"
           class="github-button">Star</a>
  * All data of this webpage is 
    * publicly auditable at <a href="https://github.com/decentral-exchange"><i class="fa fa-github-alt"></i> github</a>
    * hosted at <a href="https://github.com/decentral-exchange/decentral-exchange.github.io"><i class="fa fa-github-alt"></i> github</a>

* **Travis-CI**:
  * Fetches the **official** sources from <a href="https://github.com/bitshares/bitshares-2-ui"><i class="fa fa-github-alt"></i> github</a> and compiles them to a bundle.
  * The build script can be downloaded from <a href="https://github.com/decentral-exchange/build"><i class="fa fa-github-alt"></i> github</a>
  * The build process can be investigated at <a href="https://travis-ci.org/decentral-exchange/"><i class="fa fa-building"></i> Travis CI</a>
* **IPFS**
  * Content Delivery Network provided by <a href="http://ipfs.io"><i class="fa fa-gloab"></i> Inter-Planetary File-System</a>
  * Immuatable Permanent Data Storage
  * Peer-2-Peer data delivery
