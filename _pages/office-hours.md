---
layout: default
title: Office Hours
subtitle: 상담 시간
permalink: /office-hours/
---

<div class="wrap">
  <header style="padding:60px 0 36px;border-bottom:1px solid var(--border);">
    <div class="eyebrow">Office Hours / 상담 시간</div>
    <h1>Office <em>Hours</em></h1>
    <p class="hero-desc" style="margin-top:16px;">
      I am available for office hours by appointment.
      The best way to reach me is via KakaoTalk or email.
      <br><br>
      예약을 통해 상담 시간을 이용하실 수 있습니다.
      카카오톡 또는 이메일로 연락해 주세요.
    </p>
  </header>

  <main style="padding:40px 0 80px;">

    <div class="crs-section">
      <div class="crs-heading"><span class="crs-label">Weekly Campus Schedule / 주간 캠퍼스 일정</span><span class="crs-line"></span></div>

      <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:12px;">
        {%- assign days = "Monday,Tuesday,Wednesday,Wednesday,Thursday,Friday" | split: "," -%}
        {%- assign unis = "Korea Transportation University,Wonkwang University,Jeonbuk University (AM),Hanbat University (PM),Jeonbuk University,Jeonju Natl. Univ. of Education" | split: "," -%}
        {%- assign unis_ko = "한국교통대학교,원광대학교,전북대학교 (오전),한밭대학교 (오후),전북대학교,전주교육대학교" | split: "," -%}
        {%- assign abbrs = "UT,WKU,JBNU,HB,JBNU,JNUE" | split: "," -%}
        {%- for i in (0..5) -%}
        <div style="background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:16px;position:relative;overflow:hidden;">
          <div style="position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--accent3),var(--accent));"></div>
          <div style="font-family:'IBM Plex Mono',monospace;font-size:.65rem;color:var(--accent2);text-transform:uppercase;letter-spacing:.08em;margin-bottom:6px;">{{ days[i] }}</div>
          <div style="font-size:.9rem;font-weight:500;color:var(--text);margin-bottom:2px;">{{ abbrs[i] }}</div>
          <div style="font-size:.78rem;color:var(--sub);">{{ unis[i] }}</div>
          <div style="font-size:.72rem;color:var(--muted);margin-top:2px;">{{ unis_ko[i] }}</div>
        </div>
        {%- endfor -%}
      </div>
    </div>

    <div class="crs-section">
      <div class="crs-heading"><span class="crs-label">Contact / 연락처</span><span class="crs-line"></span></div>
      {% include about_aaron.html %}
    </div>

    <div class="crs-section">
      <div class="crs-heading"><span class="crs-label">Booking / 예약</span><span class="crs-line"></span></div>
      <div style="background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:22px;">
        <p style="margin-bottom:12px;">To schedule an appointment, please contact me via KakaoTalk or email with:</p>
        <ul style="margin-bottom:12px;">
          <li>Your name and student ID / 이름과 학번</li>
          <li>The course you are enrolled in / 수강 중인 강좌</li>
          <li>The topic you wish to discuss / 상담 주제</li>
          <li>Preferred date and time / 선호하는 날짜와 시간</li>
        </ul>
        <div class="quick-links">
          <a href="https://open.kakao.com/me/aaronkr" class="ql-btn kakao" target="_blank">💬 KakaoTalk</a>
          <a href="mailto:{{ site.email }}" class="ql-btn">✉ Email</a>
        </div>
      </div>
    </div>

  </main>
</div>
