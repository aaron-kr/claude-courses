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
    <h1 class="animate d2">Courses &amp;<br><em>Teaching</em></h1>
    <p class="hero-desc animate d3">
      <span class="lang-en">Computer Science &amp; Engineering courses taught at five Korean universities.
      Find schedules, textbooks, assignments, and policies for all active courses.</span>
      <span class="lang-ko">한국 5개 대학에서 가르치는 컴퓨터 공학 강좌입니다.
      현재 강좌의 강의 일정, 교재, 과제, 규정을 확인하세요.</span>
    </p>

    <div class="stats-bar animate d4">
      {%- assign active_courses = site.courses | where: "now", "Yes" -%}
      {%- assign total_courses  = site.courses | size -%}
      {%- comment -%} Count unique universities from active courses via logo abbr {%- endcomment -%}
      {%- assign _seen_unis = "" -%}
      {%- assign _uni_count = 0 -%}
      {%- for c in active_courses -%}
        {%- assign _ua = c.logo | remove: '-logo.png' | remove: '-logo-2.png' | upcase -%}
        {%- unless _seen_unis contains _ua -%}
          {%- assign _uni_count = _uni_count | plus: 1 -%}
          {%- assign _seen_unis = _seen_unis | append: _ua | append: "," -%}
        {%- endunless -%}
      {%- endfor -%}
      {%- comment -%} Total unique universities ever {%- endcomment -%}
      {%- assign _all_seen = "" -%}
      {%- assign _all_uni_count = 0 -%}
      {%- for c in site.courses -%}
        {%- assign _ua2 = c.logo | remove: '-logo.png' | remove: '-logo-2.png' | upcase -%}
        {%- unless _all_seen contains _ua2 -%}
          {%- assign _all_uni_count = _all_uni_count | plus: 1 -%}
          {%- assign _all_seen = _all_seen | append: _ua2 | append: "," -%}
        {%- endunless -%}
      {%- endfor -%}
      <div class="stat">
        <div class="stat-num">{{ active_courses.size }}</div>
        <div class="stat-label"><span class="lang-en">Active Courses</span><span class="lang-ko">현재 강좌</span></div>
      </div>
      <div class="stat">
        <div class="stat-num">{{ _all_uni_count }}</div>
        <div class="stat-label"><span class="lang-en">Universities</span><span class="lang-ko">대학교</span></div>
      </div>
      <div class="stat">
        <div class="stat-num">{{ total_courses }}</div>
        <div class="stat-label"><span class="lang-en">Total Courses</span><span class="lang-ko">총 강좌</span></div>
      </div>
      <div class="stat">
        <div class="stat-num">2021</div>
        <div class="stat-label"><span class="lang-en">Teaching Since</span><span class="lang-ko">첫 강의</span></div>
      </div>
    </div>

    <!-- Profile links -->
    <div class="profile-links animate d4">
      {%- if site.orcid_id -%}
      <a href="https://orcid.org/{{ site.orcid_id }}" class="profile-link" target="_blank"><span class="pl-icon">🆔</span> ORCID</a>
      {%- endif -%}
      {%- if site.github_username -%}
      <a href="https://github.com/{{ site.github_username }}" class="profile-link" target="_blank"><span class="pl-icon">⌨</span> GitHub</a>
      {%- endif -%}
      {%- if site.scholar_userid -%}
      <a href="https://scholar.google.com/citations?user={{ site.scholar_userid }}" class="profile-link" target="_blank"><span class="pl-icon">🎓</span> Google Scholar</a>
      {%- endif -%}
      {%- if site.linkedin_username -%}
      <a href="https://linkedin.com/in/{{ site.linkedin_username }}" class="profile-link" target="_blank"><span class="pl-icon">💼</span> LinkedIn</a>
      {%- endif -%}
      <a href="https://pailab.io" class="profile-link" target="_blank"><span class="pl-icon">🔬</span> PAI Lab</a>
      <a href="https://aaron.kr" class="profile-link" target="_blank"><span class="pl-icon">🌐</span> aaron.kr</a>
    </div>
  </header>

  <!-- ── Announcements ────────────────────────────────────────────────────── -->
  {%- if site.data.announcements and site.data.announcements.size > 0 -%}
  <div class="announcements-section animate d4">
    {%- for item in site.data.announcements -%}
    <div class="announce-item {{ item.type | default: 'info' }}">
      <div class="announce-meta">
        <span class="announce-date">{{ item.date | date: "%b %-d" }}</span>
        <span class="announce-type">{{ item.type | default: 'info' }}</span>
      </div>
      <div class="announce-body">
        <div class="announce-title">
          <span class="lang-en">{{ item.title }}</span>
          <span class="lang-ko">{{ item.title_ko | default: item.title }}</span>
        </div>
        <div class="announce-text">
          <span class="lang-en">{{ item.body }}</span>
          <span class="lang-ko">{{ item.body_ko | default: item.body }}</span>
        </div>
      </div>
    </div>
    {%- endfor -%}
  </div>
  {%- endif -%}

  <!-- ── Spring 2026 — Current Courses by University ───────────────────── -->
  <div class="semester-section animate d4">
    <div class="section-top">
      <div class="section-heading-row">
        <span class="section-label">
          <span class="lang-en">Spring 2026 — Current Courses</span>
          <span class="lang-ko">2026년 1학기 — 현재 강좌</span>
        </span>
        <span class="section-line"></span>
      </div>
      <div class="section-actions">
        <button class="thumb-toggle" id="thumb-toggle">
          <span class="t-icon">⊞</span>
          <span class="lang-en">Thumbnails</span><span class="lang-ko">썸네일</span>
        </button>
      </div>
    </div>

    <div id="thumb-section">
      {%- assign current_courses = site.courses | where: "now", "Yes" -%}

      {%- comment -%} University groups in teaching-day order {%- endcomment -%}
      {%- assign uni_names = "한국교통대학교,원광대학교,전북대학교,한밭대학교,전주교육대학교" | split: "," -%}
      {%- assign uni_abbrs = "UT,WKU,JBNU,HB,JNUE" | split: "," -%}
      {%- assign uni_days_en = "Monday,Tuesday,Wednesday &amp; Thursday,Wednesday,Friday" | split: "," -%}
      {%- assign uni_days_ko = "월요일,화요일,수요일 · 목요일,수요일,금요일" | split: "," -%}
      {%- assign uni_full_en = "Korea Transportation University,Wonkwang University,Jeonbuk National University,Hanbat National University,Jeonju National University of Education" | split: "," -%}

      {%- for i in (0..4) -%}
        {%- assign uni = uni_names[i] -%}
        {%- assign uni_courses = current_courses | where_exp: "c", "c.description contains uni" | sort: "importance" -%}
        {%- if uni_courses.size > 0 -%}
        <div class="uni-group">
          <div class="uni-group-header">
            <span class="uni-abbr">{{ uni_abbrs[i] }}</span>
            <span class="uni-group-name">
              <span class="lang-en">{{ uni_full_en[i] }}</span>
              <span class="lang-ko">{{ uni }}</span>
            </span>
            <span class="uni-group-day">
              <span class="lang-en">{{ uni_days_en[i] }}</span>
              <span class="lang-ko">{{ uni_days_ko[i] }}</span>
            </span>
          </div>
          <div class="course-grid">
            {%- for course in uni_courses -%}
              {% include course_card.html course=course %}
            {%- endfor -%}
          </div>
        </div>
        {%- endif -%}
      {%- endfor -%}
    </div>
  </div>

  <!-- ── Research CTA ────────────────────────────────────────────────────── -->
  <div class="research-cta animate d5">
    <div class="rc-eyebrow">
      <span class="lang-en">Research / PAI Lab</span>
      <span class="lang-ko">연구 / PAI 연구소</span>
    </div>
    <h3 class="rc-title">
      <span class="lang-en">Looking for <em>Research Assistants</em></span>
      <span class="lang-ko"><em>연구 보조원</em>을 찾습니다</span>
    </h3>
    <p class="rc-desc">
      <span class="lang-en">Interested in computer vision, NLP, or applied machine learning?
      The PAI Lab at Hanbat National University is accepting undergraduate and graduate research assistants for 2026.</span>
      <span class="lang-ko">컴퓨터 비전, 자연어 처리 또는 응용 머신러닝에 관심 있으신가요?
      한밭대학교 PAI 연구소에서 2026년도 학부 및 대학원 연구 보조원을 모집합니다.</span>
    </p>
    <div class="rc-tags">
      <span class="rc-tag">Computer Vision</span>
      <span class="rc-tag">NLP</span>
      <span class="rc-tag">Signal Processing</span>
      <span class="rc-tag">Image Processing</span>
      <span class="rc-tag">Machine Learning</span>
    </div>
    <a href="https://pailab.io" class="cta-btn" target="_blank">
      <span class="lang-en">Visit PAI Lab →</span>
      <span class="lang-ko">PAI 연구소 →</span>
    </a>
  </div>

  <!-- ── Recent Lab Notes ─────────────────────────────────────────────── -->
  <div class="lab-notes-section animate d5">
    <div class="section-top" style="margin-bottom:14px;">
      <div class="section-heading-row">
        <span class="section-label">
          <span class="lang-en">Recent Lab Notes</span>
          <span class="lang-ko">최근 연구 노트</span>
        </span>
        <span class="section-line"></span>
      </div>
      <div class="section-actions">
        <a href="https://pailab.io" class="back-btn" target="_blank">
          <span class="lang-en">All Notes →</span>
          <span class="lang-ko">전체 보기 →</span>
        </a>
      </div>
    </div>
    <div class="lab-note-list">
      <a class="lab-note-row" href="https://pailab.io" target="_blank">
        <span class="lnr-date">Apr 2026</span>
        <span class="lnr-tag">Vision</span>
        <span class="lnr-title">Exploring YOLO v11 for Real-Time Object Detection on Edge Devices</span>
        <span class="lnr-arrow">→</span>
      </a>
      <a class="lab-note-row" href="https://pailab.io" target="_blank">
        <span class="lnr-date">Mar 2026</span>
        <span class="lnr-tag">NLP</span>
        <span class="lnr-title">Fine-Tuning LLMs for Korean Technical Documentation</span>
        <span class="lnr-arrow">→</span>
      </a>
      <a class="lab-note-row" href="https://pailab.io" target="_blank">
        <span class="lnr-date">Feb 2026</span>
        <span class="lnr-tag">Signal</span>
        <span class="lnr-title">Sensor Fusion Approaches for Wearable Health Monitoring</span>
        <span class="lnr-arrow">→</span>
      </a>
      <a class="lab-note-row" href="https://pailab.io" target="_blank">
        <span class="lnr-date">Jan 2026</span>
        <span class="lnr-tag">Review</span>
        <span class="lnr-title">2025 in Review: Publications, Talks, and Teaching</span>
        <span class="lnr-arrow">→</span>
      </a>
    </div>
  </div>

  <!-- ── Archive link ──────────────────────────────────────────────────── -->
  <div style="padding-bottom:80px;text-align:center;">
    <a href="{{ '/archive' | relative_url }}" class="back-btn" style="display:inline-flex;">
      <span class="lang-en">View All Courses (Archive) →</span>
      <span class="lang-ko">전체 강좌 보기 (아카이브) →</span>
    </a>
  </div>

</div><!-- /.wrap -->

<script>
// ── Today pill ────────────────────────────────────────────────────────────────
(function() {
  const schedule = {
    1: { name: 'UT — Korea Transportation University', ko: '한국교통대학교 (월요일)' },
    2: { name: 'WKU — Wonkwang University',           ko: '원광대학교 (화요일)' },
    3: { name: 'JBNU — Jeonbuk University',           ko: '전북대학교 (수요일)' },
    4: { name: 'HB — Hanbat University',              ko: '한밭대학교 (목요일)' },
    5: { name: 'JNUE — Jeonju Natl. Univ. of Ed.',   ko: '전주교육대학교 (금요일)' },
  };
  const day = new Date().getDay();
  const pill = document.getElementById('today-pill');
  const txt  = document.getElementById('today-text');
  const isKo = document.documentElement.classList.contains('ko');
  if (day === 0 || day === 6) {
    pill.classList.add('noclass');
    txt.textContent = isKo ? '주말 — 휴강' : 'Weekend — No Class';
  } else if (schedule[day]) {
    txt.textContent = (isKo ? '오늘: ' : 'Today: ') + (isKo ? schedule[day].ko : schedule[day].name);
  } else {
    pill.classList.add('noclass');
    txt.textContent = isKo ? '오늘은 강의 없음' : 'No Class Today';
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
