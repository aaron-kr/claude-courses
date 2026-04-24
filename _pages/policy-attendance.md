---
layout: default
title: Attendance & Participation Policy
permalink: /policies/attendance/
---

<style>
.pol-page{padding:40px 0 72px}
.pol-page-layout{display:grid;grid-template-columns:170px 1fr;gap:44px;align-items:start;padding-top:32px}
.pol-sidebar{position:sticky;top:72px}
.pol-sidebar-nav{list-style:none;border-left:2px solid var(--border);padding-left:16px}
.pol-sidebar-nav li{margin-bottom:2px}
.pol-sidebar-nav a{font-size:.76rem;color:var(--muted);text-decoration:none;display:block;padding:4px 0;transition:color .2s}
.pol-sidebar-nav a:hover,.pol-sidebar-nav a.active{color:var(--accent3)}
.pol-sidebar-nav a.active{border-left:2px solid var(--accent3);margin-left:-18px;padding-left:16px}
.pol-meta-bar{display:flex;gap:0;border:1px solid var(--border);border-radius:var(--radius);overflow:hidden;background:var(--surface);margin-bottom:32px}
.pol-meta-item{flex:1;padding:9px 14px;border-right:1px solid var(--border);display:flex;flex-direction:column;gap:2px}
.pol-meta-item:last-child{border-right:none}
.pol-meta-label{font-family:'IBM Plex Mono',monospace;font-size:.56rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em}
.pol-meta-value{font-size:.8rem;color:var(--sub)}
.pol-content-section{margin-bottom:42px}
.pol-content-section h2{font-family:'Playfair Display','DM Serif Display',serif;font-size:1.3rem;font-weight:700;color:var(--text);margin-bottom:12px}
.pol-content-section p{font-size:.9rem;color:var(--sub);line-height:1.85;margin-bottom:10px}
.pol-rule-list{list-style:none;margin:10px 0}
.pol-rule-list li{display:flex;gap:12px;padding:8px 0;border-bottom:1px solid var(--border);font-size:.88rem;color:var(--sub);line-height:1.7}
.pol-rule-list li:first-child{border-top:1px solid var(--border)}
.pol-rule-num{font-family:'IBM Plex Mono',monospace;font-size:.63rem;color:var(--accent3);flex-shrink:0;width:22px;padding-top:3px}
.pol-highlight{background:rgba(109,204,221,.06);border:1px solid rgba(109,204,221,.2);border-radius:var(--radius);padding:13px 16px;margin:14px 0;font-size:.88rem;color:var(--sub);line-height:1.75}
.pol-highlight strong{color:var(--text)}
.related-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:16px}
a.related-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:18px;text-decoration:none;color:inherit;transition:border-color .2s,transform .15s,box-shadow .15s;display:flex;flex-direction:column;gap:6px;position:relative;overflow:hidden}
a.related-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--accent3),var(--accent));opacity:.5;transition:opacity .2s}
a.related-card:hover::before{opacity:1}
a.related-card:hover{border-color:rgba(109,204,221,.3);transform:translateY(-1px)}
.related-code{font-family:'IBM Plex Mono',monospace;font-size:.62rem;color:var(--accent3);letter-spacing:.06em}
.related-title{font-size:.88rem;font-weight:500;color:var(--text);line-height:1.3;margin-top:4px}
.related-desc{font-size:.75rem;color:var(--muted);margin-top:3px;line-height:1.4}
@media(max-width:900px){.pol-page-layout{grid-template-columns:1fr}.pol-sidebar{display:none}.related-grid{grid-template-columns:1fr 1fr}.pol-meta-bar{flex-wrap:wrap}}
</style>

<div class="wrap">
<header>
  <p class="eyebrow animate d1">
    <span class="lang-en">Academic Policy &mdash; POL 02</span>
    <span class="lang-ko">학사 규정 &mdash; POL 02</span>
  </p>
  <h1 class="animate d2">
    <span class="lang-en">Attendance &amp;<br><em>Participation</em></span>
    <span class="lang-ko">출석 &amp;<br><em>참여 정책</em></span>
  </h1>
</header>
<div class="pol-page">
  <a href="{{ '/policies' | relative_url }}" class="back-btn animate d1" style="margin-bottom:18px;display:inline-flex">
    ← <span class="lang-en">All Policies</span><span class="lang-ko">전체 정책</span>
  </a>
  <div class="pol-meta-bar animate d2">
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Policy Code</span><span class="lang-ko">정책 코드</span></span>
      <span class="pol-meta-value">POL &mdash; 02</span>
    </div>
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Effective</span><span class="lang-ko">시행일</span></span>
      <span class="pol-meta-value"><span class="lang-en">September 2023</span><span class="lang-ko">2023년 9월</span></span>
    </div>
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Last Updated</span><span class="lang-ko">최종 수정</span></span>
      <span class="pol-meta-value"><span class="lang-en">April 2026</span><span class="lang-ko">2026년 4월</span></span>
    </div>
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Applies To</span><span class="lang-ko">적용 범위</span></span>
      <span class="pol-meta-value"><span class="lang-en">All courses</span><span class="lang-ko">모든 강좌</span></span>
    </div>
  </div>
  <div class="pol-page-layout">
    <aside class="pol-sidebar">
      <ul class="pol-sidebar-nav">
        <li><a href="#overview" class="active"><span class="lang-en">Overview</span><span class="lang-ko">개요</span></a></li>
        <li><a href="#attendance"><span class="lang-en">Attendance</span><span class="lang-ko">출석</span></a></li>
        <li><a href="#participation"><span class="lang-en">Participation</span><span class="lang-ko">참여</span></a></li>
        <li><a href="#excused"><span class="lang-en">Excused Absences</span><span class="lang-ko">공결</span></a></li>
        <li><a href="#penalties"><span class="lang-en">Penalties</span><span class="lang-ko">감점</span></a></li>
      </ul>
    </aside>
    <main>
      <div class="pol-content-section" id="overview">
        <h2><span class="lang-en">Overview</span><span class="lang-ko">개요</span></h2>
        <p>
          <span class="lang-en">Regular attendance and active participation are fundamental to success in this course. This policy explains expectations, allowed absences, and how attendance affects your grade.</span>
          <span class="lang-ko">정기적인 출석과 적극적인 참여는 이 강좌의 성공에 필수적입니다. 이 정책은 기대 사항, 허용 결석 횟수, 출석이 성적에 미치는 영향을 설명합니다.</span>
        </p>
        <div class="pol-highlight">
          <strong><span class="lang-en">Bottom line:</span><span class="lang-ko">핵심:</span></strong>
          <span class="lang-en"> Show up, engage, and let me know in advance if you cannot attend. Missing more than 35% of class for any reason results in automatic course failure.</span>
          <span class="lang-ko"> 출석하고 참여하며, 불참이 불가피한 경우 미리 알려주세요. 어떤 이유로든 35% 이상 결석하면 자동으로 과락 처리됩니다.</span>
        </div>
      </div>

      <div class="pol-content-section" id="attendance">
        <h2><span class="lang-en">Attendance</span><span class="lang-ko">출석</span></h2>
        <p>
          <span class="lang-en">You are expected to attend <em>all</em> classes. If you miss a class, you are responsible for obtaining notes from a classmate and completing any missed work.</span>
          <span class="lang-ko">모든 수업에 참석해야 합니다. 수업을 빠진 경우, 동료로부터 수업 내용을 받거나 빠진 과제를 완료하는 것은 귀하의 책임입니다.</span>
        </p>
        <ul class="pol-rule-list">
          <li>
            <span class="pol-rule-num">01</span>
            <span><span class="lang-en"><strong>Missing &gt;15%</strong> of classes (≈3 classes in a standard semester) will begin to lower your attendance grade.</span><span class="lang-ko"><strong>15% 이상</strong> 결석 시 출석 점수가 낮아지기 시작합니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">02</span>
            <span><span class="lang-en"><strong>Missing &gt;25%</strong> of classes results in a failing attendance grade for that component.</span><span class="lang-ko"><strong>25% 이상</strong> 결석 시 출석 항목에서 과락이 됩니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">03</span>
            <span><span class="lang-en"><strong>Missing &gt;35%</strong> total (excused + unexcused combined) results in automatic course failure regardless of other grades.</span><span class="lang-ko"><strong>35% 이상</strong> 총 결석(공결 포함) 시 다른 성적에 관계없이 자동 과락 처리됩니다.</span></span>
          </li>
        </ul>
      </div>

      <div class="pol-content-section" id="participation">
        <h2><span class="lang-en">Participation</span><span class="lang-ko">참여</span></h2>
        <p>
          <span class="lang-en">Active participation is expected. Students who are regularly late, leave early, or are disengaged will receive lower grades. I do not give a daily participation grade, but I observe your habits throughout the semester.</span>
          <span class="lang-ko">적극적인 참여가 기대됩니다. 정기적으로 지각하거나 일찍 퇴장하거나 수업에 집중하지 않는 학생은 낮은 성적을 받게 됩니다. 일일 참여 점수는 없지만 학기 내내 습관을 관찰합니다.</span>
        </p>
        <p>
          <span class="lang-en">Participation includes: asking questions, answering questions, engaging with in-class exercises, and contributing positively to the learning environment.</span>
          <span class="lang-ko">참여에는 질문하기, 질문에 답하기, 수업 중 실습 참여, 학습 환경에 긍정적으로 기여하는 것이 포함됩니다.</span>
        </p>
      </div>

      <div class="pol-content-section" id="excused">
        <h2><span class="lang-en">Excused Absences</span><span class="lang-ko">공결</span></h2>
        <p>
          <span class="lang-en">For valid absences (illness, family emergency, official university business), notify me in advance if possible. Bring documentation when you return.</span>
          <span class="lang-ko">정당한 결석 사유(질병, 가족 사정, 공식 대학 업무 등)가 있는 경우 가능하면 사전에 알려주세요. 복귀 시 관련 서류를 제출하세요.</span>
        </p>
        <p>
          <span class="lang-en">Excused absences do not count against your <em>allowed absences</em> threshold but do affect your participation score, since you cannot participate while absent.</span>
          <span class="lang-ko">공결은 허용 결석 횟수 기준에 포함되지 않지만, 결석 중에는 참여할 수 없으므로 참여 점수에는 영향을 줍니다.</span>
        </p>
      </div>

      <div class="pol-content-section" id="penalties">
        <h2><span class="lang-en">Penalties</span><span class="lang-ko">감점</span></h2>
        <ul class="pol-rule-list">
          <li>
            <span class="pol-rule-num">01</span>
            <span><span class="lang-en">Arriving <strong>more than 15 minutes late</strong> counts as half an absence.</span><span class="lang-ko"><strong>15분 이상</strong> 지각은 반 결석으로 처리됩니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">02</span>
            <span><span class="lang-en">Leaving class early without permission counts as half an absence.</span><span class="lang-ko">허가 없이 수업 중 조퇴하면 반 결석으로 처리됩니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">03</span>
            <span><span class="lang-en">Using a phone during class (not for coursework) may result in a participation deduction.</span><span class="lang-ko">수업 중 (수업 목적 외) 휴대폰 사용은 참여 점수 감점으로 이어질 수 있습니다.</span></span>
          </li>
        </ul>
      </div>

      <div class="pol-content-section" id="related">
        <h2><span class="lang-en">Related Policies</span><span class="lang-ko">관련 정책</span></h2>
        <div class="related-grid">
          <a href="{{ '/policies/assignments' | relative_url }}" class="related-card">
            <span class="related-code">POL — 03</span>
            <span class="related-title"><span class="lang-en">Assignments &amp; Practice</span><span class="lang-ko">과제 및 실습</span></span>
            <span class="related-desc"><span class="lang-en">Submission rules and grading.</span><span class="lang-ko">제출 규정 및 채점.</span></span>
          </a>
          <a href="{{ '/policies/late' | relative_url }}" class="related-card">
            <span class="related-code">POL — 06</span>
            <span class="related-title"><span class="lang-en">Late Policy</span><span class="lang-ko">지각 제출 정책</span></span>
            <span class="related-desc"><span class="lang-en">Late days and penalty schedule.</span><span class="lang-ko">지각 유예 일수 및 감점 일정.</span></span>
          </a>
          <a href="{{ '/policies/ai' | relative_url }}" class="related-card">
            <span class="related-code">POL — 01</span>
            <span class="related-title"><span class="lang-en">AI &amp; ChatGPT Use</span><span class="lang-ko">AI 사용 정책</span></span>
            <span class="related-desc"><span class="lang-en">Permitted and prohibited AI use.</span><span class="lang-ko">허용 및 금지 AI 사용.</span></span>
          </a>
        </div>
      </div>
    </main>
  </div>
</div>
</div>

<script>
(function(){
  const sections = document.querySelectorAll('.pol-content-section[id]');
  const links    = document.querySelectorAll('.pol-sidebar-nav a');
  if (!sections.length || !links.length) return;
  const obs = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        links.forEach(l => l.classList.remove('active'));
        const a = document.querySelector(`.pol-sidebar-nav a[href="#${e.target.id}"]`);
        if (a) a.classList.add('active');
      }
    });
  }, { rootMargin: '-25% 0px -65% 0px' });
  sections.forEach(s => obs.observe(s));
})();
</script>
