---
permalink: /buddha
layout: default
title: "布袋和尚简介"
---

# 布袋和尚简介

<div class="buddha">

  <div id="post">
    {% for post in site.posts %}
      {% if post.title == "弥勒菩萨东土应化事迹" %}
        {{ post.content }}
      {% endif %}
    {% endfor %}
  </div>
</div>

