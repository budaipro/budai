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
│ └ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">其他</span><div class="collapse-body">
│   ├ 嫩豆腐
│   ├ 毛豆腐
│   ├ 臭豆腐
│   └ 豆腐乳</div></div>
│</div></div>
├ <div class="collapse"><strong class="collapse-toggler" data-toggle="collapse">实例<small><em>（种子）</em></small></strong><div class="collapse-body">
│ ├ <div class="collapse"><span class="collapse-toggler" data-toggle="collapse">相关证件</span><div class="collapse-body">
│ │ ├ 营业执照
│ │ └ 食品经营许可证</div></div>
│ ├ <div class="collapse"><span class="collapse-toggler" data-toggle="collapse">作坊</span><div class="collapse-body">
│ │ └ 银桥镇鹤阳村委会一社</div></div>
│ └ <div class="collapse"><span class="collapse-toggler" data-toggle="collapse">自营店</span><div class="collapse-body">
│    ├ 大关邑（下关）
│    ├ 龙溪路（下关）
│    └ 银仓路（古城）</div></div>
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">云南</span><div class="collapse-body">
│ ├ <span style="opacity: 1;">大理<small><em>（见上实例）</em></small></span>
│ └ 昆明
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">四川</span><div class="collapse-body">
│ └ 成都
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">重庆</span><div class="collapse-body">
│ └ 重庆
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">广东</span><div class="collapse-body">
│ ├ 广州
│ ├ 深圳
│ └ 珠海
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">湖北</span><div class="collapse-body">
│ └ 武汉
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">湖南</span><div class="collapse-body">
│ └ 长沙
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">江西</span><div class="collapse-body">
│ └ 南昌
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">浙江</span><div class="collapse-body">
│ ├ 杭州
│ ├ 宁波
│ └ 温州
│</div></div>
├ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">上海</span><div class="collapse-body">
│ └ 上海
│</div></div>
└ <div class="collapse muted"><span class="collapse-toggler" data-toggle="collapse">江苏</span><div class="collapse-body">
  ├ 南京
  └ 苏州</div></div>
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