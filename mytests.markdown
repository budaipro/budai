---
permalink: /mytests
layout: default
title: "测试页面"
---

<ul class="posts">
    {%- for post in site.posts -%}
        <li>
            <div><a href="{{ post.url }}">{{ post.title }}</a></div>
        </li>
    {%- endfor -%}
</ul>