---
layout: default
title: Applications Posts
permalink: /posts/applications/
---

# Category: Applications

{% assign filtered = site.posts | where: "category", "Applications" %}

{% include post-cards.html posts=filtered %}