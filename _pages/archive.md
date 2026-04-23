---
layout: default
title: Course Archive
permalink: /archive/
eyebrow: Teaching History
---

<div class="wrap">
  <header style="padding:60px 0 36px;border-bottom:1px solid var(--border);">
    <div class="eyebrow">Teaching History</div>
    <h1>Course <em>Archive</em></h1>
    <p class="hero-desc" style="margin-top:16px;">All courses taught from 2023 to present, organized by semester.</p>
  </header>

  <main style="padding:40px 0 80px;">
    {%- for cat in site.course_categories -%}
      {%- assign cat_courses = site.courses | where: "category", cat.key -%}
      {%- if cat_courses.size > 0 -%}
      <div class="semester-section" style="margin-bottom:44px;padding-top:0;">
        <div class="semester-label">{{ cat.label }}</div>
        <div class="course-grid">
          {%- assign sorted = cat_courses | sort: "importance" -%}
          {%- for course in sorted -%}
            {% include course_card.html course=course %}
          {%- endfor -%}
        </div>
      </div>
      {%- endif -%}
    {%- endfor -%}
  </main>
</div>
