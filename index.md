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

<div style="max-width: 900px; margin: 2rem auto 0;">

<div style="margin-bottom: 2rem;">
<a href="#automations" class="filter-link">Automations</a>
<a href="#applications" class="filter-link">Applications</a>
<a href="#data" class="filter-link">Data</a>
<a href="#uncategorised" class="filter-link">Uncategorised</a>
</div>

<h2 id="automations" style="font-size: 1.4rem; margin-bottom: 1rem;">Automations</h2>
{% assign automation_posts = site.posts | where: "category", "Automations" %}
{% include post-cards.html posts=automation_posts %}

<h2 id="applications" style="font-size: 1.4rem; margin: 2rem 0 1rem;">Applications</h2>
{% assign application_posts = site.posts | where: "category", "Applications" %}
{% include post-cards.html posts=application_posts %}

<h2 id="data" style="font-size: 1.4rem; margin: 2rem 0 1rem;">Data</h2>
{% assign data_posts = site.posts | where: "category", "Data" %}
{% include post-cards.html posts=data_posts %}

<h2 id="uncategorised" style="font-size: 1.4rem; margin: 2rem 0 1rem;">Uncategorised</h2>
{% assign uncategorised_posts = site.posts | where: "category", "Uncategorised" %}
{% include post-cards.html posts=uncategorised_posts %}

</div>