---
layout: default
---
<div class="brand">&copy;<strong>布袋豆腐</strong>（2023-2024）</div>
<pre>
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
      toggler.classList.toggle('active');
      body.classList.toggle('active');
    };
  });
</script>
