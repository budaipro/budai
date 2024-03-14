---
layout: default
---
<div id="imagegallery">
  <div id="imagegallery-body">
    <img src="/assets/img/tofu/gallery/buddha.jpg" alt="/assets/img/tofu/gallery/buddha.jpg">
    <img src="/assets/img/tofu/gallery/00.jpg" alt="/assets/img/tofu/gallery/00.jpg">
    <img src="/assets/img/tofu/gallery/01.jpg" alt="/assets/img/tofu/gallery/01.jpg">
    <img src="/assets/img/tofu/gallery/02.jpg" alt="/assets/img/tofu/gallery/02.jpg">
    <img src="/assets/img/tofu/gallery/03.jpg" alt="/assets/img/tofu/gallery/03.jpg">
    <img src="/assets/img/tofu/gallery/05.jpg" alt="/assets/img/tofu/gallery/05.jpg">
    <img src="/assets/img/tofu/gallery/06.jpg" alt="/assets/img/tofu/gallery/05.jpg">
    <img src="/assets/img/tofu/gallery/07.jpg" alt="/assets/img/tofu/gallery/07.jpg">
    <img src="/assets/img/tofu/gallery/08.jpg" alt="/assets/img/tofu/gallery/08.jpg">
    <img src="/assets/img/tofu/gallery/logo_orignal.png" alt="/assets/img/tofu/gallery/logo_orignal.png">
    <img src="/assets/img/tofu/gallery/09.jpg" alt="/assets/img/tofu/gallery/09.jpg">
    <img src="/assets/img/tofu/gallery/10.jpg" alt="/assets/img/tofu/gallery/10.jpg">
    <img src="/assets/img/tofu/gallery/11.jpg" alt="/assets/img/tofu/gallery/11.jpg">
    <img src="/assets/img/tofu/gallery/12.jpg" alt="/assets/img/tofu/gallery/12.jpg">
    <img src="/assets/img/tofu/gallery/13.jpg" alt="/assets/img/tofu/gallery/13.jpg">
    <img src="/assets/img/tofu/gallery/14.jpg" alt="/assets/img/tofu/gallery/14.jpg">
    <img src="/assets/img/tofu/gallery/15.jpg" alt="/assets/img/tofu/gallery/15.jpg">
    <img src="/assets/img/tofu/gallery/16.jpg" alt="/assets/img/tofu/gallery/16.jpg">
  </div>
</div>
<style>
  #imagegallery {
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;
    overflow-x: hidden;
  }

  #imagegallery-body {
    display: flex;
    gap: 10px;
    position: absolute;
    top: 0;
    animation: move 150s linear infinite;
    -moz-animation-direction: left;
  }

  #imagegallery-body img {
    align-self: center;
    width: 200px;
    height: auto;
  }

  body.on-mobile #imagegallery-body {
    top: auto;
    bottom: 0;
  }

  body.on-mobile #imagegallery img {
    width: 120px;
  }
</style>
<script>
  (function() {
    var scroller = document.getElementById('imagegallery-body');
    var scrollerWidth = scroller.offsetWidth;
    var bodyWidth = document.body.offsetWidth;
    
    scroller.style.width = scrollerWidth + 'px';
    scroller.style.right = -scrollerWidth + 'px';
    
    var style = document.createElement('style');
    style.type = 'text/css';
    
    style.innerText = '@keyframes move { 0% { right:' + (-scrollerWidth) + 'px; } 100% { right:' + bodyWidth + 'px; }}';
    scroller.parentNode.appendChild(style);
  })();
</script>

<div class="tofu">
<pre>
{% include tofu/about.html %}
{% include tofu/product/index.html %}
{% include tofu/sales/index.html %}</pre>
</div>
<style>
  .tofu {
    display: inline-block;
    min-width: 400px;
    padding: 20px 10px;
    background-color: white;
    position: relative;
    z-index: 1;
    opacity: .95;
  }

  .on-mobile .tofu {
    min-width: 100%;
  }
</style>

<div id="footer">
  <em style="color: green; font-weight: bold;">纯素产品，不含五辛。</em>
  <a href="/inn.html" target="_blank">家庭民宿↗</a>
</div>
<style>
  #footer {
    padding: 0;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
  }

  #footer:after {
    display: block;
    content: "";
    clear: both;
  }

  #footer em,
  #footer a {
    background-color: rgba(255, 255, 255, .95);
  }

  #footer a {
    float: right;
    text-decoration: underline;
  } 
</style>

<div id="notes">
  <div>告知：</div>
  <div class="note"><span class="number">①</span><span style="font-weight: bold; border-bottom: 2px solid;">同样的产品，在不同经销商处的销售价格可能不一致。</span>由于当初我们定价并未考虑到给经销商预留合理的利润，出于他们自身的运营成本，售价可能会比我们的略高一些。</div>
  <div class="note"><span class="number">②</span><span style="font-weight: bold; border-bottom: 2px solid;">如果买到的产品已变质，请联系我们退款。</span>由于豆制品在<dfn title="常温：一般指15°C到25°C的温度。">常温</dfn>下也特别容易变质，加上我们不会添加防腐剂，所以即使在生产的过程中，一疏忽都会变质<sup>发酸等</sup>。对于因这种我们还不能完全防范的情况，导致您购买到的产品是变质的，请加我们的微信请求退款。</div>
</div>
<style>
  #notes {
    line-height: 1.585;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 40px;
  }

  #notes:after {
    display: block;
    content: "";
    clear: both;
  }

  #notes .note {
    width: 330px;
    padding: 6px;
    margin-right: 10px;
    float: left;
    background-color: yellow;
  }

  #notes .number {
    font-size: 145%;
    line-height: 1;
    vertical-align: middle;
    position: relative;
    top: -3px;
  }

  .on-mobile #notes {
    position: relative;
    left: 0;
    bottom: auto;
  }

  .on-mobile #notes .note {
    width: auto;
    margin: 10px 5px;
  }
</style>
