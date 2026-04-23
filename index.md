---
layout: default
title: Courses
permalink: /
---

<div class="wrap">

  <header class="home-hero">
    <div class="today-pill animate d1" id="today-pill">
      <span class="today-dot"></span>
      <span id="today-text">Loading...</span>
    </div>

    <div class="eyebrow">Prof. Aaron Snowberger</div>
    <h1 class="animate d2">Courses &<br><em>Teaching</em></h1>
    <p class="hero-desc animate d3">
      Computer Science &amp; Engineering courses taught at five Korean universities.
      Find schedules, textbooks, assignments, and policies for all active courses.
      <br><br>
      한국 5개 대학에서 가르치는 컴퓨터 공학 강좌입니다.
      현재 강좌의 강의 일정, 교재, 과제, 규정을 확인하세요.
    </p>

    <div class="stats-bar animate d4">
      {%- assign total_courses = site.courses | size -%}
      {%- assign active_courses = site.courses | where: "now", "Yes" | size -%}
      <div class="stat">
        <div class="stat-num">{{ active_courses }}</div>
        <div class="stat-label">Active Courses</div>
      </div>
      <div class="stat">
        <div class="stat-num">5</div>
        <div class="stat-label">Universities</div>
      </div>
      <div class="stat">
        <div class="stat-num">{{ total_courses }}</div>
        <div class="stat-label">Total Courses</div>
      </div>
      <div class="stat">
        <div class="stat-num">2023</div>
        <div class="stat-label">Since</div>
      </div>
    </div>
  </header>

  <!-- ── Announcements ────────────────────────────────────────────────────── -->
  {%- if site.data.announcements and site.data.announcements.size > 0 -%}
  <div class="announcements-section animate d4">
    {%- for item in site.data.announcements -%}
    <div class="announce-item {{ item.type | default: 'info' }}">
      <div class="announce-meta">
        <span class="announce-date">{{ item.date | date: "%b %-d, %Y" }}</span>
      </div>
      <div class="announce-body">
        <strong data-en="{{ item.title }}" data-ko="{{ item.title_ko }}">{{ item.title }}</strong>
        <span data-en="{{ item.body }}" data-ko="{{ item.body_ko }}"> — {{ item.body }}</span>
      </div>
    </div>
    {%- endfor -%}
  </div>
  {%- endif -%}

  <!-- ── Current Semester ───────────────────────────────────────────────── -->
  <div class="semester-section animate d4">
    <div class="section-top">
      <div class="section-heading-row">
        <span class="section-label">Spring 2026 / 2026년 1학기</span>
        <span class="section-line"></span>
      </div>
      <div class="section-actions">
        <button class="thumb-toggle" id="thumb-toggle">
          <span class="t-icon">⊞</span> Thumbnails
        </button>
      </div>
    </div>

    <div id="thumb-section">
      <div class="course-grid">
        {%- assign current_courses = site.courses | where: "category", "2026-1" | sort: "importance" -%}
        {%- for course in current_courses -%}
          {% include course_card.html course=course %}
        {%- endfor -%}
      </div>
    </div>
  </div>

  <!-- ── Archive preview ───────────────────────────────────────────────── -->
  <div class="semester-section" style="padding-bottom:80px;">
    <div class="section-top">
      <div class="section-heading-row">
        <span class="section-label">Previous Semesters</span>
        <span class="section-line"></span>
      </div>
      <div class="section-actions">
        <a href="{{ '/archive' | relative_url }}" class="back-btn">Archive →</a>
      </div>
    </div>
    {%- assign past_categories = site.course_categories | shift -%}
    {%- for cat in past_categories -%}
      {%- assign cat_courses = site.courses | where: "category", cat.key -%}
      {%- if cat_courses.size > 0 -%}
      <div class="semester-label">{{ cat.label }}</div>
      <div class="course-grid">
        {%- assign sorted = cat_courses | sort: "importance" -%}
        {%- for course in sorted -%}
          {% include course_card.html course=course %}
        {%- endfor -%}
      </div>
      {%- endif -%}
    {%- endfor -%}
  </div>

</div><!-- /.wrap -->

<script>
// ── Today pill ────────────────────────────────────────────────────────────────
(function() {
  const schedule = {
    1: { name: 'UT — Korea Transportation University', ko: '한국교통대학교 (월요일)' },
    2: { name: 'WKU — Wonkwang University',           ko: '원광대학교 (화요일)' },
    3: { name: 'JBNU — Jeonbuk University',           ko: '전북대학교 (수요일)' },
    4: { name: 'JBNU — Jeonbuk University',           ko: '전북대학교 (목요일)' },
    5: { name: 'JNUE — Jeonju Natl. Univ. of Ed.',   ko: '전주교육대학교 (금요일)' },
  };
  const day = new Date().getDay(); // 0=Sun, 6=Sat
  const pill = document.getElementById('today-pill');
  const txt  = document.getElementById('today-text');
  if (day === 0 || day === 6) {
    pill.classList.add('noclass');
    txt.textContent = 'Weekend — No Class / 주말 — 휴강';
  } else if (schedule[day]) {
    txt.textContent = 'Today: ' + schedule[day].name;
  } else {
    pill.classList.add('noclass');
    txt.textContent = 'No Class Today / 오늘은 강의 없음';
  }
})();

// ── Thumbnail toggle ──────────────────────────────────────────────────────────
const _tt = document.getElementById('thumb-toggle');
if (_tt) {
  const _sec = document.getElementById('thumb-section');
  _tt.addEventListener('click', () => {
    const a = _sec.classList.toggle('thumbs-active');
    _tt.classList.toggle('active', a);
    const ic = _tt.querySelector('.t-icon');
    if (ic) ic.textContent = a ? '⊟' : '⊞';
  });
}
</script>
