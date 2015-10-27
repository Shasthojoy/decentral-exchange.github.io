## Where?

### BitShares 2.0
<div class="text-center">
{% assign versions = (site.version | sort: 'build' | reverse) %}
{% for v in versions limit:1%}
<a class="btn btn-lg btn-success" href="ipfs://{{ v.hash }}">
  <i class="fa fa-users fa-3x pull-left"></i> Decentralized<br/>
                                          <small>v: <tt>{{v.commit}}</tt></small><br/>
                                          <small>(requires IPFS)</small></a>
<a class="btn btn-lg btn-danger" href="http://ipfs.io/ipfs/{{ v.hash }}">
  <i class="fa fa-user fa-3x pull-left"></i> Centralized<br/>
                                          <small>v: <tt>{{v.commit}}</tt></small><br/>
                                          <small>(via ipfs.io)</small></a>
{% endfor %}
</div>

### MUSE
<div class="text-center">
{% assign versions = (site.muse-version | sort: 'build' | reverse) %}
{% for v in versions limit:1%}
<a class="btn btn-lg btn-success" href="ipfs://{{ v.hash }}">
  <i class="fa fa-users fa-3x pull-left"></i> Decentralized<br/>
                                          <small>v: <tt>{{v.commit}}</tt></small><br/>
                                          <small>(requires IPFS)</small></a>
<a class="btn btn-lg btn-danger" href="http://ipfs.io/ipfs/{{ v.hash }}">
  <i class="fa fa-user fa-3x pull-left"></i> Centralized<br/>
                                          <small>v: <tt>{{v.commit}}</tt></small><br/>
                                          <small>(via ipfs.io)</small></a>
{% endfor %}
</div>

## Screenshot?

Yes! Screenshot!

![Screenshot of the decentral exchange](images/dex.png)
