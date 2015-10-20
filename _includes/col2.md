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

## Screenshot?

Yes! Screenshot!

![Screenshot of the decentral exchange](images/dex.png)
