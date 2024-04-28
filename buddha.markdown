---
permalink: buddha
layout: default
title: "布袋和尚简介"
---

# 布袋和尚简介

<figure class="figure">
  <img src="https://cdn.jsdelivr.net/gh/budaipro/assets@latest/img/Budai,_British_Museum.jpg" alt="布袋和尚像">
  <figcaption>布袋和尚像</figcaption>
</figure>

<div class="buddha">

  <div id="post">
    {% for post in site.posts %}
      {% if post.title == "「弥勒菩萨」东土应化事迹" %}
        {{ post.content }}
      {% endif %}
    {% endfor %}
  </div>
</div>

