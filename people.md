---
layout: page
title: people
permalink: /people/
horizontal: true
---

<hr>
<!-- pages/people.md -->
<div class="people">
  <div class="container">

    <!-- ==================== PRINCIPAL INVESTIGATOR ==================== -->
    {%- assign pis = site.people | where: "category", "pi" -%}
    {%- for person in pis -%}
      {% include people.html %}
      <hr>
    {%- endfor %}

    <!-- ==================== GRAD STUDENTS ==================== -->
    <h2 class="category-heading" style="margin-top: 2rem; margin-bottom: 1.5rem;">Graduate Students</h2>
    {%- assign phds = site.people | where: "category", "grad" | sort: "slug" -%}
    {%- for person in phds -%}
      {% include people.html %}
      <hr>
    {%- endfor %}

    <!-- ==================== UNDERGRADUATE RESEARCHERS ==================== -->
    <h2 class="category-heading" style="margin-top: 2rem; margin-bottom: 1.5rem;">Undergraduate Students</h2>
    {%- assign undergrads = site.people | where: "category", "undergrad" | sort: "slug" -%}
    {%- for person in undergrads -%}
      {% include people.html %}
      <hr>
    {%- endfor %}

  </div>
</div>
