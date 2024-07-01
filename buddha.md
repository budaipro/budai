---
permalink: /buddha
layout: default
title: "布袋和尚简介"
---

# 布袋和尚简介

<div class="buddha">

{%- comment -%}
 <figure class="figure" style="margin: 0;">
  <img src="https://gcore.jsdelivr.net/gh/budaipro/assets/img/Budai,_British_Museum.jpg" alt="Budai,_British_Museum.jpg">
 </figure>
 {%- endcomment -%}

  <div id="post">
    {% for post in site.posts %}
      {% if post.title == "弥勒菩萨东土应化事迹" %}
        {{ post.content }}
      {% endif %}
    {% endfor %}
  </div>
</div>

