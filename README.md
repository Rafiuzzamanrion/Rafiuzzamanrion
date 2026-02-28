<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Rafiuzzaman Rion – GitHub Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #050810;
    --bg2: #0a0f1e;
    --bg3: #0d1425;
    --accent: #00d4ff;
    --accent2: #ff3cac;
    --accent3: #7b5ea7;
    --gold: #ffd166;
    --text: #e8eaf0;
    --muted: #7a8299;
    --card: rgba(255,255,255,0.03);
    --border: rgba(0,212,255,0.12);
    --glow: 0 0 40px rgba(0,212,255,0.15);
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    overflow-x: hidden;
    min-height: 100vh;
  }

  /* Animated grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
    z-index: 0;
    animation: gridShift 20s linear infinite;
  }

  @keyframes gridShift {
    0% { transform: translateY(0); }
    100% { transform: translateY(60px); }
  }

  /* Radial glows */
  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse 800px 500px at 20% 10%, rgba(0,212,255,0.06) 0%, transparent 70%),
      radial-gradient(ellipse 600px 400px at 80% 80%, rgba(255,60,172,0.06) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  .wrapper {
    position: relative;
    z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 48px 24px;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 64px 24px 48px;
    position: relative;
  }

  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(0,212,255,0.08);
    border: 1px solid rgba(0,212,255,0.25);
    border-radius: 100px;
    padding: 6px 18px;
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 28px;
    animation: fadeDown 0.8s ease both;
  }

  .hero-badge::before {
    content: '';
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--accent);
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%,100% { opacity:1; transform:scale(1); }
    50% { opacity:0.4; transform:scale(0.8); }
  }

  .hero h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(42px, 8vw, 72px);
    font-weight: 800;
    line-height: 1.05;
    letter-spacing: -2px;
    animation: fadeDown 0.9s ease 0.1s both;
    background: linear-gradient(135deg, #fff 0%, var(--accent) 50%, var(--accent2) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-sub {
    font-family: 'Syne', sans-serif;
    font-size: 16px;
    color: var(--muted);
    margin-top: 12px;
    letter-spacing: 1px;
    animation: fadeDown 1s ease 0.2s both;
  }

  .hero-sub span { color: var(--accent); }

  .hero-desc {
    max-width: 560px;
    margin: 24px auto 0;
    font-size: 13px;
    line-height: 1.8;
    color: #8a93ab;
    animation: fadeDown 1s ease 0.3s both;
  }

  .hero-cta {
    display: flex;
    justify-content: center;
    gap: 12px;
    margin-top: 32px;
    flex-wrap: wrap;
    animation: fadeDown 1s ease 0.4s both;
  }

  .btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 24px;
    border-radius: 8px;
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 600;
    text-decoration: none;
    cursor: pointer;
    transition: all 0.25s;
    letter-spacing: 0.5px;
  }

  .btn-primary {
    background: linear-gradient(135deg, var(--accent), #0099cc);
    color: #000;
    box-shadow: 0 4px 24px rgba(0,212,255,0.3);
  }
  .btn-primary:hover { transform:translateY(-2px); box-shadow: 0 8px 32px rgba(0,212,255,0.5); }

  .btn-outline {
    background: transparent;
    color: var(--text);
    border: 1px solid rgba(255,255,255,0.15);
  }
  .btn-outline:hover { border-color: var(--accent); color: var(--accent); transform:translateY(-2px); }

  /* ── DIVIDER ── */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--accent), var(--accent2), transparent);
    margin: 48px 0;
    opacity: 0.3;
  }

  /* ── SECTION TITLES ── */
  .section-label {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 28px;
  }

  .section-label h2 {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--accent);
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── ABOUT GRID ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 48px;
  }

  @media (max-width: 600px) { .about-grid { grid-template-columns: 1fr; } }

  .about-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    display: flex;
    align-items: flex-start;
    gap: 14px;
    transition: all 0.3s;
    animation: fadeUp 0.6s ease both;
  }

  .about-card:hover {
    background: rgba(0,212,255,0.05);
    border-color: rgba(0,212,255,0.3);
    transform: translateY(-3px);
    box-shadow: var(--glow);
  }

  .about-card .icon {
    font-size: 20px;
    min-width: 20px;
    margin-top: 2px;
  }

  .about-card .label {
    font-family: 'Syne', sans-serif;
    font-size: 12px;
    font-weight: 600;
    color: var(--accent);
    letter-spacing: 0.5px;
    margin-bottom: 4px;
  }

  .about-card .value {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.5;
  }

  /* ── SKILLS ── */
  .skills-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 48px;
  }

  .skill-tag {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 8px 14px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 8px;
    font-size: 12px;
    font-weight: 500;
    color: var(--text);
    cursor: default;
    transition: all 0.25s;
    animation: fadeUp 0.5s ease both;
  }

  .skill-tag:hover {
    background: rgba(0,212,255,0.08);
    border-color: var(--accent);
    color: var(--accent);
    transform: translateY(-2px);
  }

  .skill-tag .dot {
    width: 5px; height: 5px;
    border-radius: 50%;
    background: var(--accent);
  }

  .skill-tag.pink .dot { background: var(--accent2); }
  .skill-tag.pink:hover { background: rgba(255,60,172,0.08); border-color: var(--accent2); color: var(--accent2); }

  .skill-tag.gold .dot { background: var(--gold); }
  .skill-tag.gold:hover { background: rgba(255,209,102,0.08); border-color: var(--gold); color: var(--gold); }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
    margin-bottom: 48px;
  }

  @media (max-width: 600px) { .projects-grid { grid-template-columns: 1fr; } }

  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 24px;
    text-decoration: none;
    color: var(--text);
    transition: all 0.3s;
    position: relative;
    overflow: hidden;
    animation: fadeUp 0.6s ease both;
    display: block;
  }

  .project-card::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(0,212,255,0.05) 0%, transparent 60%);
    opacity: 0;
    transition: opacity 0.3s;
  }

  .project-card:hover::before { opacity: 1; }

  .project-card:hover {
    border-color: rgba(0,212,255,0.35);
    transform: translateY(-4px);
    box-shadow: 0 16px 48px rgba(0,212,255,0.1);
  }

  .project-card.pink:hover {
    border-color: rgba(255,60,172,0.35);
    box-shadow: 0 16px 48px rgba(255,60,172,0.1);
  }

  .project-card.pink::before {
    background: linear-gradient(135deg, rgba(255,60,172,0.05) 0%, transparent 60%);
  }

  .project-top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 12px;
  }

  .project-icon {
    font-size: 24px;
  }

  .project-arrow {
    font-size: 16px;
    color: var(--muted);
    transition: all 0.25s;
  }

  .project-card:hover .project-arrow {
    color: var(--accent);
    transform: translate(3px, -3px);
  }

  .project-card.pink:hover .project-arrow { color: var(--accent2); }

  .project-name {
    font-family: 'Syne', sans-serif;
    font-size: 16px;
    font-weight: 700;
    margin-bottom: 8px;
  }

  .project-desc {
    font-size: 11px;
    color: var(--muted);
    line-height: 1.6;
    margin-bottom: 16px;
  }

  .project-tags {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
  }

  .project-tag {
    padding: 3px 10px;
    background: rgba(0,212,255,0.07);
    border: 1px solid rgba(0,212,255,0.15);
    border-radius: 4px;
    font-size: 10px;
    color: var(--accent);
    letter-spacing: 0.5px;
  }

  .project-card.pink .project-tag {
    background: rgba(255,60,172,0.07);
    border-color: rgba(255,60,172,0.15);
    color: var(--accent2);
  }

  /* ── STATS CARDS ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
    margin-bottom: 48px;
  }

  @media (max-width: 600px) { .stats-row { grid-template-columns: 1fr; } }

  .stat-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 28px 20px;
    text-align: center;
    transition: all 0.3s;
    animation: fadeUp 0.6s ease both;
  }

  .stat-card:hover {
    background: rgba(0,212,255,0.05);
    border-color: rgba(0,212,255,0.3);
    transform: translateY(-3px);
  }

  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 36px;
    font-weight: 800;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    line-height: 1;
    margin-bottom: 8px;
  }

  .stat-label {
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  /* ── CONNECT ── */
  .connect-grid {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    margin-bottom: 48px;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 12px 20px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    font-size: 12px;
    font-family: 'Syne', sans-serif;
    font-weight: 600;
    color: var(--text);
    text-decoration: none;
    cursor: pointer;
    transition: all 0.25s;
  }

  .connect-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(0,0,0,0.3);
  }

  .connect-btn.gh:hover { background: rgba(255,255,255,0.08); border-color: rgba(255,255,255,0.3); }
  .connect-btn.li:hover { background: rgba(10,102,194,0.15); border-color: rgba(10,102,194,0.5); color: #4a9fd4; }
  .connect-btn.em:hover { background: rgba(0,212,255,0.08); border-color: var(--accent); color: var(--accent); }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding-top: 24px;
  }

  .footer p {
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 1px;
  }

  .footer .wave {
    font-size: 28px;
    animation: wave 2.5s infinite;
    display: inline-block;
    transform-origin: 70% 70%;
  }

  @keyframes wave {
    0%,60%,100% { transform: rotate(0); }
    10%,30% { transform: rotate(20deg); }
    20%,40% { transform: rotate(-10deg); }
    50% { transform: rotate(10deg); }
  }

  /* ── TYPING ── */
  .typing-wrapper {
    display: inline-block;
    position: relative;
    min-height: 28px;
  }

  .typing {
    font-family: 'JetBrains Mono', monospace;
    font-size: 14px;
    color: var(--accent);
    display: inline;
  }

  .cursor {
    display: inline-block;
    width: 2px;
    height: 1em;
    background: var(--accent);
    margin-left: 2px;
    vertical-align: middle;
    animation: blink 1s step-end infinite;
  }

  @keyframes blink { 50% { opacity: 0; } }

  /* ── ANIMATIONS ── */
  @keyframes fadeDown {
    from { opacity:0; transform:translateY(-16px); }
    to { opacity:1; transform:translateY(0); }
  }

  @keyframes fadeUp {
    from { opacity:0; transform:translateY(16px); }
    to { opacity:1; transform:translateY(0); }
  }

  /* Stagger children */
  .about-card:nth-child(1) { animation-delay: 0.05s; }
  .about-card:nth-child(2) { animation-delay: 0.1s; }
  .about-card:nth-child(3) { animation-delay: 0.15s; }
  .about-card:nth-child(4) { animation-delay: 0.2s; }

  .project-card:nth-child(1) { animation-delay: 0.05s; }
  .project-card:nth-child(2) { animation-delay: 0.1s; }
  .project-card:nth-child(3) { animation-delay: 0.15s; }
  .project-card:nth-child(4) { animation-delay: 0.2s; }

  .stat-card:nth-child(1) { animation-delay: 0.05s; }
  .stat-card:nth-child(2) { animation-delay: 0.1s; }
  .stat-card:nth-child(3) { animation-delay: 0.15s; }

  .skill-tag:nth-child(odd) { animation-delay: 0.05s; }
  .skill-tag:nth-child(even) { animation-delay: 0.1s; }
</style>
</head>
<body>

<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-badge">Available for opportunities</div>
    <h1>Rafiuzzaman Rion</h1>
    <p class="hero-sub">
      Full-Stack Developer &nbsp;·&nbsp; 
      <span class="typing-wrapper">
        <span class="typing" id="typing"></span><span class="cursor"></span>
      </span>
    </p>
    <p class="hero-desc">
      Based in Dhaka, Bangladesh 🇧🇩 — I build modern, scalable web applications with the MERN stack, 
      transforming complex ideas into elegant digital experiences.
    </p>
    <div class="hero-cta">
      <a href="https://github.com/Rafiuzzamanrion" class="btn btn-primary">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"/></svg>
        GitHub
      </a>
      <a href="mailto:rion@example.com" class="btn btn-outline">
        📩 Contact Me
      </a>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ABOUT -->
  <div class="section-label"><h2>// About</h2></div>
  <div class="about-grid">
    <div class="about-card">
      <div class="icon">🌱</div>
      <div>
        <div class="label">Currently Learning</div>
        <div class="value">Python · C++ · Cloud Technologies</div>
      </div>
    </div>
    <div class="about-card">
      <div class="icon">🚀</div>
      <div>
        <div class="label">Work Status</div>
        <div class="value">Open for freelance &amp; remote opportunities</div>
      </div>
    </div>
    <div class="about-card">
      <div class="icon">🧑‍🏫</div>
      <div>
        <div class="label">Community</div>
        <div class="value">Mentoring junior developers &amp; sharing knowledge</div>
      </div>
    </div>
    <div class="about-card">
      <div class="icon">🏆</div>
      <div>
        <div class="label">Focus</div>
        <div class="value">Clean code · Best practices · Competitive coding</div>
      </div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section-label"><h2>// Tech Stack</h2></div>
  <div class="skills-grid">
    <div class="skill-tag"><span class="dot"></span>React.js</div>
    <div class="skill-tag"><span class="dot"></span>Next.js</div>
    <div class="skill-tag"><span class="dot"></span>Node.js</div>
    <div class="skill-tag"><span class="dot"></span>Express.js</div>
    <div class="skill-tag"><span class="dot"></span>MongoDB</div>
    <div class="skill-tag"><span class="dot"></span>TypeScript</div>
    <div class="skill-tag pink"><span class="dot"></span>Python</div>
    <div class="skill-tag pink"><span class="dot"></span>FastAPI</div>
    <div class="skill-tag pink"><span class="dot"></span>C++</div>
    <div class="skill-tag pink"><span class="dot"></span>PostgreSQL</div>
    <div class="skill-tag gold"><span class="dot"></span>Docker</div>
    <div class="skill-tag gold"><span class="dot"></span>AWS</div>
    <div class="skill-tag gold"><span class="dot"></span>Tailwind CSS</div>
    <div class="skill-tag"><span class="dot"></span>Git &amp; GitHub</div>
    <div class="skill-tag"><span class="dot"></span>REST APIs</div>
    <div class="skill-tag pink"><span class="dot"></span>GraphQL</div>
  </div>

  <!-- STATS -->
  <div class="section-label"><h2>// Impact</h2></div>
  <div class="stats-row">
    <div class="stat-card">
      <div class="stat-num">15+</div>
      <div class="stat-label">Open Source Contributions</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">3+</div>
      <div class="stat-label">Years Experience</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">∞</div>
      <div class="stat-label">Problems Solved</div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section-label"><h2>// Featured Projects</h2></div>
  <div class="projects-grid">
    <a href="https://mymanager.com/" class="project-card" target="_blank">
      <div class="project-top">
        <div class="project-icon">📊</div>
        <div class="project-arrow">↗</div>
      </div>
      <div class="project-name">MyManager</div>
      <div class="project-desc">Full-featured business management solution with real-time data, team collaboration, and analytics.</div>
      <div class="project-tags">
        <span class="project-tag">MongoDB</span>
        <span class="project-tag">Express</span>
        <span class="project-tag">React</span>
        <span class="project-tag">Node</span>
      </div>
    </a>
    <a href="http://lipikaai-staging-jwkyl.ondigitalocean.app" class="project-card pink" target="_blank">
      <div class="project-top">
        <div class="project-icon">🤖</div>
        <div class="project-arrow">↗</div>
      </div>
      <div class="project-name">LipikaAI</div>
      <div class="project-desc">AI-powered tools platform built with full-stack architecture. Smart, fast, and extensible.</div>
      <div class="project-tags">
        <span class="project-tag">AI / ML</span>
        <span class="project-tag">Full-Stack</span>
        <span class="project-tag">API</span>
      </div>
    </a>
    <a href="https://github.com/Rafiuzzamanrion/my_portfolio_latest" class="project-card" target="_blank">
      <div class="project-top">
        <div class="project-icon">🎨</div>
        <div class="project-arrow">↗</div>
      </div>
      <div class="project-name">Portfolio</div>
      <div class="project-desc">Personal portfolio built with Next.js &amp; Tailwind CSS — blazing fast and beautifully designed.</div>
      <div class="project-tags">
        <span class="project-tag">Next.js</span>
        <span class="project-tag">Tailwind</span>
        <span class="project-tag">SSR</span>
      </div>
    </a>
    <a href="https://www.rafiuzzamanrion.me/about/about-dark/" class="project-card pink" target="_blank">
      <div class="project-top">
        <div class="project-icon">⚙️</div>
        <div class="project-arrow">↗</div>
      </div>
      <div class="project-name">MM Client</div>
      <div class="project-desc">Polished client-side app for project management with intuitive UX and fast performance.</div>
      <div class="project-tags">
        <span class="project-tag">React</span>
        <span class="project-tag">Client-Side</span>
        <span class="project-tag">UI/UX</span>
      </div>
    </a>
  </div>

  <!-- GITHUB STATS -->
  <div class="section-label"><h2>// GitHub Stats</h2></div>
  <div style="display:grid; gap:12px; margin-bottom:48px;">
    <img src="https://nirzak-streak-stats.vercel.app/?user=Rafiuzzamanrion&theme=radical&hide_border=true&background=050810&stroke=00d4ff&ring=ff3cac&fire=ffd166&currStreakNum=ffffff&sideNums=ffffff&currStreakLabel=00d4ff&sideLabels=7a8299&dates=7a8299" alt="GitHub Streak" style="border-radius:12px; width:100%;"/>
    <div style="display:grid; grid-template-columns:1fr 1fr; gap:12px;">
      <img src="https://github-readme-stats.vercel.app/api?username=Rafiuzzamanrion&theme=radical&hide_border=true&bg_color=050810&title_color=00d4ff&text_color=e8eaf0&icon_color=ff3cac" alt="GitHub Stats" style="border-radius:12px; width:100%;"/>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Rafiuzzamanrion&layout=compact&theme=radical&hide_border=true&bg_color=050810&title_color=00d4ff&text_color=e8eaf0" alt="Top Languages" style="border-radius:12px; width:100%;"/>
    </div>
    <img src="https://github-readme-activity-graph.vercel.app/graph?username=Rafiuzzamanrion&bg_color=050810&color=00d4ff&line=ff3cac&point=ffd166&area=true&hide_border=true" alt="Activity Graph" style="border-radius:12px; width:100%;"/>
  </div>

  <!-- CONNECT -->
  <div class="section-label"><h2>// Let's Connect</h2></div>
  <div class="connect-grid">
    <a href="https://github.com/Rafiuzzamanrion" class="connect-btn gh" target="_blank">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"/></svg>
      GitHub
    </a>
    <a href="https://linkedin.com" class="connect-btn li" target="_blank">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>
    <a href="mailto:rion@example.com" class="connect-btn em">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
      Email Me
    </a>
  </div>

  <div class="divider"></div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="wave">👋</div>
    <p style="margin-top:16px;">Thanks for stopping by — let's build something incredible together.</p>
    <p style="margin-top:8px; color: rgba(122,130,153,0.5);">Made with passion in Dhaka, Bangladesh 🇧🇩</p>
  </div>

</div>

<script>
// Typing animation
const phrases = [
  "MERN Stack Developer",
  "Open Source Contributor",
  "Cloud Enthusiast",
  "Competitive Coder",
  "Lifelong Learner"
];

let pi = 0, ci = 0, deleting = false;
const el = document.getElementById('typing');

function type() {
  const current = phrases[pi];
  if (!deleting) {
    el.textContent = current.slice(0, ci + 1);
    ci++;
    if (ci === current.length) { deleting = true; setTimeout(type, 2000); return; }
  } else {
    el.textContent = current.slice(0, ci - 1);
    ci--;
    if (ci === 0) { deleting = false; pi = (pi + 1) % phrases.length; }
  }
  setTimeout(type, deleting ? 50 : 80);
}
type();
</script>
</body>
</html>
