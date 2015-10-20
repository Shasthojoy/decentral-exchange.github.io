---
layout: default
---

<div class="row">
 <div class="col-md-4">
{% capture my_include %}{% include col1.md %}{% endcapture %}
{{ my_include | markdownify }}
 </div>
 <div class="col-md-4">
{% capture my_include %}{% include col2.md %}{% endcapture %}
{{ my_include | markdownify }}
 </div>
 <div class="col-md-4">
{% capture my_include %}{% include col3.md %}{% endcapture %}
{{ my_include | markdownify }}
 </div>
</div>
