## Using P2P Content Delivery with IPFS

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
