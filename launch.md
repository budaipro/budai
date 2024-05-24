---
permalink: /launch
layout: default
title: "启动"
---

<h1>启动</h1>

<pre style="font-size: 13pt;">
<div class="collapse"><span class="collapse-toggler" data-toggle="collapse">布袋<sup>&reg;</sup>豆腐</span><div class="collapse-body">
├ <div class="collapse"><span class="collapse-toggler" data-toggle="collapse">产品</span><div class="collapse-body">
│ ├ 豆腐
│ ├ 豆腐干
│ ├ 油豆腐
│ └ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">其他</span><div class="collapse-body">
│   ├ <span class="muted">嫩豆腐</span>
│   ├ <span class="muted">毛豆腐</span>
│   ├ <span class="muted">臭豆腐</span>
│   └ <span class="muted">豆腐乳</span></div></div>
│</div></div>
├ <div class="collapse"><strong class="collapse-toggler" data-toggle="collapse">实例<small><em>（种子）</em></small></strong><div class="collapse-body">
│ ├ <div class="collapse"><span class="collapse-toggler" data-toggle="collapse">相关证件</span><div class="collapse-body">
│ │ ├ 营业执照
│ │ └ 食品经营许可证</div></div>
│ ├ <div class="collapse"><span class="collapse-toggler" data-toggle="collapse">作坊</span><div class="collapse-body">
│ │ └ 银桥镇鹤阳村委会一社</div></div>
│ └ <div class="collapse"><span class="collapse-toggler" data-toggle="collapse">自营店</span><div class="collapse-body">
│   ├ 大关邑（下关）
│   ├ 龙溪路（下关）
│   └ 银仓路（古城）</div></div></div></div>
│
├ <div class="collapse"><span class="collapse-toggler" data-toggle="collapse">云南</span><div class="collapse-body">
│ ├ <span>大理<small><em>（见上实例）</em></small></span>
│ └ <span class="muted">昆明</span>
│</div></div>
├ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">四川</span><div class="collapse-body">
│ └ <span class="muted">成都</span>
│</div></div>
├ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">重庆</span><div class="collapse-body">
│ └ <span class="muted">重庆</span>
│</div></div>
├ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">广东</span><div class="collapse-body">
│ ├ <span class="muted">广州</span>
│ ├ <span class="muted">深圳</span>
│ └ <span class="muted">珠海</span>
│</div></div>
├ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">湖北</span><div class="collapse-body">
│ └ <span class="muted">武汉</span>
│</div></div>
├ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">湖南</span><div class="collapse-body">
│ └ <span class="muted">长沙</span>
│</div></div>
├ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">江西</span><div class="collapse-body">
│ └ <span class="muted">南昌</span>
│</div></div>
├ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">浙江</span><div class="collapse-body">
│ ├ <span class="muted">杭州</span>
│ ├ <span class="muted">宁波</span>
│ └ <span class="muted">温州</span>
│</div></div>
├ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">上海</span><div class="collapse-body">
│ └ <span class="muted">上海</span>
│</div></div>
└ <div class="collapse"><span class="collapse-toggler muted" data-toggle="collapse">江苏</span><div class="collapse-body">
  ├ <span class="muted">南京</span>
  └ <span class="muted">苏州</span></div></div>
</div></div></pre>

<script>    
  window.addEventListener('load', function() {
    document.querySelectorAll('.collapse')
      .forEach(function(collapse) {
        var toggler = collapse.querySelector('.collapse-toggler');
        var body = collapse.querySelector('.collapse-body');
        
        toggler.onclick = function() {
          toggler.classList.toggle('active');
          body.classList.toggle('active');
        };
      });
  }, false);
</script>