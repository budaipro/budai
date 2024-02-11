---
layout: default
---
<pre>
<div class="brand"><span>&copy;</span><strong>布袋豆腐</strong></div>
{% include tofu/about.html %}
{% include tofu/product/index.html %}
{% include tofu/sales/index.html %}
</pre>
<script>
document.querySelectorAll('.collapse')  
  .forEach(function(collapse) {
    var toggler = collapse.querySelector('.collapse-toggler');
    var body = collapse.querySelector('.collapse-body');
    
    toggler.onclick = function() {
      var togglerStyle = toggler.style;
      var bodyStyle = body.style;
      
      if (bodyStyle.display !== 'inline') {
        togglerStyle.fontWeight = 'bold';
        bodyStyle.display = 'inline';
      } else {
        togglerStyle.fontWeight = 'normal';
        bodyStyle.display = '';
      }
    };
  });
</script>
