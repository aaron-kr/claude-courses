---
layout: default
title: AI & ChatGPT Use Policy
permalink: /policies/ai/
---

<style>
.section-heading{display:flex;align-items:center;gap:14px;margin-bottom:20px}
.section-label-sm{font-family:'IBM Plex Mono',monospace;font-size:.75rem;color:var(--muted);text-transform:uppercase;letter-spacing:.12em;white-space:nowrap}
.section-line-sm{flex:1;height:1px;background:var(--border)}
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
    <span class="lang-en">Academic Policy &mdash; POL 01</span>
    <span class="lang-ko">학사 규정 &mdash; POL 01</span>
  </p>
  <h1 class="animate d2">
    <span class="lang-en">AI &amp; ChatGPT<br><em>Use Policy</em></span>
    <span class="lang-ko">AI &amp; ChatGPT<br><em>사용 정책</em></span>
  </h1>
</header>
<div class="pol-page">
  <a href="{{ '/policies' | relative_url }}" class="back-btn animate d1" style="margin-bottom:18px;display:inline-flex">
    ← <span class="lang-en">All Policies</span><span class="lang-ko">전체 정책</span>
  </a>
  <div class="pol-meta-bar animate d2">
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Policy Code</span><span class="lang-ko">정책 코드</span></span>
      <span class="pol-meta-value">POL &mdash; 01</span>
    </div>
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Effective</span><span class="lang-ko">시행일</span></span>
      <span class="pol-meta-value"><span class="lang-en">September 2023</span><span class="lang-ko">2023년 9월</span></span>
    </div>
    <div class="pol-meta-item">
      <span class="pol-meta-label"><span class="lang-en">Last Updated</span><span class="lang-ko">최종 수정</span></span>
      <span class="pol-meta-value"><span class="lang-en">January 2025</span><span class="lang-ko">2025년 1월</span></span>
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
        <li><a href="#permitted"><span class="lang-en">Permitted</span><span class="lang-ko">허용</span></a></li>
        <li><a href="#prohibited"><span class="lang-en">Prohibited</span><span class="lang-ko">금지</span></a></li>
        <li><a href="#disclosure"><span class="lang-en">Disclosure</span><span class="lang-ko">공개</span></a></li>
        <li><a href="#consequences"><span class="lang-en">Consequences</span><span class="lang-ko">결과</span></a></li>
        <li><a href="#rationale"><span class="lang-en">Rationale</span><span class="lang-ko">취지</span></a></li>
      </ul>
    </aside>
    <main>
      <div class="pol-content-section" id="overview">
        <h2><span class="lang-en">Overview</span><span class="lang-ko">개요</span></h2>
        <p>
          <span class="lang-en">Generative AI tools &mdash; including ChatGPT, Claude, Gemini, and Copilot &mdash; are powerful aids for learning. This policy establishes clear boundaries, balancing pedagogical value with academic integrity.</span>
          <span class="lang-ko">ChatGPT, Claude, Gemini, Copilot 등의 생성형 AI 도구는 강력한 학습 보조 수단입니다. 이 정책은 교육적 가치와 학문적 성실성 사이에서 명확한 경계를 설정합니다.</span>
        </p>
        <div class="pol-highlight">
          <strong><span class="lang-en">Bottom line:</span><span class="lang-ko">핵심:</span></strong>
          <span class="lang-en"> Use AI as a thinking partner and learning aid. Do not use it to generate the substance of work you submit as your own. Disclosure is always mandatory.</span>
          <span class="lang-ko"> AI를 사고 파트너이자 학습 보조로 활용하세요. 본인의 것으로 제출하는 작업물의 실질적인 내용을 생성하는 데는 사용하지 마세요. 공개는 항상 의무입니다.</span>
        </div>
      </div>

      <div class="pol-content-section" id="permitted">
        <h2><span class="lang-en">What is Permitted</span><span class="lang-ko">허용 사항</span></h2>
        <ul class="pol-rule-list">
          <li><span class="pol-rule-num">01</span><span><span class="lang-en">Using AI to <strong>brainstorm ideas</strong> or break down a problem &mdash; as long as the final work reflects your own analysis.</span><span class="lang-ko">문제를 <strong>브레인스토밍하거나</strong> 분석하는 데 AI 사용 &mdash; 단, 최종 작업물은 본인의 분석을 반영해야 합니다.</span></span></li>
          <li><span class="pol-rule-num">02</span><span><span class="lang-en">Using AI to <strong>understand concepts</strong> from course material, as a supplement to textbooks.</span><span class="lang-ko">교과서 보충으로 수업 자료의 <strong>개념을 이해</strong>하는 데 AI 사용.</span></span></li>
          <li><span class="pol-rule-num">03</span><span><span class="lang-en">Using AI to <strong>debug code</strong> you wrote, or to explain error messages. The solution logic must be yours.</span><span class="lang-ko">직접 작성한 코드를 <strong>디버깅</strong>하거나 오류 메시지를 이해하는 데 AI 사용. 해결 로직은 본인의 것이어야 합니다.</span></span></li>
          <li><span class="pol-rule-num">04</span><span><span class="lang-en">Using AI to <strong>improve grammar or clarity</strong> of writing you have already drafted.</span><span class="lang-ko">이미 초안을 작성한 글의 <strong>문법이나 명확성을 개선</strong>하는 데 AI 사용.</span></span></li>
        </ul>
      </div>

      <div class="pol-content-section" id="prohibited">
        <h2><span class="lang-en">What is Prohibited</span><span class="lang-ko">금지 사항</span></h2>
        <ul class="pol-rule-list">
          <li><span class="pol-rule-num">01</span><span><span class="lang-en">Submitting AI-generated text as your own analysis, reasoning, or argumentation.</span><span class="lang-ko">AI가 생성한 텍스트를 본인의 분석, 추론, 논증으로 제출.</span></span></li>
          <li><span class="pol-rule-num">02</span><span><span class="lang-en">Using AI to generate complete or near-complete solutions to homework or programming assignments.</span><span class="lang-ko">숙제나 프로그래밍 과제의 완전하거나 거의 완전한 해결책을 생성하는 데 AI 사용.</span></span></li>
          <li><span class="pol-rule-num">03</span><span><span class="lang-en">Using any AI tool during exams, quizzes, or in-class assessments unless explicitly permitted.</span><span class="lang-ko">명시적으로 허용되지 않는 한 시험, 퀴즈, 수업 내 평가 중 AI 도구 사용.</span></span></li>
          <li><span class="pol-rule-num">04</span><span><span class="lang-en">Failing to disclose AI use. Undisclosed use is academic dishonesty regardless of extent.</span><span class="lang-ko">AI 사용 미공개. 공개하지 않은 사용은 범위에 관계없이 학문적 부정행위입니다.</span></span></li>
        </ul>
      </div>

      <div class="pol-content-section" id="disclosure">
        <h2><span class="lang-en">Disclosure Requirements</span><span class="lang-ko">공개 요건</span></h2>
        <p>
          <span class="lang-en">Add a disclosure statement at the end of any submission where AI was involved. Example:</span>
          <span class="lang-ko">AI가 관여된 모든 제출물 끝에 공개 선언을 추가하세요. 예시:</span>
        </p>
        <div class="pol-highlight" style="font-family:'IBM Plex Mono',monospace;font-size:.78rem;line-height:1.75">
          <strong><span class="lang-en">AI Disclosure:</span><span class="lang-ko">AI 공개:</span></strong>
          <span class="lang-en"> I used ChatGPT to brainstorm the structure of my answer in Problem 3. The full response was written by me based on course materials. I used Claude to check grammar in the final writeup.</span>
          <span class="lang-ko"> ChatGPT를 사용하여 문제 3의 답변 구조를 브레인스토밍했습니다. 전체 응답은 수업 자료를 바탕으로 제가 작성했습니다. 최종 작성에서 문법 검토를 위해 Claude를 사용했습니다.</span>
        </div>
        <p>
          <span class="lang-en">Be specific: name the tool, describe how you used it, and clarify what the final output reflects of your own work.</span>
          <span class="lang-ko">구체적으로: 도구 이름, 사용 방법, 최종 결과물에서 본인의 작업이 어떻게 반영되었는지 명확히 하세요.</span>
        </p>
      </div>

      <div class="pol-content-section" id="consequences">
        <h2><span class="lang-en">Consequences</span><span class="lang-ko">결과</span></h2>
        <ul class="pol-rule-list">
          <li><span class="pol-rule-num">⚠</span><span><strong><span class="lang-en">Minor:</span><span class="lang-ko">경미:</span></strong> <span class="lang-en">Used AI beyond permitted scope but disclosed → Zero on the assignment, verbal warning.</span><span class="lang-ko">허용 범위를 초과한 AI 사용이나 공개함 → 과제 0점, 구두 경고.</span></span></li>
          <li><span class="pol-rule-num">⚠</span><span><strong><span class="lang-en">Major:</span><span class="lang-ko">중대:</span></strong> <span class="lang-en">AI-generated submission without disclosure → Failing grade and university honor committee report.</span><span class="lang-ko">공개 없이 AI 생성 제출물 → 과락 및 대학 명예위원회 보고.</span></span></li>
        </ul>
      </div>

      <div class="pol-content-section" id="rationale">
        <h2><span class="lang-en">Rationale</span><span class="lang-ko">취지</span></h2>
        <p>
          <span class="lang-en">I permit AI use because working effectively with these tools is a genuine skill you will need in your career. The goal of your education is to develop <em>your</em> ability to reason and create. If AI does that work for you, you don&rsquo;t develop. The assessment is not the point &mdash; the learning is.</span>
          <span class="lang-ko">AI 도구를 효과적으로 활용하는 것은 커리어에서 필요한 진정한 기술이기 때문에 AI 사용을 허용합니다. 여러분의 교육 목표는 <em>여러분의</em> 추론하고 창조하는 능력을 개발하는 것입니다. AI가 그 작업을 대신하면 여러분은 성장하지 않습니다. 평가가 목적이 아니라 학습이 목적입니다.</span>
        </p>
      </div>

      <div class="pol-content-section">
        <h2><span class="lang-en">Related Policies</span><span class="lang-ko">관련 정책</span></h2>
        <div class="related-grid">
          <a class="related-card" href="{{ '/policies/assignments' | relative_url }}">
            <span class="related-code">POL &mdash; 03</span>
            <span class="related-title"><span class="lang-en">Assignment &amp; Collaboration</span><span class="lang-ko">과제 및 협업</span></span>
            <span class="related-desc"><span class="lang-en">Individual vs group work, plagiarism rules, code-sharing guidelines.</span><span class="lang-ko">개인 vs 그룹 과제, 표절 규정, 코드 공유 지침.</span></span>
          </a>
          <a class="related-card" href="{{ '/policies/tests' | relative_url }}">
            <span class="related-code">POL &mdash; 04</span>
            <span class="related-title"><span class="lang-en">Exam &amp; Assessment Policy</span><span class="lang-ko">시험 및 평가 정책</span></span>
            <span class="related-desc"><span class="lang-en">Closed-book rules, makeup exams, disability accommodations.</span><span class="lang-ko">닫힌 책 규정, 보충 시험, 장애 학생 배려.</span></span>
          </a>
          <a class="related-card" href="{{ '/policies/attendance' | relative_url }}">
            <span class="related-code">POL &mdash; 02</span>
            <span class="related-title"><span class="lang-en">Attendance Policy</span><span class="lang-ko">출석 규정</span></span>
            <span class="related-desc"><span class="lang-en">Absence limits, excused absences, participation grading.</span><span class="lang-ko">결석 한도, 공결, 참여 점수.</span></span>
          </a>
        </div>
      </div>
    </main>
  </div><!-- .pol-page-layout -->
</div><!-- .pol-page -->
</div><!-- .wrap -->

<script>
const sIds = ['overview','permitted','prohibited','disclosure','consequences','rationale'];
const obs = new IntersectionObserver(e => {
  e.forEach(x => {
    if (x.isIntersecting) {
      document.querySelectorAll('.pol-sidebar-nav a').forEach(a => a.classList.remove('active'));
      const a = document.querySelector(`.pol-sidebar-nav a[href="#${x.target.id}"]`);
      if (a) a.classList.add('active');
    }
  });
}, {rootMargin: '-25% 0px -65% 0px'});
sIds.forEach(id => { const el = document.getElementById(id); if (el) obs.observe(el); });
</script>
