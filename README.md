<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SYED SHAHE SYED SHAHE SUHEL — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=DM+Mono:wght@300;400;500&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0a0a0f;
    --bg2: #111118;
    --bg3: #1a1a24;
    --surface: #1e1e2a;
    --border: rgba(255,255,255,0.08);
    --border2: rgba(255,255,255,0.14);
    --text: #e8e8f0;
    --muted: #8888a8;
    --accent: #7c6bff;
    --accent2: #b49aff;
    --glow: rgba(124,107,255,0.15);
    --coral: #ff6b6b;
    --teal: #4ecdc4;
    --amber: #ffd93d;
    --green: #6bcb77;
    --font-display: 'Playfair Display', serif;
    --font-mono: 'DM Mono', monospace;
    --font-body: 'DM Sans', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-body);
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* SCROLLBAR */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--accent); border-radius: 2px; }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; justify-content: space-between; align-items: center;
    padding: 1.25rem 4rem;
    background: rgba(10,10,15,0.85);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo {
    font-family: var(--font-mono);
    font-size: 0.9rem;
    color: var(--accent2);
    letter-spacing: 0.05em;
  }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-size: 0.85rem;
    color: var(--muted);
    text-decoration: none;
    letter-spacing: 0.05em;
    font-family: var(--font-mono);
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent2); }

  /* SECTIONS */
  section { position: relative; }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    display: flex; flex-direction: column; justify-content: center;
    padding: 8rem 4rem 4rem;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background: radial-gradient(ellipse 80% 60% at 60% 40%, rgba(124,107,255,0.12) 0%, transparent 60%),
                radial-gradient(ellipse 40% 40% at 10% 80%, rgba(78,205,196,0.08) 0%, transparent 50%);
  }
  .hero-grid {
    position: absolute; inset: 0;
    background-image:
      linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
    background-size: 60px 60px;
    mask-image: radial-gradient(ellipse 80% 80% at 50% 50%, black 20%, transparent 70%);
  }
  .hero-content { position: relative; max-width: 900px; }
  .hero-tag {
    display: inline-flex; align-items: center; gap: 0.5rem;
    font-family: var(--font-mono); font-size: 0.8rem; color: var(--accent2);
    background: rgba(124,107,255,0.1); border: 1px solid rgba(124,107,255,0.25);
    padding: 0.35rem 0.9rem; border-radius: 20px;
    margin-bottom: 1.5rem; letter-spacing: 0.05em;
  }
  .hero-tag::before { content: ''; width: 6px; height: 6px; background: var(--accent); border-radius: 50%; animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.5;transform:scale(1.3)} }
  .hero-name {
    font-family: var(--font-display);
    font-size: clamp(3.5rem, 8vw, 7rem);
    line-height: 1.05;
    letter-spacing: -0.02em;
    margin-bottom: 0.5rem;
  }
  .hero-name em { color: var(--accent2); font-style: italic; }
  .hero-title {
    font-family: var(--font-mono);
    font-size: clamp(1rem, 2.5vw, 1.4rem);
    color: var(--muted);
    margin-bottom: 1.5rem;
    letter-spacing: 0.02em;
  }
  .hero-title span { color: var(--teal); }
  .hero-desc {
    max-width: 500px; font-size: 1.05rem; color: var(--muted);
    line-height: 1.8; margin-bottom: 2.5rem;
  }
  .hero-ctas { display: flex; gap: 1rem; flex-wrap: wrap; }
  .btn-primary {
    padding: 0.8rem 2rem;
    background: var(--accent);
    color: #fff; border: none; border-radius: 8px;
    font-size: 0.9rem; font-family: var(--font-body); font-weight: 500;
    cursor: pointer; text-decoration: none;
    transition: all 0.2s;
    box-shadow: 0 0 30px rgba(124,107,255,0.3);
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 0 40px rgba(124,107,255,0.5); }
  .btn-ghost {
    padding: 0.8rem 2rem;
    background: transparent;
    color: var(--text); border: 1px solid var(--border2);
    border-radius: 8px; font-size: 0.9rem; font-family: var(--font-body);
    cursor: pointer; text-decoration: none;
    transition: all 0.2s;
  }
  .btn-ghost:hover { border-color: var(--accent2); color: var(--accent2); }
  .hero-scroll {
    position: absolute; bottom: 2.5rem; left: 4rem;
    display: flex; align-items: center; gap: 0.75rem;
    font-family: var(--font-mono); font-size: 0.75rem; color: var(--muted);
  }
  .scroll-line {
    width: 40px; height: 1px;
    background: linear-gradient(90deg, transparent, var(--muted));
    animation: expand 2s ease-in-out infinite;
  }
  @keyframes expand { 0%,100%{width:20px;opacity:0.4} 50%{width:50px;opacity:1} }

  /* ── ABOUT ── */
  #about {
    padding: 7rem 4rem;
    background: var(--bg2);
  }
  .section-label {
    font-family: var(--font-mono); font-size: 0.75rem;
    color: var(--accent); letter-spacing: 0.15em;
    text-transform: uppercase; margin-bottom: 1rem;
  }
  .about-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 5rem;
    max-width: 1100px; margin: 0 auto;
    align-items: center;
  }
  .about-visual {
    position: relative; display: flex; justify-content: center;
  }
  .about-avatar {
    width: 320px; height: 380px;
    background: var(--bg3);
    border-radius: 24px;
    border: 1px solid var(--border2);
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    position: relative; overflow: hidden;
  }
  .avatar-glow {
    position: absolute;
    width: 200px; height: 200px;
    background: radial-gradient(circle, rgba(124,107,255,0.3), transparent 70%);
    top: -50px; left: 50%; transform: translateX(-50%);
  }
  .avatar-initials {
    font-family: var(--font-display);
    font-size: 5rem; color: var(--accent2); position: relative; z-index: 1;
  }
  .avatar-name {
    font-family: var(--font-mono); font-size: 0.85rem;
    color: var(--muted); margin-top: 0.5rem; position: relative; z-index: 1;
  }
  .floating-badge {
    position: absolute;
    background: var(--surface); border: 1px solid var(--border2);
    border-radius: 12px; padding: 0.6rem 1rem;
    font-family: var(--font-mono); font-size: 0.75rem;
    display: flex; align-items: center; gap: 0.5rem;
  }
  .floating-badge.top-right { top: -10px; right: -20px; }
  .floating-badge.bottom-left { bottom: 20px; left: -30px; }
  .badge-dot { width: 8px; height: 8px; border-radius: 50%; }
  .about-text h2 {
    font-family: var(--font-display);
    font-size: clamp(2rem, 4vw, 3rem);
    line-height: 1.2; margin-bottom: 1.5rem;
  }
  .about-text h2 span { color: var(--accent2); font-style: italic; }
  .about-text p { color: var(--muted); line-height: 1.9; margin-bottom: 1.2rem; }
  .about-stats {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 1rem; margin-top: 2rem;
  }
  .stat-card {
    background: var(--bg3); border: 1px solid var(--border);
    border-radius: 12px; padding: 1.25rem;
    text-align: center;
  }
  .stat-number {
    font-family: var(--font-display);
    font-size: 2rem; color: var(--accent2); display: block;
  }
  .stat-label { font-size: 0.75rem; color: var(--muted); font-family: var(--font-mono); }

  /* ── SKILLS ── */
  #skills {
    padding: 7rem 4rem;
    background: var(--bg);
  }
  .skills-header {
    max-width: 600px; margin: 0 auto 4rem; text-align: center;
  }
  .skills-header h2 {
    font-family: var(--font-display);
    font-size: clamp(2rem, 4vw, 3rem); margin-bottom: 1rem;
  }
  .skills-header p { color: var(--muted); }
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 1.5rem; max-width: 1100px; margin: 0 auto;
  }
  .skill-category {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: 16px; padding: 1.75rem;
    transition: border-color 0.3s, transform 0.2s;
  }
  .skill-category:hover {
    border-color: var(--border2); transform: translateY(-3px);
  }
  .skill-cat-header {
    display: flex; align-items: center; gap: 0.75rem; margin-bottom: 1.25rem;
  }
  .skill-icon {
    width: 36px; height: 36px; border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem;
  }
  .skill-cat-name {
    font-size: 0.95rem; font-weight: 600; color: var(--text);
  }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .skill-tag {
    font-family: var(--font-mono); font-size: 0.75rem;
    padding: 0.3rem 0.75rem; border-radius: 6px;
    border: 1px solid;
  }
  .tag-purple { color: var(--accent2); border-color: rgba(124,107,255,0.3); background: rgba(124,107,255,0.08); }
  .tag-teal   { color: var(--teal); border-color: rgba(78,205,196,0.3); background: rgba(78,205,196,0.08); }
  .tag-coral  { color: var(--coral); border-color: rgba(255,107,107,0.3); background: rgba(255,107,107,0.08); }
  .tag-amber  { color: var(--amber); border-color: rgba(255,217,61,0.3); background: rgba(255,217,61,0.08); }
  .tag-green  { color: var(--green); border-color: rgba(107,203,119,0.3); background: rgba(107,203,119,0.08); }

  /* ── PROJECTS ── */
  #projects {
    padding: 7rem 4rem;
    background: var(--bg2);
  }
  .projects-header {
    max-width: 600px; margin: 0 auto 4rem; text-align: center;
  }
  .projects-header h2 {
    font-family: var(--font-display);
    font-size: clamp(2rem, 4vw, 3rem); margin-bottom: 1rem;
  }
  .projects-grid {
    display: grid; grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
    gap: 1.5rem; max-width: 1100px; margin: 0 auto;
  }
  .project-card {
    background: var(--bg3); border: 1px solid var(--border);
    border-radius: 20px; overflow: hidden;
    transition: border-color 0.3s, transform 0.3s;
    display: flex; flex-direction: column;
  }
  .project-card:hover { border-color: var(--accent); transform: translateY(-4px); }
  .project-thumb {
    height: 180px; position: relative; overflow: hidden;
    display: flex; align-items: center; justify-content: center;
  }
  .project-emoji { font-size: 3.5rem; position: relative; z-index: 1; }
  .project-body { padding: 1.5rem; flex: 1; display: flex; flex-direction: column; }
  .project-meta {
    display: flex; align-items: center; justify-content: space-between;
    margin-bottom: 0.75rem;
  }
  .project-year {
    font-family: var(--font-mono); font-size: 0.7rem; color: var(--muted);
  }
  .project-status {
    font-family: var(--font-mono); font-size: 0.7rem;
    padding: 0.2rem 0.6rem; border-radius: 20px;
  }
  .status-live { color: var(--green); background: rgba(107,203,119,0.1); }
  .status-wip  { color: var(--amber); background: rgba(255,217,61,0.1); }
  .project-title {
    font-family: var(--font-display);
    font-size: 1.4rem; margin-bottom: 0.6rem;
  }
  .project-desc { color: var(--muted); font-size: 0.9rem; line-height: 1.7; margin-bottom: 1.25rem; flex: 1; }
  .project-stack { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-bottom: 1.25rem; }
  .project-stack span {
    font-family: var(--font-mono); font-size: 0.7rem; color: var(--muted);
    background: var(--surface); border: 1px solid var(--border);
    padding: 0.2rem 0.6rem; border-radius: 4px;
  }
  .project-links { display: flex; gap: 0.75rem; }
  .proj-link {
    font-size: 0.8rem; font-family: var(--font-mono);
    color: var(--accent2); text-decoration: none;
    border: 1px solid rgba(124,107,255,0.3);
    padding: 0.4rem 0.9rem; border-radius: 6px;
    transition: all 0.2s;
  }
  .proj-link:hover { background: rgba(124,107,255,0.1); }

  /* ── CONTACT ── */
  #contact {
    padding: 7rem 4rem;
    background: var(--bg);
  }
  .contact-inner {
    max-width: 700px; margin: 0 auto; text-align: center;
  }
  .contact-inner h2 {
    font-family: var(--font-display);
    font-size: clamp(2rem, 4vw, 3.5rem); margin-bottom: 1rem;
  }
  .contact-inner h2 em { color: var(--accent2); font-style: italic; }
  .contact-inner > p { color: var(--muted); margin-bottom: 3rem; }
  .contact-form {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: 20px; padding: 2.5rem;
    text-align: left;
  }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-bottom: 1rem; }
  .form-group { display: flex; flex-direction: column; gap: 0.5rem; }
  .form-group label {
    font-family: var(--font-mono); font-size: 0.75rem; color: var(--muted);
    letter-spacing: 0.05em;
  }
  .form-group input,
  .form-group textarea {
    background: var(--bg3); border: 1px solid var(--border);
    border-radius: 10px; padding: 0.85rem 1rem;
    color: var(--text); font-family: var(--font-body); font-size: 0.95rem;
    transition: border-color 0.2s, box-shadow 0.2s;
    outline: none; width: 100%;
  }
  .form-group textarea { resize: vertical; min-height: 130px; }
  .form-group input:focus,
  .form-group textarea:focus {
    border-color: var(--accent);
    box-shadow: 0 0 0 3px rgba(124,107,255,0.15);
  }
  .form-group.full { margin-bottom: 1rem; }
  .form-submit {
    width: 100%; padding: 1rem;
    background: var(--accent); color: #fff;
    border: none; border-radius: 10px;
    font-size: 0.95rem; font-weight: 600; font-family: var(--font-body);
    cursor: pointer; transition: all 0.2s; margin-top: 0.5rem;
  }
  .form-submit:hover { background: var(--accent2); transform: translateY(-1px); }
  .form-success {
    display: none; text-align: center; padding: 2rem;
    color: var(--green); font-family: var(--font-mono); font-size: 0.9rem;
  }

  /* ── CHATBOT ── */
  #chatbot {
    padding: 7rem 4rem;
    background: var(--bg2);
  }
  .chatbot-container {
    max-width: 750px; margin: 0 auto;
  }
  .chatbot-header { text-align: center; margin-bottom: 2rem; }
  .chatbot-header h2 {
    font-family: var(--font-display);
    font-size: clamp(2rem, 4vw, 3rem); margin-bottom: 0.75rem;
  }
  .chatbot-header p { color: var(--muted); }
  .chat-window {
    background: var(--bg3); border: 1px solid var(--border);
    border-radius: 20px; overflow: hidden;
  }
  .chat-topbar {
    display: flex; align-items: center; gap: 0.75rem;
    padding: 1rem 1.25rem;
    border-bottom: 1px solid var(--border);
    background: var(--surface);
  }
  .chat-topbar-dots { display: flex; gap: 5px; }
  .chat-topbar-dots span {
    width: 10px; height: 10px; border-radius: 50%;
  }
  .dot-r { background: #ff5f57; }
  .dot-y { background: #ffbd2e; }
  .dot-g { background: #28c840; }
  .chat-topbar-title {
    font-family: var(--font-mono); font-size: 0.8rem; color: var(--muted);
    margin-left: 0.5rem;
  }
  .chat-online {
    margin-left: auto; display: flex; align-items: center; gap: 0.4rem;
    font-family: var(--font-mono); font-size: 0.7rem; color: var(--green);
  }
  .chat-online::before { content: ''; width: 6px; height: 6px; background: var(--green); border-radius: 50%; animation: pulse 2s infinite; }
  .chat-messages {
    height: 380px; overflow-y: auto; padding: 1.5rem; display: flex; flex-direction: column; gap: 1rem;
  }
  .chat-messages::-webkit-scrollbar { width: 3px; }
  .chat-messages::-webkit-scrollbar-thumb { background: var(--border2); }
  .msg { display: flex; gap: 0.75rem; align-items: flex-start; }
  .msg.user { flex-direction: row-reverse; }
  .msg-avatar {
    width: 32px; height: 32px; border-radius: 50%; flex-shrink: 0;
    display: flex; align-items: center; justify-content: center;
    font-size: 0.8rem; font-weight: 600;
  }
  .ai-avatar { background: rgba(124,107,255,0.2); color: var(--accent2); border: 1px solid rgba(124,107,255,0.3); }
  .user-avatar { background: rgba(78,205,196,0.2); color: var(--teal); border: 1px solid rgba(78,205,196,0.3); }
  .msg-bubble {
    max-width: 75%; padding: 0.75rem 1rem;
    border-radius: 16px; font-size: 0.9rem; line-height: 1.6;
  }
  .ai-bubble {
    background: var(--surface); border: 1px solid var(--border);
    border-bottom-left-radius: 4px; color: var(--text);
  }
  .user-bubble {
    background: rgba(124,107,255,0.2); border: 1px solid rgba(124,107,255,0.3);
    border-bottom-right-radius: 4px; color: var(--text);
  }
  .msg-time { font-size: 0.7rem; color: var(--muted); margin-top: 0.25rem; font-family: var(--font-mono); }
  .typing { display: flex; gap: 4px; align-items: center; padding: 0.6rem 0.2rem; }
  .typing span {
    width: 7px; height: 7px; background: var(--muted); border-radius: 50%;
    animation: bounce 1.2s ease-in-out infinite;
  }
  .typing span:nth-child(2) { animation-delay: 0.2s; }
  .typing span:nth-child(3) { animation-delay: 0.4s; }
  @keyframes bounce { 0%,80%,100%{transform:translateY(0)} 40%{transform:translateY(-6px)} }
  .chat-inputarea {
    border-top: 1px solid var(--border);
    padding: 1rem 1.25rem;
    display: flex; gap: 0.75rem; align-items: center;
  }
  .chat-input {
    flex: 1; background: var(--bg); border: 1px solid var(--border);
    border-radius: 12px; padding: 0.75rem 1rem;
    color: var(--text); font-family: var(--font-body); font-size: 0.9rem;
    outline: none; transition: border-color 0.2s;
  }
  .chat-input:focus { border-color: var(--accent); }
  .chat-send {
    background: var(--accent); border: none; border-radius: 12px;
    padding: 0.75rem 1.25rem; color: #fff; cursor: pointer;
    font-size: 0.85rem; font-family: var(--font-body); font-weight: 500;
    transition: all 0.2s; white-space: nowrap;
  }
  .chat-send:hover { background: var(--accent2); transform: scale(1.02); }
  .chat-send:disabled { opacity: 0.5; cursor: not-allowed; transform: none; }
  .chat-suggestions {
    padding: 0 1.25rem 1rem;
    display: flex; flex-wrap: wrap; gap: 0.5rem;
  }
  .suggestion-chip {
    font-family: var(--font-mono); font-size: 0.72rem;
    color: var(--muted); background: var(--surface);
    border: 1px solid var(--border); border-radius: 20px;
    padding: 0.3rem 0.75rem; cursor: pointer; transition: all 0.2s;
  }
  .suggestion-chip:hover { color: var(--accent2); border-color: rgba(124,107,255,0.4); }

  /* FOOTER */
  footer {
    text-align: center; padding: 2rem;
    border-top: 1px solid var(--border);
    font-family: var(--font-mono); font-size: 0.75rem; color: var(--muted);
  }

  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { gap: 1.5rem; }
    #hero, #about, #skills, #projects, #contact, #chatbot { padding: 5rem 1.5rem; }
    .about-grid { grid-template-columns: 1fr; gap: 3rem; }
    .about-avatar { width: 100%; max-width: 300px; margin: 0 auto; }
    .form-row { grid-template-columns: 1fr; }
    .hero-scroll { left: 1.5rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">// SYED SHAHE SUHEL.</div>
  <ul class="nav-links">
    <li><a href="#about">about</a></li>
    <li><a href="#skills">skills</a></li>
    <li><a href="#projects">projects</a></li>
    <li><a href="#contact">contact</a></li>
    <li><a href="#chatbot">chat</a></li>
  </ul>
</nav>

<!-- ① HERO -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-content">
    <div class="hero-tag">Available for freelance &amp; full-time</div>
    <h1 class="hero-name">SYED SHAHE SUHEL <em>Chen</em></h1>
    <p class="hero-title">Full-Stack Engineer &nbsp;/&nbsp; <span>UI/UX Designer</span> &nbsp;/&nbsp; Open Source</p>
    <p class="hero-desc">I build thoughtful digital experiences — from sleek interfaces to robust backends. Obsessed with the craft of software and the art of simplicity.</p>
    <div class="hero-ctas">
      <a href="#projects" class="btn-primary">View My Work</a>
      <a href="#contact" class="btn-ghost">Get in Touch</a>
    </div>
  </div>
  <div class="hero-scroll">
    <div class="scroll-line"></div>
    <span>scroll to explore</span>
  </div>
</section>

<!-- ② ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-visual">
      <div class="about-avatar">
        <div class="avatar-glow"></div>
        <div class="avatar-initials">AC</div>
        <div class="avatar-name">@SYED SHAHE SUHELchen.dev</div>
      </div>
      <div class="floating-badge top-right">
        <div class="badge-dot" style="background:var(--green)"></div>
        <span>Open to work</span>
      </div>
      <div class="floating-badge bottom-left">
        <span>📍sage university, INDIA</span>
      </div>
    </div>
    <div class="about-text">
      <div class="section-label">// about me</div>.
      <h2>Turning ideas into <span>elegant</span> code</h2>
      <p>Hey! I'm SYED SHAHE SUHEL — an ai engneering student studying 2nd year from sage university bhopal. has completed 12 guithub projects and 15 projects shipped and completed 2 internships .</p>
      <div class="about-stats">
        <div class="stat-card">
          <span class="stat-number">2+</span>
          <span class="stat-label">years exp</span>
        </div>
        <div class="stat-card">
          <span class="stat-number">15</span>
          <span class="stat-label">projects shipped</span>
        </div>
        <div class="stat-card">
          <span class="stat-number">12</span>
          <span class="stat-label">GitHub stars</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ③ SKILLS -->
<section id="skills">
  <div class="skills-header">
    <div class="section-label">// skills & tools</div>
    <h2>What I Work With</h2>
    <p style="color:var(--muted)">A curated toolkit built over years of shipping real products</p>
  </div>
  <div class="skills-grid">
    <div class="skill-category">
      <div class="skill-cat-header">
        <div class="skill-icon" style="background:rgba(124,107,255,0.15)">⚡</div>
        <div class="skill-cat-name">Frontend</div>
      </div>
      <div class="skill-tags">
        <span class="skill-tag tag-purple">React</span>
        <span class="skill-tag tag-purple">Next.js</span>
        <span class="skill-tag tag-purple">TypeScript</span>
        <span class="skill-tag tag-purple">Tailwind CSS</span>
        <span class="skill-tag tag-purple">Framer Motion</span>
        <span class="skill-tag tag-purple">Three.js</span>
      </div>
    </div>
    <div class="skill-category">
      <div class="skill-cat-header">
        <div class="skill-icon" style="background:rgba(78,205,196,0.15)">🔧</div>
        <div class="skill-cat-name">Backend</div>
      </div>
      <div class="skill-tags">
        <span class="skill-tag tag-teal">Node.js</span>
        <span class="skill-tag tag-teal">Python</span>
        <span class="skill-tag tag-teal">FastAPI</span>
        <span class="skill-tag tag-teal">GraphQL</span>
        <span class="skill-tag tag-teal">REST APIs</span>
        <span class="skill-tag tag-teal">PostgreSQL</span>
      </div>
    </div>
    <div class="skill-category">
      <div class="skill-cat-header">
        <div class="skill-icon" style="background:rgba(255,107,107,0.15)">🤖</div>
        <div class="skill-cat-name">AI / ML</div>
      </div>
      <div class="skill-tags">
        <span class="skill-tag tag-coral">Claude API</span>
        <span class="skill-tag tag-coral">OpenAI</span>
        <span class="skill-tag tag-coral">LangChain</span>
        <span class="skill-tag tag-coral">RAG</span>
        <span class="skill-tag tag-coral">Embeddings</span>
        <span class="skill-tag tag-coral">Fine-tuning</span>
      </div>
    </div>
    <div class="skill-category">
      <div class="skill-cat-header">
        <div class="skill-icon" style="background:rgba(255,217,61,0.15)">☁️</div>
        <div class="skill-cat-name">DevOps & Cloud</div>
      </div>
      <div class="skill-tags">
        <span class="skill-tag tag-amber">AWS</span>
        <span class="skill-tag tag-amber">Docker</span>
        <span class="skill-tag tag-amber">Kubernetes</span>
        <span class="skill-tag tag-amber">Terraform</span>
        <span class="skill-tag tag-amber">CI/CD</span>
        <span class="skill-tag tag-amber">Vercel</span>
      </div>
    </div>
    <div class="skill-category">
      <div class="skill-cat-header">
        <div class="skill-icon" style="background:rgba(107,203,119,0.15)">🎨</div>
        <div class="skill-cat-name">Design</div>
      </div>
      <div class="skill-tags">
        <span class="skill-tag tag-green">Figma</span>
        <span class="skill-tag tag-green">Design Systems</span>
        <span class="skill-tag tag-green">Prototyping</span>
        <span class="skill-tag tag-green">UX Research</span>
        <span class="skill-tag tag-green">Accessibility</span>
      </div>
    </div>
    <div class="skill-category">
      <div class="skill-cat-header">
        <div class="skill-icon" style="background:rgba(124,107,255,0.15)">🗄️</div>
        <div class="skill-cat-name">Databases</div>
      </div>
      <div class="skill-tags">
        <span class="skill-tag tag-purple">PostgreSQL</span>
        <span class="skill-tag tag-purple">MongoDB</span>
        <span class="skill-tag tag-purple">Redis</span>
        <span class="skill-tag tag-purple">Supabase</span>
        <span class="skill-tag tag-purple">Prisma</span>
        <span class="skill-tag tag-purple">Pinecone</span>
      </div>
    </div>
  </div>
</section>

<!-- ④ PROJECTS -->
<section id="projects">
  <div class="projects-header">
    <div class="section-label">// selected work</div>
    <h2>Projects</h2>
    <p style="color:var(--muted)">Things I've built that I'm proud of</p>
  </div>
  <div class="projects-grid">

    <div class="project-card">
      <div class="project-thumb" style="background:linear-gradient(135deg,#1a1230,#2d1f5e)">
        <div class="project-emoji">🚀</div>
      </div>
      <div class="project-body">
        <div class="project-meta">
          <span class="project-year">2024</span>
          <span class="project-status status-live">● Live</span>
        </div>
        <div class="project-title">Orbit — SaaS Dashboard</div>
        <p class="project-desc">Analytics platform for e-commerce teams. Real-time data visualization, AI-powered insights, multi-tenant architecture serving 500+ clients.</p>
        <div class="project-stack">
          <span>Next.js</span><span>TypeScript</span><span>PostgreSQL</span><span>Redis</span><span>AWS</span>
        </div>
        <div class="project-links">
          <a href="#" class="proj-link">↗ Live Demo</a>
          <a href="#" class="proj-link">GitHub</a>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-thumb" style="background:linear-gradient(135deg,#0d2a2a,#0f4a45)">
        <div class="project-emoji">🧠</div>
      </div>
      <div class="project-body">
        <div class="project-meta">
          <span class="project-year">2024</span>
          <span class="project-status status-live">● Live</span>
        </div>
        <div class="project-title">Mnemonic — AI Study App</div>
        <p class="project-desc">Adaptive learning platform using spaced repetition + Claude AI to generate personalized flashcards and quizzes from any document.</p>
        <div class="project-stack">
          <span>React</span><span>Python</span><span>FastAPI</span><span>Claude API</span><span>Pinecone</span>
        </div>
        <div class="project-links">
          <a href="#" class="proj-link">↗ Live Demo</a>
          <a href="#" class="proj-link">GitHub</a>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-thumb" style="background:linear-gradient(135deg,#2a1a0d,#5e3a1a)">
        <div class="project-emoji">🗺️</div>
      </div>
      <div class="project-body">
        <div class="project-meta">
          <span class="project-year">2023</span>
          <span class="project-status status-wip">◐ WIP</span>
        </div>
        <div class="project-title">Pathfinder — Travel OS</div>
        <p class="project-desc">All-in-one travel planning tool. Collaborative itineraries, budget tracking, packing lists, and offline maps. 15k+ downloads on iOS.</p>
        <div class="project-stack">
          <span>React Native</span><span>Expo</span><span>Node.js</span><span>MongoDB</span>
        </div>
        <div class="project-links">
          <a href="#" class="proj-link">↗ App Store</a>
          <a href="#" class="proj-link">GitHub</a>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-thumb" style="background:linear-gradient(135deg,#1a0d2a,#3a1a5e)">
        <div class="project-emoji">⚙️</div>
      </div>
      <div class="project-body">
        <div class="project-meta">
          <span class="project-year">2023</span>
          <span class="project-status status-live">● Live</span>
        </div>
        <div class="project-title">FlowKit — UI Component Lib</div>
        <p class="project-desc">Open-source React component library with 80+ accessible, customizable components. 4.2k GitHub stars, 200+ contributors worldwide.</p>
        <div class="project-stack">
          <span>React</span><span>TypeScript</span><span>Storybook</span><span>Radix UI</span>
        </div>
        <div class="project-links">
          <a href="#" class="proj-link">↗ Docs</a>
          <a href="#" class="proj-link">GitHub</a>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-thumb" style="background:linear-gradient(135deg,#0d1a2a,#1a3a5e)">
        <div class="project-emoji">🔐</div>
      </div>
      <div class="project-body">
        <div class="project-meta">
          <span class="project-year">2022</span>
          <span class="project-status status-live">● Live</span>
        </div>
        <div class="project-title">Vault — Password Manager</div>
        <p class="project-desc">End-to-end encrypted password manager with zero-knowledge architecture. Browser extension + mobile app. Audited by Trail of Bits.</p>
        <div class="project-stack">
          <span>Electron</span><span>Rust</span><span>WebAssembly</span><span>AES-256</span>
        </div>
        <div class="project-links">
          <a href="#" class="proj-link">↗ Download</a>
          <a href="#" class="proj-link">GitHub</a>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-thumb" style="background:linear-gradient(135deg,#1a2a0d,#3a5e1a)">
        <div class="project-emoji">📊</div>
      </div>
      <div class="project-body">
        <div class="project-meta">
          <span class="project-year">2022</span>
          <span class="project-status status-live">● Live</span>
        </div>
        <div class="project-title">Pulse — Dev Metrics CLI</div>
        <p class="project-desc">Terminal tool for tracking team velocity, code quality metrics, and deployment frequency. Integrates with GitHub, Jira, and Linear.</p>
        <div class="project-stack">
          <span>Go</span><span>SQLite</span><span>REST APIs</span><span>Cobra CLI</span>
        </div>
        <div class="project-links">
          <a href="#" class="proj-link">↗ Install</a>
          <a href="#" class="proj-link">GitHub</a>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- ⑤ CONTACT -->
<section id="contact">
  <div class="contact-inner">
    <div class="section-label">// get in touch</div>
    <h2>Let's Build Something <em>Great</em></h2>
    <p>Whether it's a project, collaboration, or just a hello — my inbox is always open.</p>

    <div class="contact-form">
      <div id="form-content">
        <div class="form-row">
          <div class="form-group">
            <label>Your Name</label>
            <input type="text" id="form-name" placeholder="Jane Smith">
          </div>
          <div class="form-group">
            <label>Email Address</label>
            <input type="email" id="form-email" placeholder="jane@example.com">
          </div>
        </div>
        <div class="form-group full">
          <label>Subject</label>
          <input type="text" id="form-subject" placeholder="Project inquiry, collaboration...">
        </div>
        <div class="form-group full">
          <label>Message</label>
          <textarea id="form-message" placeholder="Tell me about your project or idea..."></textarea>
        </div>
        <button class="form-submit" onclick="submitForm()">Send Message →</button>
      </div>
      <div class="form-success" id="form-success">
        ✓ &nbsp; Message sent! I'll get back to you within 24 hours.
      </div>
    </div>
  </div>
</section>

<!-- ⑥ CHATBOT -->
<section id="chatbot">
  <div class="chatbot-container">
    <div class="chatbot-header">
      <div class="section-label">// ai assistant</div>
      <h2>Ask Me Anything</h2>
      <p style="color:var(--muted)">Powered by Claude — ask about my work, skills, or availability</p>
    </div>

    <div class="chat-window">
      <div class="chat-topbar">
        <div class="chat-topbar-dots">
          <span class="dot-r"></span>
          <span class="dot-y"></span>
          <span class="dot-g"></span>
        </div>
        <div class="chat-topbar-title">SYED SHAHE SUHEL.chen — AI Assistant</div>
        <div class="chat-online">Online</div>
      </div>

      <div class="chat-messages" id="chat-messages">
        <div class="msg">
          <div class="msg-avatar ai-avatar">AC</div>
          <div>
            <div class="msg-bubble ai-bubble">
              👋 Hi there! I'm SYED SHAHE SUHEL's AI assistant. I can tell you about his projects, skills, experience, and availability. What would you like to know?
            </div>
            <div class="msg-time">Just now</div>
          </div>
        </div>
      </div>

      <div class="chat-suggestions" id="suggestions">
        <span class="suggestion-chip" onclick="useSuggestion(this)">What are your top skills?</span>
        <span class="suggestion-chip" onclick="useSuggestion(this)">Tell me about your projects</span>
        <span class="suggestion-chip" onclick="useSuggestion(this)">Are you available for hire?</span>
        <span class="suggestion-chip" onclick="useSuggestion(this)">What's your tech stack?</span>
      </div>

      <div class="chat-inputarea">
        <input type="text" class="chat-input" id="chat-input"
          placeholder="Ask me anything about SYED SHAHE SUHEL..."
          onkeydown="if(event.key==='Enter') sendChat()">
        <button class="chat-send" id="send-btn" onclick="sendChat()">Send ↗</button>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2025 SYED SHAHE SYED SHAHE SUHEL — Built with ❤️ and too much coffee &nbsp;·&nbsp; SYED SHAHE SUHEL@SYED SHAHE SUHELchen.dev</p>
</footer>

<script>
// ── CONTACT FORM ──
function submitForm() {
  const name = document.getElementById('form-name').value.trim();
  const email = document.getElementById('form-email').value.trim();
  const msg = document.getElementById('form-message').value.trim();
  if (!name || !email || !msg) { alert('Please fill in all required fields.'); return; }
  document.getElementById('form-content').style.display = 'none';
  document.getElementById('form-success').style.display = 'block';
}

// ── CHATBOT ──
const SYSTEM_PROMPT = `You are SYED SHAHE SYED SHAHE SUHEL's AI portfolio assistant. Respond as a helpful, concise assistant representing SYED SHAHE SUHEL.

About SYED SHAHE SUHEL:
- Full-stack engineer with 6+ years of experience based in San Francisco, CA
- Expert in: React, Next.js, TypeScript, Node.js, Python, FastAPI, PostgreSQL, AWS, Docker
- Also skilled in AI/ML: Claude API, OpenAI, LangChain, RAG systems, embeddings
- Design skills: Figma, UX research, accessibility, design systems
- Notable projects: Orbit (SaaS dashboard), Mnemonic (AI study app), Pathfinder (travel app), FlowKit (open-source UI library), Vault (password manager), Pulse (dev metrics CLI)
- Open source contributor with 12k+ GitHub stars
- Available for freelance and full-time opportunities
- Email: SYED SHAHE SUHEL@SYED SHAHE SUHELchen.dev
- Passionate about clean code, great UX, and mentoring junior developers

Keep responses friendly, concise (2-3 sentences max unless more detail is asked), and professional. Use emojis sparingly. Don't make up information not listed above.`;

let chatHistory = [];

function getTime() {
  return new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });
}

function appendMsg(role, text) {
  const container = document.getElementById('chat-messages');
  const isUser = role === 'user';
  const div = document.createElement('div');
  div.className = `msg ${isUser ? 'user' : ''}`;
  div.innerHTML = `
    <div class="msg-avatar ${isUser ? 'user-avatar' : 'ai-avatar'}">${isUser ? 'You' : 'AC'}</div>
    <div>
      <div class="msg-bubble ${isUser ? 'user-bubble' : 'ai-bubble'}">${text.replace(/\n/g,'<br>')}</div>
      <div class="msg-time">${getTime()}</div>
    </div>`;
  container.appendChild(div);
  container.scrollTop = container.scrollHeight;
}

function showTyping() {
  const container = document.getElementById('chat-messages');
  const div = document.createElement('div');
  div.className = 'msg'; div.id = 'typing-indicator';
  div.innerHTML = `
    <div class="msg-avatar ai-avatar">AC</div>
    <div class="msg-bubble ai-bubble"><div class="typing"><span></span><span></span><span></span></div></div>`;
  container.appendChild(div);
  container.scrollTop = container.scrollHeight;
}

function removeTyping() {
  const el = document.getElementById('typing-indicator');
  if (el) el.remove();
}

function useSuggestion(el) {
  document.getElementById('chat-input').value = el.textContent;
  document.getElementById('suggestions').style.display = 'none';
  sendChat();
}

async function sendChat() {
  const input = document.getElementById('chat-input');
  const btn = document.getElementById('send-btn');
  const text = input.value.trim();
  if (!text) return;

  input.value = '';
  btn.disabled = true;
  document.getElementById('suggestions').style.display = 'none';

  appendMsg('user', text);
  chatHistory.push({ role: 'user', content: text });

  showTyping();

  try {
    const response = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        model: 'claude-sonnet-4-20250514',
        max_tokens: 1000,
        system: SYSTEM_PROMPT,
        messages: chatHistory
      })
    });

    const data = await response.json();
    const reply = data.content?.[0]?.text || "Sorry, I couldn't fetch a response right now. Please try again!";
    removeTyping();
    appendMsg('ai', reply);
    chatHistory.push({ role: 'assistant', content: reply });
  } catch (err) {
    removeTyping();
    appendMsg('ai', 'Oops — something went wrong. Please try again in a moment!');
  }

  btn.disabled = false;
  input.focus();
}
</script>

</body>
</html>
