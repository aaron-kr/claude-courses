---
layout: default
title: Collaboration Policy
permalink: /policies/collaboration/
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
    <span class="lang-en">Academic Policy &mdash; POL 05</span>
    <span class="lang-ko">학사 규정 &mdash; POL 05</span>
  </p>
  <h1 class="animate d2">
    <span class="lang-en">Collaboration<br><em>Policy</em></span>
    <span class="lang-ko">협업<br><em>정책</em></span>
  </h1>
</header>
<div class="pol-page">
  <a href="{{ '/policies' | relative_url }}" class="back-btn animate d1" style="margin-bottom:18px;display:inline-flex">
    ← <span class="lang-en">All Policies</span><span class="lang-ko">전체 정책</span>
  </a>
  <div class="pol-meta-bar animate d2">
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Policy Code</span><span class="lang-ko">정책 코드</span></span>
      <span class="pol-meta-value">POL &mdash; 05</span>
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
        <li><a href="#individual"><span class="lang-en">Individual Work</span><span class="lang-ko">개인 작업</span></a></li>
        <li><a href="#group"><span class="lang-en">Group Work</span><span class="lang-ko">그룹 작업</span></a></li>
        <li><a href="#integrity"><span class="lang-en">Academic Integrity</span><span class="lang-ko">학문적 성실성</span></a></li>
      </ul>
    </aside>
    <main>
      <div class="pol-content-section" id="overview">
        <h2><span class="lang-en">Overview</span><span class="lang-ko">개요</span></h2>
        <p>
          <span class="lang-en">Learning together is valuable, but submitting work that is not your own is not. This policy defines what types of collaboration are acceptable for different kinds of work.</span>
          <span class="lang-ko">함께 배우는 것은 가치 있지만, 자신의 것이 아닌 작업을 제출하는 것은 그렇지 않습니다. 이 정책은 다양한 종류의 작업에 허용되는 협업 유형을 정의합니다.</span>
        </p>
        <div class="pol-highlight">
          <strong><span class="lang-en">Bottom line:</span><span class="lang-ko">핵심:</span></strong>
          <span class="lang-en"> Discuss approaches freely. Write your own solutions. Note who you worked with. During exams, no collaboration of any kind is permitted.</span>
          <span class="lang-ko"> 접근 방식은 자유롭게 논의하세요. 직접 해결책을 작성하세요. 함께 작업한 사람을 명시하세요. 시험 중에는 어떠한 협업도 허용되지 않습니다.</span>
        </div>
      </div>

      <div class="pol-content-section" id="individual">
        <h2><span class="lang-en">Individual Work</span><span class="lang-ko">개인 작업</span></h2>
        <p>
          <span class="lang-en">Homework assignments must be done individually &mdash; each student submits their own answers. However, it is acceptable to discuss approaches and help each other understand problems.</span>
          <span class="lang-ko">과제는 개별적으로 수행해야 합니다. 각 학생은 자신의 답안을 제출합니다. 그러나 접근 방식을 논의하고 문제 이해를 돕는 것은 허용됩니다.</span>
        </p>
        <ul class="pol-rule-list">
          <li>
            <span class="pol-rule-num">01</span>
            <span><span class="lang-en">You may discuss problems and approaches with classmates.</span><span class="lang-ko">동급생과 문제와 접근 방식을 논의할 수 있습니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">02</span>
            <span><span class="lang-en">You must write your own code and answers independently &mdash; no copying.</span><span class="lang-ko">코드와 답안은 독립적으로 직접 작성해야 합니다 &mdash; 복사 금지.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">03</span>
            <span><span class="lang-en">Indicate on each submission who you collaborated with (name in a comment or footnote).</span><span class="lang-ko">각 제출물에 함께 작업한 사람(주석이나 각주에 이름)을 표시하세요.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">04</span>
            <span><span class="lang-en">You are responsible for understanding any solution that arose from collaboration.</span><span class="lang-ko">협력을 통해 도출된 해결책을 이해하는 책임은 본인에게 있습니다.</span></span>
          </li>
        </ul>
      </div>

      <div class="pol-content-section" id="group">
        <h2><span class="lang-en">Group Work</span><span class="lang-ko">그룹 작업</span></h2>
        <p>
          <span class="lang-en">Group projects are an explicit exception &mdash; full collaboration within your group is expected and encouraged. Groups are assigned by the instructor.</span>
          <span class="lang-ko">그룹 프로젝트는 명시적인 예외입니다 &mdash; 그룹 내 완전한 협업이 기대되고 권장됩니다. 그룹은 강사가 배정합니다.</span>
        </p>
        <ul class="pol-rule-list">
          <li>
            <span class="pol-rule-num">01</span>
            <span><span class="lang-en">All group members are expected to contribute meaningfully to the project.</span><span class="lang-ko">모든 그룹원이 프로젝트에 의미 있게 기여할 것이 기대됩니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">02</span>
            <span><span class="lang-en">Individual contributions are tracked via GitHub commit history.</span><span class="lang-ko">개인 기여도는 GitHub 커밋 이력을 통해 추적됩니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">03</span>
            <span><span class="lang-en">Collaboration with students <em>outside</em> your assigned group is not permitted.</span><span class="lang-ko">배정된 그룹 <em>외부</em> 학생과의 협업은 허용되지 않습니다.</span></span>
          </li>
        </ul>
      </div>

      <div class="pol-content-section" id="integrity">
        <h2><span class="lang-en">Academic Integrity</span><span class="lang-ko">학문적 성실성</span></h2>
        <p>
          <span class="lang-en">Submitting another student's work as your own, copying code without attribution, or facilitating academic dishonesty are violations of academic integrity. Consequences may include a zero on the assignment, course failure, or referral to the university.</span>
          <span class="lang-ko">다른 학생의 작업을 자신의 것으로 제출하거나, 귀속 없이 코드를 복사하거나, 학문적 부정행위를 조장하는 것은 학문적 성실성 위반입니다. 결과로 과제 0점, 과락 또는 대학교 신고가 될 수 있습니다.</span>
        </p>
        <p>
          <span class="lang-en">See the <a href="{{ '/policies/ai' | relative_url }}">AI &amp; ChatGPT Use Policy</a> for rules about AI-generated content, which is covered separately.</span>
          <span class="lang-ko">AI 생성 콘텐츠에 관한 규정은 별도로 다루는 <a href="{{ '/policies/ai' | relative_url }}">AI &amp; ChatGPT 사용 정책</a>을 참조하세요.</span>
        </p>
      </div>

      <div class="pol-content-section" id="related">
        <h2><span class="lang-en">Related Policies</span><span class="lang-ko">관련 정책</span></h2>
        <div class="related-grid">
          <a href="{{ '/policies/ai' | relative_url }}" class="related-card">
            <span class="related-code">POL — 01</span>
            <span class="related-title"><span class="lang-en">AI &amp; ChatGPT Use</span><span class="lang-ko">AI 사용 정책</span></span>
            <span class="related-desc"><span class="lang-en">Permitted and prohibited AI use.</span><span class="lang-ko">허용 및 금지 AI 사용.</span></span>
          </a>
          <a href="{{ '/policies/assignments' | relative_url }}" class="related-card">
            <span class="related-code">POL — 03</span>
            <span class="related-title"><span class="lang-en">Assignments &amp; Practice</span><span class="lang-ko">과제 및 실습</span></span>
            <span class="related-desc"><span class="lang-en">Submission rules and grading.</span><span class="lang-ko">제출 규정 및 채점.</span></span>
          </a>
          <a href="{{ '/policies/tests' | relative_url }}" class="related-card">
            <span class="related-code">POL — 04</span>
            <span class="related-title"><span class="lang-en">Tests &amp; Exams</span><span class="lang-ko">시험 정책</span></span>
            <span class="related-desc"><span class="lang-en">Exam rules for written and programming portions.</span><span class="lang-ko">필기 및 프로그래밍 시험 규정.</span></span>
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
