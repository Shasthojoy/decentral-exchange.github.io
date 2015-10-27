## P2P Content Delivery with IPFS

If you would like to use IPFS as content delivery, you should install
[IPFS](https://ipfs.io/) via [Go](http://golang.org):

    go get -u github.com/ipfs/go-ipfs/cmd/ipfs

Run the daemon to fetch the data with

    ipfs daemon

Investigate the current data structure with

{% for v in versions limit:1%}
    ipfs ls {{v.hash}}
{% endfor %}

If you want to support the P2P content delivery network, please consider
`pinning` these files to become a seed:

{% for v in versions limit:1%}
    ipfs pin add -r {{v.hash}}
{% endfor %}

## All Revisions


### BitShares 2.0
{% assign versions = (site.version | sort: 'build' | reverse) %}
<ul><small>
 {% for v in versions %}
  <li><tt>{{ v.date }}</tt>
   - <a href="http://ipfs.io/ipfs/{{ v.hash }}">IPFS</a> 
   / <a href="https://github.com/decentral-exchange/wallet/archive/{{ v.commit }}.zip"><i class="fa fa-file-archive-o"></i></a>
   / <a href="https://github.com/decentral-exchange/wallet/tree/{{ v.commit }}"><i class="fa fa-github-alt"></i></a>
  </li>
 {% endfor %}
</small></ul>

### MUSE
{% assign versions = (site.muse-version | sort: 'build' | reverse) %}
<ul><small>
{% for v in versions %}
 <li><tt>{{ v.date }}</tt>
  - <a href="http://ipfs.io/ipfs/{{ v.hash }}">IPFS</a> 
  / <a href="https://github.com/decentral-exchange/wallet/archive/{{ v.commit }}.zip"><i class="fa fa-file-archive-o"></i></a>
  / <a href="https://github.com/decentral-exchange/wallet/tree/{{ v.commit }}"><i class="fa fa-github-alt"></i></a>
 </li>
{% endfor %}
</small></ul>
