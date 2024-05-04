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

<hr>

<ul>
  {%- for tag in site.tags -%}
    <li>
      <h3>《{{ tag[0] }}》</h3>
      <ul>
        {%- for post in tag[1] -%}
          <li><a href="{{post.url}}">{{post.title}}</a></li>
        {%- endfor -%}
      </ul>
    </li>
  {%- endfor -%}
</ul>