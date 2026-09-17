---
layout: default
title: Home
---

<div style="
  max-width: 600px;
  margin: 3rem auto;
  padding: 2rem;
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  text-align: center;
">

  <img src="/assets/images/profile.jpg" alt="Profile picture" style="
    width: 120px;
    height: 120px;
    object-fit: cover;
    border-radius: 50%;
    margin-bottom: 1rem;
  ">

  <h1 style="font-size: 2rem; font-weight: bold; color: #000000; margin-bottom: 0.5rem;">
  sydocs
  </h1>

  <p style="font-size: 0.9rem; color: #000000; margin: 0;">
  Documenting my learnings~ 
  </p>

</div>

<div style="max-width: 700px; margin: 2rem auto 0;">

[Automations](/posts/automations/){: .filter-link } 
[Applications](/posts/applications/){: .filter-link }
[Data](/posts/data/){: .filter-link } 
[Uncategorised](/posts/uncategorised/){: .filter-link }

{% include post-cards.html posts=site.posts %}

</div>