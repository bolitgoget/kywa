# kywa
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>2026 청소년 글로벌 역량강화 파견단 | 활동기록</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Jua&family=Noto+Sans+KR:wght@400;500;700;900&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root{
    --navy:#152144;
    --navy-2:#1f3164;
    --sky:#3e8fcc;
    --sky-light:#cfe7f7;
    --yellow:#ffc93c;
    --coral:#ff6b5b;
    --cream:#f7f4ea;
    --paper:#ffffff;
    --ink:#1b2230;
    --ink-soft:#5b6270;
    --line:#d8d2c0;
    --radius:18px;
    --maxw:1180px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--cream);
    color:var(--ink);
    font-family:"Noto Sans KR", sans-serif;
    -webkit-font-smoothing:antialiased;
  }
  .eyebrow{
    font-family:"Space Mono", monospace;
    letter-spacing:.14em;
    text-transform:uppercase;
    font-size:.72rem;
    font-weight:700;
  }
  h1,h2,h3,.display{
    font-family:"Jua", sans-serif;
    font-weight:400;
    line-height:1.15;
    letter-spacing:-.01em;
  }
  a{color:inherit; text-decoration:none;}
  img{max-width:100%;display:block;}

  /* ===== Skip link / focus ===== */
  a:focus-visible, button:focus-visible{
    outline:3px solid var(--coral);
    outline-offset:2px;
  }

  /* ===== Top identity bar ===== */
  .topbar{
    background:var(--navy);
    color:#fff;
    padding:10px 24px;
    font-size:.78rem;
  }
  .topbar-inner{
    max-width:var(--maxw);
    margin:0 auto;
    display:flex;
    justify-content:space-between;
    align-items:center;
    color:#b9c4de;
  }
  .topbar-inner strong{color:#fff;font-weight:700;}

  /* ===== Header / hero ===== */
  header.hero{
    position:relative;
    background:linear-gradient(180deg, var(--navy) 0%, var(--navy-2) 62%, #274a86 100%);
    color:#fff;
    overflow:hidden;
    padding:56px 24px 84px;
  }
  .hero-inner{
    max-width:var(--maxw);
    margin:0 auto;
    position:relative;
    z-index:2;
  }
  .hero-top{
    display:flex;
    justify-content:space-between;
    align-items:flex-start;
    gap:24px;
    flex-wrap:wrap;
  }
  .brand{
    display:flex;
    align-items:center;
    gap:12px;
  }
  .brand-mark{
    width:46px;height:46px;border-radius:50%;
    background:var(--yellow);
    display:flex;align-items:center;justify-content:center;
    font-family:"Jua",sans-serif;color:var(--navy);font-size:1.3rem;
    flex-shrink:0;
  }
  .brand-text .eyebrow{color:var(--sky-light);}
  .brand-text strong{display:block;font-size:1.05rem;font-weight:700;}

  .hero-title{
    margin:44px 0 0;
    font-size:clamp(2.1rem, 5.2vw, 3.6rem);
    max-width:18ch;
  }
  .hero-title span{color:var(--yellow);}
  .hero-sub{
    margin:16px 0 0;
    max-width:52ch;
    color:#cfd8ee;
    font-size:1.02rem;
    line-height:1.7;
  }

  /* boarding pass strip */
  .boarding-pass{
    margin-top:40px;
    background:rgba(255,255,255,.06);
    border:1px solid rgba(255,255,255,.22);
    border-radius:var(--radius);
    backdrop-filter:blur(6px);
    display:flex;
    flex-wrap:wrap;
    position:relative;
  }
  .bp-field{
    flex:1 1 140px;
    padding:16px 20px;
    border-right:1px dashed rgba(255,255,255,.3);
  }
  .bp-field:last-child{border-right:none;}
  .bp-field .eyebrow{color:var(--sky-light);display:block;margin-bottom:6px;}
  .bp-field strong{font-family:"Space Mono",monospace;font-size:1.02rem;letter-spacing:.02em;}
  .bp-route{
    display:flex;align-items:center;gap:10px;
    font-family:"Space Mono",monospace;font-weight:700;
  }
  .bp-route .plane{color:var(--yellow);font-size:1.1rem;}

  .flight-path{
    position:absolute;
    inset:0;
    z-index:1;
    opacity:.5;
    pointer-events:none;
  }

  /* ===== Ticket tab navigation ===== */
  nav.ticket-nav{
    max-width:var(--maxw);
    margin:-46px auto 0;
    padding:0 24px;
    position:relative;
    z-index:3;
    display:grid;
    grid-template-columns:repeat(5,1fr);
    gap:14px;
  }
  .ticket-tab{
    appearance:none;
    border:1px solid var(--line);
    background:var(--paper);
    border-radius:14px;
    padding:16px 14px 14px;
    cursor:pointer;
    text-align:left;
    display:flex;
    flex-direction:column;
    gap:10px;
    position:relative;
    box-shadow:0 10px 24px rgba(21,33,68,.10);
    transition:transform .18s ease, box-shadow .18s ease, background .18s ease;
    color:var(--ink);
  }
  .ticket-tab:hover{transform:translateY(-3px);}
  .ticket-tab .stub-no{
    font-family:"Space Mono",monospace;
    font-size:.68rem;
    color:var(--ink-soft);
    letter-spacing:.08em;
  }
  .ticket-tab .stub-icon{
    width:30px;height:30px;
    border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    background:var(--sky-light);
    color:var(--navy);
  }
  .ticket-tab .stub-icon svg{width:16px;height:16px;}
  .ticket-tab .stub-label{
    font-family:"Jua",sans-serif;
    font-size:1.02rem;
  }
  .ticket-tab::after{
    content:"";
    position:absolute;
    right:12px; top:12px; bottom:12px;
    border-right:1px dashed var(--line);
  }
  .ticket-tab[aria-selected="true"]{
    background:var(--navy);
    color:#fff;
    border-color:var(--navy);
    box-shadow:0 14px 28px rgba(21,33,68,.28);
  }
  .ticket-tab[aria-selected="true"] .stub-no{color:var(--yellow);}
  .ticket-tab[aria-selected="true"] .stub-icon{background:var(--yellow);color:var(--navy);}
  .ticket-tab[aria-selected="true"]::after{border-color:rgba(255,255,255,.3);}

  @media (max-width:820px){
    nav.ticket-nav{grid-template-columns:repeat(2,1fr);margin-top:-28px;}
    .ticket-tab::after{display:none;}
  }

  /* ===== Main content ===== */
  main{
    max-width:var(--maxw);
    margin:0 auto;
    padding:64px 24px 100px;
  }
  .panel{display:none;}
  .panel.active{display:block;animation:fadein .35s ease;}
  @keyframes fadein{from{opacity:0;transform:translateY(8px);}to{opacity:1;transform:translateY(0);}}

  .section-head{
    display:flex;
    align-items:baseline;
    gap:14px;
    margin-bottom:32px;
    flex-wrap:wrap;
  }
  .section-head .eyebrow{color:var(--coral);}
  .section-head h2{font-size:clamp(1.6rem,3vw,2.1rem);margin:0;}
  .section-head p{margin:0;color:var(--ink-soft);}

  /* stat row */
  .stat-row{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:16px;
    margin:36px 0 48px;
  }
  .stat-card{
    background:var(--paper);
    border:1px solid var(--line);
    border-radius:var(--radius);
    padding:20px;
  }
  .stat-card strong{
    font-family:"Space Mono",monospace;
    font-size:1.8rem;
    color:var(--navy);
    display:block;
  }
  .stat-card span{color:var(--ink-soft);font-size:.85rem;}

  /* delegate grid */
  .grid-cards{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:18px;
  }
  .delegate-card{
    background:var(--paper);
    border:1px solid var(--line);
    border-radius:var(--radius);
    padding:20px;
    text-align:center;
    transition: transform 0.2s;
  }
  .delegate-card:hover {
    transform: translateY(-5px);
  }
  .avatar{
    width:64px;height:64px;border-radius:50%;
    margin:0 auto 12px;
    background:conic-gradient(from 180deg, var(--sky), var(--yellow), var(--coral), var(--sky));
    display:flex;align-items:center;justify-content:center;
    color:#fff;font-family:"Jua",sans-serif;font-size:1.1rem;
    border:3px solid #fff;
    box-shadow:0 0 0 1px var(--line);
  }
  .delegate-card h3{margin:0 0 4px;font-size:1.05rem;}
  .delegate-card p{margin:0;color:var(--ink-soft);font-size:.85rem;}
  .tag{
    display:inline-block;
    margin-top:10px;
    font-family:"Space Mono",monospace;
    font-size:.68rem;
    background:var(--sky-light);
    color:var(--navy);
    padding:3px 8px;
    border-radius:20px;
  }

  /* timeline (사전활동) */
  .timeline{
    position:relative;
    padding-left:32px;
    border-left:2px dashed var(--line);
  }
  .timeline-item{
    position:relative;
    padding-bottom:36px;
  }
  .timeline-item:last-child{padding-bottom:0;}
  .timeline-item::before{
    content:"";
    position:absolute;
    left:-40px; top:2px;
    width:16px;height:16px;
    border-radius:50%;
    background:var(--yellow);
    border:3px solid var(--navy);
  }
  .timeline-date{
    font-family:"Space Mono",monospace;
    font-size:.78rem;
    color:var(--coral);
    font-weight:700;
  }
  .timeline-item h3{margin:6px 0 6px;font-size:1.15rem;}
  .timeline-item p{margin:0;color:var(--ink-soft);line-height:1.65;}

  /* dispatch itinerary (파견활동) */
  .itinerary{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
  }
  .day-card{
    background:var(--paper);
    border:1px solid var(--line);
    border-radius:var(--radius);
    overflow:hidden;
    box-shadow: 0 4px 12px rgba(0,0,0,0.03);
  }
  .day-card .day-photo{
    height:130px;
    background:linear-gradient(135deg, var(--sky), var(--navy));
    display:flex;align-items:center;justify-content:center;
    color:#fff; font-family:"Space Mono",monospace; font-size:.75rem; letter-spacing:.08em;
  }
  .day-card .day-body{padding:16px 18px 20px;}
  .day-card .day-no{
    font-family:"Space Mono",monospace;
    color:var(--coral);
    font-size:.75rem;
    font-weight:700;
  }
  .day-card h3{margin:6px 0 8px;font-size:1.08rem;}
  .day-card p{margin:0;color:var(--ink-soft);font-size:.9rem;line-height:1.6;}

  /* records / journal (파견단의 기록) */
  .journal-list{display:flex;flex-direction:column;gap:0;}
  .journal-item{
    display:grid;
    grid-template-columns:120px 1fr auto;
    gap:20px;
    align-items:center;
    padding:22px 4px;
    border-bottom:1px solid var(--line);
  }
  .journal-item:first-child{border-top:1px solid var(--line);}
  .journal-date{
    font-family:"Space Mono",monospace;
    font-size:.85rem;
    color:var(--ink-soft);
  }
  .journal-item h3{margin:0 0 6px;font-size:1.08rem;}
  .journal-item p{margin:0;color:var(--ink-soft);font-size:.9rem;}
  .journal-author{
    font-family:"Space Mono",monospace;
    font-size:.72rem;
    background:var(--cream);
    border:1px solid var(--line);
    padding:5px 10px;
    border-radius:20px;
    white-space:nowrap;
  }

  /* album */
  .album-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:14px;
  }
  .album-item{
    aspect-ratio:1/1;
    border-radius:14px;
    position:relative;
    overflow:hidden;
    display:flex;
    align-items:flex-end;
    color:#fff;
    transition: transform 0.2s;
  }
  .album-item:hover {
    transform: scale(1.03);
  }
  .album-item span{
    position:relative;
    z-index:2;
    padding:10px 12px;
    font-size:.78rem;
    font-family:"Space Mono",monospace;
  }
  .album-item::before{
    content:"";
    position:absolute;inset:0;
    background:linear-gradient(180deg, transparent 40%, rgba(0,0,0,.55));
    z-index:1;
  }
  .album-item.c1{background:linear-gradient(135deg,#3e8fcc,#152144);}
  .album-item.c2{background:linear-gradient(135deg,#ffc93c,#ff6b5b);}
  .album-item.c3{background:linear-gradient(135deg,#274a86,#3e8fcc);}
  .album-item.c4{background:linear-gradient(135deg,#ff6b5b,#152144);}
  .album-item.c5{background:linear-gradient(135deg,#3e8fcc,#ffc93c);}
  .album-item.c6{background:linear-gradient(135deg,#152144,#ff6b5b);}
  .album-item.c7{background:linear-gradient(135deg,#ffc93c,#274a86);}
  .album-item.c8{background:linear-gradient(135deg,#274a86,#ff6b5b);}

  /* footer */
  footer{
    background:var(--navy);
    color:#b9c4de;
    padding:40px 24px;
    font-size:.82rem;
  }
  .footer-inner{
    max-width:var(--maxw);
    margin:0 auto;
    display:flex;
    justify-content:space-between;
    flex-wrap:wrap;
    gap:16px;
  }
  .footer-inner strong{color:#fff;}

  @media (max-width:900px){
    .grid-cards{grid-template-columns:repeat(2,1fr);}
    .itinerary{grid-template-columns:repeat(2,1fr);}
    .album-grid{grid-template-columns:repeat(3,1fr);}
    .stat-row{grid-template-columns:repeat(2,1fr);}
    .journal-item{grid-template-columns:1fr;text-align:left;}
  }
  @media (max-width:520px){
    .grid-cards{grid-template-columns:1fr; gap:12px;}
    .itinerary{grid-template-columns:1fr;}
    .album-grid{grid-template-columns:repeat(2,1fr);}
  }

  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    .panel.active{animation:none;}
    .ticket-tab{transition:none;}
  }
</style>
</head>
<body>

<div class="topbar">
  <div class="topbar-inner">
    <span><strong>2026 청소년 글로벌 역량강화사업</strong> 파견대표단 활동기록 공간</span>
    <span>여성가족부 · 한국청소년활동진흥원</span>
  </div>
</div>

<header class="hero">
  <svg class="flight-path" viewBox="0 0 1180 260" preserveAspectRatio="none" aria-hidden="true">
    <path d="M -20 220 C 250 60, 550 260, 820 90 S 1150 40, 1220 20" fill="none" stroke="#ffffff" stroke-width="2" stroke-dasharray="2 10" stroke-linecap="round"/>
  </svg>
  <div class="hero-inner">
    <div class="hero-top">
      <div class="brand">
        <div class="brand-mark">청</div>
        <div class="brand-text">
          <span class="eyebrow">International Youth Exchange</span>
          <strong>청소년국제교류네트워크</strong>
        </div>
      </div>
      <span class="eyebrow" style="color:#cfd8ee;">ACTIVITY LOG · SINCE 2026</span>
    </div>

    <h1 class="hero-title">2026년 청소년 글로벌<br>역량강화사업 <span>파견대표단</span></h1>
    <p class="hero-sub">전 세계를 무대로 성장한 청소년 파견대표단의 준비 과정부터 현지 활동, 귀국 후 기록까지 —
      한 팀의 여정을 담은 공식 활동기록 공간입니다.</p>

    <div class="boarding-pass">
      <div class="bp-field">
        <span class="eyebrow">FROM</span>
        <strong>REPUBLIC OF KOREA</strong>
      </div>
      <div class="bp-field">
        <span class="eyebrow">ROUTE</span>
        <div class="bp-route"><span>KOR</span><span class="plane">✈</span><span>DEU</span></div>
      </div>
      <div class="bp-field">
        <span class="eyebrow">TEAM</span>
        <strong>2026 GYEP-DELEGATION</strong>
      </div>
      <div class="bp-field">
        <span class="eyebrow">STATUS</span>
        <strong>진행중 · IN PROGRESS</strong>
      </div>
    </div>
  </div>
</header>

<nav class="ticket-nav" role="tablist" aria-label="파견단 활동기록 메뉴">
  <button class="ticket-tab" role="tab" aria-selected="true" aria-controls="panel-team" id="tab-team" data-target="panel-team">
    <span class="stub-no">STUB 01</span>
    <span class="stub-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="8" r="3.2"/><path d="M5 20c1.2-3.6 4-5.5 7-5.5s5.8 1.9 7 5.5"/></svg></span>
    <span class="stub-label">파견단</span>
  </button>
  <button class="ticket-tab" role="tab" aria-selected="false" aria-controls="panel-pre" id="tab-pre" data-target="panel-pre">
    <span class="stub-no">STUB 02</span>
    <span class="stub-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="4" y="3" width="16" height="18" rx="2"/><path d="M8 8h8M8 12h8M8 16h5"/></svg></span>
    <span class="stub-label">사전활동</span>
  </button>
  <button class="ticket-tab" role="tab" aria-selected="false" aria-controls="panel-dispatch" id="tab-dispatch" data-target="panel-dispatch">
    <span class="stub-no">STUB 03</span>
    <span class="stub-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="9"/><path d="M3 12h18M12 3c2.5 2.6 3.8 5.7 3.8 9s-1.3 6.4-3.8 9c-2.5-2.6-3.8-5.7-3.8-9S9.5 5.6 12 3z"/></svg></span>
    <span class="stub-label">파견활동</span>
  </button>
  <button class="ticket-tab" role="tab" aria-selected="false" aria-controls="panel-log" id="tab-log" data-target="panel-log">
    <span class="stub-no">STUB 04</span>
    <span class="stub-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 19V6a2 2 0 0 1 2-2h9l5 5v10a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2z"/><path d="M15 4v5h5"/><path d="M8 13h8M8 17h5"/></svg></span>
    <span class="stub-label">파견단의 기록</span>
  </button>
  <button class="ticket-tab" role="tab" aria-selected="false" aria-controls="panel-album" id="tab-album" data-target="panel-album">
    <span class="stub-no">STUB 05</span>
    <span class="stub-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="6" width="18" height="14" rx="2"/><circle cx="12" cy="13" r="3.2"/><path d="M8 6l1.4-2h5.2L16 6"/></svg></span>
    <span class="stub-label">앨범</span>
  </button>
</nav>

<main>

  <section class="panel active" id="panel-team" role="tabpanel" aria-labelledby="tab-team">
    <div class="section-head">
      <span class="eyebrow">ABOUT THE TEAM</span>
      <h2>2026 파견대표단을 소개합니다</h2>
    </div>
    <p style="max-width:70ch;color:var(--ink-soft);line-height:1.8;margin-bottom:32px;">
      2026년 청소년 글로벌 역량강화사업 파견대표단은 엄격한 공개모집을 통해 선발된 전국의 인재들로 구성되었습니다. 
      지속가능한 발전, 문화다양성, 그리고 글로벌 연대를 목표로 현지 국가의 청소년들과 소통하며 미래의 주역으로 발돋움하고 있습니다.
    </p>

    <div class="stat-row">
      <div class="stat-card"><strong>20명</strong><span>파견 인원</span></div>
      <div class="stat-card"><strong>독일</strong><span>파견 국가</span></div>
      <div class="stat-card"><strong>14일</strong><span>파견 기간</span></div>
      <div class="stat-card"><strong>2026</strong><span>파견 연도</span></div>
    </div>

    <div class="grid-cards">
      <div class="delegate-card">
        <div class="avatar">기획</div>
        <h3>권보성</h3>
        <p>미디어 기록 / 총괄 팀장</p>
        <span class="tag">LEADER</span>
      </div>
      <div class="delegate-card">
        <div class="avatar">통역</div>
        <h3>김지민</h3>
        <p>독일어 통역 / 교류 기획</p>
        <span class="tag">DELEGATE</span>
      </div>
      <div class="delegate-card">
        <div class="avatar">학술</div>
        <h3>이정우</h3>
        <p>글로벌 이슈 분석 / 세미나</p>
        <span class="tag">DELEGATE</span>
      </div>
      <div class="delegate-card">
        <div class="avatar">문화</div>
        <h3>박서연</h3>
        <p>문화예술 교류 / 콘텐츠 제작</p>
        <span class="tag">DELEGATE</span>
      </div>
    </div>
  </section>

  <section class="panel" id="panel-pre" role="tabpanel" aria-labelledby="tab-pre">
    <div class="section-head">
      <span class="eyebrow">BEFORE DEPARTURE</span>
      <h2>사전활동</h2>
      <p>파견 전 철저한 준비 과정을 시간순으로 기록합니다</p>
    </div>

    <div class="timeline">
      <div class="timeline-item">
        <span class="timeline-date">2026. 05. 16</span>
        <h3>발대식 및 오리엔테이션</h3>
        <p>여성가족부 및 한국청소년활동진흥원 주관 하에 파견대표단 공식 발대식을 개최하고 안전 수칙 교육 및 전체 로드맵을 공유했습니다.</p>
      </div>
      <div class="timeline-item">
        <span class="timeline-date">2026. 05 ~ 06</span>
        <h3>심화 어학 및 문화다양성 교육</h3>
        <p>독일의 역사, 사회구조, 그리고 기초 생활 독일어를 집중 학습하며 현지인들과 깊이 있게 소통할 수 있는 역량을 키웠습니다.</p>
      </div>
      <div class="timeline-item">
        <span class="timeline-date">2026. 06. 13</span>
        <h3>글로벌 이슈 팀빌딩 워크숍</h3>
        <p>지속가능발전목표(SDGs)와 난민 국제 분담 지원을 주제로 현지 모의 유네스코 총회 발표 자료를 기획하고 역할을 분담했습니다.</p>
      </div>
      <div class="timeline-item">
        <span class="timeline-date">2026. 06. 25</span>
        <h3>최종 점검 및 시뮬레이션</h3>
        <p>현지 청소년 단체와 진행할 문화 교류 프로그램을 최종 리허설하고, 파견 물품 및 단체복 배부 등 출국 준비를 완벽히 마쳤습니다.</p>
      </div>
    </div>
  </section>

  <section class="panel" id="panel-dispatch" role="tabpanel" aria-labelledby="tab-dispatch">
    <div class="section-head">
      <span class="eyebrow">ON SITE</span>
      <h2>파견활동</h2>
      <p>현지에서 진행된 핵심 일정을 생생하게 정리했습니다</p>
    </div>

    <div class="itinerary">
      <div class="day-card">
        <div class="day-photo" style="background: linear-gradient(135deg, #152144, #3e8fcc)">FRANKFURT ARRIVAL</div>
        <div class="day-body">
          <span class="day-no">DAY 01</span>
          <h3>프랑크푸르트 도착 및 환영식</h3>
          <p>긴 비행 끝에 현지 파트너 기관의 따뜻한 환영 속에 입국했습니다. 전체 일정 오리엔테이션과 현지 생활 안내를 받았습니다.</p>
        </div>
      </div>
      <div class="day-card">
        <div class="day-photo" style="background: linear-gradient(135deg, #3e8fcc, #ffc93c)">YOUTH EXCHANGE</div>
        <div class="day-body">
          <span class="day-no">DAY 02</span>
          <h3>독일 청소년 연합 교류 세미나</h3>
          <p>현지 청소년들과 만나 서로의 문화를 소개했습니다. 디지털 시대의 노동 인권과 청소년의 역할에 대해 열띤 토론을 나눴습니다.</p>
        </div>
      </div>
      <div class="day-card">
        <div class="day-photo" style="background: linear-gradient(135deg, #ff6b5b, #152144)">ECO CITY ECO-TOUR</div>
        <div class="day-body">
          <span class="day-no">DAY 03</span>
          <h3>친환경 도시 프라이부르크 탐방</h3>
          <p>세계적인 생태 도시 프라이부르크를 방문해 신재생 에너지 인프라와 친환경 건축 양식을 직접 시찰하며 지속가능한 미래를 배웠습니다.</p>
        </div>
      </div>
    </div>
  </section>

  <section class="panel" id="panel-log" role="tabpanel" aria-labelledby="tab-log">
    <div class="section-head">
      <span class="eyebrow">DELEGATE LOG</span>
      <h2>파견단의 기록</h2>
      <p>단원들이 현장에서 매일 직접 작성한 생생한 에세이와 기록입니다</p>
    </div>

    <div class="journal-list">
      <div class="journal-item">
        <span class="journal-date">2026.06.28</span>
        <div>
          <h3>낯선 공기 속, 첫 발을 내딛다</h3>
          <p>독일 땅에 첫발을 내디뎠을 때의 설렘과 긴장감. 거리에 가득한 낯선 독일어 간판을 보며 비로소 파견단 대표로서의 책임감이 느껴지기 시작했다.</p>
        </div>
        <span class="journal-author">권보성 단원</span>
      </div>
      <div class="journal-item">
        <span class="journal-date">2026.06.30</span>
        <div>
          <h3>언어의 벽을 넘어선 뜨거운 연대</h3>
          <p>독일 청소년들과의 세미나 시간, 서툰 언어였지만 눈빛과 몸짓으로 세계 시민으로서의 고민을 나눴다. 우리는 같은 시대를 살아가는 친구였다.</p>
        </div>
        <span class="journal-author">김지민 단원</span>
      </div>
      <div class="journal-item">
        <span class="journal-date">2026.07.02</span>
        <div>
          <h3>태양광 마을에서 찾은 도시의 미래</h3>
          <p>보방(Vauban) 지구의 친환경 주거 단지를 걸으며, 자연과 인간이 공존하는 건축이 무엇인지 깨달았다. 귀국 후 우리나라 도시 기획에도 접목해보고 싶다.</p>
        </div>
        <span class="journal-author">이정우 단원</span>
      </div>
    </div>
  </section>

  <section class="panel" id="panel-album" role="tabpanel" aria-labelledby="tab-album">
    <div class="section-head">
      <span class="eyebrow">PHOTO ARCHIVE</span>
      <h2>앨범</h2>
      <p>파견대표단이 함께 만든 빛나는 순간들의 아카이브</p>
    </div>

    <div class="album-grid">
      <div class="album-item c1"><span>📸 발대식 단체사진</span></div>
      <div class="album-item c2"><span>✈ 인천공항 출국 전</span></div>
      <div class="album-item c3"><span>🏛 파트너 기관 환영식</span></div>
      <div class="album-item c4"><span>🗣 글로벌 이슈 토론</span></div>
      <div class="album-item c5"><span>🌿 프라이부르크 현장학습</span></div>
      <div class="album-item c6"><span>🥨 현지 전통 문화체험</span></div>
      <div class="album-item c7"><span>🇩🇪 브란덴부르크 문 앞에서</span></div>
      <div class="album-item c8"><span>🛫 성과보고회 및 귀국</span></div>
    </div>
  </section>

</main>

<footer>
  <div class="footer-inner">
    <div>
      <strong>2026 청소년 글로벌 역량강화사업 파견대표단</strong><br>
      본 페이지는 파견대표단의 공식 활동 기록 및 포트폴리오 공간입니다.
    </div>
    <div>여성가족부 · 한국청소년활동진흥원(KYWA)<br>© 2026 International Youth Exchange Network</div>
  </div>
</footer>

<script>
  const tabs = document.querySelectorAll('.ticket-tab');
  const panels = document.querySelectorAll('.panel');

  tabs.forEach(tab => {
    tab.addEventListener('click', () => {
      // 기존 선택 해제
      tabs.forEach(t => t.setAttribute('aria-selected', 'false'));
      panels.forEach(p => p.classList.remove('active'));

      // 현재 탭 활성화
      tab.setAttribute('aria-selected', 'true');
      document.getElementById(tab.dataset.target).classList.add('active');
      
      // 화면 스크롤 이동
      document.querySelector('main').scrollIntoView({behavior:'smooth', block:'start'});
    });
  });
</script>

</body>
</html>
