---
layout: page
title: Archive
---
# Archive #

<p>
{% for post in site.posts %}
  {% if post.wordpress_id == null and post.plyturonnet == null %}
    <span class="archive-date">{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a><br />
  {% endif %}
{% endfor %}
</p>
# phansch.de #

<small>All posts from my old blog on blog.phansch.de. The early ones are in German and I do not plan on translating them.</small>
<p id="phansch">
{% for post in site.posts %}
  {% if post.wordpress_id != null and post.plyturonnet == null %}
    <span class="archive-date">{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a><br />
  {% endif %}
{% endfor %}
</p>

# plyturon.net #

<small>Posts from plyturon.net. My old gaming blog.</small>
<p id="plyturon">
{% for post in site.posts %}
  {% if post.plyturonnet %}
    <span class="archive-date">{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a><br />
  {% endif %}
{% endfor %}
</p>