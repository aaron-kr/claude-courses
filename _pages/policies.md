---
layout: default
title: Academic Policies
subtitle: 학사 규정
permalink: /policies/
eyebrow: Academic Policies
---

<style>
/* Policy page specific styles */
.policy-featured-grid { display: grid; grid-template-columns: repeat(auto-fill,minmax(280px,1fr)); gap: 16px; margin-bottom: 44px; }
.policy-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 24px;
  text-decoration: none;
  color: inherit;
  display: flex;
  flex-direction: column;
  gap: 10px;
  position: relative;
  overflow: hidden;
  transition: border-color .2s, transform .18s;
  &::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: linear-gradient(90deg, var(--accent3), var(--accent), var(--accent2)); }
  &:hover { border-color: #3a3a5a; transform: translateY(-1px); }
}
.policy-card-icon { font-size: 1.5rem; }
.policy-card-tag  { font-family: 'IBM Plex Mono', monospace; font-size: .6rem; color: var(--accent3); text-transform: uppercase; letter-spacing: .1em; }
.policy-card-title { font-size: 1rem; font-weight: 500; color: var(--text); line-height: 1.3; }
.policy-card-desc  { font-size: .82rem; color: var(--sub); line-height: 1.55; flex: 1; }
.policy-card-arrow { font-size: .75rem; color: var(--muted); margin-top: 4px; }
a.policy-card:hover .policy-card-arrow { color: var(--accent3); }

.policy-list-row {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 13px 4px;
  border-bottom: 1px solid var(--border);
  text-decoration: none;
  color: inherit;
  transition: background .15s;
  &:first-child { border-top: 1px solid var(--border); }
  &:hover { background: var(--surface); }
}
.plr-icon  { font-size: 1.1rem; width: 28px; flex-shrink: 0; text-align: center; }
.plr-main  { flex: 1; min-width: 0; }
.plr-title { font-size: .9rem; font-weight: 500; color: var(--text); }
.plr-desc  { font-size: .78rem; color: var(--muted); margin-top: 2px; }
.plr-tag   { font-family: 'IBM Plex Mono', monospace; font-size: .6rem; padding: 2px 8px; border-radius: 3px; background: var(--tag-bg); border: 1px solid var(--border); color: var(--muted); white-space: nowrap; }
.plr-arrow { font-size: .75rem; color: var(--muted); opacity: 0; transition: opacity .18s, transform .18s; }
a.policy-list-row:hover .plr-arrow { opacity: 1; transform: translateX(3px); }

.faq-item { border-bottom: 1px solid var(--border); &:first-child { border-top: 1px solid var(--border); } }
.faq-q { display: flex; align-items: center; justify-content: space-between; gap: 12px; padding: 14px 4px; cursor: pointer; font-size: .9rem; font-weight: 500; color: var(--text); user-select: none; &:hover { color: var(--accent2); } }
.faq-chevron { font-size: .75rem; color: var(--muted); transition: transform .25s; flex-shrink: 0; }
.faq-a { display: none; padding: 0 4px 14px; font-size: .88rem; color: var(--sub); line-height: 1.75; }
.faq-item.open .faq-a { display: block; }
.faq-item.open .faq-chevron { transform: rotate(180deg); }
</style>

<div class="wrap">
  <header style="padding:60px 0 36px;border-bottom:1px solid var(--border);">
    <div class="eyebrow">
      <span class="lang-en">Academic Policies / Guidelines</span>
      <span class="lang-ko">학사 규정 / 지침</span>
    </div>
    <h1>Policies &amp;<br><em>Guidelines</em></h1>
    <p style="margin-top:16px;max-width:560px;font-size:.95rem;color:var(--muted);line-height:1.8;border-left:2px solid var(--border);padding-left:18px;">
      <span class="lang-en">These policies apply to all courses taught by Prof. Aaron Snowberger.
      Individual course pages may note course-specific variations.</span>
      <span class="lang-ko">이 규정은 Aaron Snowberger 교수가 가르치는 모든 강좌에 적용됩니다.
      강좌별 세부 사항은 각 강좌 페이지를 확인하세요.</span>
    </p>
  </header>

  <main style="padding:40px 0 80px;max-width:760px;">

    <!-- ── Featured Policy ─────────────────────────────────────────────── -->
    <div class="crs-heading" style="margin-bottom:16px;">
      <span class="crs-label">
        <span class="lang-en">Featured Policy</span>
        <span class="lang-ko">주요 정책</span>
      </span>
      <span class="crs-line"></span>
    </div>

    <div class="policy-featured-grid" style="margin-bottom:36px;">
      <a class="policy-card" href="{{ '/policies/ai' | relative_url }}">
        <span class="policy-card-icon">🤖</span>
        <span class="policy-card-tag">
          <span class="lang-en">AI Tools &amp; ChatGPT</span>
          <span class="lang-ko">AI 도구 및 ChatGPT</span>
        </span>
        <div class="policy-card-title">
          <span class="lang-en">AI &amp; ChatGPT Usage Policy</span>
          <span class="lang-ko">AI 및 ChatGPT 사용 정책</span>
        </div>
        <div class="policy-card-desc">
          <span class="lang-en">When and how AI tools may be used for coursework, assignments, and exams. Includes disclosure requirements.</span>
          <span class="lang-ko">과제, 시험에서 AI 도구를 언제, 어떻게 사용할 수 있는지와 공개 요건을 안내합니다.</span>
        </div>
        <div class="policy-card-arrow">Read full policy →</div>
      </a>
    </div>

    <!-- ── All Policies (list rows) ────────────────────────────────────── -->
    <div class="crs-heading" style="margin-bottom:12px;">
      <span class="crs-label">
        <span class="lang-en">All Policies</span>
        <span class="lang-ko">전체 규정</span>
      </span>
      <span class="crs-line"></span>
    </div>

    <div style="margin-bottom:44px;">
      <a class="policy-list-row" href="{{ '/policies/attendance' | relative_url }}">
        <span class="plr-icon">📋</span>
        <div class="plr-main">
          <div class="plr-title">
            <span class="lang-en">Attendance &amp; Participation</span>
            <span class="lang-ko">출석 및 참여</span>
          </div>
          <div class="plr-desc">
            <span class="lang-en">Absence limits, excused absences, participation expectations.</span>
            <span class="lang-ko">결석 한도, 공결, 참여 기대치.</span>
          </div>
        </div>
        <span class="plr-tag">Core / 핵심</span>
        <span class="plr-arrow">→</span>
      </a>

      <a class="policy-list-row" href="{{ '/policies/assignments' | relative_url }}">
        <span class="plr-icon">📝</span>
        <div class="plr-main">
          <div class="plr-title">
            <span class="lang-en">Assignments &amp; Practice Exercises</span>
            <span class="lang-ko">과제 및 실습</span>
          </div>
          <div class="plr-desc">
            <span class="lang-en">Submission formats, GitHub Classroom, practice vs. graded work.</span>
            <span class="lang-ko">제출 방식, GitHub Classroom, 연습 과제와 채점 과제.</span>
          </div>
        </div>
        <span class="plr-tag">Core / 핵심</span>
        <span class="plr-arrow">→</span>
      </a>

      <a class="policy-list-row" href="{{ '/policies/tests' | relative_url }}">
        <span class="plr-icon">📖</span>
        <div class="plr-main">
          <div class="plr-title">
            <span class="lang-en">Tests &amp; Exams</span>
            <span class="lang-ko">시험</span>
          </div>
          <div class="plr-desc">
            <span class="lang-en">Midterm and final exam format, closed-book vs. open-book rules, regrading.</span>
            <span class="lang-ko">중간·기말고사 형식, 닫힌/열린 책 규정, 재평가.</span>
          </div>
        </div>
        <span class="plr-tag">Core / 핵심</span>
        <span class="plr-arrow">→</span>
      </a>

      <a class="policy-list-row" href="{{ '/policies/collaboration' | relative_url }}">
        <span class="plr-icon">🤝</span>
        <div class="plr-main">
          <div class="plr-title">
            <span class="lang-en">Collaboration Policy</span>
            <span class="lang-ko">협업 정책</span>
          </div>
          <div class="plr-desc">
            <span class="lang-en">What constitutes acceptable collaboration on homework and projects.</span>
            <span class="lang-ko">과제 및 프로젝트에서 허용되는 협업 범위.</span>
          </div>
        </div>
        <span class="plr-tag">Academic / 학문</span>
        <span class="plr-arrow">→</span>
      </a>

      <a class="policy-list-row" href="{{ '/policies/late' | relative_url }}">
        <span class="plr-icon">⏰</span>
        <div class="plr-main">
          <div class="plr-title">
            <span class="lang-en">Late Policy</span>
            <span class="lang-ko">지각 제출 정책</span>
          </div>
          <div class="plr-desc">
            <span class="lang-en">6 late days per semester, penalty schedule, zero-credit cutoff.</span>
            <span class="lang-ko">학기당 6일 지각, 감점 일정, 0점 기준.</span>
          </div>
        </div>
        <span class="plr-tag">Deadlines / 기한</span>
        <span class="plr-arrow">→</span>
      </a>

      <a class="policy-list-row" href="{{ '/policies/ai' | relative_url }}">
        <span class="plr-icon">🤖</span>
        <div class="plr-main">
          <div class="plr-title">
            <span class="lang-en">AI &amp; ChatGPT Usage Policy</span>
            <span class="lang-ko">AI 및 ChatGPT 사용 정책</span>
          </div>
          <div class="plr-desc">
            <span class="lang-en">Allowed and prohibited uses of AI tools in coursework.</span>
            <span class="lang-ko">수업에서 AI 도구의 허용 및 금지 사용.</span>
          </div>
        </div>
        <span class="plr-tag">★ Featured</span>
        <span class="plr-arrow">→</span>
      </a>
    </div>

    <!-- ── FAQ ─────────────────────────────────────────────────────────── -->
    <div class="crs-heading" style="margin-bottom:12px;">
      <span class="crs-label">
        <span class="lang-en">Frequently Asked Questions</span>
        <span class="lang-ko">자주 묻는 질문</span>
      </span>
      <span class="crs-line"></span>
    </div>

    <div id="faq-list" style="margin-bottom:40px;">

      <div class="faq-item">
        <div class="faq-q">
          <span class="lang-en">What happens if I miss more than 3 classes?</span>
          <span class="lang-ko">수업을 3회 이상 결석하면 어떻게 되나요?</span>
          <span class="faq-chevron">▾</span>
        </div>
        <div class="faq-a">
          <span class="lang-en">Missing more than 15% of total class hours (approximately 3 classes in a 3-credit course) will lower your attendance score. Missing more than 25% will result in a failing grade for attendance. Missing more than 35% total (including excused) will result in course failure.</span>
          <span class="lang-ko">총 수업 시간의 15% 이상 결석하면 출석 점수가 낮아집니다. 25% 이상 결석하면 출석 부분에서 과락이 됩니다. 공결 포함 35% 이상 결석하면 과락이 됩니다.</span>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-q">
          <span class="lang-en">Can I use ChatGPT to help with my homework?</span>
          <span class="lang-ko">숙제에 ChatGPT를 사용할 수 있나요?</span>
          <span class="faq-chevron">▾</span>
        </div>
        <div class="faq-a">
          <span class="lang-en">You may use AI tools to <em>understand</em> concepts and debug your thinking, but you may NOT submit AI-generated code or text as your own work. You must be able to explain everything you submit. If you use AI for any part of an assignment, you must disclose it. See the AI Policy for full details.</span>
          <span class="lang-ko">AI 도구를 개념 이해와 디버깅 보조로 사용할 수 있지만, AI가 생성한 코드나 텍스트를 자신의 작업으로 제출할 수 없습니다. 제출한 모든 내용을 설명할 수 있어야 합니다. AI를 사용했다면 반드시 공개해야 합니다. 자세한 내용은 AI 사용 정책을 참조하세요.</span>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-q">
          <span class="lang-en">How many late days do I get?</span>
          <span class="lang-ko">지각 제출 유예 일수는 몇 일인가요?</span>
          <span class="faq-chevron">▾</span>
        </div>
        <div class="faq-a">
          <span class="lang-en">You have 6 total late days per semester, usable across any assignments. After those are used, there is a 50% penalty per late day. Assignments receive zero credit 48 hours after the late-day limit is exceeded.</span>
          <span class="lang-ko">학기당 총 6일의 지각 유예 일수가 있으며, 어떤 과제에도 사용 가능합니다. 이를 초과하면 지각일당 50% 감점이 적용됩니다. 유예 일수 초과 후 48시간이 지나면 0점 처리됩니다.</span>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-q">
          <span class="lang-en">Is the course graded on a curve (상대평가)?</span>
          <span class="lang-ko">이 강의는 상대평가인가요?</span>
          <span class="faq-chevron">▾</span>
        </div>
        <div class="faq-a">
          <span class="lang-en">Most university courses in Korea use relative grading (상대평가) by default, where grade distribution follows university-mandated quotas. Some special or small-enrollment courses may use absolute grading (절대평가). Check your individual course page for specifics.</span>
          <span class="lang-ko">한국 대부분의 대학 강의는 기본적으로 상대평가로 운영됩니다. 일부 특수 강의나 소규모 강의는 절대평가를 적용할 수 있습니다. 각 강좌 페이지에서 구체적인 내용을 확인하세요.</span>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-q">
          <span class="lang-en">What if I think my test was graded incorrectly?</span>
          <span class="lang-ko">시험 채점이 잘못된 것 같으면 어떻게 하나요?</span>
          <span class="faq-chevron">▾</span>
        </div>
        <div class="faq-a">
          <span class="lang-en">Submit a regrading request by email with a clear explanation of what you believe was graded incorrectly and why. Note that regrading may result in your grade going up <em>or</em> down.</span>
          <span class="lang-ko">잘못 채점된 부분과 그 이유를 명확히 작성하여 이메일로 재평가 요청을 제출하세요. 재평가 결과 점수가 올라가거나 내려갈 수 있습니다.</span>
        </div>
      </div>

    </div>

  </main>
</div>

<script>
// FAQ accordion
document.querySelectorAll('.faq-q').forEach(q => {
  q.addEventListener('click', () => {
    const item = q.closest('.faq-item');
    const wasOpen = item.classList.contains('open');
    document.querySelectorAll('.faq-item.open').forEach(i => i.classList.remove('open'));
    if (!wasOpen) item.classList.add('open');
  });
});
</script>
