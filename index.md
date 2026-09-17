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

<div style="max-width: 900px; margin: 2rem auto 0; display: flex; gap: 2rem; align-items: flex-start;">

<nav style="
  flex: 0 0 140px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  position: sticky;
  top: 2rem;
">
<a href="https://sydocs.github.io/#automations" class="filter-link">Automations</a>
<a href="https://sydocs.github.io/#applications" class="filter-link">Applications</a>
<a href="https://sydocs.github.io/#data" class="filter-link">Data</a>
<a href="https://sydocs.github.io/#uncategorised" class="filter-link">Uncategorised</a>
</nav>

<div style="flex: 1; min-width: 0;">

<div id="automations">
{% assign automation_posts = site.posts | where: "category", "Automations" %}
{% include post-cards.html posts=automation_posts %}
</div>

<div id="applications" style="margin-top: 2rem;">
{% assign application_posts = site.posts | where: "category", "Applications" %}
{% include post-cards.html posts=application_posts %}
</div>

<div id="data" style="margin-top: 2rem;">
{% assign data_posts = site.posts | where: "category", "Data" %}
{% include post-cards.html posts=data_posts %}
</div>

<div id="uncategorised" style="margin-top: 2rem;">
{% assign uncategorised_posts = site.posts | where: "category", "Uncategorised" %}
{% include post-cards.html posts=uncategorised_posts %}
</div>

</div>

</div>