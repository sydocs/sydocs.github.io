---
layout: default
title: Applications Posts
permalink: /posts/applications/
---

# Category: Applications

{% assign filtered = site.posts | where: "category", "Applications" %}

{% for post in filtered %}
  {% assign card_link = post.repo %}
  {% if post.has_writeup %}
    {% assign card_link = post.url | relative_url %}
  {% endif %}

<div onclick="window.location='{{ card_link }}'" style="
  cursor: pointer;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 1rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
">

<span style="font-size: 1.2rem; font-weight: bold; color: #333;">
    {{ post.title }}
</span><br>

  {% if post.category %}
<span style="font-size: 0.8rem; color: #666;">Category: {{ post.category }}</span><br>
  {% endif %}

<span style="color: #999; font-size: 0.9rem;">
    {{ post.date | date: "%B %-d, %Y" }}
</span><br>

  {% if post.has_writeup and post.repo %}
<div style="margin-top: 14px;">
<a href="{{ post.repo }}" target="_blank" onclick="event.stopPropagation()" style="text-decoration: none; color: inherit;">github</a>
</div>
  {% endif %}

</div>
{% endfor %}