---
layout: default
title: Home
---

<div style="
  max-width: 900px;
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

<style>
.category-section { display: none; }
.category-section.active { display: block; }
.category-section > div {
display: grid !important;
grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)) !important;
gap: 16px !important;
overflow-x: visible !important;
}
.filter-link.active-filter {
font-weight: 700;
text-decoration: underline;
}
</style>

<div style="max-width: 1200px; margin: 2rem auto 0;">

<nav style="display: flex; gap: 24px; margin-bottom: 2rem;">
<a href="#automations" class="filter-link" onclick="return showCategory('automations', this)">Automations</a>
<a href="#applications" class="filter-link" onclick="return showCategory('applications', this)">Applications</a>
<a href="#data" class="filter-link" onclick="return showCategory('data', this)">Data</a>
<a href="#uncategorised" class="filter-link" onclick="return showCategory('uncategorised', this)">Uncategorised</a>
</nav>

<div id="automations" class="category-section">
{% assign automation_posts = site.posts | where: "category", "Automations" %}
{% include post-cards.html posts=automation_posts %}
</div>

<div id="applications" class="category-section">
{% assign application_posts = site.posts | where: "category", "Applications" %}
{% include post-cards.html posts=application_posts %}
</div>

<div id="data" class="category-section">
{% assign data_posts = site.posts | where: "category", "Data" %}
{% include post-cards.html posts=data_posts %}
</div>

<div id="uncategorised" class="category-section">
{% assign uncategorised_posts = site.posts | where: "category", "Uncategorised" %}
{% include post-cards.html posts=uncategorised_posts %}
</div>

</div>

<script>
function showCategory(id, link) {
  document.querySelectorAll('.category-section').forEach(function(el) {
    el.classList.remove('active');
  });
  document.getElementById(id).classList.add('active');

  document.querySelectorAll('.filter-link').forEach(function(a) {
    a.classList.remove('active-filter');
  });
if (link) { link.classList.add('active-filter'); }

  history.replaceState(null, '', '#' + id);
return false;
}

document.addEventListener('DOMContentLoaded', function() {
var hash = window.location.hash.replace('#', '') || 'automations';
var link = document.querySelector('a[href$="#' + hash + '"]');
showCategory(hash, link);
});
</script>