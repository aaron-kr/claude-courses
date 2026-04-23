---
layout: default
title: Office Hours
subtitle: 상담 시간
permalink: /office-hours/
---

<div class="wrap">
  <header style="padding:60px 0 36px;border-bottom:1px solid var(--border);">
    <div class="today-pill animate d1" id="today-pill-oh">
      <span class="today-dot"></span>
      <span id="today-text-oh">Loading...</span>
    </div>
    <div class="eyebrow">
      <span class="lang-en">Office Hours / Contact</span>
      <span class="lang-ko">상담 시간 / 연락처</span>
    </div>
    <h1>Office <em>Hours</em></h1>
    <p style="margin-top:16px;max-width:560px;font-size:.95rem;color:var(--muted);line-height:1.8;border-left:2px solid var(--border);padding-left:18px;">
      <span class="lang-en">Available by appointment. Contact me via KakaoTalk or email in advance.</span>
      <span class="lang-ko">예약을 통해 상담 시간을 이용하실 수 있습니다. 카카오톡 또는 이메일로 사전 연락해 주세요.</span>
    </p>
  </header>

  <main style="padding:40px 0 80px;">

    <!-- ── How to Reach Me ─────────────────────────────────────────────── -->
    <div class="crs-section">
      <div class="crs-heading">
        <span class="crs-label">
          <span class="lang-en">How to Reach Me</span>
          <span class="lang-ko">연락 방법</span>
        </span>
        <span class="crs-line"></span>
      </div>
      <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:14px;margin-bottom:32px;">

        <!-- KakaoTalk -->
        <div style="background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:22px;position:relative;overflow:hidden;">
          <div style="position:absolute;top:0;left:0;right:0;height:3px;background:#fee500;"></div>
          <div style="font-size:1.6rem;margin-bottom:10px;">💬</div>
          <div style="font-family:'IBM Plex Mono',monospace;font-size:.72rem;color:var(--accent);text-transform:uppercase;letter-spacing:.1em;margin-bottom:6px;">KakaoTalk</div>
          <div style="font-size:.88rem;color:var(--text);margin-bottom:6px;">
            <span class="lang-en">Fastest response (usually same day)</span>
            <span class="lang-ko">가장 빠른 응답 (보통 당일)</span>
          </div>
          <div style="font-size:.8rem;color:var(--muted);margin-bottom:14px;">
            <span class="lang-en">Best for quick questions, scheduling, urgent issues.</span>
            <span class="lang-ko">간단한 질문, 일정 조율, 긴급한 사항에 적합합니다.</span>
          </div>
          <a href="https://open.kakao.com/me/aaronkr" class="ql-btn kakao" target="_blank" style="display:inline-flex;">
            💬 <span class="lang-en">Open KakaoTalk</span><span class="lang-ko">카카오톡 열기</span>
          </a>
        </div>

        <!-- Email -->
        <div style="background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:22px;position:relative;overflow:hidden;">
          <div style="position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--accent3),var(--accent));"></div>
          <div style="font-size:1.6rem;margin-bottom:10px;">✉</div>
          <div style="font-family:'IBM Plex Mono',monospace;font-size:.72rem;color:var(--accent2);text-transform:uppercase;letter-spacing:.1em;margin-bottom:6px;">Email</div>
          <div style="font-size:.88rem;color:var(--text);margin-bottom:6px;">
            <span class="lang-en">Response within 1–2 business days</span>
            <span class="lang-ko">영업일 기준 1~2일 이내 응답</span>
          </div>
          <div style="font-size:.8rem;color:var(--muted);margin-bottom:14px;">
            <span class="lang-en">Best for formal requests, grade inquiries, documents.</span>
            <span class="lang-ko">공식 요청, 성적 문의, 서류 관련에 적합합니다.</span>
          </div>
          <a href="mailto:{{ site.email }}" class="ql-btn" style="display:inline-flex;">
            ✉ {{ site.email | replace: '@', ' &#064; ' }}
          </a>
        </div>

        <!-- Booking -->
        <div style="background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:22px;position:relative;overflow:hidden;">
          <div style="position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--accent),var(--accent2));"></div>
          <div style="font-size:1.6rem;margin-bottom:10px;">📅</div>
          <div style="font-family:'IBM Plex Mono',monospace;font-size:.72rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;margin-bottom:6px;">
            <span class="lang-en">Book a Meeting</span>
            <span class="lang-ko">미팅 예약</span>
          </div>
          <div style="font-size:.88rem;color:var(--text);margin-bottom:6px;">
            <span class="lang-en">Schedule via cal.com (coming soon)</span>
            <span class="lang-ko">cal.com으로 예약 (준비 중)</span>
          </div>
          <div style="font-size:.8rem;color:var(--muted);margin-bottom:14px;">
            <span class="lang-en">Pick a time slot that works for both of us.</span>
            <span class="lang-ko">서로에게 편한 시간을 선택해 주세요.</span>
          </div>
          <a href="https://cal.com/aaronkr" class="ql-btn" target="_blank" style="display:inline-flex;">
            📅 <span class="lang-en">Book Time →</span><span class="lang-ko">시간 예약 →</span>
          </a>
        </div>

      </div>
    </div>

    <!-- ── Weekly Campus Schedule ─────────────────────────────────────── -->
    <div class="crs-section">
      <div class="crs-heading">
        <span class="crs-label">
          <span class="lang-en">Weekly Campus Schedule</span>
          <span class="lang-ko">주간 캠퍼스 일정</span>
        </span>
        <span class="crs-line"></span>
      </div>
      <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:12px;">
        {%- assign days_en = "Monday,Tuesday,Wednesday AM,Wednesday PM,Thursday,Friday" | split: "," -%}
        {%- assign days_ko = "월요일,화요일,수요일 오전,수요일 오후,목요일,금요일" | split: "," -%}
        {%- assign unis_en = "Korea Transportation University,Wonkwang University,Jeonbuk University,Hanbat University,Jeonbuk University,Jeonju Natl. Univ. of Education" | split: "," -%}
        {%- assign unis_ko = "한국교통대학교,원광대학교,전북대학교,한밭대학교,전북대학교,전주교육대학교" | split: "," -%}
        {%- assign abbrs = "UT,WKU,JBNU,HB,JBNU,JNUE" | split: "," -%}
        {%- for i in (0..5) -%}
        <div style="background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:16px;position:relative;overflow:hidden;">
          <div style="position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--accent3),var(--accent));"></div>
          <div style="font-family:'IBM Plex Mono',monospace;font-size:.65rem;color:var(--accent2);text-transform:uppercase;letter-spacing:.08em;margin-bottom:6px;">
            <span class="lang-en">{{ days_en[i] }}</span>
            <span class="lang-ko">{{ days_ko[i] }}</span>
          </div>
          <div style="font-size:.9rem;font-weight:500;color:var(--text);margin-bottom:2px;">{{ abbrs[i] }}</div>
          <div style="font-size:.78rem;color:var(--muted);">
            <span class="lang-en">{{ unis_en[i] }}</span>
            <span class="lang-ko">{{ unis_ko[i] }}</span>
          </div>
        </div>
        {%- endfor -%}
      </div>
    </div>

    <!-- ── Contact / Instructor box ───────────────────────────────────── -->
    <div class="crs-section">
      <div class="crs-heading">
        <span class="crs-label">
          <span class="lang-en">Contact / Instructor</span>
          <span class="lang-ko">연락처 / 강사 소개</span>
        </span>
        <span class="crs-line"></span>
      </div>
      {% include about_aaron.html %}
    </div>

  </main>
</div>

<script>
// Today pill for office hours page
(function() {
  const schedule = {
    1: { name: 'UT — Korea Transportation University', ko: '한국교통대학교 (월요일)' },
    2: { name: 'WKU — Wonkwang University',           ko: '원광대학교 (화요일)' },
    3: { name: 'JBNU — Jeonbuk University',           ko: '전북대학교 (수요일)' },
    4: { name: 'HB — Hanbat University',              ko: '한밭대학교 (목요일)' },
    5: { name: 'JNUE — Jeonju Natl. Univ. of Ed.',   ko: '전주교육대학교 (금요일)' },
  };
  const day = new Date().getDay();
  const pill = document.getElementById('today-pill-oh');
  const txt  = document.getElementById('today-text-oh');
  if (!pill || !txt) return;
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
</script>
