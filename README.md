<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Rudra Prajapati — 2096</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Orbitron:wght@400;500;700;900&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  :root {
    --void: #02020A;
    --deep: #070714;
    --panel: #0C0C1E;
    --glass: rgba(255,255,255,0.03);
    --rim: rgba(139,92,246,0.18);
    --violet: #8B5CF6;
    --indigo: #4F46E5;
    --plasma: #C084FC;
    --cyan: #22D3EE;
    --neon: #A78BFA;
    --ghost: rgba(167,139,250,0.12);
    --text: #E2E0FF;
    --muted: #6B6A8A;
    --dim: #3B3A5C;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--void);
    color: var(--text);
    font-family: 'Space Grotesk', sans-serif;
    overflow-x: hidden;
    min-height: 100vh;
  }

  /* ── STARFIELD ── */
  #stars {
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    overflow: hidden;
  }
  #stars span {
    position: absolute;
    border-radius: 50%;
    background: #fff;
    animation: twinkle var(--d, 4s) ease-in-out infinite;
    opacity: 0;
  }
  @keyframes twinkle {
    0%,100% { opacity: 0; transform: scale(0.8); }
    50% { opacity: var(--o, 0.6); transform: scale(1); }
  }

  /* ── GRID OVERLAY ── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    z-index: 0;
    background-image:
      linear-gradient(rgba(139,92,246,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(139,92,246,0.03) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
  }

  /* ── LAYOUT ── */
  .wrap { position: relative; z-index: 1; max-width: 1100px; margin: 0 auto; padding: 0 32px; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 60px 32px;
    position: relative;
    z-index: 1;
  }

  .hero-glow {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -60%);
    width: 700px;
    height: 700px;
    background: radial-gradient(ellipse, rgba(139,92,246,0.15) 0%, transparent 70%);
    pointer-events: none;
  }

  .era-tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.3em;
    color: var(--muted);
    text-transform: uppercase;
    border: 1px solid var(--dim);
    padding: 6px 18px;
    border-radius: 2px;
    margin-bottom: 40px;
    position: relative;
  }
  .era-tag::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
    background: var(--violet);
  }

  .hero-name {
    font-family: 'Orbitron', monospace;
    font-size: clamp(42px, 7vw, 88px);
    font-weight: 900;
    line-height: 0.95;
    letter-spacing: -0.02em;
    background: linear-gradient(135deg, #FFFFFF 0%, #C084FC 40%, #8B5CF6 70%, #4F46E5 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 16px;
  }

  .hero-sub {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--violet);
    letter-spacing: 0.25em;
    text-transform: uppercase;
    margin-bottom: 32px;
  }

  .hero-desc {
    max-width: 580px;
    font-size: 17px;
    line-height: 1.7;
    color: #9B9BC0;
    margin-bottom: 52px;
  }

  .hero-cta {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .btn {
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    text-decoration: none;
    padding: 14px 32px;
    border-radius: 2px;
    transition: all 0.25s;
    cursor: pointer;
    border: none;
  }
  .btn-primary {
    background: linear-gradient(135deg, var(--indigo), var(--violet));
    color: #fff;
    box-shadow: 0 0 30px rgba(139,92,246,0.35);
  }
  .btn-primary:hover { box-shadow: 0 0 50px rgba(139,92,246,0.6); transform: translateY(-2px); }
  .btn-ghost {
    background: transparent;
    color: var(--neon);
    border: 1px solid var(--rim);
  }
  .btn-ghost:hover { background: var(--ghost); border-color: var(--violet); transform: translateY(-2px); }

  /* ── SCROLL INDICATOR ── */
  .scroll-hint {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    color: var(--dim);
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.2em;
  }
  .scroll-line {
    width: 1px;
    height: 50px;
    background: linear-gradient(to bottom, var(--violet), transparent);
    animation: scrollPulse 2s ease-in-out infinite;
  }
  @keyframes scrollPulse { 0%,100%{opacity:0.3} 50%{opacity:1} }

  /* ── SECTION ── */
  section { padding: 120px 0; position: relative; z-index: 1; }

  .sec-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.35em;
    color: var(--violet);
    text-transform: uppercase;
    margin-bottom: 16px;
  }
  .sec-title {
    font-family: 'Orbitron', monospace;
    font-size: clamp(26px, 4vw, 42px);
    font-weight: 700;
    line-height: 1.1;
    margin-bottom: 60px;
    color: #fff;
  }
  .sec-title span { color: var(--plasma); }

  /* ── DIVIDER ── */
  .divider {
    width: 100%;
    height: 1px;
    background: linear-gradient(to right, transparent, var(--rim), transparent);
    position: relative;
    z-index: 1;
  }

  /* ── IDENTITY BLOCK ── */
  .identity-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
    background: var(--rim);
    border: 1px solid var(--rim);
    margin-bottom: 40px;
  }
  .id-cell {
    background: var(--panel);
    padding: 28px 32px;
  }
  .id-cell-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.3em;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 8px;
  }
  .id-cell-value {
    font-size: 16px;
    color: var(--text);
    font-weight: 500;
  }
  .id-cell-value.accent { color: var(--plasma); }

  /* ── STATUS BADGE ── */
  .status-row {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    margin-bottom: 60px;
  }
  .status-badge {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.15em;
    padding: 8px 20px;
    border: 1px solid var(--rim);
    border-radius: 1px;
    color: var(--neon);
    background: var(--ghost);
    position: relative;
    overflow: hidden;
  }
  .status-badge::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 2px;
    background: var(--violet);
  }
  .status-badge.active { border-color: rgba(34,211,238,0.3); color: var(--cyan); }
  .status-badge.active::before { background: var(--cyan); }

  /* ── TECH MATRIX ── */
  .tech-matrix {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));
    gap: 2px;
    background: var(--rim);
    border: 1px solid var(--rim);
  }
  .tech-cell {
    background: var(--panel);
    padding: 24px 20px;
    text-align: center;
    transition: background 0.2s;
    cursor: default;
  }
  .tech-cell:hover { background: var(--ghost); }
  .tech-icon {
    font-size: 28px;
    margin-bottom: 10px;
    display: block;
  }
  .tech-name {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.12em;
    color: var(--muted);
    text-transform: uppercase;
  }
  .tech-cell:hover .tech-name { color: var(--neon); }

  /* ── AI EXPERTISE ── */
  .ai-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
    background: var(--rim);
    border: 1px solid var(--rim);
  }
  .ai-card {
    background: var(--panel);
    padding: 32px;
    position: relative;
    overflow: hidden;
    transition: background 0.25s;
  }
  .ai-card:hover { background: var(--ghost); }
  .ai-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--indigo), var(--violet), var(--plasma));
    transform: scaleX(0);
    transition: transform 0.3s;
    transform-origin: left;
  }
  .ai-card:hover::after { transform: scaleX(1); }
  .ai-domain {
    font-family: 'Orbitron', monospace;
    font-size: 13px;
    font-weight: 600;
    color: #fff;
    margin-bottom: 8px;
  }
  .ai-detail {
    font-size: 13px;
    color: var(--muted);
    line-height: 1.6;
    margin-bottom: 20px;
  }
  .ai-bar-wrap {
    height: 2px;
    background: var(--dim);
    border-radius: 1px;
    overflow: hidden;
  }
  .ai-bar {
    height: 100%;
    background: linear-gradient(90deg, var(--indigo), var(--plasma));
    border-radius: 1px;
    animation: barGrow 1.5s ease-out forwards;
    transform-origin: left;
    transform: scaleX(0);
  }
  @keyframes barGrow { to { transform: scaleX(1); } }
  .ai-level {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.2em;
    color: var(--violet);
    text-transform: uppercase;
    margin-top: 10px;
  }

  /* ── PROJECTS ── */
  .project-list { display: flex; flex-direction: column; gap: 2px; }
  .project-card {
    background: var(--panel);
    border: 1px solid var(--rim);
    padding: 40px;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 32px;
    align-items: start;
    transition: border-color 0.25s, background 0.25s;
    position: relative;
    overflow: hidden;
  }
  .project-card::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
    background: linear-gradient(to bottom, var(--indigo), var(--violet));
    transform: scaleY(0);
    transition: transform 0.35s;
    transform-origin: top;
  }
  .project-card:hover { border-color: rgba(139,92,246,0.4); background: var(--ghost); }
  .project-card:hover::before { transform: scaleY(1); }
  .proj-tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.25em;
    color: var(--violet);
    text-transform: uppercase;
    margin-bottom: 12px;
  }
  .proj-title {
    font-family: 'Orbitron', monospace;
    font-size: 20px;
    font-weight: 700;
    color: #fff;
    margin-bottom: 12px;
  }
  .proj-desc {
    font-size: 15px;
    color: var(--muted);
    line-height: 1.7;
    margin-bottom: 24px;
    max-width: 560px;
  }
  .proj-tags {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }
  .proj-tag-item {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    padding: 5px 14px;
    border: 1px solid var(--dim);
    color: var(--neon);
    letter-spacing: 0.1em;
  }
  .proj-status {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.15em;
    color: var(--cyan);
    border: 1px solid rgba(34,211,238,0.25);
    padding: 6px 14px;
    white-space: nowrap;
    text-align: center;
  }

  /* ── CERTS ── */
  .cert-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 2px;
    background: var(--rim);
    border: 1px solid var(--rim);
  }
  .cert-card {
    background: var(--panel);
    padding: 32px 24px;
    text-align: center;
    transition: background 0.2s;
  }
  .cert-card:hover { background: var(--ghost); }
  .cert-logo {
    font-size: 36px;
    margin-bottom: 12px;
    display: block;
    filter: grayscale(0.3);
    transition: filter 0.2s;
  }
  .cert-card:hover .cert-logo { filter: none; }
  .cert-name {
    font-family: 'Orbitron', monospace;
    font-size: 12px;
    font-weight: 600;
    color: #fff;
    margin-bottom: 4px;
  }
  .cert-sub {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.15em;
    color: var(--muted);
    text-transform: uppercase;
  }

  /* ── CONNECT ── */
  .connect-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
    background: var(--rim);
    border: 1px solid var(--rim);
  }
  .connect-card {
    background: var(--panel);
    padding: 40px 32px;
    text-align: center;
    text-decoration: none;
    color: inherit;
    transition: background 0.25s;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
  }
  .connect-card:hover { background: var(--ghost); }
  .connect-icon { font-size: 32px; }
  .connect-platform {
    font-family: 'Orbitron', monospace;
    font-size: 13px;
    font-weight: 600;
    color: #fff;
  }
  .connect-handle {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.08em;
  }

  /* ── FOOTER ── */
  footer {
    position: relative;
    z-index: 1;
    padding: 60px 32px;
    text-align: center;
    border-top: 1px solid var(--rim);
  }
  .footer-quote {
    font-family: 'Orbitron', monospace;
    font-size: 14px;
    font-weight: 400;
    color: var(--dim);
    letter-spacing: 0.08em;
    line-height: 1.7;
    max-width: 600px;
    margin: 0 auto 24px;
  }
  .footer-copy {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: var(--dim);
    letter-spacing: 0.2em;
  }

  /* ── SCAN LINES ── */
  .scanlines {
    position: fixed;
    inset: 0;
    z-index: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,0,0,0.03) 2px,
      rgba(0,0,0,0.03) 4px
    );
    pointer-events: none;
  }

  /* ── FOCUS NODE ── */
  .focus-section {
    background: var(--panel);
    border: 1px solid var(--rim);
    padding: 48px;
  }
  .focus-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 40px;
  }
  .focus-group-title {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.3em;
    color: var(--violet);
    text-transform: uppercase;
    margin-bottom: 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--dim);
  }
  .focus-item {
    font-size: 14px;
    color: var(--muted);
    padding: 8px 0;
    padding-left: 20px;
    position: relative;
    line-height: 1.5;
  }
  .focus-item::before {
    content: '→';
    position: absolute;
    left: 0;
    color: var(--violet);
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    .ai-grid, .connect-grid, .focus-grid { grid-template-columns: 1fr; }
    .cert-row { grid-template-columns: repeat(2, 1fr); }
    .identity-grid { grid-template-columns: 1fr; }
    .project-card { grid-template-columns: 1fr; }
    .tech-matrix { grid-template-columns: repeat(3, 1fr); }
    section { padding: 80px 0; }
  }

  /* ── ANIMATED BORDER ── */
  .glow-border {
    position: relative;
  }
  .glow-border::after {
    content: '';
    position: absolute;
    inset: -1px;
    background: linear-gradient(135deg, var(--indigo), var(--violet), var(--plasma), var(--cyan), var(--indigo));
    background-size: 300% 300%;
    animation: borderSpin 6s linear infinite;
    z-index: -1;
    border-radius: inherit;
  }
  @keyframes borderSpin { 0% { background-position: 0% 50%; } 100% { background-position: 300% 50%; } }
</style>
</head>
<body>

<div class="scanlines"></div>
<div id="stars"></div>

<!-- HERO -->
<section class="hero">
  <div class="hero-glow"></div>
  <div class="era-tag">NEURAL EPOCH 2096 · PROFILE NODE ACTIVE</div>
  <h1 class="hero-name">RUDRA<br/>PRAJAPATI</h1>
  <p class="hero-sub">Software Engineer · AI Architect · Product Builder</p>
  <p class="hero-desc">
    Engineering scalable digital systems at the intersection of artificial intelligence, 
    human experience, and distributed infrastructure. Currently building Jio Tap — 
    a new protocol for human identity.
  </p>
  <div class="hero-cta">
    <a href="mailto:rudraprajapati494@gmail.com" class="btn btn-primary">Establish Link</a>
    <a href="https://github.com/RudraPrajapati01" class="btn btn-ghost">View Repository</a>
    <a href="https://www.linkedin.com/in/rudra-prajapati-9329b9279/" class="btn btn-ghost">Neural Network</a>
  </div>
  <div class="scroll-hint">
    <div class="scroll-line"></div>
    <span>Scroll</span>
  </div>
</section>

<div class="divider"></div>

<!-- IDENTITY -->
<section>
  <div class="wrap">
    <p class="sec-label">// Identity Record</p>
    <h2 class="sec-title">Who I <span>Am</span></h2>

    <div class="identity-grid">
      <div class="id-cell">
        <div class="id-cell-label">Full Designation</div>
        <div class="id-cell-value">Rudra Prajapati</div>
      </div>
      <div class="id-cell">
        <div class="id-cell-label">Current Node</div>
        <div class="id-cell-value accent">India · Grid Online</div>
      </div>
      <div class="id-cell">
        <div class="id-cell-label">Primary Role</div>
        <div class="id-cell-value">Full Stack Engineer · AI Builder</div>
      </div>
      <div class="id-cell">
        <div class="id-cell-label">Academic System</div>
        <div class="id-cell-value">JG University · BCA Sem 4</div>
      </div>
      <div class="id-cell">
        <div class="id-cell-label">Active Mission</div>
        <div class="id-cell-value accent">Building Jio Tap Platform</div>
      </div>
      <div class="id-cell">
        <div class="id-cell-label">Status</div>
        <div class="id-cell-value accent">Open to Opportunities</div>
      </div>
    </div>

    <div class="status-row">
      <div class="status-badge active">⬤ Available for Internships</div>
      <div class="status-badge active">⬤ Freelance Ready</div>
      <div class="status-badge">Startup Collaborations</div>
      <div class="status-badge">Open Source Contributor</div>
      <div class="status-badge">AI Engineering Projects</div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- TECH STACK -->
<section>
  <div class="wrap">
    <p class="sec-label">// Technology Matrix</p>
    <h2 class="sec-title">Stack <span>Arsenal</span></h2>
    <div class="tech-matrix">
      <div class="tech-cell"><span class="tech-icon">⚛️</span><span class="tech-name">React</span></div>
      <div class="tech-cell"><span class="tech-icon">🟢</span><span class="tech-name">Node.js</span></div>
      <div class="tech-cell"><span class="tech-icon">🐍</span><span class="tech-name">Python</span></div>
      <div class="tech-cell"><span class="tech-icon">🌐</span><span class="tech-name">HTML</span></div>
      <div class="tech-cell"><span class="tech-icon">🎨</span><span class="tech-name">CSS</span></div>
      <div class="tech-cell"><span class="tech-icon">🟨</span><span class="tech-name">JavaScript</span></div>
      <div class="tech-cell"><span class="tech-icon">🍃</span><span class="tech-name">MongoDB</span></div>
      <div class="tech-cell"><span class="tech-icon">🐬</span><span class="tech-name">MySQL</span></div>
      <div class="tech-cell"><span class="tech-icon">🔥</span><span class="tech-name">Firebase</span></div>
      <div class="tech-cell"><span class="tech-icon">⚡</span><span class="tech-name">Express</span></div>
      <div class="tech-cell"><span class="tech-icon">💨</span><span class="tech-name">Tailwind</span></div>
      <div class="tech-cell"><span class="tech-icon">📦</span><span class="tech-name">Vite</span></div>
      <div class="tech-cell"><span class="tech-icon">☁️</span><span class="tech-name">Vercel</span></div>
      <div class="tech-cell"><span class="tech-icon">🐙</span><span class="tech-name">GitHub</span></div>
      <div class="tech-cell"><span class="tech-icon">📡</span><span class="tech-name">REST API</span></div>
      <div class="tech-cell"><span class="tech-icon">🧪</span><span class="tech-name">Postman</span></div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- AI EXPERTISE -->
<section>
  <div class="wrap">
    <p class="sec-label">// Cognitive Modules</p>
    <h2 class="sec-title">AI / ML <span>Expertise</span></h2>
    <div class="ai-grid">
      <div class="ai-card">
        <div class="ai-domain">AI Product Engineering</div>
        <div class="ai-detail">Integrating LLM systems into production-grade modern applications.</div>
        <div class="ai-bar-wrap"><div class="ai-bar" style="width:92%"></div></div>
        <div class="ai-level">Advanced · 92%</div>
      </div>
      <div class="ai-card">
        <div class="ai-domain">Prompt Engineering</div>
        <div class="ai-detail">Optimizing workflows and outputs using large language model chains.</div>
        <div class="ai-bar-wrap"><div class="ai-bar" style="width:90%"></div></div>
        <div class="ai-level">Advanced · 90%</div>
      </div>
      <div class="ai-card">
        <div class="ai-domain">Recommendation Systems</div>
        <div class="ai-detail">Intelligent content and user matching with behavioral signal processing.</div>
        <div class="ai-bar-wrap"><div class="ai-bar" style="width:72%"></div></div>
        <div class="ai-level">Intermediate · 72%</div>
      </div>
      <div class="ai-card">
        <div class="ai-domain">AI Automation</div>
        <div class="ai-detail">Building productivity pipelines and intelligent workflow automation systems.</div>
        <div class="ai-bar-wrap"><div class="ai-bar" style="width:75%"></div></div>
        <div class="ai-level">Intermediate · 75%</div>
      </div>
      <div class="ai-card">
        <div class="ai-domain">Data Processing</div>
        <div class="ai-detail">Python-powered ETL pipelines for structured and unstructured data.</div>
        <div class="ai-bar-wrap"><div class="ai-bar" style="width:70%"></div></div>
        <div class="ai-level">Intermediate · 70%</div>
      </div>
      <div class="ai-card">
        <div class="ai-domain">AI Application Dev</div>
        <div class="ai-detail">Architecting full-stack AI-enabled products from zero to deployment.</div>
        <div class="ai-bar-wrap"><div class="ai-bar" style="width:88%"></div></div>
        <div class="ai-level">Advanced · 88%</div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- PROJECTS -->
<section>
  <div class="wrap">
    <p class="sec-label">// Active Builds</p>
    <h2 class="sec-title">Featured <span>Projects</span></h2>
    <div class="project-list">

      <div class="project-card">
        <div>
          <div class="proj-tag">// PRODUCT · ACTIVE BUILD</div>
          <h3 class="proj-title">Jio Tap Mobile Application</h3>
          <p class="proj-desc">
            Smart NFC & QR-based digital networking platform. Eliminates paper business cards — professionals share instant digital identity profiles via tap or scan. Built for scale, speed, and elegance.
          </p>
          <div class="proj-tags">
            <span class="proj-tag-item">React Native</span>
            <span class="proj-tag-item">Node.js</span>
            <span class="proj-tag-item">Firebase</span>
            <span class="proj-tag-item">NFC</span>
            <span class="proj-tag-item">QR Protocol</span>
          </div>
        </div>
        <div class="proj-status">⬤ LIVE BUILD</div>
      </div>

      <div class="project-card">
        <div>
          <div class="proj-tag">// WEB PLATFORM · ENTERPRISE</div>
          <h3 class="proj-title">Jio Tap Web Platform</h3>
          <p class="proj-desc">
            Enterprise-ready web system for professional digital identity. Full analytics dashboard, admin control, product catalog, portfolio management, and smart sharing across devices.
          </p>
          <div class="proj-tags">
            <span class="proj-tag-item">React</span>
            <span class="proj-tag-item">Node.js</span>
            <span class="proj-tag-item">MySQL</span>
            <span class="proj-tag-item">REST API</span>
          </div>
        </div>
        <div class="proj-status">⬤ LIVE BUILD</div>
      </div>

      <div class="project-card">
        <div>
          <div class="proj-tag">// AI SYSTEM · RESEARCH</div>
          <h3 class="proj-title">AI Job Recommendation Engine</h3>
          <p class="proj-desc">
            Intelligent career matching platform using ML to align user skill profiles with relevant job opportunities. Multi-user system with smart scoring and authentication.
          </p>
          <div class="proj-tags">
            <span class="proj-tag-item">Python</span>
            <span class="proj-tag-item">Flask</span>
            <span class="proj-tag-item">MySQL</span>
            <span class="proj-tag-item">ML Engine</span>
          </div>
        </div>
        <div class="proj-status" style="color: var(--neon); border-color: rgba(167,139,250,0.3);">⬤ COMPLETE</div>
      </div>

    </div>
  </div>
</section>

<div class="divider"></div>

<!-- CERTIFICATIONS -->
<section>
  <div class="wrap">
    <p class="sec-label">// Verified Credentials</p>
    <h2 class="sec-title">Certi<span>fications</span></h2>
    <div class="cert-row">
      <div class="cert-card">
        <span class="cert-logo">☁️</span>
        <div class="cert-name">AWS</div>
        <div class="cert-sub">Cloud Computing</div>
      </div>
      <div class="cert-card">
        <span class="cert-logo">🔴</span>
        <div class="cert-name">Oracle</div>
        <div class="cert-sub">Database Systems</div>
      </div>
      <div class="cert-card">
        <span class="cert-logo">🎓</span>
        <div class="cert-name">NPTEL</div>
        <div class="cert-sub">Professional Cert</div>
      </div>
      <div class="cert-card">
        <span class="cert-logo">🌐</span>
        <div class="cert-name">Cisco</div>
        <div class="cert-sub">Networking</div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- CURRENT FOCUS -->
<section>
  <div class="wrap">
    <p class="sec-label">// Active Processes</p>
    <h2 class="sec-title">Current <span>Focus</span></h2>
    <div class="focus-section">
      <div class="focus-grid">
        <div>
          <div class="focus-group-title">Learning Modules</div>
          <div class="focus-item">Advanced React Architecture</div>
          <div class="focus-item">AI Engineering & LLM Systems</div>
          <div class="focus-item">System Design Patterns</div>
          <div class="focus-item">Cloud Infrastructure</div>
          <div class="focus-item">Machine Learning Fundamentals</div>
        </div>
        <div>
          <div class="focus-group-title">Building Now</div>
          <div class="focus-item">Jio Tap Mobile Application</div>
          <div class="focus-item">Jio Tap Web Platform</div>
          <div class="focus-item">AI Powered Product Suite</div>
        </div>
        <div>
          <div class="focus-group-title">Exploring</div>
          <div class="focus-item">SaaS Architecture Models</div>
          <div class="focus-item">Startup Ecosystems</div>
          <div class="focus-item">Open Source Communities</div>
        </div>
        <div>
          <div class="focus-group-title">Open To</div>
          <div class="focus-item">Software Engineering Internships</div>
          <div class="focus-item">Freelance Dev Projects</div>
          <div class="focus-item">Startup Collaborations</div>
          <div class="focus-item">Open Source Contributions</div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- CONNECT -->
<section>
  <div class="wrap">
    <p class="sec-label">// Communication Channels</p>
    <h2 class="sec-title">Establish <span>Connection</span></h2>
    <div class="connect-grid">
      <a href="mailto:rudraprajapati494@gmail.com" class="connect-card">
        <span class="connect-icon">✉️</span>
        <div class="connect-platform">Gmail</div>
        <div class="connect-handle">rudraprajapati494@gmail.com</div>
      </a>
      <a href="https://www.linkedin.com/in/rudra-prajapati-9329b9279/" class="connect-card" target="_blank">
        <span class="connect-icon">🔗</span>
        <div class="connect-platform">LinkedIn</div>
        <div class="connect-handle">rudra-prajapati-9329b9279</div>
      </a>
      <a href="https://github.com/RudraPrajapati01" class="connect-card" target="_blank">
        <span class="connect-icon">⚙️</span>
        <div class="connect-platform">GitHub</div>
        <div class="connect-handle">RudraPrajapati01</div>
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-quote">
    "Engineering scalable systems that create meaningful impact<br/>
    through intelligence, reliability, and relentless iteration."
  </div>
  <div class="footer-copy">RUDRA PRAJAPATI · NODE ACTIVE · INDIA · 2096</div>
</footer>

<script>
  // Generate starfield
  const stars = document.getElementById('stars');
  for (let i = 0; i < 200; i++) {
    const s = document.createElement('span');
    const size = Math.random() * 2 + 0.5;
    s.style.cssText = `
      width: ${size}px; height: ${size}px;
      left: ${Math.random() * 100}%;
      top: ${Math.random() * 100}%;
      --d: ${3 + Math.random() * 5}s;
      --o: ${0.3 + Math.random() * 0.6};
      animation-delay: ${Math.random() * 6}s;
    `;
    stars.appendChild(s);
  }

  // IntersectionObserver for AI bars
  const bars = document.querySelectorAll('.ai-bar');
  const obs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.style.animation = 'barGrow 1.5s ease-out forwards';
        obs.unobserve(e.target);
      }
    });
  }, { threshold: 0.3 });
  bars.forEach(b => { b.style.transform = 'scaleX(0)'; obs.observe(b); });
</script>

</body>
</html>
