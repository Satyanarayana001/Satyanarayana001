<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Satyanarayana – GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Sora:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0c10;
    --surface: #111318;
    --border: #1e2330;
    --accent: #00d4aa;
    --accent2: #7c6af7;
    --accent3: #f59e0b;
    --text: #e2e8f0;
    --muted: #6b7280;
    --card: #151820;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Sora', sans-serif;
    min-height: 100vh;
    padding: 40px 20px;
    background-image:
      radial-gradient(ellipse 80% 50% at 50% -10%, rgba(0,212,170,0.08) 0%, transparent 60%),
      radial-gradient(ellipse 60% 40% at 90% 80%, rgba(124,106,247,0.06) 0%, transparent 60%);
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
  }

  /* ── HEADER ── */
  .header {
    text-align: center;
    padding: 60px 0 40px;
    animation: fadeUp 0.8s ease both;
  }

  .greeting {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--accent);
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 16px;
    opacity: 0.9;
  }

  .greeting::before { content: '> '; }

  h1 {
    font-size: clamp(36px, 6vw, 60px);
    font-weight: 700;
    letter-spacing: -1.5px;
    line-height: 1.1;
    background: linear-gradient(135deg, #ffffff 0%, #a8b4d0 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .tagline {
    margin-top: 14px;
    font-size: 16px;
    color: var(--muted);
    font-weight: 300;
    letter-spacing: 0.3px;
  }

  .tagline strong {
    color: var(--text);
    font-weight: 600;
  }

  /* ── BADGES ── */
  .badges {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 28px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 8px 16px;
    border-radius: 100px;
    font-size: 13px;
    font-weight: 600;
    font-family: 'JetBrains Mono', monospace;
    border: 1px solid;
    transition: all 0.25s ease;
    cursor: pointer;
    text-decoration: none;
  }
  .badge:hover { transform: translateY(-2px); }

  .badge-green  { border-color: rgba(0,212,170,0.4); color: var(--accent);  background: rgba(0,212,170,0.06); }
  .badge-purple { border-color: rgba(124,106,247,0.4); color: #a78bfa;  background: rgba(124,106,247,0.06); }
  .badge-orange { border-color: rgba(245,158,11,0.4); color: var(--accent3); background: rgba(245,158,11,0.06); }
  .badge-blue   { border-color: rgba(56,189,248,0.4); color: #38bdf8;   background: rgba(56,189,248,0.06); }

  /* ── DIVIDER ── */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border) 30%, var(--border) 70%, transparent);
    margin: 40px 0;
  }

  /* ── SECTION TITLE ── */
  .section-title {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
    animation: fadeUp 0.8s 0.2s ease both;
  }

  .about-item {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    display: flex;
    align-items: flex-start;
    gap: 14px;
    transition: border-color 0.25s, transform 0.25s;
  }
  .about-item:hover { border-color: rgba(0,212,170,0.3); transform: translateY(-3px); }

  .about-icon {
    font-size: 20px;
    width: 40px;
    height: 40px;
    background: var(--surface);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    border: 1px solid var(--border);
  }

  .about-text { font-size: 13px; line-height: 1.6; color: var(--muted); }
  .about-text strong { color: var(--text); font-weight: 600; display: block; margin-bottom: 2px; font-size: 14px; }

  /* ── SKILLS ── */
  .skills-section { animation: fadeUp 0.8s 0.3s ease both; }

  .skill-group { margin-bottom: 24px; }
  .skill-group-label {
    font-size: 12px;
    font-family: 'JetBrains Mono', monospace;
    color: var(--muted);
    margin-bottom: 12px;
    letter-spacing: 1px;
  }

  .skill-pills { display: flex; flex-wrap: wrap; gap: 8px; }
  .pill {
    padding: 6px 14px;
    border-radius: 8px;
    font-size: 13px;
    font-weight: 600;
    border: 1px solid var(--border);
    background: var(--card);
    color: var(--text);
    transition: all 0.2s;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .pill:hover { border-color: var(--accent); color: var(--accent); transform: translateY(-2px); }
  .pill .dot { width: 7px; height: 7px; border-radius: 50%; }
  .dot-html  { background: #e34c26; }
  .dot-css   { background: #264de4; }
  .dot-js    { background: #f7df1e; }
  .dot-react { background: #61dafb; }
  .dot-py    { background: #3572a5; }
  .dot-git   { background: #f05032; }
  .dot-node  { background: #68a063; }
  .dot-sql   { background: #00758f; }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 16px;
    animation: fadeUp 0.8s 0.4s ease both;
  }

  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 24px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.25s, transform 0.25s;
  }
  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    opacity: 0;
    transition: opacity 0.25s;
  }
  .project-card:hover { border-color: rgba(0,212,170,0.25); transform: translateY(-4px); }
  .project-card:hover::before { opacity: 1; }

  .project-icon { font-size: 24px; margin-bottom: 14px; }

  .project-title {
    font-size: 15px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 8px;
  }

  .project-desc { font-size: 13px; color: var(--muted); line-height: 1.6; margin-bottom: 16px; }

  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .tag {
    font-size: 11px;
    font-family: 'JetBrains Mono', monospace;
    padding: 3px 9px;
    border-radius: 5px;
    background: var(--surface);
    border: 1px solid var(--border);
    color: var(--muted);
  }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 14px;
    animation: fadeUp 0.8s 0.5s ease both;
  }

  .stat-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    transition: border-color 0.25s, transform 0.25s;
  }
  .stat-card:hover { border-color: rgba(124,106,247,0.35); transform: translateY(-3px); }

  .stat-number {
    font-size: 28px;
    font-weight: 700;
    font-family: 'JetBrains Mono', monospace;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .stat-label { font-size: 12px; color: var(--muted); margin-top: 4px; letter-spacing: 0.5px; }

  /* ── CONNECT ── */
  .connect-row {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 12px;
    animation: fadeUp 0.8s 0.6s ease both;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 9px;
    padding: 11px 22px;
    border-radius: 10px;
    font-size: 14px;
    font-weight: 600;
    border: 1px solid var(--border);
    background: var(--card);
    color: var(--text);
    text-decoration: none;
    transition: all 0.25s;
    cursor: pointer;
  }
  .connect-btn:hover { border-color: var(--accent); color: var(--accent); transform: translateY(-2px); background: rgba(0,212,170,0.04); }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding: 40px 0 10px;
    font-size: 13px;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    animation: fadeUp 0.8s 0.7s ease both;
  }
  .footer span { color: var(--accent); }

  /* ── ANIMATION ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── GITHUB FRAME ── */
  .github-frame {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 30px 80px rgba(0,0,0,0.5);
  }

  .frame-bar {
    background: #1a1d25;
    border-bottom: 1px solid var(--border);
    padding: 14px 20px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .dot-r { width: 12px; height: 12px; border-radius: 50%; background: #ff5f57; }
  .dot-y { width: 12px; height: 12px; border-radius: 50%; background: #febc2e; }
  .dot-g { width: 12px; height: 12px; border-radius: 50%; background: #28c840; }
  .frame-url {
    margin-left: 12px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: var(--muted);
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 4px 12px;
    flex: 1;
    max-width: 280px;
  }

  .frame-content { padding: 0 40px 40px; }
</style>
</head>
<body>
<div class="container">
  <div class="github-frame">
    <div class="frame-bar">
      <div class="dot-r"></div>
      <div class="dot-y"></div>
      <div class="dot-g"></div>
      <div class="frame-url">github.com/Satyanarayana001</div>
    </div>
    <div class="frame-content">

      <!-- HEADER -->
      <div class="header">
        <div class="greeting">console.log("Welcome to my profile")</div>
        <h1>Satyanarayana<br>Kotar</h1>
        <p class="tagline">
          <strong>CSE Student</strong> @ BVC Engineering College &nbsp;·&nbsp;
          <strong>Aspiring SDE</strong> &nbsp;·&nbsp; Full Stack &amp; AI Enthusiast
        </p>
        <div class="badges">
          <span class="badge badge-green">🎓 3rd Year B.Tech</span>
          <span class="badge badge-purple">🚀 SDE Intern Seeker</span>
          <span class="badge badge-orange">🏆 Hackathon Participant</span>
          <span class="badge badge-blue">📍 Odalarevu, AP</span>
        </div>
      </div>

      <div class="divider"></div>

      <!-- ABOUT -->
      <div class="section-title">About Me</div>
      <div class="about-grid">
        <div class="about-item">
          <div class="about-icon">🔭</div>
          <div class="about-text">
            <strong>Currently Building</strong>
            Full Stack web apps with React & Node.js
          </div>
        </div>
        <div class="about-item">
          <div class="about-icon">🌱</div>
          <div class="about-text">
            <strong>Learning</strong>
            DSA, System Design & AI integration
          </div>
        </div>
        <div class="about-item">
          <div class="about-icon">🎯</div>
          <div class="about-text">
            <strong>Goal</strong>
            Land an SDE internship at a top tech company
          </div>
        </div>
        <div class="about-item">
          <div class="about-icon">⚡</div>
          <div class="about-text">
            <strong>Fun Fact</strong>
            I debug code faster with coffee ☕
          </div>
        </div>
      </div>

      <div class="divider"></div>

      <!-- SKILLS -->
      <div class="section-title">Tech Stack</div>
      <div class="skills-section">
        <div class="skill-group">
          <div class="skill-group-label">// Frontend</div>
          <div class="skill-pills">
            <span class="pill"><span class="dot dot-html"></span>HTML5</span>
            <span class="pill"><span class="dot dot-css"></span>CSS3</span>
            <span class="pill"><span class="dot dot-js"></span>JavaScript</span>
            <span class="pill"><span class="dot dot-react"></span>React</span>
          </div>
        </div>
        <div class="skill-group">
          <div class="skill-group-label">// Backend & Tools</div>
          <div class="skill-pills">
            <span class="pill"><span class="dot dot-py"></span>Python</span>
            <span class="pill"><span class="dot dot-node"></span>Node.js</span>
            <span class="pill"><span class="dot dot-sql"></span>SQL</span>
            <span class="pill"><span class="dot dot-git"></span>Git & GitHub</span>
          </div>
        </div>
      </div>

      <div class="divider"></div>

      <!-- PROJECTS -->
      <div class="section-title">Featured Projects</div>
      <div class="projects-grid">
        <div class="project-card">
          <div class="project-icon">🔐</div>
          <div class="project-title">Password Generator</div>
          <div class="project-desc">Secure, customizable password generator with strength indicator and copy-to-clipboard functionality.</div>
          <div class="project-tags">
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
            <span class="tag">JavaScript</span>
          </div>
        </div>
        <div class="project-card">
          <div class="project-icon">🌐</div>
          <div class="project-title">Portfolio Website</div>
          <div class="project-desc">Personal portfolio showcasing projects, skills, and experience. Fully responsive with smooth animations.</div>
          <div class="project-tags">
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
            <span class="tag">JavaScript</span>
          </div>
        </div>
        <div class="project-card">
          <div class="project-icon">📚</div>
          <div class="project-title">FSD Practice Projects</div>
          <div class="project-desc">A collection of full stack development exercises exploring modern web development patterns.</div>
          <div class="project-tags">
            <span class="tag">React</span>
            <span class="tag">Node.js</span>
            <span class="tag">HTML/CSS</span>
          </div>
        </div>
      </div>

      <div class="divider"></div>

      <!-- STATS -->
      <div class="section-title">GitHub Stats</div>
      <div class="stats-grid">
        <div class="stat-card">
          <div class="stat-number">23+</div>
          <div class="stat-label">Repositories</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">HTML</div>
          <div class="stat-label">Top Language</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">3rd</div>
          <div class="stat-label">Year B.Tech</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">∞</div>
          <div class="stat-label">Coffee Consumed</div>
        </div>
      </div>

      <div class="divider"></div>

      <!-- CONNECT -->
      <div class="section-title">Let's Connect</div>
      <div class="connect-row">
        <span class="connect-btn">📧 Gmail</span>
        <span class="connect-btn">💼 LinkedIn</span>
        <span class="connect-btn">🐙 GitHub</span>
        <span class="connect-btn">🌐 Portfolio</span>
      </div>

      <!-- FOOTER -->
      <div class="footer">
        <span>⭐</span> &nbsp; "Keep learning. Keep building." &nbsp; <span>⭐</span>
        <br><br>
        <div style="color:#2a2e3d; font-size:11px; margin-top:4px;">
          Profile views counter · Last updated March 2026
        </div>
      </div>

    </div>
  </div>
</div>
</body>
</html>
