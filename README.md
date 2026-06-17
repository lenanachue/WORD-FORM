# WORD-FORM
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Word Forms – Cấu Tạo Từ | English Grammar</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Merriweather:wght@400;700&display=swap');

  :root {
    --ocean-deep:    #0a2342;
    --ocean-mid:     #1a4a7a;
    --ocean-light:   #2176ae;
    --wave:          #48a9e4;
    --foam:          #b4dff5;
    --seafoam:       #d6f0fb;
    --sand:          #f0f8ff;
    --coral:         #ff7f6b;
    --seagrass:      #2ec4b6;
    --gold:          #f4c542;
    --white:         #ffffff;
    --text-dark:     #0d2137;
    --text-mid:      #2a4a6b;
    --border:        #cce7f5;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Nunito', sans-serif;
    background: var(--sand);
    color: var(--text-dark);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ─── OCEAN HEADER ─── */
  .hero {
    position: relative;
    background: linear-gradient(160deg, var(--ocean-deep) 0%, var(--ocean-mid) 50%, var(--ocean-light) 100%);
    padding: 56px 24px 100px;
    text-align: center;
    overflow: hidden;
  }
  .hero::after {
    content: '';
    position: absolute;
    bottom: -2px; left: 0; right: 0;
    height: 60px;
    background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 60'%3E%3Cpath fill='%23f0f8ff' d='M0,40 C360,0 720,60 1080,20 C1260,0 1380,30 1440,20 L1440,60 L0,60 Z'/%3E%3C/svg%3E") center/cover no-repeat;
  }
  .bubbles { position: absolute; inset: 0; pointer-events: none; }
  .bubble {
    position: absolute; border-radius: 50%;
    background: rgba(255,255,255,.12);
    animation: rise 8s infinite ease-in;
  }
  .bubble:nth-child(1)  { width:18px; height:18px; left:8%;  animation-delay:0s;   animation-duration:7s; }
  .bubble:nth-child(2)  { width:10px; height:10px; left:18%; animation-delay:1.5s; animation-duration:9s; }
  .bubble:nth-child(3)  { width:24px; height:24px; left:32%; animation-delay:0.8s; animation-duration:8s; }
  .bubble:nth-child(4)  { width:14px; height:14px; left:55%; animation-delay:2.2s; animation-duration:6s; }
  .bubble:nth-child(5)  { width:20px; height:20px; left:72%; animation-delay:0.3s; animation-duration:10s;}
  .bubble:nth-child(6)  { width:8px;  height:8px;  left:88%; animation-delay:3s;   animation-duration:7s; }
  .bubble:nth-child(7)  { width:16px; height:16px; left:45%; animation-delay:4s;   animation-duration:8s; }
  .bubble:nth-child(8)  { width:12px; height:12px; left:65%; animation-delay:1s;   animation-duration:9s; }
  @keyframes rise {
    0%   { transform: translateY(0) scale(1); opacity:.6; }
    100% { transform: translateY(-300px) scale(1.3); opacity:0; }
  }

  .fish { font-size: 2.2rem; position: absolute; animation: swim 18s linear infinite; }
  .fish:nth-child(1) { top: 35%; animation-delay: 0s; }
  .fish:nth-child(2) { top: 60%; animation-delay: 7s; font-size: 1.6rem; }
  @keyframes swim {
    0%   { left: -80px; transform: scaleX(1); }
    49%  { left: 110%; transform: scaleX(1); }
    50%  { left: 110%; transform: scaleX(-1); }
    100% { left: -80px; transform: scaleX(-1); }
  }

  .hero-badge {
    display: inline-block;
    background: rgba(255,255,255,.15);
    color: var(--foam);
    font-size: .78rem; font-weight:700; letter-spacing:.12em; text-transform:uppercase;
    padding: 4px 14px; border-radius:20px; margin-bottom:18px;
    border: 1px solid rgba(255,255,255,.25);
  }
  .hero h1 {
    font-family: 'Merriweather', serif;
    font-size: clamp(2rem, 5vw, 3.2rem);
    color: var(--white); line-height: 1.2; font-weight:700;
    text-shadow: 0 2px 12px rgba(0,0,0,.3);
    margin-bottom: 14px;
  }
  .hero h1 span { color: var(--gold); }
  .hero p {
    color: var(--foam); font-size: 1.05rem; max-width: 560px; margin: 0 auto 28px;
    line-height: 1.7;
  }
  .hero-icons { font-size: 2.8rem; letter-spacing: 8px; }

  /* ─── NAV PILLS ─── */
  .nav-wrap { background: var(--white); border-bottom: 2px solid var(--border); position: sticky; top:0; z-index:99; }
  .nav-pills {
    display: flex; gap:4px; overflow-x:auto; padding: 10px 20px;
    max-width: 1100px; margin: 0 auto; scrollbar-width: none;
  }
  .nav-pills::-webkit-scrollbar { display:none; }
  .nav-pill {
    flex-shrink: 0; padding: 6px 16px;
    border-radius: 20px; font-size: .85rem; font-weight:700;
    cursor: pointer; border: 2px solid var(--border);
    background: var(--sand); color: var(--text-mid);
    transition: all .2s;
    text-decoration: none; display: inline-block;
  }
  .nav-pill:hover, .nav-pill.active {
    background: var(--ocean-mid); color: var(--white); border-color: var(--ocean-mid);
  }

  /* ─── LAYOUT ─── */
  .main { max-width: 1000px; margin: 0 auto; padding: 40px 20px 80px; }

  /* ─── SECTION HEADINGS ─── */
  .section-title {
    display: flex; align-items: center; gap: 12px;
    font-size: 1.5rem; font-weight:900; color: var(--ocean-deep);
    margin: 48px 0 24px; padding-bottom: 10px;
    border-bottom: 3px solid var(--wave);
  }
  .section-title .icon { font-size: 1.8rem; }

  .subsection-title {
    font-size: 1.15rem; font-weight:800; color: var(--ocean-mid);
    margin: 32px 0 14px; padding-left: 14px;
    border-left: 4px solid var(--seagrass);
  }

  /* ─── THEORY CARD ─── */
  .theory-card {
    background: var(--white); border-radius: 16px;
    border: 1.5px solid var(--border);
    box-shadow: 0 4px 20px rgba(33,118,174,.07);
    padding: 28px 28px 24px; margin-bottom: 24px;
    transition: box-shadow .2s;
  }
  .theory-card:hover { box-shadow: 0 8px 32px rgba(33,118,174,.13); }

  /* ─── SUFFIX TABLE ─── */
  .suffix-table {
    width: 100%; border-collapse: collapse; margin-top: 8px;
    font-size: .93rem;
  }
  .suffix-table th {
    background: linear-gradient(90deg, var(--ocean-mid), var(--ocean-light));
    color: var(--white); padding: 10px 14px; text-align: left;
    font-weight:700;
  }
  .suffix-table th:first-child { border-radius: 8px 0 0 0; }
  .suffix-table th:last-child  { border-radius: 0 8px 0 0; }
  .suffix-table td {
    padding: 9px 14px; border-bottom: 1px solid var(--border);
    vertical-align: top; line-height: 1.6;
  }
  .suffix-table tr:nth-child(even) td { background: var(--seafoam); }
  .suffix-table tr:last-child td:first-child { border-radius: 0 0 0 8px; }
  .suffix-table tr:last-child td:last-child  { border-radius: 0 0 8px 0; }
  .suffix-badge {
    display: inline-block; background: var(--ocean-light); color: var(--white);
    font-size: .82rem; font-weight:800; padding: 2px 10px; border-radius: 12px;
    font-family: monospace; letter-spacing:.03em;
  }
  .pos-badge {
    display: inline-block; font-size: .75rem; font-weight:700;
    padding: 2px 8px; border-radius: 10px; margin: 2px;
  }
  .pos-n  { background:#dbeafe; color:#1d4ed8; }
  .pos-v  { background:#dcfce7; color:#166534; }
  .pos-a  { background:#fef3c7; color:#92400e; }
  .pos-adv{ background:#fce7f3; color:#9d174d; }

  /* ─── EXAMPLE BOX ─── */
  .example-box {
    background: linear-gradient(135deg, var(--seafoam), #e8f6ff);
    border-left: 4px solid var(--wave);
    border-radius: 0 10px 10px 0;
    padding: 12px 16px; margin: 4px 0;
    font-size: .9rem; color: var(--text-mid);
    line-height: 1.7;
  }
  .ex-word { font-weight:800; color: var(--ocean-deep); }
  .ex-arrow { color: var(--wave); font-weight:900; margin: 0 4px; }

  /* ─── RULE GRID ─── */
  .rule-grid {
    display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 14px; margin-top: 8px;
  }
  .rule-item {
    background: var(--white); border: 1.5px solid var(--border);
    border-radius: 12px; padding: 14px 16px;
    transition: transform .15s, box-shadow .15s;
  }
  .rule-item:hover { transform: translateY(-2px); box-shadow: 0 6px 18px rgba(33,118,174,.12); }
  .rule-formula {
    font-size: .88rem; font-weight:800; color: var(--ocean-mid);
    font-family: monospace; margin-bottom: 6px;
    background: var(--seafoam); padding: 4px 10px; border-radius:6px;
    display: inline-block;
  }
  .rule-example { font-size: .85rem; color: var(--text-mid); line-height:1.6; }

  /* ─── QUICK QUIZ ─── */
  .quiz-box {
    background: linear-gradient(135deg, #fff9e6, #fffde0);
    border: 2px solid var(--gold);
    border-radius: 16px; padding: 24px 28px; margin: 28px 0;
  }
  .quiz-title {
    font-size: 1rem; font-weight:900; color: #7c5800;
    margin-bottom: 16px; display: flex; align-items:center; gap:8px;
  }
  .quiz-question { margin-bottom: 14px; }
  .quiz-question p { font-size: .95rem; font-weight:700; color: var(--text-dark); margin-bottom:8px; }
  .quiz-options { display: flex; flex-wrap: wrap; gap: 8px; }
  .quiz-opt {
    padding: 7px 18px; border-radius: 20px; border: 2px solid var(--border);
    background: var(--white); font-size: .88rem; font-weight:700;
    cursor: pointer; color: var(--text-mid); transition: all .18s;
  }
  .quiz-opt:hover   { border-color: var(--ocean-light); color: var(--ocean-light); }
  .quiz-opt.correct { background: #d1fae5; border-color: #059669; color: #065f46; }
  .quiz-opt.wrong   { background: #fee2e2; border-color: #dc2626; color: #991b1b; }
  .quiz-opt:disabled { cursor: default; }
  .feedback {
    font-size: .88rem; font-weight:700; margin-top:8px;
    padding: 6px 12px; border-radius:8px; display:none;
  }
  .feedback.show { display: block; }
  .feedback.ok  { background:#d1fae5; color:#065f46; }
  .feedback.err { background:#fee2e2; color:#991b1b; }

  /* ─── SUMMARY DIAGRAM ─── */
  .diagram-wrap {
    background: var(--white); border-radius: 20px;
    border: 2px solid var(--border);
    padding: 32px 20px; margin: 16px 0 32px;
    box-shadow: 0 4px 24px rgba(33,118,174,.08);
    overflow-x: auto;
  }
  .diagram-center {
    text-align: center; margin-bottom: 28px;
  }
  .diagram-center .core-word {
    display: inline-block;
    background: linear-gradient(135deg, var(--ocean-deep), var(--ocean-light));
    color: var(--white); font-size: 1.3rem; font-weight:900;
    padding: 16px 36px; border-radius: 50px;
    box-shadow: 0 4px 16px rgba(10,35,66,.25);
    letter-spacing:.05em;
  }
  .diagram-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 16px;
  }
  .diagram-card {
    border-radius: 14px; padding: 18px 16px;
    text-align: center;
  }
  .diagram-card.noun   { background: linear-gradient(135deg,#dbeafe,#bfdbfe); border: 2px solid #93c5fd; }
  .diagram-card.verb   { background: linear-gradient(135deg,#dcfce7,#bbf7d0); border: 2px solid #86efac; }
  .diagram-card.adj    { background: linear-gradient(135deg,#fef3c7,#fde68a); border: 2px solid #fcd34d; }
  .diagram-card.adv    { background: linear-gradient(135deg,#fce7f3,#fbcfe8); border: 2px solid #f9a8d4; }
  .diagram-card-label {
    font-size: .75rem; font-weight:900; letter-spacing:.12em; text-transform:uppercase;
    margin-bottom: 10px; opacity:.75;
  }
  .diagram-card.noun .diagram-card-label { color:#1d4ed8; }
  .diagram-card.verb .diagram-card-label { color:#166534; }
  .diagram-card.adj  .diagram-card-label { color:#92400e; }
  .diagram-card.adv  .diagram-card-label { color:#9d174d; }
  .suffix-pill {
    display: inline-block; font-size: .82rem; font-weight:800;
    font-family: monospace; padding: 4px 12px; border-radius: 14px; margin: 3px;
  }
  .diagram-card.noun .suffix-pill { background:#1d4ed8; color:#fff; }
  .diagram-card.verb .suffix-pill { background:#166534; color:#fff; }
  .diagram-card.adj  .suffix-pill { background:#92400e; color:#fff; }
  .diagram-card.adv  .suffix-pill { background:#9d174d; color:#fff; }

  /* ─── CONTEXT RULE TABLE ─── */
  .context-table { width:100%; border-collapse:collapse; font-size:.9rem; }
  .context-table th {
    background: var(--seagrass); color:#fff; padding:10px 14px; text-align:left;
    font-weight:800;
  }
  .context-table td { padding:9px 14px; border-bottom:1px solid var(--border); line-height:1.6; }
  .context-table tr:nth-child(even) td { background: #f0fdf4; }
  .context-table .ctx-clue {
    font-weight:800; color: var(--seagrass); font-family:monospace;
  }
  .ctx-pos { font-weight:700; color: var(--ocean-mid); }

  /* ─── NOTE BOX ─── */
  .note-box {
    background: linear-gradient(135deg,#e0f2fe,#f0f9ff);
    border-left: 4px solid var(--wave); border-radius:0 12px 12px 0;
    padding: 16px 18px; margin: 18px 0;
    font-size: .92rem; color: var(--text-mid); line-height:1.8;
  }
  .note-box strong { color: var(--ocean-deep); }

  /* ─── EXERCISE SECTION ─── */
  .exercise-header {
    background: linear-gradient(135deg, var(--ocean-mid), var(--ocean-light));
    color: var(--white); border-radius: 14px 14px 0 0;
    padding: 18px 24px; display:flex; align-items:center; gap:10px;
  }
  .exercise-header h3 { font-size: 1.1rem; font-weight:900; }
  .exercise-body { background: var(--white); border: 1.5px solid var(--border); border-top:none; border-radius:0 0 14px 14px; padding: 24px; margin-bottom:28px; }

  .ex-question {
    display: flex; gap: 12px; margin-bottom: 20px;
    align-items: flex-start;
  }
  .ex-num {
    min-width: 32px; height: 32px; border-radius: 50%;
    background: var(--ocean-light); color: var(--white);
    display: flex; align-items:center; justify-content:center;
    font-size: .85rem; font-weight:900; flex-shrink:0; margin-top:2px;
  }
  .ex-content { flex:1; }
  .ex-sentence { font-size: .95rem; color: var(--text-dark); font-weight:600; margin-bottom: 8px; line-height:1.6; }
  .ex-options { display:flex; flex-wrap:wrap; gap:8px; }
  .ex-opt {
    padding: 6px 16px; border-radius: 18px;
    border: 2px solid var(--border); background: var(--white);
    font-size: .88rem; font-weight:700; cursor: pointer;
    color: var(--text-mid); transition: all .18s;
  }
  .ex-opt:hover   { border-color: var(--ocean-light); color: var(--ocean-light); }
  .ex-opt.correct { background:#d1fae5; border-color:#059669; color:#065f46; pointer-events:none; }
  .ex-opt.wrong   { background:#fee2e2; border-color:#dc2626; color:#991b1b; }
  .ex-opt:disabled { cursor:default; }
  .ex-feedback {
    font-size: .83rem; margin-top: 6px; display:none;
    padding: 5px 10px; border-radius:8px; font-weight:700; line-height:1.5;
  }
  .ex-feedback.show { display:block; }
  .ex-feedback.ok  { background:#d1fae5; color:#065f46; }
  .ex-feedback.err { background:#fee2e2; color:#991b1b; }

  /* Score */
  .score-bar {
    background: var(--seafoam); border:1.5px solid var(--border);
    border-radius:12px; padding:16px 20px; margin-top: 8px;
    display:flex; align-items:center; gap:14px;
  }
  .score-num { font-size: 1.6rem; font-weight:900; color: var(--ocean-deep); }
  .score-label { font-size: .85rem; color: var(--text-mid); font-weight:700; }
  .score-msg { font-size: .88rem; color: var(--text-mid); }

  /* Check button */
  .check-btn {
    background: linear-gradient(135deg, var(--ocean-mid), var(--ocean-light));
    color: var(--white); border: none; border-radius: 24px;
    padding: 11px 28px; font-size: .95rem; font-weight:800;
    cursor: pointer; transition: all .2s; margin-top: 8px;
    display:inline-flex; align-items:center; gap:8px;
    box-shadow: 0 4px 14px rgba(33,118,174,.3);
  }
  .check-btn:hover { transform: translateY(-2px); box-shadow: 0 6px 20px rgba(33,118,174,.4); }

  /* ─── FOOTER ─── */
  .footer {
    background: var(--ocean-deep); color: var(--foam);
    text-align:center; padding: 32px 20px;
    font-size: .88rem;
  }
  .footer-fish { font-size: 2rem; margin-bottom: 8px; }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 600px) {
    .rule-grid { grid-template-columns: 1fr; }
    .diagram-grid { grid-template-columns: 1fr 1fr; }
    .theory-card { padding: 18px 14px; }
    .exercise-body { padding: 14px; }
  }
</style>
</head>
<body>

<!-- ═══ HERO ═══ -->
<header class="hero">
  <div class="bubbles">
    <div class="bubble"></div><div class="bubble"></div><div class="bubble"></div>
    <div class="bubble"></div><div class="bubble"></div><div class="bubble"></div>
    <div class="bubble"></div><div class="bubble"></div>
    <div class="fish">🐠</div><div class="fish">🐟</div>
  </div>
  <div style="position:relative;z-index:2">
    <div class="hero-badge">🌊 English Grammar – Chuyên Đề 14</div>
    <h1>Cấu Tạo Từ<br><span>Word Forms</span></h1>
    <p>Khám phá cách tiếng Anh tạo ra hàng nghìn từ vựng chỉ từ một gốc từ đơn giản – như đại dương rộng lớn từ một giọt nước.</p>
    <div class="hero-icons">🐙 🦀 🐚 🐋 🦑</div>
  </div>
</header>

<!-- ═══ NAV ═══ -->
<nav class="nav-wrap">
  <div class="nav-pills">
    <a class="nav-pill" href="#ly-thuyet">📘 Lý Thuyết</a>
    <a class="nav-pill" href="#danh-tu">Danh Từ</a>
    <a class="nav-pill" href="#dong-tu">Động Từ</a>
    <a class="nav-pill" href="#tinh-tu">Tính Từ</a>
    <a class="nav-pill" href="#trang-tu">Trạng Từ</a>
    <a class="nav-pill" href="#trat-tu-tu">Trật Tự Từ</a>
    <a class="nav-pill" href="#so-do">📊 Sơ Đồ</a>
    <a class="nav-pill" href="#bai-tap">✏️ Bài Tập</a>
  </div>
</nav>

<!-- ═══ MAIN ═══ -->
<main class="main">

  <!-- ════ PHẦN LÝ THUYẾT ════ -->
  <section id="ly-thuyet">
    <div class="section-title"><span class="icon">📘</span> A. Cách Cấu Tạo Từ</div>

    <div class="note-box">
      <strong>💡 Tại sao phải học Word Forms?</strong><br>
      Tiếng Anh sử dụng <strong>hậu tố (suffix)</strong> và <strong>tiền tố (prefix)</strong> để biến đổi một từ gốc thành nhiều từ loại khác nhau.
      Ví dụ: <strong>beauty</strong> (n) → <strong>beautiful</strong> (adj) → <strong>beautify</strong> (v) → <strong>beautifully</strong> (adv).
      Nắm vững các quy tắc này giúp em nhận ra và sử dụng từ chính xác hơn.
    </div>

    <!-- ════ I. DANH TỪ ════ -->
    <div id="danh-tu" class="subsection-title">I. Cách Cấu Tạo Danh Từ (Noun) 🪸</div>

    <div class="theory-card">
      <p style="font-size:.92rem;color:var(--text-mid);margin-bottom:14px;">
        Danh từ thường được tạo thành bằng cách thêm hậu tố vào sau <strong>động từ</strong> hoặc <strong>tính từ</strong>.
        Dưới đây là những hậu tố danh từ phổ biến nhất:
      </p>

      <div class="subsection-title" style="margin-top:0;font-size:1rem;">Từ động từ → danh từ</div>
      <div class="rule-grid">
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:var(--coral)">-ment</span> → N</div>
          <div class="rule-example">
            develop <span class="ex-arrow">→</span> <strong>develop<span style="color:var(--coral)">ment</span></strong><br>
            entertain <span class="ex-arrow">→</span> <strong>entertain<span style="color:var(--coral)">ment</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:var(--coral)">-ance/-ence</span> → N</div>
          <div class="rule-example">
            attend <span class="ex-arrow">→</span> <strong>attend<span style="color:var(--coral)">ance</span></strong><br>
            depend <span class="ex-arrow">→</span> <strong>depend<span style="color:var(--coral)">ence</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:var(--coral)">-ion/-ation</span> → N</div>
          <div class="rule-example">
            invent <span class="ex-arrow">→</span> <strong>invent<span style="color:var(--coral)">ion</span></strong><br>
            inform <span class="ex-arrow">→</span> <strong>inform<span style="color:var(--coral)">ation</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:var(--coral)">-al</span> → N</div>
          <div class="rule-example">
            survive <span class="ex-arrow">→</span> <strong>surviv<span style="color:var(--coral)">al</span></strong><br>
            arrive <span class="ex-arrow">→</span> <strong>arriv<span style="color:var(--coral)">al</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:var(--coral)">-ing</span> → N</div>
          <div class="rule-example">
            teach <span class="ex-arrow">→</span> <strong>teach<span style="color:var(--coral)">ing</span></strong><br>
            train <span class="ex-arrow">→</span> <strong>train<span style="color:var(--coral)">ing</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:var(--coral)">-er/-or/-ar</span> → N <span style="font-size:.75rem;opacity:.7">(người làm)</span></div>
          <div class="rule-example">
            work <span class="ex-arrow">→</span> <strong>work<span style="color:var(--coral)">er</span></strong><br>
            act <span class="ex-arrow">→</span> <strong>act<span style="color:var(--coral)">or</span></strong> &nbsp;|&nbsp;
            lie <span class="ex-arrow">→</span> <strong>li<span style="color:var(--coral)">ar</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:var(--coral)">-ant/-ee/-ist</span> → N</div>
          <div class="rule-example">
            assist <span class="ex-arrow">→</span> <strong>assist<span style="color:var(--coral)">ant</span></strong><br>
            employ <span class="ex-arrow">→</span> <strong>employ<span style="color:var(--coral)">ee</span></strong><br>
            type <span class="ex-arrow">→</span> <strong>typ<span style="color:var(--coral)">ist</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:var(--coral)">-age</span> → N</div>
          <div class="rule-example">
            marry <span class="ex-arrow">→</span> <strong>marri<span style="color:var(--coral)">age</span></strong><br>
            carry <span class="ex-arrow">→</span> <strong>carri<span style="color:var(--coral)">age</span></strong>
          </div>
        </div>
      </div>

      <div class="subsection-title" style="font-size:1rem;margin-top:22px;">Từ tính từ → danh từ</div>
      <div class="rule-grid">
        <div class="rule-item">
          <div class="rule-formula">Adj + <span style="color:var(--coral)">-ness</span> → N</div>
          <div class="rule-example">
            rich <span class="ex-arrow">→</span> <strong>rich<span style="color:var(--coral)">ness</span></strong><br>
            polite <span class="ex-arrow">→</span> <strong>polite<span style="color:var(--coral)">ness</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">Adj + <span style="color:var(--coral)">-ity/-ty/-cy</span> → N</div>
          <div class="rule-example">
            able <span class="ex-arrow">→</span> <strong>abil<span style="color:var(--coral)">ity</span></strong><br>
            certain <span class="ex-arrow">→</span> <strong>certain<span style="color:var(--coral)">ty</span></strong><br>
            proficient <span class="ex-arrow">→</span> <strong>proficien<span style="color:var(--coral)">cy</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">Adj + <span style="color:var(--coral)">-th/-dom</span> → N</div>
          <div class="rule-example">
            warm <span class="ex-arrow">→</span> <strong>warm<span style="color:var(--coral)">th</span></strong><br>
            free <span class="ex-arrow">→</span> <strong>free<span style="color:var(--coral)">dom</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:var(--coral)">-hood/-ship</span> → N</div>
          <div class="rule-example">
            child <span class="ex-arrow">→</span> <strong>child<span style="color:var(--coral)">hood</span></strong><br>
            friend <span class="ex-arrow">→</span> <strong>friend<span style="color:var(--coral)">ship</span></strong>
          </div>
        </div>
      </div>
    </div>

    <!-- MINI QUIZ 1 -->
    <div class="quiz-box">
      <div class="quiz-title">🎯 Ôn Tập Nhanh – Danh Từ</div>

      <div class="quiz-question" id="q1">
        <p>1. Từ "develop" (v), ta thêm hậu tố nào để tạo danh từ?</p>
        <div class="quiz-options">
          <button class="quiz-opt" onclick="checkQuiz(this,'q1',true,'-ment → development')">-ment</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q1',false)">-ness</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q1',false)">-ive</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q1',false)">-al</button>
        </div>
        <div class="feedback" id="fb-q1"></div>
      </div>

      <div class="quiz-question" id="q2">
        <p>2. "rich" (adj) → ______ (n) : điền hậu tố phù hợp</p>
        <div class="quiz-options">
          <button class="quiz-opt" onclick="checkQuiz(this,'q2',false)">-ity</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q2',true,'-ness → richness')">-ness</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q2',false)">-ance</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q2',false)">-hood</button>
        </div>
        <div class="feedback" id="fb-q2"></div>
      </div>

      <div class="quiz-question" id="q3">
        <p>3. Từ nào là danh từ chỉ NGƯỜI trong nhóm sau?</p>
        <div class="quiz-options">
          <button class="quiz-opt" onclick="checkQuiz(this,'q3',false)">arrival</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q3',false)">invention</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q3',true,'Từ đuôi -er/-or/-ist/-ant/-ee chỉ người: employer, actor, typist...')">employer</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q3',false)">freedom</button>
        </div>
        <div class="feedback" id="fb-q3"></div>
      </div>
    </div>

    <!-- ════ II. ĐỘNG TỪ ════ -->
    <div id="dong-tu" class="subsection-title">II. Cách Cấu Tạo Động Từ (Verb) 🐙</div>

    <div class="theory-card">
      <div class="rule-grid">
        <div class="rule-item">
          <div class="rule-formula">Adj + <span style="color:#059669">-en</span> → V</div>
          <div class="rule-example">
            wide <span class="ex-arrow">→</span> <strong>wid<span style="color:#059669">en</span></strong> (mở rộng)<br>
            short <span class="ex-arrow">→</span> <strong>short<span style="color:#059669">en</span></strong> (thu ngắn)
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula"><span style="color:#059669">en-</span> + Adj → V</div>
          <div class="rule-example">
            <span style="color:#059669">en</span>rich (làm giàu)<br>
            <span style="color:#059669">en</span>large (phóng to)
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N/Adj + <span style="color:#059669">-ise/-ize</span> → V</div>
          <div class="rule-example">
            social <span class="ex-arrow">→</span> social<span style="color:#059669">ize</span><br>
            industrial <span class="ex-arrow">→</span> industrial<span style="color:#059669">ize</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#059669">-fy</span> → V</div>
          <div class="rule-example">
            beauty <span class="ex-arrow">→</span> beauti<span style="color:#059669">fy</span> (làm đẹp)<br>
            public <span class="ex-arrow">→</span> publi<span style="color:#059669">cize</span>
          </div>
        </div>
      </div>
    </div>

    <!-- MINI QUIZ 2 -->
    <div class="quiz-box">
      <div class="quiz-title">🎯 Ôn Tập Nhanh – Động Từ</div>
      <div class="quiz-question" id="q4">
        <p>1. "beauty" (n) → ______ (v): làm đẹp</p>
        <div class="quiz-options">
          <button class="quiz-opt" onclick="checkQuiz(this,'q4',false)">beautiness</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q4',true,'beauty + fy → beautify (làm đẹp)')">beautify</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q4',false)">beauten</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q4',false)">beautize</button>
        </div>
        <div class="feedback" id="fb-q4"></div>
      </div>
      <div class="quiz-question" id="q5">
        <p>2. Muốn làm giàu cho ai → "en + ____"</p>
        <div class="quiz-options">
          <button class="quiz-opt" onclick="checkQuiz(this,'q5',false)">enness</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q5',false)">ension</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q5',true,'en + rich = enrich (làm giàu)')">enrich</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q5',false)">enrichment</button>
        </div>
        <div class="feedback" id="fb-q5"></div>
      </div>
    </div>

    <!-- ════ III. TÍNH TỪ ════ -->
    <div id="tinh-tu" class="subsection-title">III. Cách Cấu Tạo Tính Từ (Adjective) 🦀</div>

    <div class="theory-card">
      <div class="rule-grid">
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#92400e">-ful</span> → Adj</div>
          <div class="rule-example">
            care <span class="ex-arrow">→</span> care<span style="color:#92400e">ful</span> (cẩn thận)<br>
            success <span class="ex-arrow">→</span> success<span style="color:#92400e">ful</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#92400e">-less</span> → Adj</div>
          <div class="rule-example">
            hope <span class="ex-arrow">→</span> hope<span style="color:#92400e">less</span> (vô vọng)<br>
            home <span class="ex-arrow">→</span> home<span style="color:#92400e">less</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#92400e">-ous</span> → Adj</div>
          <div class="rule-example">
            danger <span class="ex-arrow">→</span> danger<span style="color:#92400e">ous</span><br>
            industry <span class="ex-arrow">→</span> industri<span style="color:#92400e">ous</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#92400e">-al</span> → Adj</div>
          <div class="rule-example">
            nation <span class="ex-arrow">→</span> nation<span style="color:#92400e">al</span><br>
            nature <span class="ex-arrow">→</span> natur<span style="color:#92400e">al</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#92400e">-able/-ible</span> → Adj</div>
          <div class="rule-example">
            reason <span class="ex-arrow">→</span> reason<span style="color:#92400e">able</span><br>
            response <span class="ex-arrow">→</span> respons<span style="color:#92400e">ible</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#92400e">-y</span> → Adj</div>
          <div class="rule-example">
            rain <span class="ex-arrow">→</span> rain<span style="color:#92400e">y</span><br>
            sun <span class="ex-arrow">→</span> sun<span style="color:#92400e">ny</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#92400e">-ic</span> → Adj</div>
          <div class="rule-example">
            economy <span class="ex-arrow">→</span> econom<span style="color:#92400e">ic</span><br>
            history <span class="ex-arrow">→</span> histor<span style="color:#92400e">ic</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:#92400e">-ing/-ed</span> → Adj</div>
          <div class="rule-example">
            interest <span class="ex-arrow">→</span> interest<span style="color:#92400e">ing</span> / interest<span style="color:#92400e">ed</span><br>
            bore <span class="ex-arrow">→</span> bor<span style="color:#92400e">ing</span> / bor<span style="color:#92400e">ed</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span style="color:#92400e">-ive</span> → Adj</div>
          <div class="rule-example">
            impress <span class="ex-arrow">→</span> impress<span style="color:#92400e">ive</span><br>
            invent <span class="ex-arrow">→</span> invent<span style="color:#92400e">ive</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span style="color:#92400e">-ish/-like/-some</span></div>
          <div class="rule-example">
            fool <span class="ex-arrow">→</span> fool<span style="color:#92400e">ish</span> (ngốc)<br>
            child <span class="ex-arrow">→</span> child<span style="color:#92400e">like</span><br>
            hand <span class="ex-arrow">→</span> hand<span style="color:#92400e">some</span>
          </div>
        </div>
      </div>

      <div class="note-box" style="margin-top:18px;">
        <strong>⚠️ Lưu ý quan trọng:</strong> -ing và -ed đều có thể là tính từ nhưng nghĩa khác nhau!<br>
        • <strong>-ing</strong>: mô tả bản chất của sự vật/sự việc → The book is <strong>interesting</strong>. (cuốn sách tẻ nhạt)<br>
        • <strong>-ed</strong>: mô tả cảm xúc của người → I am <strong>interested</strong> in this book. (tôi thích)<br>
        → Tương tự: boring/bored, disappointing/disappointed, exciting/excited...
      </div>
    </div>

    <!-- MINI QUIZ 3 -->
    <div class="quiz-box">
      <div class="quiz-title">🎯 Ôn Tập Nhanh – Tính Từ</div>
      <div class="quiz-question" id="q6">
        <p>1. "The movie was very ____. I fell asleep." (tẻ nhạt – tính chất của phim)</p>
        <div class="quiz-options">
          <button class="quiz-opt" onclick="checkQuiz(this,'q6',true,'-ing mô tả bản chất của sự vật: boring')">boring</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q6',false)">bored</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q6',false)">boreness</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q6',false)">boredom</button>
        </div>
        <div class="feedback" id="fb-q6"></div>
      </div>
      <div class="quiz-question" id="q7">
        <p>2. "danger" (n) → ______ (adj)</p>
        <div class="quiz-options">
          <button class="quiz-opt" onclick="checkQuiz(this,'q7',false)">dangerful</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q7',false)">dangerly</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q7',true,'danger + ous → dangerous')">dangerous</button>
          <button class="quiz-opt" onclick="checkQuiz(this,'q7',false)">dangeral</button>
        </div>
        <div class="feedback" id="fb-q7"></div>
      </div>
    </div>

    <!-- ════ IV. TRẠNG TỪ ════ -->
    <div id="trang-tu" class="subsection-title">IV. Cách Cấu Tạo Trạng Từ (Adverb) 🐚</div>

    <div class="theory-card">
      <div class="rule-item" style="max-width:360px;margin-bottom:16px;">
        <div class="rule-formula">Adj + <span style="color:#9d174d">-ly</span> → Adv</div>
        <div class="rule-example">
          slow <span class="ex-arrow">→</span> slow<span style="color:#9d174d">ly</span><br>
          rapid <span class="ex-arrow">→</span> rapid<span style="color:#9d174d">ly</span><br>
          careful <span class="ex-arrow">→</span> careful<span style="color:#9d174d">ly</span>
        </div>
      </div>

      <div class="note-box">
        <strong>⚠️ Những ngoại lệ quan trọng phải nhớ:</strong><br>
        🔹 <strong>fast</strong>: vừa là tính từ, vừa là trạng từ → KHÔNG có "fastly"<br>
        🔹 <strong>hard</strong> (adj/adv = chăm chỉ) ≠ <strong>hardly</strong> (adv = hầu như không)<br>
        🔹 <strong>good</strong> (adj) → trạng từ là <strong>well</strong> → KHÔNG có "goodly"<br>
        🔹 <strong>-ly</strong> có thể là tính từ: <em>friend<strong>ly</strong></em> (adj), <em>like<strong>ly</strong></em> (adj)
      </div>
    </div>

    <!-- ════ V. TRẬT TỰ TỪ ════ -->
    <div id="trat-tu-tu" class="section-title" style="margin-top:48px;"><span class="icon">🧭</span> B. Trật Tự Từ – Nhận Biết Từ Loại</div>

    <div class="theory-card">
      <p style="font-size:.92rem;color:var(--text-mid);margin-bottom:14px;">
        Muốn điền đúng từ loại, hãy nhìn vào <strong>từ xung quanh vị trí trống</strong> để xác định cần Danh từ, Động từ, Tính từ hay Trạng từ.
      </p>
      <table class="context-table">
        <thead>
          <tr><th>Dấu hiệu nhận biết</th><th>Từ loại cần điền</th><th>Ví dụ minh hoạ</th></tr>
        </thead>
        <tbody>
          <tr>
            <td><span class="ctx-clue">to be (am/is/are/was/were) + ___</span></td>
            <td><span class="ctx-pos">Tính từ (Adj)</span></td>
            <td>The book is so <strong>interesting</strong>.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">Động từ thường + ___</span></td>
            <td><span class="ctx-pos">Trạng từ (Adv)</span></td>
            <td>He runs <strong>quickly</strong>.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">a/an/the + ___</span> (mạo từ)</td>
            <td><span class="ctx-pos">Danh từ (N)</span></td>
            <td>The <strong>development</strong> of industry…</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">my/your/his/her/our/their + ___</span></td>
            <td><span class="ctx-pos">Danh từ (N)</span></td>
            <td>He failed because of his <strong>laziness</strong>.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">___ + danh từ (trước danh từ)</span></td>
            <td><span class="ctx-pos">Tính từ (Adj)</span></td>
            <td>Copperheads are <strong>poisonous</strong> snakes.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">Trước tính từ</span></td>
            <td><span class="ctx-pos">Trạng từ (Adv)</span></td>
            <td>The matter is <strong>comparatively</strong> complicated.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">Sau giới từ (of/in/on/at/with...)</span></td>
            <td><span class="ctx-pos">Danh từ (N)</span></td>
            <td>30 years of <strong>marriage</strong>.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">some/any/many/much + ___</span></td>
            <td><span class="ctx-pos">Danh từ (N)</span></td>
            <td>There are many <strong>people</strong> waiting.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">look/seem/get/become/feel + ___</span></td>
            <td><span class="ctx-pos">Tính từ (Adj)</span></td>
            <td>She looks <strong>happier</strong> than yesterday.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">to + ___</span> (sau "to" nguyên thể)</td>
            <td><span class="ctx-pos">Động từ (V nguyên dạng)</span></td>
            <td>We have to <strong>conserve</strong> resources.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">will/can/must/should + ___</span></td>
            <td><span class="ctx-pos">Động từ (V nguyên dạng)</span></td>
            <td>We will <strong>enrich</strong> our vocabulary.</td>
          </tr>
          <tr>
            <td><span class="ctx-clue">___ and/or/but ___ (cân bằng)</span></td>
            <td><span class="ctx-pos">Cùng từ loại với vế kia</span></td>
            <td>She is <strong>confident</strong> and positive.</td>
          </tr>
        </tbody>
      </table>

      <!-- MINI QUIZ trật tự từ -->
      <div class="quiz-box" style="margin-top:20px;">
        <div class="quiz-title">🎯 Ôn Tập – Trật Tự Từ</div>
        <div class="quiz-question" id="q8">
          <p>1. "He failed the exam because of his ______" – ô trống cần từ loại gì?</p>
          <div class="quiz-options">
            <button class="quiz-opt" onclick="checkQuiz(this,'q8',true,'Sau tính từ sở hữu his → cần DANH TỪ: laziness')">Danh từ (N)</button>
            <button class="quiz-opt" onclick="checkQuiz(this,'q8',false)">Tính từ (Adj)</button>
            <button class="quiz-opt" onclick="checkQuiz(this,'q8',false)">Trạng từ (Adv)</button>
            <button class="quiz-opt" onclick="checkQuiz(this,'q8',false)">Động từ (V)</button>
          </div>
          <div class="feedback" id="fb-q8"></div>
        </div>
        <div class="quiz-question" id="q9">
          <p>2. "The matter is comparatively ______" – ô trống cần từ loại gì?</p>
          <div class="quiz-options">
            <button class="quiz-opt" onclick="checkQuiz(this,'q9',false)">Danh từ (N)</button>
            <button class="quiz-opt" onclick="checkQuiz(this,'q9',true,'Sau to be và trạng từ comparatively → cần TÍNH TỪ')">Tính từ (Adj)</button>
            <button class="quiz-opt" onclick="checkQuiz(this,'q9',false)">Trạng từ (Adv)</button>
            <button class="quiz-opt" onclick="checkQuiz(this,'q9',false)">Động từ (V)</button>
          </div>
          <div class="feedback" id="fb-q9"></div>
        </div>
      </div>
    </div>
  </section>

  <!-- ════ SƠ ĐỒ TỔNG HỢP ════ -->
  <section id="so-do">
    <div class="section-title"><span class="icon">📊</span> Sơ Đồ Tổng Hợp – Dễ Ghi Nhớ</div>

    <div class="diagram-wrap">
      <div class="diagram-center">
        <div style="margin-bottom:10px;font-size:.85rem;color:var(--text-mid);font-weight:700;">TỪ GỐC</div>
        <div class="core-word">ROOT WORD</div>
        <div style="margin-top:18px;font-size:1.5rem;">⬇️⬇️⬇️⬇️</div>
        <div style="font-size:.82rem;color:var(--text-mid);margin-top:6px;font-weight:600;">Thêm hậu tố → tạo ra 4 từ loại</div>
      </div>

      <div class="diagram-grid">
        <!-- NOUN -->
        <div class="diagram-card noun">
          <div class="diagram-card-label">🪸 Danh từ (N)</div>
          <div><span class="suffix-pill">-ment</span><span class="suffix-pill">-ance</span><span class="suffix-pill">-ence</span></div>
          <div><span class="suffix-pill">-ion</span><span class="suffix-pill">-ation</span><span class="suffix-pill">-al</span></div>
          <div><span class="suffix-pill">-ing</span><span class="suffix-pill">-age</span><span class="suffix-pill">-er</span></div>
          <div><span class="suffix-pill">-or</span><span class="suffix-pill">-ant</span><span class="suffix-pill">-ee</span></div>
          <div><span class="suffix-pill">-ist</span><span class="suffix-pill">-ar</span><span class="suffix-pill">-ness</span></div>
          <div><span class="suffix-pill">-ity</span><span class="suffix-pill">-ty</span><span class="suffix-pill">-cy</span></div>
          <div><span class="suffix-pill">-th</span><span class="suffix-pill">-dom</span><span class="suffix-pill">-ism</span></div>
          <div><span class="suffix-pill">-hood</span><span class="suffix-pill">-ship</span></div>
          <div style="margin-top:8px;font-size:.78rem;color:#1d4ed8;font-weight:600;">
            Vị trí: sau a/an/the, my/your/his..., giới từ, some/many/much
          </div>
        </div>

        <!-- VERB -->
        <div class="diagram-card verb">
          <div class="diagram-card-label">🐙 Động từ (V)</div>
          <div><span class="suffix-pill">-en</span><span class="suffix-pill">en-</span></div>
          <div><span class="suffix-pill">-ize/-ise</span><span class="suffix-pill">-fy</span></div>
          <div style="margin-top:8px;font-size:.78rem;color:#166534;font-weight:600;">
            Vị trí: sau to/will/can/must/should<br>
            Ví dụ: widen, enrich, socialize, beautify
          </div>
        </div>

        <!-- ADJ -->
        <div class="diagram-card adj">
          <div class="diagram-card-label">🦀 Tính từ (Adj)</div>
          <div><span class="suffix-pill">-ful</span><span class="suffix-pill">-less</span><span class="suffix-pill">-ous</span></div>
          <div><span class="suffix-pill">-al</span><span class="suffix-pill">-able</span><span class="suffix-pill">-ible</span></div>
          <div><span class="suffix-pill">-ic</span><span class="suffix-pill">-ive</span><span class="suffix-pill">-y</span></div>
          <div><span class="suffix-pill">-ly</span><span class="suffix-pill">-ing</span><span class="suffix-pill">-ed</span></div>
          <div><span class="suffix-pill">-ish</span><span class="suffix-pill">-like</span><span class="suffix-pill">-some</span></div>
          <div><span class="suffix-pill">-ern</span><span class="suffix-pill">-ent</span></div>
          <div style="margin-top:8px;font-size:.78rem;color:#92400e;font-weight:600;">
            Vị trí: sau to be/look/seem/feel, trước danh từ
          </div>
        </div>

        <!-- ADV -->
        <div class="diagram-card adv">
          <div class="diagram-card-label">🐚 Trạng từ (Adv)</div>
          <div><span class="suffix-pill">-ly</span></div>
          <div style="margin-top:8px;font-size:.78rem;color:#9d174d;font-weight:600;">
            Vị trí: sau động từ thường, trước tính từ/trạng từ khác<br><br>
            ⚠️ Ngoại lệ:<br>
            • fast (adj & adv) → không có fastly<br>
            • hard (adj & adv) ≠ hardly<br>
            • good (adj) → well (adv)
          </div>
        </div>
      </div>

      <!-- Context clues summary -->
      <div style="margin-top:28px;padding:20px;background:var(--seafoam);border-radius:14px;">
        <div style="font-size:1rem;font-weight:900;color:var(--ocean-deep);margin-bottom:12px;text-align:center;">
          🧭 Bảng Nhận Biết Từ Loại Theo Vị Trí
        </div>
        <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:10px;font-size:.85rem;">
          <div style="background:#dbeafe;padding:10px 14px;border-radius:10px;border-left:4px solid #3b82f6;">
            <div style="font-weight:800;color:#1d4ed8">📌 DANH TỪ (N)</div>
            a/an/the + <strong>___</strong><br>
            my/his/her + <strong>___</strong><br>
            of/in/on + <strong>___</strong><br>
            many/much + <strong>___</strong>
          </div>
          <div style="background:#dcfce7;padding:10px 14px;border-radius:10px;border-left:4px solid #22c55e;">
            <div style="font-weight:800;color:#166534">📌 ĐỘNG TỪ (V)</div>
            to + <strong>___</strong><br>
            will/can/should + <strong>___</strong><br>
            have to/need to + <strong>___</strong>
          </div>
          <div style="background:#fef3c7;padding:10px 14px;border-radius:10px;border-left:4px solid #f59e0b;">
            <div style="font-weight:800;color:#92400e">📌 TÍNH TỪ (Adj)</div>
            to be + <strong>___</strong><br>
            look/seem/feel + <strong>___</strong><br>
            <strong>___</strong> + danh từ<br>
            trạng từ + <strong>___</strong>
          </div>
          <div style="background:#fce7f3;padding:10px 14px;border-radius:10px;border-left:4px solid #ec4899;">
            <div style="font-weight:800;color:#9d174d">📌 TRẠNG TỪ (Adv)</div>
            <strong>___</strong> sau động từ<br>
            <strong>___</strong> trước tính từ<br>
            <strong>___</strong> , câu... (đầu câu)<br>
            and/or + <strong>___</strong> (cân bằng Adv)
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ════ BÀI TẬP ════ -->
  <section id="bai-tap">
    <div class="section-title"><span class="icon">✏️</span> Bài Tập Luyện Tập</div>

    <!-- EXERCISE 1 -->
    <div>
      <div class="exercise-header">
        <span style="font-size:1.4rem">🐠</span>
        <div>
          <h3>Exercise 1 – Chọn đáp án đúng (A, B, C hoặc D)</h3>
          <div style="font-size:.82rem;opacity:.85;margin-top:2px;">Áp dụng quy tắc nhận biết từ loại theo vị trí trong câu</div>
        </div>
      </div>
      <div class="exercise-body">

        <div class="ex-question">
          <div class="ex-num">1</div>
          <div class="ex-content">
            <div class="ex-sentence">Faraday made many ______ in the field of physics and chemistry.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-1',false,'Sau "many" cần danh từ số nhiều, không phải động từ.')">A. discover</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-1',true,'✅ Sau "many" cần danh từ số nhiều → discoveries')">B. discoveries</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-1',false,'Đây là động từ chia quá khứ, không phải danh từ.')">C. discovered</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-1',false,'-ing ở đây không phải danh từ phù hợp sau "many".')">D. discovering</button>
            </div>
            <div class="ex-feedback" id="ex1-1"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">2</div>
          <div class="ex-content">
            <div class="ex-sentence">Faraday was an ______ in Davy's laboratory.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-2',false,'assistance = sự hỗ trợ (khái niệm), không phải người.')">A. assistance</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-2',false,'assist là động từ, không đứng sau "an".')">B. assist</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-2',true,'✅ Sau mạo từ "an" → cần danh từ. assistant = người phụ tá')">C. assistant</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-2',false,'assisted là tính từ/động từ quá khứ, không phải danh từ người.')">D. assisted</button>
            </div>
            <div class="ex-feedback" id="ex1-2"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">3</div>
          <div class="ex-content">
            <div class="ex-sentence">The generator is one of Faraday's most important ______.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-3',true,'✅ "one of + N(số nhiều)" → achievements. Sau "important" cần danh từ.')">A. achievements</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-3',false,'achievement (số ít) không dùng sau "one of".')">B. achievement</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-3',false,'achieve là động từ, không đứng sau "most important".')">C. achieve</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-3',false,'achieving không phù hợp ở vị trí này.')">D. achieving</button>
            </div>
            <div class="ex-feedback" id="ex1-3"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">4</div>
          <div class="ex-content">
            <div class="ex-sentence">His ______ of the generator is very famous.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-4',false,'invent là động từ, không đứng sau "his".')">A. invent</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-4',false,'inventive là tính từ, không đứng sau "his".')">B. inventive</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-4',true,'✅ Sau "his" (tính từ sở hữu) → cần danh từ: invention')">C. invention</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-4',false,'inventor = người phát minh, không phù hợp nghĩa câu.')">D. inventor</button>
            </div>
            <div class="ex-feedback" id="ex1-4"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">5</div>
          <div class="ex-content">
            <div class="ex-sentence">We will ______ our English vocabulary if we read English books every day.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-5',false,'rich là tính từ, không đứng sau "will".')">A. rich</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-5',false,'richness là danh từ, không đứng sau "will".')">B. richness</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-5',true,'✅ Sau "will" cần động từ nguyên dạng → enrich (làm giàu)')">C. enrich</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-5',false,'richly là trạng từ, không đứng sau "will".')">D. richly</button>
            </div>
            <div class="ex-feedback" id="ex1-5"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">6</div>
          <div class="ex-content">
            <div class="ex-sentence">You study very well. It's ______ that you will fail the exam.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-6',false,'possible = có thể. Nhưng nghĩa câu "học giỏi → không thể trượt".')">A. possible</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-6',true,'✅ Sau "It\'s" cần tính từ. impossible = không thể (phù hợp nghĩa)')">B. impossible</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-6',false,'possibility là danh từ.')">C. possibility</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-6',false,'impossibility là danh từ.')">D. impossibility</button>
            </div>
            <div class="ex-feedback" id="ex1-6"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">7</div>
          <div class="ex-content">
            <div class="ex-sentence">Lan always shares her ______ with me.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-7',true,'✅ Sau "her" (tính từ sở hữu) → cần danh từ: sadness')">A. sadness</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-7',false,'sad là tính từ, không đứng sau "her".')">B. sad</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-7',false,'sadly là trạng từ.')">C. sadly</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-7',false,'unsad không phải từ tiếng Anh.')">D. unsad</button>
            </div>
            <div class="ex-feedback" id="ex1-7"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">8</div>
          <div class="ex-content">
            <div class="ex-sentence">These children have the ______ to imitate animals' voice.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-8',false,'able là tính từ, không đứng sau "the".')">A. able</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-8',true,'✅ Sau mạo từ "the" → cần danh từ: ability (năng lực)')">B. ability</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-8',false,'disable là động từ.')">C. disable</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-8',false,'disability = sự tàn tật, không phù hợp nghĩa.')">D. disability</button>
            </div>
            <div class="ex-feedback" id="ex1-8"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">9</div>
          <div class="ex-content">
            <div class="ex-sentence">Money doesn't bring ______ to man.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-9',false,'happy là tính từ, không đứng sau "bring".')">A. happy</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-9',true,'✅ bring + N → happiness (danh từ = niềm hạnh phúc)')">B. happiness</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-9',false,'happily là trạng từ.')">C. happily</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-9',false,'unhappy là tính từ.')">D. unhappy</button>
            </div>
            <div class="ex-feedback" id="ex1-9"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">10</div>
          <div class="ex-content">
            <div class="ex-sentence">Good students aren't ______ intelligent students.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex1-10',false,'necessary là tính từ, nhưng câu cần trạng từ bổ nghĩa cho tính từ "intelligent".')">A. necessary</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-10',false,'necessity là danh từ.')">B. necessity</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-10',true,'✅ Trước tính từ "intelligent" → cần trạng từ: necessarily')">C. necessarily</button>
              <button class="ex-opt" onclick="checkEx(this,'ex1-10',false,'unnecessary là tính từ.')">D. unnecessary</button>
            </div>
            <div class="ex-feedback" id="ex1-10"></div>
          </div>
        </div>

        <div class="score-bar" id="score1-bar" style="display:none">
          <div>
            <div class="score-num" id="score1-num">0/10</div>
            <div class="score-label">điểm Exercise 1</div>
          </div>
          <div class="score-msg" id="score1-msg"></div>
        </div>
      </div>
    </div>

    <!-- EXERCISE 2 -->
    <div>
      <div class="exercise-header">
        <span style="font-size:1.4rem">🐋</span>
        <div>
          <h3>Exercise 2 – Chọn đáp án đúng (A, B, C hoặc D)</h3>
          <div style="font-size:.82rem;opacity:.85;margin-top:2px;">Luyện tập nâng cao – nhận biết từ loại trong ngữ cảnh đa dạng</div>
        </div>
      </div>
      <div class="exercise-body">

        <div class="ex-question">
          <div class="ex-num">1</div>
          <div class="ex-content">
            <div class="ex-sentence">I don't believe what he has just said. It is ______.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-1',false,'reason là danh từ, không đứng sau "is".')">A. reason</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-1',true,'✅ Sau "is" → tính từ: unreasonable (vô lí)')">B. unreasonable</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-1',false,'reasonably là trạng từ.')">C. reasonably</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-1',false,'reasoning là danh từ/gerund.')">D. reasoning</button>
            </div>
            <div class="ex-feedback" id="ex2-1"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">2</div>
          <div class="ex-content">
            <div class="ex-sentence">The teacher does everything in order to ______ her students.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-2',false,'courage là danh từ, không đứng sau "to".')">A. courage</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-2',true,'✅ in order to + V (nguyên dạng) → encourage (khuyến khích)')">B. encourage</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-2',false,'encouragement là danh từ.')">C. encouragement</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-2',false,'encouraged là tính từ/quá khứ.')">D. encouraged</button>
            </div>
            <div class="ex-feedback" id="ex2-2"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">3</div>
          <div class="ex-content">
            <div class="ex-sentence">What is his ______? Is he American or English?</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-3',false,'national là tính từ, không đứng sau "his".')">A. national</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-3',true,'✅ Sau "his" → danh từ: nationality (quốc tịch)')">B. nationality</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-3',false,'nationalize là động từ.')">C. nationalize</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-3',false,'international là tính từ.')">D. international</button>
            </div>
            <div class="ex-feedback" id="ex2-3"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">4</div>
          <div class="ex-content">
            <div class="ex-sentence">You should spend your free time ______.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-4',false,'useful là tính từ, không bổ nghĩa cho động từ "spend".')">A. useful</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-4',false,'useless không phù hợp nghĩa.')">B. useless</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-4',true,'✅ Sau động từ "spend" → trạng từ: usefully (một cách có ích)')">C. usefully</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-4',false,'uselessly không phù hợp nghĩa.')">D. uselessly</button>
            </div>
            <div class="ex-feedback" id="ex2-4"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">5</div>
          <div class="ex-content">
            <div class="ex-sentence">Please decide what you want to do. You must make a ______.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-5',false,'decide là động từ, không đứng sau "a".')">A. decide</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-5',true,'✅ Sau "a" → danh từ. Cụm: make a decision (đưa ra quyết định)')">B. decision</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-5',false,'decisive là tính từ.')">C. decisive</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-5',false,'decisively là trạng từ.')">D. decisively</button>
            </div>
            <div class="ex-feedback" id="ex2-5"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">6</div>
          <div class="ex-content">
            <div class="ex-sentence">He is interested in the ______ of old buildings.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-6',false,'preserve là động từ, không đứng sau "the".')">A. preserve</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-6',true,'✅ Sau "the" → danh từ: preservation (sự gìn giữ)')">B. preservation</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-6',false,'preservative là tính từ.')">C. preservative</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-6',false,'preserved là tính từ/quá khứ.')">D. preserved</button>
            </div>
            <div class="ex-feedback" id="ex2-6"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">7</div>
          <div class="ex-content">
            <div class="ex-sentence">He has very high ______ of his only son.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-7',false,'expect là động từ, không đứng sau "high".')">A. expect</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-7',true,'✅ Sau tính từ "high" → danh từ: expectation (sự kỳ vọng)')">B. expectation</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-7',false,'expected là tính từ.')">C. expected</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-7',false,'expectedly là trạng từ.')">D. expectedly</button>
            </div>
            <div class="ex-feedback" id="ex2-7"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">8</div>
          <div class="ex-content">
            <div class="ex-sentence">All of us need the ______ of fresh air.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-8',false,'provide là động từ.')">A. provide</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-8',false,'provided là tính từ.')">B. provided</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-8',true,'✅ Sau "the" → danh từ: provision (nguồn cung cấp)')">C. provision</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-8',false,'provisions = lương thực dự trữ, không phù hợp nghĩa ở đây.')">D. provisions</button>
            </div>
            <div class="ex-feedback" id="ex2-8"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">9</div>
          <div class="ex-content">
            <div class="ex-sentence">Farmers need to ______ crops.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-9',false,'rotation là danh từ, không đứng sau "to".')">A. rotation</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-9',true,'✅ need to + V nguyên dạng → rotate (luân canh)')">B. rotate</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-9',false,'rotational là tính từ.')">C. rotational</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-9',false,'rotationally là trạng từ.')">D. rotationally</button>
            </div>
            <div class="ex-feedback" id="ex2-9"></div>
          </div>
        </div>

        <div class="ex-question">
          <div class="ex-num">10</div>
          <div class="ex-content">
            <div class="ex-sentence">We are discussing about a problem of great ______.</div>
            <div class="ex-options">
              <button class="ex-opt" onclick="checkEx(this,'ex2-10',false,'important là tính từ, không đứng sau "great".')">A. important</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-10',true,'✅ Sau tính từ "great" → danh từ: importance (tầm quan trọng)')">B. importance</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-10',false,'importantly là trạng từ.')">C. importantly</button>
              <button class="ex-opt" onclick="checkEx(this,'ex2-10',false,'import = nhập khẩu, không phù hợp nghĩa.')">D. import</button>
            </div>
            <div class="ex-feedback" id="ex2-10"></div>
          </div>
        </div>

        <div class="score-bar" id="score2-bar" style="display:none">
          <div>
            <div class="score-num" id="score2-num">0/10</div>
            <div class="score-label">điểm Exercise 2</div>
          </div>
          <div class="score-msg" id="score2-msg"></div>
        </div>
      </div>
    </div>

    <!-- TOTAL SCORE -->
    <div style="background:linear-gradient(135deg,var(--ocean-mid),var(--ocean-light));border-radius:20px;padding:28px 24px;text-align:center;color:#fff;margin-top:16px;" id="total-score-box" style="display:none">
      <div style="font-size:2.2rem;margin-bottom:6px;" id="total-emoji">🏆</div>
      <div style="font-size:2rem;font-weight:900;" id="total-score-num">–</div>
      <div style="opacity:.85;font-size:.95rem;margin-top:4px;">Tổng điểm (20 câu)</div>
      <div style="margin-top:10px;font-size:1rem;font-weight:700;opacity:.9;" id="total-msg"></div>
    </div>
  </section>

</main>

<!-- FOOTER -->
<footer class="footer">
  <div class="footer-fish">🐠 🐙 🦀 🐚 🐋</div>
  <div style="font-weight:700;margin-bottom:6px;">Word Forms – Cấu Tạo Từ</div>
  <div style="opacity:.7;">Chuyên Đề 14 · Tiếng Anh Cấp 2 & Cấp 3</div>
</footer>

<script>
  // ──────── MINI QUIZ ────────
  function checkQuiz(btn, qid, correct, explanation) {
    const container = document.getElementById(qid);
    if (container.dataset.done) return;
    container.dataset.done = '1';
    const buttons = container.querySelectorAll('.quiz-opt');
    buttons.forEach(b => { b.disabled = true; });
    const fb = document.getElementById('fb-' + qid);
    if (correct) {
      btn.classList.add('correct');
      fb.textContent = '✅ Chính xác! ' + (explanation || '');
      fb.className = 'feedback show ok';
    } else {
      btn.classList.add('wrong');
      fb.textContent = '❌ Chưa đúng. ' + (explanation || 'Hãy xem lại quy tắc bên trên!');
      fb.className = 'feedback show err';
      // Highlight correct answer if we know it
      buttons.forEach(b => {
        if (b.getAttribute('onclick') && b.getAttribute('onclick').includes(',true,')) {
          b.classList.add('correct');
        }
      });
    }
  }

  // ──────── EXERCISES ────────
  const scores = { ex1: 0, ex2: 0 };
  const answered = {};

  function checkEx(btn, id, correct, explanation) {
    if (answered[id]) return;
    answered[id] = true;

    const content = btn.closest('.ex-content');
    const allBtns = content.querySelectorAll('.ex-opt');
    allBtns.forEach(b => b.disabled = true);

    const fb = document.getElementById(id);
    if (correct) {
      btn.classList.add('correct');
      fb.textContent = explanation || '✅ Chính xác!';
      fb.className = 'ex-feedback show ok';
      // update score
      const exKey = id.startsWith('ex1') ? 'ex1' : 'ex2';
      scores[exKey]++;
    } else {
      btn.classList.add('wrong');
      fb.textContent = '❌ ' + (explanation || 'Chưa đúng. Xem lại quy tắc!');
      fb.className = 'ex-feedback show err';
      // Highlight correct
      allBtns.forEach(b => {
        if (b.getAttribute('onclick') && b.getAttribute('onclick').includes(',true,')) {
          b.classList.add('correct');
        }
      });
    }

    // Check if exercise complete
    updateScore(id.startsWith('ex1') ? 'ex1' : 'ex2');
  }

  function updateScore(exKey) {
    const prefix = exKey + '-';
    const total = 10;
    let done = 0;
    for (let i = 1; i <= total; i++) {
      if (answered[prefix + i]) done++;
    }
    const n = scores[exKey];
    const scoreBar = document.getElementById('score' + exKey.slice(2) + '-bar');
    const scoreNum = document.getElementById('score' + exKey.slice(2) + '-num');
    const scoreMsg = document.getElementById('score' + exKey.slice(2) + '-msg');
    if (done === total) {
      scoreBar.style.display = 'flex';
      scoreNum.textContent = n + '/10';
      if (n === 10)      scoreMsg.textContent = '🏆 Xuất sắc! Em làm đúng tất cả!';
      else if (n >= 8)   scoreMsg.textContent = '⭐ Rất tốt! Tiếp tục phát huy nhé!';
      else if (n >= 6)   scoreMsg.textContent = '👍 Khá! Ôn lại phần lý thuyết để cải thiện thêm.';
      else               scoreMsg.textContent = '💪 Cố gắng hơn! Xem lại sơ đồ tổng hợp và thử lại.';

      // update total
      const ex1Done = Array.from({length:10},(_,i)=>answered['ex1-'+(i+1)]).every(Boolean);
      const ex2Done = Array.from({length:10},(_,i)=>answered['ex2-'+(i+1)]).every(Boolean);
      if (ex1Done && ex2Done) {
        const total2 = scores.ex1 + scores.ex2;
        const box = document.getElementById('total-score-box');
        box.style.display = 'block';
        document.getElementById('total-score-num').textContent = total2 + '/20';
        const emoji = total2 >= 18 ? '🏆' : total2 >= 14 ? '⭐' : total2 >= 10 ? '👍' : '💪';
        document.getElementById('total-emoji').textContent = emoji;
        const msg = total2 >= 18 ? 'Tuyệt vời! Em đã nắm vững Word Forms!' :
                    total2 >= 14 ? 'Rất tốt! Hãy ôn thêm những câu sai nhé.' :
                    total2 >= 10 ? 'Khá! Cần ôn lại quy tắc nhận biết từ loại.' :
                                   'Hãy xem lại toàn bộ lý thuyết và thử lại nhé.';
        document.getElementById('total-msg').textContent = msg;
      }
    }
  }

  // ──────── SMOOTH SCROLL NAV ────────
  document.querySelectorAll('.nav-pill').forEach(pill => {
    pill.addEventListener('click', function(e) {
      document.querySelectorAll('.nav-pill').forEach(p => p.classList.remove('active'));
      this.classList.add('active');
    });
  });

  // Active nav on scroll
  const sections = document.querySelectorAll('section[id], div[id]');
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(s => {
      const top = s.getBoundingClientRect().top;
      if (top < 120) current = s.id;
    });
    document.querySelectorAll('.nav-pill').forEach(p => {
      p.classList.remove('active');
      if (p.getAttribute('href') === '#' + current) p.classList.add('active');
    });
  });
</script>
</body>
</html>
