---
layout: default
title: Tests & Exams Policy
permalink: /policies/tests/
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
    <span class="lang-en">Academic Policy &mdash; POL 04</span>
    <span class="lang-ko">학사 규정 &mdash; POL 04</span>
  </p>
  <h1 class="animate d2">
    <span class="lang-en">Tests &amp;<br><em>Exams</em></span>
    <span class="lang-ko">시험 &amp;<br><em>시험 정책</em></span>
  </h1>
</header>
<div class="pol-page">
  <a href="{{ '/policies' | relative_url }}" class="back-btn animate d1" style="margin-bottom:18px;display:inline-flex">
    ← <span class="lang-en">All Policies</span><span class="lang-ko">전체 정책</span>
  </a>
  <div class="pol-meta-bar animate d2">
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Policy Code</span><span class="lang-ko">정책 코드</span></span>
      <span class="pol-meta-value">POL &mdash; 04</span>
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
        <li><a href="#written"><span class="lang-en">Written (Closed)</span><span class="lang-ko">필기 (닫힌 책)</span></a></li>
        <li><a href="#programming"><span class="lang-en">Programming (Open)</span><span class="lang-ko">프로그래밍 (열린 책)</span></a></li>
        <li><a href="#general"><span class="lang-en">General Rules</span><span class="lang-ko">일반 규정</span></a></li>
        <li><a href="#regrading"><span class="lang-en">Regrading</span><span class="lang-ko">재채점</span></a></li>
      </ul>
    </aside>
    <main>
      <div class="pol-content-section" id="overview">
        <h2><span class="lang-en">Overview</span><span class="lang-ko">개요</span></h2>
        <p>
          <span class="lang-en">Most courses have a midterm exam and a final exam. Each exam has two portions: a written (closed-book) portion and a programming (open-book) portion. Different rules apply to each.</span>
          <span class="lang-ko">대부분의 강좌에는 중간고사와 기말고사가 있습니다. 각 시험은 필기(닫힌 책) 부분과 프로그래밍(열린 책) 부분으로 구성됩니다. 각 부분에 다른 규정이 적용됩니다.</span>
        </p>
        <div class="pol-highlight">
          <strong><span class="lang-en">Bottom line:</span><span class="lang-ko">핵심:</span></strong>
          <span class="lang-en"> No phones during any test. During programming portions you may reference material, but you must write all code yourself. Cheating results in a zero for the entire exam.</span>
          <span class="lang-ko"> 시험 중에는 휴대폰을 사용할 수 없습니다. 프로그래밍 부분에서는 자료를 참고할 수 있지만, 모든 코드는 직접 작성해야 합니다. 부정행위는 전체 시험 0점 처리됩니다.</span>
        </div>
      </div>

      <div class="pol-content-section" id="written">
        <h2><span class="lang-en">Written (Closed-Book) Portions</span><span class="lang-ko">필기 (닫힌 책) 부분</span></h2>
        <p>
          <span class="lang-en">No phones, notes, AI tools, or resources of any kind. You must work completely independently.</span>
          <span class="lang-ko">휴대폰, 노트, AI 도구 등 어떤 자료도 사용할 수 없습니다. 완전히 독립적으로 작업해야 합니다.</span>
        </p>
        <ul class="pol-rule-list">
          <li>
            <span class="pol-rule-num">01</span>
            <span><span class="lang-en">All electronic devices must be off and in your bag — not on your desk.</span><span class="lang-ko">모든 전자기기는 꺼서 가방에 넣어야 합니다 — 책상 위에 두면 안 됩니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">02</span>
            <span><span class="lang-en">No notes, textbooks, or printed materials of any kind.</span><span class="lang-ko">노트, 교과서 또는 인쇄된 자료는 어떤 것도 허용되지 않습니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">03</span>
            <span><span class="lang-en">Questions should be directed to the instructor only — no talking to other students.</span><span class="lang-ko">질문은 강사에게만 해야 합니다 — 다른 학생과 대화하면 안 됩니다.</span></span>
          </li>
        </ul>
      </div>

      <div class="pol-content-section" id="programming">
        <h2><span class="lang-en">Programming (Open-Book) Portions</span><span class="lang-ko">프로그래밍 (열린 책) 부분</span></h2>
        <p>
          <span class="lang-en">You may use any reference &mdash; including the Internet and AI tools &mdash; but <strong>you must write all code yourself</strong>. Pasting AI output directly is not allowed.</span>
          <span class="lang-ko">인터넷과 AI 도구를 포함한 모든 자료를 참고용으로 사용할 수 있지만, <strong>모든 코드는 직접 작성해야 합니다</strong>. AI 출력을 직접 붙여넣는 것은 허용되지 않습니다.</span>
        </p>
        <p>
          <span class="lang-en">Code copied from ChatGPT or other AI tools often does not function correctly and will not receive full credit. Understanding what you submit is your responsibility.</span>
          <span class="lang-ko">ChatGPT나 다른 AI 도구에서 복사한 코드는 종종 제대로 작동하지 않으며 만점을 받지 못합니다. 제출하는 내용을 이해하는 것은 귀하의 책임입니다.</span>
        </p>
        <ul class="pol-rule-list">
          <li>
            <span class="pol-rule-num">01</span>
            <span><span class="lang-en">Phone use is still <strong>prohibited</strong> even during the open-book portion.</span><span class="lang-ko">열린 책 부분에서도 휴대폰 사용은 여전히 <strong>금지</strong>됩니다.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">02</span>
            <span><span class="lang-en">You may not share your screen, code, or answers with other students.</span><span class="lang-ko">다른 학생과 화면, 코드 또는 답안을 공유할 수 없습니다.</span></span>
          </li>
        </ul>
      </div>

      <div class="pol-content-section" id="general">
        <h2><span class="lang-en">General Rules</span><span class="lang-ko">일반 규정</span></h2>
        <ul class="pol-rule-list">
          <li>
            <span class="pol-rule-num">01</span>
            <span><span class="lang-en">No cellphones during any test portion.</span><span class="lang-ko">시험 중 휴대폰 사용 금지.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">02</span>
            <span><span class="lang-en">No bathroom breaks during tests. Plan ahead.</span><span class="lang-ko">시험 중 화장실 이용 금지. 미리 준비하세요.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">03</span>
            <span><span class="lang-en">No talking during any test. Cheating = zero for the entire exam, not just one portion.</span><span class="lang-ko">시험 중 대화 금지. 부정행위 = 일부가 아닌 전체 시험 0점.</span></span>
          </li>
          <li>
            <span class="pol-rule-num">04</span>
            <span><span class="lang-en">Arrive on time. Students arriving late may not receive extra time to finish.</span><span class="lang-ko">제시간에 도착하세요. 늦게 도착한 학생은 추가 시간을 받지 못할 수 있습니다.</span></span>
          </li>
        </ul>
      </div>

      <div class="pol-content-section" id="regrading">
        <h2><span class="lang-en">Regrading</span><span class="lang-ko">재채점</span></h2>
        <p>
          <span class="lang-en">If you believe a grading error was made, you may request a regrade by email within one week of receiving your score. Explain specifically which question(s) you believe were graded incorrectly and why.</span>
          <span class="lang-ko">채점 오류가 있다고 판단되면 성적을 받은 후 1주일 이내에 이메일로 재채점을 요청할 수 있습니다. 어느 문항이 잘못 채점되었는지, 그 이유를 구체적으로 설명하세요.</span>
        </p>
        <div class="pol-highlight">
          <strong><span class="lang-en">Note:</span><span class="lang-ko">참고:</span></strong>
          <span class="lang-en"> Regrading may result in your score going <em>up or down</em>. The entire exam is subject to review when a regrade is requested.</span>
          <span class="lang-ko"> 재채점 결과 점수가 <em>오르거나 내릴 수 있습니다</em>. 재채점 요청 시 전체 시험이 검토 대상이 됩니다.</span>
        </div>
      </div>

      <div class="pol-content-section" id="related">
        <h2><span class="lang-en">Related Policies</span><span class="lang-ko">관련 정책</span></h2>
        <div class="related-grid">
          <a href="{{ '/policies/ai' | relative_url }}" class="related-card">
            <span class="related-code">POL — 01</span>
            <span class="related-title"><span class="lang-en">AI &amp; ChatGPT Use</span><span class="lang-ko">AI 사용 정책</span></span>
            <span class="related-desc"><span class="lang-en">Permitted and prohibited AI use.</span><span class="lang-ko">허용 및 금지 AI 사용.</span></span>
          </a>
          <a href="{{ '/policies/collaboration' | relative_url }}" class="related-card">
            <span class="related-code">POL — 05</span>
            <span class="related-title"><span class="lang-en">Collaboration</span><span class="lang-ko">협업 정책</span></span>
            <span class="related-desc"><span class="lang-en">What counts as acceptable help.</span><span class="lang-ko">허용되는 협업 범위.</span></span>
          </a>
          <a href="{{ '/policies/assignments' | relative_url }}" class="related-card">
            <span class="related-code">POL — 03</span>
            <span class="related-title"><span class="lang-en">Assignments &amp; Practice</span><span class="lang-ko">과제 및 실습</span></span>
            <span class="related-desc"><span class="lang-en">Submission rules and grading.</span><span class="lang-ko">제출 규정 및 채점.</span></span>
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
