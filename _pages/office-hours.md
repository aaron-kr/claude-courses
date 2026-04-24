---
layout: default
title: Office Hours
permalink: /office-hours/
---

<style>
.oh-page{padding:44px 0 72px}
.week-grid{display:grid;grid-template-columns:repeat(5,1fr);gap:12px}
.day-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:16px;position:relative;overflow:hidden;transition:border-color .2s}
.day-logo{position:absolute;top:10px;right:10px;width:44px;height:44px;display:flex;flex-direction:column;align-items:center;justify-content:center;font-family:'IBM Plex Mono',monospace;font-size:.52rem;font-weight:500;letter-spacing:.06em;text-transform:uppercase;color:var(--text);border:1.5px solid var(--text);opacity:.1;line-height:1.3;text-align:center;z-index:0;pointer-events:none}
.day-logo .dl-abbr{font-size:.68rem;font-weight:500}
.day-card.today-card{border-color:rgba(109,204,221,.45)}
.day-card.today-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--accent3),var(--accent2))}
.today-chip-sm{position:absolute;top:10px;left:10px;font-family:'IBM Plex Mono',monospace;font-size:.52rem;letter-spacing:.1em;text-transform:uppercase;background:rgba(109,204,221,.12);color:var(--accent3);border:1px solid rgba(109,204,221,.28);border-radius:3px;padding:2px 6px;z-index:2}
.day-name{font-family:'IBM Plex Mono',monospace;font-size:.62rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;margin-bottom:8px}
.day-school{font-size:.85rem;font-weight:500;color:var(--text);line-height:1.3;margin-bottom:4px}
.day-school-kr{font-family:'IBM Plex Mono',monospace;font-size:.62rem;color:var(--muted)}
.day-oh{margin-top:10px;padding-top:10px;border-top:1px solid var(--border)}
.day-oh-label{font-family:'IBM Plex Mono',monospace;font-size:.56rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;display:block;margin-bottom:4px}
.day-oh-time{font-size:.78rem;color:var(--accent2)}
.day-oh-room{font-size:.7rem;color:var(--muted);font-family:'IBM Plex Mono',monospace;margin-top:2px}
.oh-heading{display:flex;align-items:center;gap:14px;margin:36px 0 18px}
.oh-label{font-family:'IBM Plex Mono',monospace;font-size:.72rem;color:var(--muted);text-transform:uppercase;letter-spacing:.12em;white-space:nowrap}
.oh-line{flex:1;height:1px;background:var(--border)}
.contact-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.contact-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:18px;position:relative;overflow:hidden}
.contact-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px}
.contact-card.c1::before{background:linear-gradient(90deg,#fee500,#fbbf24)}
.contact-card.c2::before{background:linear-gradient(90deg,var(--accent),var(--accent2))}
.contact-card.c3::before{background:linear-gradient(90deg,var(--accent2),var(--accent3))}
.contact-rank{font-family:'IBM Plex Mono',monospace;font-size:.57rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;margin-bottom:7px;display:block}
.contact-name{font-size:.9rem;font-weight:500;color:var(--text);margin-bottom:5px}
.contact-desc{font-size:.78rem;color:var(--sub);line-height:1.65;margin-bottom:11px}
.contact-link{display:inline-flex;align-items:center;gap:6px;font-family:'IBM Plex Mono',monospace;font-size:.67rem;letter-spacing:.04em;text-decoration:none;padding:5px 13px;border-radius:var(--radius);border:1px solid var(--border);color:var(--sub);background-size:205% 100%;background-position:100%;transition:background-position .32s ease,color .2s,border-color .2s}
.contact-link.cl-kakao{background-image:linear-gradient(to right,#fee500 50%,var(--tag-bg) 50%)}
.contact-link.cl-kakao:hover{background-position:0;color:#2a1800;border-color:#fee500}
.contact-link.cl-email{background-image:linear-gradient(to right,var(--accent) 50%,var(--tag-bg) 50%)}
.contact-link.cl-email:hover{background-position:0;color:#fff;border-color:var(--accent)}
.contact-link.cl-campus{background-image:linear-gradient(to right,var(--accent3) 50%,var(--tag-bg) 50%)}
.contact-link.cl-campus:hover{background-position:0;color:var(--bg);border-color:var(--accent3)}
.booking-box{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);overflow:hidden;margin-top:14px;position:relative}
.booking-box::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--accent3),var(--accent),var(--accent2))}
.booking-header{padding:20px 24px 16px;border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:12px}
.booking-title{font-family:'Playfair Display','DM Serif Display',serif;font-size:1.15rem;font-weight:700;color:var(--text)}
.booking-title span{font-family:'IBM Plex Mono',monospace;font-size:.65rem;font-weight:400;color:var(--accent3);background:rgba(109,204,221,.1);border:1px solid rgba(109,204,221,.22);border-radius:3px;padding:2px 8px;margin-left:10px;vertical-align:middle}
.booking-meta{font-size:.8rem;color:var(--muted)}
.booking-footer{padding:14px 24px;border-top:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:10px}
.booking-note{font-size:.78rem;color:var(--muted)}
.booking-link{font-family:'IBM Plex Mono',monospace;font-size:.68rem;color:var(--accent3);text-decoration:none;letter-spacing:.04em}
.booking-link:hover{text-decoration:underline}
@media(max-width:800px){.week-grid{grid-template-columns:repeat(3,1fr)}.contact-grid{grid-template-columns:1fr}}
@media(max-width:500px){.week-grid{grid-template-columns:repeat(2,1fr)}}
</style>

<div class="wrap">
<header>
  <div class="today-pill animate d1" id="today-pill">
    <span class="today-dot"></span>
    <span id="today-text">Loading&hellip;</span>
  </div>
  <p class="eyebrow animate d1">
    <span class="lang-en">Availability &amp; Contact</span>
    <span class="lang-ko">가용성 및 연락처</span>
  </p>
  <h1 class="animate d2">Office<br><em>Hours</em></h1>
  <p class="hero-desc animate d3">
    <span class="lang-en">I teach at a different campus each weekday. Office hours are held after class at that day&rsquo;s campus. For quick questions, <strong style="color:var(--text)">KakaoTalk is always the fastest route</strong>.</span>
    <span class="lang-ko">매일 다른 캠퍼스에서 강의합니다. 상담 시간은 그 날 강의 후 해당 캠퍼스에서 진행됩니다. 빠른 질문은 <strong style="color:var(--text)">카카오톡이 가장 빠릅니다</strong>.</span>
  </p>
</header>
<div class="oh-page">

  <div class="oh-heading animate d3">
    <span class="oh-label"><span class="lang-en">Weekly Campus Schedule</span><span class="lang-ko">주간 캠퍼스 일정</span></span>
    <span class="oh-line"></span>
  </div>
  <div class="week-grid animate d4" id="week-grid">

    <div class="day-card" data-day="1">
      <div class="day-logo"><span class="dl-abbr">UT</span></div>
      <div class="day-name"><span class="lang-en">Monday</span><span class="lang-ko">월요일</span></div>
      <div class="day-school"><span class="lang-en">Korea Transportation Univ.</span><span class="lang-ko">한국교통대학교</span></div>
      <div class="day-school-kr">교통대 (UT)</div>
      <div class="day-oh">
        <span class="day-oh-label"><span class="lang-en">Office Hours</span><span class="lang-ko">상담 시간</span></span>
        <div class="day-oh-time"><span class="lang-en">After class</span><span class="lang-ko">수업 후</span></div>
        <div class="day-oh-room">충주캠퍼스</div>
      </div>
    </div>

    <div class="day-card" data-day="2">
      <div class="day-logo"><span class="dl-abbr">WKU</span></div>
      <div class="day-name"><span class="lang-en">Tuesday</span><span class="lang-ko">화요일</span></div>
      <div class="day-school"><span class="lang-en">Wonkwang University</span><span class="lang-ko">원광대학교</span></div>
      <div class="day-school-kr">원광대 (WKU)</div>
      <div class="day-oh">
        <span class="day-oh-label"><span class="lang-en">Office Hours</span><span class="lang-ko">상담 시간</span></span>
        <div class="day-oh-time"><span class="lang-en">After class</span><span class="lang-ko">수업 후</span></div>
        <div class="day-oh-room">익산캠퍼스</div>
      </div>
    </div>

    <div class="day-card" data-day="3">
      <div class="day-logo"><span class="dl-abbr">JBNU</span></div>
      <div class="day-name"><span class="lang-en">Wednesday</span><span class="lang-ko">수요일</span></div>
      <div class="day-school"><span class="lang-en">Jeonbuk National Univ.</span><span class="lang-ko">전북대학교</span></div>
      <div class="day-school-kr">전북대 (JBNU)</div>
      <div class="day-oh">
        <span class="day-oh-label"><span class="lang-en">Office Hours</span><span class="lang-ko">상담 시간</span></span>
        <div class="day-oh-time"><span class="lang-en">After class (AM)</span><span class="lang-ko">수업 후 (오전)</span></div>
        <div class="day-oh-room">전주캠퍼스</div>
      </div>
    </div>

    <div class="day-card" data-day="4">
      <div class="day-logo"><span class="dl-abbr">HB</span></div>
      <div class="day-name"><span class="lang-en">Thursday</span><span class="lang-ko">목요일</span></div>
      <div class="day-school"><span class="lang-en">Hanbat University</span><span class="lang-ko">한밭대학교</span></div>
      <div class="day-school-kr">한밭대 (HB)</div>
      <div class="day-oh">
        <span class="day-oh-label"><span class="lang-en">Office Hours</span><span class="lang-ko">상담 시간</span></span>
        <div class="day-oh-time"><span class="lang-en">After class</span><span class="lang-ko">수업 후</span></div>
        <div class="day-oh-room">대전캠퍼스</div>
      </div>
    </div>

    <div class="day-card" data-day="5">
      <div class="day-logo"><span class="dl-abbr">JNUE</span></div>
      <div class="day-name"><span class="lang-en">Friday</span><span class="lang-ko">금요일</span></div>
      <div class="day-school"><span class="lang-en">Jeonju Natl. Univ. of Ed.</span><span class="lang-ko">전주교육대학교</span></div>
      <div class="day-school-kr">전주교육대 (JNUE)</div>
      <div class="day-oh">
        <span class="day-oh-label"><span class="lang-en">Office Hours</span><span class="lang-ko">상담 시간</span></span>
        <div class="day-oh-time"><span class="lang-en">After class</span><span class="lang-ko">수업 후</span></div>
        <div class="day-oh-room">전주캠퍼스</div>
      </div>
    </div>

  </div><!-- .week-grid -->

  <div class="oh-heading">
    <span class="oh-label"><span class="lang-en">How to Reach Me</span><span class="lang-ko">연락 방법</span></span>
    <span class="oh-line"></span>
  </div>
  <div class="contact-grid">
    <div class="contact-card c1">
      <span class="contact-rank">① <span class="lang-en">Quickest</span><span class="lang-ko">가장 빠름</span></span>
      <div class="contact-name">KakaoTalk Open Chat</div>
      <p class="contact-desc">
        <span class="lang-en">Best for quick questions, logistics, and anything time-sensitive. I check this throughout the day at all campuses.</span>
        <span class="lang-ko">빠른 질문, 일정 조율, 긴급 사항에 가장 좋습니다. 모든 캠퍼스에서 하루 종일 확인합니다.</span>
      </p>
      <a href="https://open.kakao.com/me/aaronkr" class="contact-link cl-kakao" target="_blank">💬 <span class="lang-en">Open KakaoTalk</span><span class="lang-ko">카카오톡 열기</span></a>
    </div>
    <div class="contact-card c2">
      <span class="contact-rank">② <span class="lang-en">Formal</span><span class="lang-ko">공식 문의</span></span>
      <div class="contact-name">Email</div>
      <p class="contact-desc">
        <span class="lang-en">For formal requests or anything needing a written record. Include your student ID and course. Response within 48 hrs on weekdays.</span>
        <span class="lang-ko">공식 요청이나 기록이 필요한 사항에 적합합니다. 학번과 강좌명을 포함해 주세요. 평일 48시간 이내 답변.</span>
      </p>
      <a href="mailto:{{ site.email }}" class="contact-link cl-email">✉ {{ site.email | replace: '@', ' &#064; ' }}</a>
    </div>
    <div class="contact-card c3">
      <span class="contact-rank">③ <span class="lang-en">In Person</span><span class="lang-ko">직접 방문</span></span>
      <div class="contact-name"><span class="lang-en">On Campus</span><span class="lang-ko">캠퍼스 방문</span></div>
      <p class="contact-desc">
        <span class="lang-en">Find me after class at the campus where I teach that day. No appointment needed during posted OH. For other times, email or book below.</span>
        <span class="lang-ko">해당 요일 강의 후 캠퍼스에서 만날 수 있습니다. 공지된 상담 시간에는 예약 불필요. 그 외 시간은 이메일 또는 아래에서 예약하세요.</span>
      </p>
      <a href="#week-grid" class="contact-link cl-campus">📍 <span class="lang-en">See Weekly Schedule ↑</span><span class="lang-ko">주간 일정 보기 ↑</span></a>
    </div>
  </div>

  <div class="oh-heading">
    <span class="oh-label"><span class="lang-en">Book a Meeting</span><span class="lang-ko">미팅 예약</span></span>
    <span class="oh-line"></span>
  </div>
  <div class="booking-box">
    <div class="booking-header">
      <div>
        <div class="booking-title">Aaron Snowberger <span>cal.com/aaronkr</span></div>
        <div class="booking-meta">
          <span class="lang-en">30 min or 1 hr &middot; Video call or on-campus &middot; Asia/Seoul</span>
          <span class="lang-ko">30분 또는 1시간 &middot; 화상통화 또는 캠퍼스 &middot; 아시아/서울</span>
        </div>
      </div>
    </div>
    <div style="padding:28px 24px;font-size:.88rem;color:var(--sub);line-height:1.75;">
      <span class="lang-en">Book a time slot via <strong style="color:var(--accent2)">Cal.com</strong> — free, open-source scheduling that embeds anywhere. Pick a 30-minute check-in or 1-hour deep-dive slot.</span>
      <span class="lang-ko"><strong style="color:var(--accent2)">Cal.com</strong>을 통해 시간을 예약하세요 — 어디서나 임베드 가능한 무료 오픈소스 스케줄링 도구입니다. 30분 간단 상담 또는 1시간 심화 상담 중 선택하세요.</span>
    </div>
    <div class="booking-footer">
      <span class="booking-note">
        <span class="lang-en">ⓘ Set up your own at cal.com — free, open-source, embeddable anywhere</span>
        <span class="lang-ko">ⓘ cal.com에서 직접 만들어 보세요 — 무료, 오픈소스, 어디서나 임베드 가능</span>
      </span>
      <a href="https://cal.com/aaronkr" target="_blank" class="booking-link">
        <span class="lang-en">Book at cal.com/aaronkr →</span>
        <span class="lang-ko">cal.com/aaronkr에서 예약 →</span>
      </a>
    </div>
  </div>

  <!-- Booking recommendation box (restored) -->
  <div class="oh-heading" style="margin-top:28px"><span class="oh-label">Tools &amp; Recommendations</span><span class="oh-line"></span></div>
  <div style="background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:24px;display:flex;gap:24px;align-items:flex-start;position:relative;overflow:hidden;margin-bottom:52px">
    <div style="position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--accent2),var(--accent3),var(--accent))"></div>
    <div style="flex:1">
      <div style="font-family:'Playfair Display','DM Serif Display',serif;font-size:1.05rem;font-weight:700;color:var(--text);margin-bottom:8px">My recommended setup for booking</div>
      <p style="font-size:.85rem;color:var(--sub);line-height:1.75;margin-bottom:14px">Because I teach at five campuses and student needs vary by course, I recommend <strong style="color:var(--accent2)">Cal.com</strong> for booking outside regular OH. It’s free, open-source, embeds on any webpage, and supports multiple event types (30 min check-in, 1-hr deep dive, etc.).</p>
      <div style="background:rgba(126,184,247,.06);border:1px solid rgba(126,184,247,.18);border-radius:var(--radius);padding:12px 16px;font-size:.82rem;color:var(--sub);line-height:1.7">
        <strong style="color:var(--accent2)">Cal.com</strong> — free, open-source, embeddable &nbsp;·&nbsp;
        <strong style="color:var(--accent3)">Calendly</strong> — also good, more polished UI &nbsp;·&nbsp;
        <strong style="color:var(--accent)">Notion Scheduling</strong> — if you already use Notion for your courses
      </div>
    </div>
    <div style="display:flex;flex-direction:column;gap:8px;flex-shrink:0;min-width:145px">
      <a href="https://cal.com" target="_blank" style="display:flex;align-items:center;justify-content:center;gap:6px;font-family:'IBM Plex Mono',monospace;font-size:.69rem;letter-spacing:.04em;text-decoration:none;padding:8px 16px;border-radius:var(--radius);border:1px solid var(--border);color:var(--sub);background-image:linear-gradient(to right,var(--accent2) 50%,var(--surface) 50%);background-size:205% 100%;background-position:100%;transition:background-position .32s ease,color .2s,border-color .2s" onmouseover="this.style.backgroundPosition='0';this.style.color='var(--bg)'" onmouseout="this.style.backgroundPosition='100%';this.style.color='var(--sub)'">📅 Cal.com →</a>
      <a href="https://calendly.com" target="_blank" style="display:flex;align-items:center;justify-content:center;gap:6px;font-family:'IBM Plex Mono',monospace;font-size:.69rem;letter-spacing:.04em;text-decoration:none;padding:8px 16px;border-radius:var(--radius);border:1px solid var(--border);color:var(--sub);background-image:linear-gradient(to right,var(--accent3) 50%,var(--surface) 50%);background-size:205% 100%;background-position:100%;transition:background-position .32s ease,color .2s,border-color .2s" onmouseover="this.style.backgroundPosition='0';this.style.color='var(--bg)'" onmouseout="this.style.backgroundPosition='100%';this.style.color='var(--sub)'">📅 Calendly →</a>
    </div>
  </div>

</div><!-- .oh-page -->
</div><!-- .wrap -->

<script>
(function(){
  const campuses = {
    1: { en: 'Korea Transportation University', ko: '한국교통대학교 (월요일)' },
    2: { en: 'Wonkwang University',             ko: '원광대학교 (화요일)' },
    3: { en: 'Jeonbuk National University',     ko: '전북대학교 (수요일)' },
    4: { en: 'Hanbat University',               ko: '한밭대학교 (목요일)' },
    5: { en: 'Jeonju Natl. Univ. of Ed.',       ko: '전주교육대학교 (금요일)' }
  };
  const pill = document.getElementById('today-pill');
  const txt  = document.getElementById('today-text');
  const d    = new Date().getDay();
  const isKo = document.documentElement.classList.contains('ko');
  if (campuses[d]) {
    if (txt) txt.innerHTML = (isKo ? '오늘: <strong style="color:var(--text)">' : 'Today at: <strong style="color:var(--text)">') + (isKo ? campuses[d].ko : campuses[d].en) + '</strong>';
    const card = document.querySelector(`.day-card[data-day="${d}"]`);
    if (card) {
      card.classList.add('today-card');
      card.insertAdjacentHTML('afterbegin', '<span class="today-chip-sm">Today</span>');
    }
  } else {
    if (txt) txt.innerHTML = isKo ? '주말 — 휴강' : 'No classes today &mdash; weekend';
    if (pill) pill.classList.add('noclass');
  }
})();
</script>
