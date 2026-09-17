---
layout: default
title: Posts
permalink: /post/
---
# Posts
[Automation](/posts/automation/){: .filter-link } 
[Applications](/posts/applications/){: .filter-link }
[Data](/posts/data/){: .filter-link } 
[Uncategorised](/posts/uncategorised/){: .filter-link }

{% for post in site.posts %}
  {% assign card_link = post.repo %}
  {% if post.has_writeup %}
    {% assign card_link = post.url | relative_url %}
  {% endif %}

<div onclick="window.location='{{ card_link }}'" style="
  cursor: pointer;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  padding: 1rem 1.5rem;
  margin-bottom: 1.5rem;
">

<span style="font-size: 1.2rem; font-weight: bold; color: #333;">
    {{ post.title }}
</span><br>

  {% if post.category %}
<span style="font-size: 0.8rem; color: #666;">Category: {{ post.category }}</span><br>
  {% endif %}

  {% if post.date %}
<span style="color: #999; font-size: 0.9rem;">
    {{ post.date | date: "%B %-d, %Y" }}
</span><br>
  {% endif %}

  {% if post.has_writeup and post.repo %}
<div style="margin-top: 14px;">
<a href="{{ post.repo }}" target="_blank" onclick="event.stopPropagation()" style="color: #e8a33d; font-weight: 500; font-size: 13px; text-decoration: none;">github</a>
</div>
  {% endif %}

</div>
{% endfor %}