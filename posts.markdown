---
layout: post
---
<div>
{% for post in site.posts %}
    <div style="padding-left: 50px;">{{ post.content }}</div>
{% endfor %}
</div>
