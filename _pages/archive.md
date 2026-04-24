---
layout: default
title: Course Archive
permalink: /archive/
eyebrow: Teaching History
---

<div class="wrap">
  <header style="padding:60px 0 36px;border-bottom:1px solid var(--border);">
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
    <div class="section-top">
    <div class="section-heading-row"><span class="section-label" id="group-mode-label">By Semester</span><span class="section-line"></span></div>
    <div class="section-actions">
      <button class="filter-toggle-btn" id="filter-toggle-btn">⚙ Filters</button>
      <button class="thumb-toggle" id="thumb-toggle"><span class="t-icon">⊞</span> Thumbnails</button>
    </div>
  </div>
  <div class="filter-panel" id="filter-panel">
    <div class="ctrl-row">
      <span class="ctrl-row-label">Topic</span>
      <button class="pill active" data-filter="all">All</button>
      <button class="pill pill-blue" data-filter="ml">ML</button>
      <button class="pill pill-blue" data-filter="theory">Theory</button>
      <button class="pill pill-blue" data-filter="systems">Systems</button>
      <button class="pill pill-blue" data-filter="seminar">Seminar</button>
    </div>
    <div class="ctrl-row">
      <span class="ctrl-row-label">Year</span>
      <button class="pill active" data-year="all">All</button>
      <button class="pill pill-teal" data-year="2025">2025</button>
      <button class="pill pill-teal" data-year="2024">2024</button>
      <button class="pill pill-teal" data-year="2023">2023</button>
    </div>
    <div class="ctrl-row">
      <span class="ctrl-row-label">Sort</span>
      <button class="pill active" data-sort="newest">Newest</button>
      <button class="pill" data-sort="oldest">Oldest</button>
      <button class="pill" data-sort="az">A → Z</button>
      <button class="pill" data-sort="uni">By University</button>
    </div>
  </div>
    <div style="display:flex;gap:8px;margin-top:20px;flex-wrap:wrap;align-items:center;">
      <button class="filter-toggle-btn" id="filter-toggle">
        <span>⚙</span>
        <span class="lang-en">Filters</span><span class="lang-ko">필터</span>
      </button>
      <button class="thumb-toggle" id="arch-thumb-toggle">
        <span class="t-icon">⊞</span>
        <span class="lang-en">Thumbnails</span><span class="lang-ko">썸네일</span>
      </button>
      <span id="arch-count" style="font-family:'IBM Plex Mono',monospace;font-size:.65rem;color:var(--muted);margin-left:6px;"></span>
    </div>
<div class="semester-group is-current" data-year="2025" data-order="1">
      <div class="group-heading"><span class="group-label">Spring 2025</span><span class="current-chip">● Current</span><span class="group-line"></span></div>
      <ul class="archive-list">
<a class="archive-item" href="course.html" data-level="ml" data-title="Advanced Machine Learning" data-school="yonsei">
  <div class="item-thumb" style="background:linear-gradient(180deg,#3d28a0,#9b65ff)"></div>
  <div class="item-content">
    <span class="item-code">CS 4820</span>
    <div class="item-main">
      <div class="item-title">Advanced Machine Learning</div>
      <div class="item-subtitle">고급 머신러닝 / Advanced ML</div>
      <div class="item-meta-row">
        <span class="item-meta-val">Tue/Thu 2:00–3:30</span>
        <span class="item-meta-val">Eng 302</span>
        <span class="item-tag ml">ML</span>
        <span class="archived-badge current-bdg">CURRENT</span>
      </div>
    </div>
  </div>
  <span class="item-arrow">→</span>
  <div class="uni-badge"><span class="ub-abbr">YU</span><span>연세</span></div>
</a><a class="archive-item" href="#" data-level="theory" data-title="Algorithms &amp; Complexity" data-school="yonsei">
  <div class="item-thumb" style="background:linear-gradient(180deg,#0c4a78,#7eb8f7)"></div>
  <div class="item-content">
    <span class="item-code">CS 3310</span>
    <div class="item-main">
      <div class="item-title">Algorithms &amp; Complexity</div>
      <div class="item-subtitle">알고리즘 / Algorithms</div>
      <div class="item-meta-row">
        <span class="item-meta-val">Mon/Wed 10:30–12:00</span>
        <span class="item-meta-val">Science B-12</span>
        <span class="item-tag theory">Theory</span>
        <span class="archived-badge current-bdg">CURRENT</span>
      </div>
    </div>
  </div>
  <span class="item-arrow">→</span>
  <div class="uni-badge"><span class="ub-abbr">YU</span><span>연세</span></div>
</a><a class="archive-item" href="#" data-level="seminar" data-title="Seminar: Foundation Models" data-school="yonsei">
  <div class="item-thumb" style="background:linear-gradient(180deg,#1e3a8a,#4338ca)"></div>
  <div class="item-content">
    <span class="item-code">CS 6001</span>
    <div class="item-main">
      <div class="item-title">Seminar: Foundation Models</div>
      <div class="item-subtitle">기반 모델 세미나</div>
      <div class="item-meta-row">
        <span class="item-meta-val">Fri 2:00–4:00</span>
        <span class="item-meta-val">Grad Rm 8</span>
        <span class="item-tag seminar">Seminar</span>
        <span class="archived-badge current-bdg">CURRENT</span>
      </div>
    </div>
  </div>
  <span class="item-arrow">→</span>
  <div class="uni-badge"><span class="ub-abbr">YU</span><span>연세</span></div>
</a><a class="archive-item" href="#" data-level="systems" data-title="Distributed Systems" data-school="kaist">
  <div class="item-thumb" style="background:linear-gradient(180deg,#5b21b6,#c026d3)"></div>
  <div class="item-content">
    <span class="item-code">CS 5510</span>
    <div class="item-main">
      <div class="item-title">Distributed Systems</div>
      <div class="item-subtitle">분산 시스템</div>
      <div class="item-meta-row">
        <span class="item-meta-val">Tue/Thu 9:00–10:30</span>
        <span class="item-meta-val">N1 201</span>
        <span class="item-tag systems">Systems</span>
        <span class="archived-badge current-bdg">CURRENT</span>
      </div>
    </div>
  </div>
  <span class="item-arrow">→</span>
  <div class="uni-badge"><span class="ub-abbr">KA</span><span>카이스트</span></div>
</a><a class="archive-item" href="#" data-level="ml" data-title="ML for Systems" data-school="kaist">
  <div class="item-thumb" style="background:linear-gradient(180deg,#0e6490,#1d4ed8)"></div>
  <div class="item-content">
    <span class="item-code">CS 4910</span>
    <div class="item-main">
      <div class="item-title">ML for Systems</div>
      <div class="item-subtitle">시스템 ML</div>
      <div class="item-meta-row">
        <span class="item-meta-val">Mon/Wed 1:00–2:30</span>
        <span class="item-meta-val">N1 115</span>
        <span class="item-tag ml">ML</span>
        <span class="archived-badge current-bdg">CURRENT</span>
      </div>
    </div>
  </div>
  <span class="item-arrow">→</span>
  <div class="uni-badge"><span class="ub-abbr">KA</span><span>카이스트</span></div>
</a><a class="archive-item" href="#" data-level="ml" data-title="Intro to AI" data-school="skku">
  <div class="item-thumb" style="background:linear-gradient(180deg,#b45309,#16a34a)"></div>
  <div class="item-content">
    <span class="item-code">CS 3110</span>
    <div class="item-main">
      <div class="item-title">Intro to AI</div>
      <div class="item-subtitle">인공지능 개론</div>
      <div class="item-meta-row">
        <span class="item-meta-val">Mon/Thu 3:00–4:30</span>
        <span class="item-meta-val">Eng 201</span>
        <span class="item-tag ml">AI</span>
        <span class="archived-badge current-bdg">CURRENT</span>
      </div>
    </div>
  </div>
  <span class="item-arrow">→</span>
  <div class="uni-badge"><span class="ub-abbr">SK</span><span>성균관</span></div>
</a><a class="archive-item" href="#" data-level="theory" data-title="Data Structures" data-school="skku">
  <div class="item-thumb" style="background:linear-gradient(180deg,#b91c1c,#ea580c)"></div>
  <div class="item-content">
    <span class="item-code">CS 2210</span>
    <div class="item-main">
      <div class="item-title">Data Structures</div>
      <div class="item-subtitle">자료 구조</div>
      <div class="item-meta-row">
        <span class="item-meta-val">Tue/Fri 10:00–11:30</span>
        <span class="item-meta-val">IT 305</span>
        <span class="item-tag theory">Theory</span>
        <span class="archived-badge current-bdg">CURRENT</span>
      </div>
    </div>
  </div>
  <span class="item-arrow">→</span>
  <div class="uni-badge"><span class="ub-abbr">SK</span><span>성균관</span></div>
</a>
      </ul>
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
        <button class="pill" data-filter="uni" data-value="UT">UT</button>
        <button class="pill" data-filter="uni" data-value="WKU">WKU</button>
        <button class="pill" data-filter="uni" data-value="JBNU">JBNU</button>
        <button class="pill" data-filter="uni" data-value="HB">HB</button>
        <button class="pill" data-filter="uni" data-value="JNUE">JNUE</button>
        <button class="pill" data-filter="uni" data-value="DJU">DJU</button>
        <button class="pill" data-filter="uni" data-value="IKSAN">Iksan HS</button>
      </div>
    </div>
  </header>

  <main id="archive-main" style="padding:32px 0 80px;">
    {%- for cat in site.course_categories -%}
      {%- assign cat_courses = site.courses | where: "category", cat.key | sort: "importance" -%}
      {%- if cat_courses.size > 0 -%}
      {%- assign is_current = cat_courses | where: "now", "Yes" | size -%}
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
                <span class="item-uni">{{ course.description | split: ' • ' | last }}</span>
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
