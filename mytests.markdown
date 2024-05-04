---
permalink: /mytests
layout: default
title: "测试页面"
---

<div class="posts">
    {%- for post in site.posts -%}
        <div>
            <div><a href="{{ post.url }}">{{ post.title }}</a></div>
        </div>
    {%- endfor -%}
</div>