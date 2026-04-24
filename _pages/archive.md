---
layout: default
title: Course Archive
permalink: /archive/
eyebrow: Teaching History
---

<div class="wrap">
  <header class="page-header">
    <div class="eyebrow">
      <span class="lang-en">Teaching History</span>
      <span class="lang-ko">강의 이력</span>
    </div>
    <h1>Course <em>Archive</em></h1>
    <p class="hero-desc" style="margin-top:16px;">
      <span class="lang-en">All courses taught from 2021 to present, organized by semester.</span>
      <span class="lang-ko">2021년부터 현재까지 강의한 모든 강좌를 학기별로 정리했습니다.</span>
    </p>

    <!-- Filter + Thumbnail controls -->
    <div class="section-top" style="margin-top:28px;">
      <div class="section-heading-row">
        <span class="section-label">
          <span class="lang-en">By Semester</span>
          <span class="lang-ko">학기별</span>
        </span>
        <span class="section-line"></span>
      </div>
      <div class="section-actions">
        <button class="filter-toggle-btn" id="filter-toggle">
          ⚙ <span class="lang-en">Filters</span><span class="lang-ko">필터</span>
        </button>
        <button class="thumb-toggle" id="arch-thumb-toggle">
          <span class="t-icon">⊞</span>
          <span class="lang-en">Thumbnails</span><span class="lang-ko">썸네일</span>
        </button>
        <span id="arch-count" style="font-family:'IBM Plex Mono',monospace;font-size:.65rem;color:var(--muted);margin-left:6px;"></span>
      </div>
    </div>
    <div class="filter-panel" id="filter-panel">
      <div class="ctrl-row">
        <span class="ctrl-row-label"><span class="lang-en">Semester</span><span class="lang-ko">학기</span></span>
        <button class="pill pill-blue active" data-filter="sem" data-value="all">
          <span class="lang-en">All</span><span class="lang-ko">전체</span>
        </button>
        {%- for cat in site.course_categories -%}
        {%- assign cat_courses = site.courses | where: "category", cat.key -%}
        {%- if cat_courses.size > 0 -%}
        <button class="pill pill-blue" data-filter="sem" data-value="{{ cat.key }}">{{ cat.label }}</button>
        {%- endif -%}
        {%- endfor -%}
      </div>
      <div class="ctrl-row">
        <span class="ctrl-row-label"><span class="lang-en">University</span><span class="lang-ko">대학교</span></span>
        <button class="pill active" data-filter="uni" data-value="all">
          <span class="lang-en">All</span><span class="lang-ko">전체</span>
        </button>
        <button class="pill" data-filter="uni" data-value="UT"><span class="lang-en">UT</span><span class="lang-ko">교통대</span></button>
        <button class="pill" data-filter="uni" data-value="WKU"><span class="lang-en">WKU</span><span class="lang-ko">원광대</span></button>
        <button class="pill" data-filter="uni" data-value="JBNU"><span class="lang-en">JBNU</span><span class="lang-ko">전북대</span></button>
        <button class="pill" data-filter="uni" data-value="HB"><span class="lang-en">HB</span><span class="lang-ko">한밭대</span></button>
        <button class="pill" data-filter="uni" data-value="JNUE"><span class="lang-en">JNUE</span><span class="lang-ko">전주교대</span></button>
        <button class="pill" data-filter="uni" data-value="DJU"><span class="lang-en">DJU</span><span class="lang-ko">대전대</span></button>
        <button class="pill" data-filter="uni" data-value="IKSAN"><span class="lang-en">Iksan HS</span><span class="lang-ko">익산 고교</span></button>
      </div>
    </div>
  </header>

  <main id="archive-main" style="padding:32px 0 80px;">
    {%- for cat in site.course_categories -%}
      {%- assign cat_courses = site.courses | where: "category", cat.key | sort: "importance" -%}
      {%- if cat_courses.size > 0 -%}
      {%- assign is_current = cat_courses | where_exp: "c", "c.now" | size -%}
      <div class="semester-group{% if is_current > 0 %} is-current{% endif %}" data-sem="{{ cat.key }}">
        <div class="group-heading">
          <span class="group-label">{{ cat.label }}</span>
          {%- if is_current > 0 -%}<span class="current-chip">Current</span>{%- endif -%}
          <span class="group-line"></span>
        </div>
        <ul class="archive-list">
          {%- for course in cat_courses -%}
            {%- assign _uni = course.logo | remove: '-logo.png' | remove: '-logo-2.png' | upcase -%}
            {%- assign _info = course.information | first -%}
            {%- assign _tl = course.title | downcase -%}
            {%- if _tl contains 'machine learning' or _tl contains 'deep learning' or _tl contains 'ai ' -%}
              {%- assign _tc = 'ai-tag' -%}{%- assign _tl2 = 'AI/ML' -%}
            {%- elsif _tl contains 'database' or _tl contains 'sql' or _tl contains 'data struct' -%}
              {%- assign _tc = 'data' -%}{%- assign _tl2 = 'Data' -%}
            {%- elsif _tl contains 'web' or _tl contains 'php' or _tl contains 'node' or _tl contains 'html' -%}
              {%- assign _tc = 'web' -%}{%- assign _tl2 = 'Web' -%}
            {%- elsif _tl contains 'python' or _tl contains 'java' or _tl contains 'c++' or _tl contains 'programming' -%}
              {%- assign _tc = 'theory' -%}{%- assign _tl2 = 'Programming' -%}
            {%- elsif _tl contains 'iot' or _tl contains 'circuit' or _tl contains 'device' or _tl contains 'semiconductor' or _tl contains 'medical' -%}
              {%- assign _tc = 'systems' -%}{%- assign _tl2 = 'Systems' -%}
            {%- elsif _tl contains 'electric' or _tl contains 'power' or _tl contains 'hydrogen' -%}
              {%- assign _tc = 'ee' -%}{%- assign _tl2 = 'EE' -%}
            {%- else -%}
              {%- assign _tc = 'theory' -%}{%- assign _tl2 = 'CS' -%}
            {%- endif -%}
            <li>
              <a class="archive-item"
                 href="{{ course.url | relative_url }}"
                 data-uni="{{ _uni }}"
                 data-sem="{{ course.category }}">
                {%- if course.img -%}
                <div class="item-thumb" style="background-image:url('{{ course.img | relative_url }}')"></div>
                {%- else -%}
                <div class="item-thumb"></div>
                {%- endif -%}
                <div class="item-content">
                  <div class="item-code">
                    <span class="uni-init-tag">{{ _uni }}</span>
                    {{ course.description | split: ' • ' | first }}
                    {%- unless course.now %}<span class="archived-badge">Archived</span>{%- endunless -%}
                  </div>
                  <div class="item-main">
                    <div class="item-title">{{ course.title }}</div>
                    {%- if course.subtitle %}<div class="item-subtitle">{{ course.subtitle }}</div>{%- endif -%}
                    <div class="item-meta-row">
                      <span class="item-tag {{ _tc }}">{{ _tl2 }}</span>
                      {%- if _info.time -%}<span class="item-meta-val">{{ _info.time }}</span>{%- endif -%}
                      {%- if _info.location -%}<span class="item-meta-val">{{ _info.location }}</span>{%- endif -%}
                    </div>
                  </div>
                </div>
                <div class="uni-badge"><span class="ub-abbr">{{ _uni }}</span></div>
                <span class="item-arrow">→</span>
              </a>
            </li>
          {%- endfor -%}
        </ul>
      </div>
      {%- endif -%}
    {%- endfor -%}
  </main>
</div>

<script>
// ── Archive filter + thumbnail logic ─────────────────────────────────────────
(function() {
  let activeSem = 'all';
  let activeUni = 'all';

  const allRows = document.querySelectorAll('.archive-item');

  function countVisible() {
    let n = 0;
    allRows.forEach(r => { if (!r.closest('li').classList.contains('arch-hidden')) n++; });
    const el = document.getElementById('arch-count');
    if (el) el.textContent = n + ' course' + (n !== 1 ? 's' : '');
  }

  function applyFilters() {
    allRows.forEach(row => {
      const li = row.closest('li');
      const sem = row.dataset.sem;
      const uni = row.dataset.uni;
      const semOk = activeSem === 'all' || sem === activeSem;
      const uniOk = activeUni === 'all' || uni === activeUni;
      li.classList.toggle('arch-hidden', !(semOk && uniOk));
    });
    // Hide semester group headings with no visible rows
    document.querySelectorAll('.semester-group').forEach(sec => {
      const anyVis = [...sec.querySelectorAll('li')].some(li => !li.classList.contains('arch-hidden'));
      sec.style.display = anyVis ? '' : 'none';
    });
    countVisible();
  }

  // Filter buttons
  document.querySelectorAll('[data-filter]').forEach(btn => {
    btn.addEventListener('click', () => {
      const group = btn.dataset.filter;
      const val   = btn.dataset.value;
      document.querySelectorAll(`[data-filter="${group}"]`).forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      if (group === 'sem') activeSem = val;
      if (group === 'uni') activeUni = val;
      applyFilters();
    });
  });

  // Filter panel toggle
  const filterToggle = document.getElementById('filter-toggle');
  const filterPanel  = document.getElementById('filter-panel');
  if (filterToggle && filterPanel) {
    filterToggle.addEventListener('click', () => {
      const o = filterPanel.classList.toggle('open');
      filterToggle.classList.toggle('open', o);
    });
  }

  // Thumbnail toggle
  const archThumbToggle = document.getElementById('arch-thumb-toggle');
  if (archThumbToggle) {
    const main = document.getElementById('archive-main');
    archThumbToggle.addEventListener('click', () => {
      const a = main.classList.toggle('thumbs-active');
      archThumbToggle.classList.toggle('active', a);
      const ic = archThumbToggle.querySelector('.t-icon');
      if (ic) ic.textContent = a ? '⊟' : '⊞';
    });
  }

  countVisible();
})();
</script>
