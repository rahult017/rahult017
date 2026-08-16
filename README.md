<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>Rahul Thakur — AI Systems Architect</title>

  <meta
    name="description"
    content="Rahul Thakur — AI Systems Architect, Backend Engineer and AI Builder."
  />

  <style>
    /* =========================================================
       RESET
    ========================================================= */

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #030712;
      --bg-2: #050816;
      --card: rgba(7, 13, 31, 0.82);
      --card-hover: rgba(13, 20, 43, 0.95);

      --border: rgba(99, 102, 241, 0.25);
      --border-bright: rgba(139, 92, 246, 0.65);

      --purple: #7c3aed;
      --purple-light: #a855f7;
      --cyan: #00f5ff;
      --blue: #3b82f6;
      --green: #22c55e;

      --text: #f8fafc;
      --muted: #94a3b8;
      --muted-2: #64748b;

      --radius: 14px;

      --glow-purple:
        0 0 30px rgba(124, 58, 237, 0.18);

      --glow-cyan:
        0 0 30px rgba(0, 245, 255, 0.15);
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      min-height: 100vh;
      background:
        radial-gradient(
          circle at 80% 10%,
          rgba(76, 29, 149, 0.25),
          transparent 28%
        ),
        radial-gradient(
          circle at 10% 30%,
          rgba(6, 182, 212, 0.08),
          transparent 25%
        ),
        var(--bg);

      color: var(--text);

      font-family:
        Inter,
        ui-sans-serif,
        system-ui,
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        sans-serif;

      line-height: 1.5;
      overflow-x: hidden;
    }

    ::selection {
      background: var(--purple);
      color: white;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    /* =========================================================
       BACKGROUND
    ========================================================= */

    body::before {
      content: "";
      position: fixed;
      inset: 0;

      pointer-events: none;

      background-image:
        linear-gradient(
          rgba(255, 255, 255, 0.018) 1px,
          transparent 1px
        ),
        linear-gradient(
          90deg,
          rgba(255, 255, 255, 0.018) 1px,
          transparent 1px
        );

      background-size: 50px 50px;

      mask-image: linear-gradient(
        to bottom,
        black,
        transparent 85%
      );

      z-index: -2;
    }

    .ambient {
      position: fixed;
      width: 500px;
      height: 500px;

      border-radius: 50%;

      filter: blur(100px);

      opacity: 0.12;

      pointer-events: none;

      z-index: -1;
    }

    .ambient.one {
      top: -250px;
      right: -150px;
      background: #7c3aed;
    }

    .ambient.two {
      top: 40%;
      left: -300px;
      background: #06b6d4;
    }

    /* =========================================================
       MAIN
    ========================================================= */

    .container {
      width: min(1180px, calc(100% - 32px));
      margin: 16px auto 40px;
    }

    /* =========================================================
       GLASS CARD
    ========================================================= */

    .card {
      position: relative;

      background:
        linear-gradient(
          145deg,
          rgba(15, 23, 42, 0.9),
          rgba(3, 7, 18, 0.88)
        );

      border: 1px solid var(--border);

      border-radius: var(--radius);

      box-shadow:
        inset 0 1px 0 rgba(255,255,255,0.025),
        0 15px 50px rgba(0,0,0,0.18);

      overflow: hidden;

      transition:
        transform 0.25s ease,
        border-color 0.25s ease,
        box-shadow 0.25s ease;
    }

    .card:hover {
      transform: translateY(-3px);

      border-color: var(--border-bright);

      box-shadow:
        var(--glow-purple),
        inset 0 1px 0 rgba(255,255,255,0.04);
    }

    .card::before {
      content: "";

      position: absolute;

      width: 160px;
      height: 160px;

      top: -100px;
      right: -80px;

      border-radius: 50%;

      background: var(--purple);

      filter: blur(80px);

      opacity: 0.12;

      pointer-events: none;
    }

    /* =========================================================
       TOP NAV
    ========================================================= */

    .topbar {
      height: 48px;

      display: flex;
      align-items: center;
      justify-content: space-between;

      padding: 0 20px;

      border-bottom: 1px solid rgba(99,102,241,0.16);

      background: rgba(2,6,23,0.65);

      font-family: "SFMono-Regular", Consolas, monospace;
      font-size: 13px;
    }

    .terminal {
      color: var(--cyan);
    }

    .terminal::before {
      content: "> ";
      color: var(--purple-light);
    }

    .window-controls {
      display: flex;
      gap: 8px;
    }

    .window-controls span {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      display: block;
    }

    .window-controls span:nth-child(1) {
      background: #ef4444;
    }

    .window-controls span:nth-child(2) {
      background: #eab308;
    }

    .window-controls span:nth-child(3) {
      background: #22c55e;
    }

    /* =========================================================
       HERO
    ========================================================= */

    .hero {
      min-height: 410px;

      display: grid;
      grid-template-columns: 1.05fr 0.95fr;

      border-bottom: 1px solid var(--border);
    }

    .hero-content {
      padding: 46px 42px;

      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .eyebrow {
      font-family: monospace;

      color: var(--cyan);

      font-size: 14px;

      margin-bottom: 10px;
    }

    .hero h1 {
      font-size: clamp(44px, 6vw, 76px);

      line-height: 0.95;

      letter-spacing: -4px;

      font-weight: 850;

      margin-bottom: 15px;
    }

    .hero h1 span {
      color: var(--purple-light);
    }

    .role {
      font-size: clamp(17px, 2vw, 23px);

      font-weight: 650;

      color: var(--cyan);

      margin-bottom: 28px;
    }

    .hero-description {
      max-width: 550px;

      padding: 18px 20px;

      border: 1px solid rgba(124,58,237,0.3);

      border-radius: 10px;

      background: rgba(15,23,42,0.55);

      color: #e2e8f0;

      font-size: 17px;

      margin-bottom: 22px;

      box-shadow: inset 3px 0 0 var(--purple);
    }

    .hero-description strong {
      color: var(--cyan);
    }

    .meta {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
    }

    .meta-item {
      padding: 9px 13px;

      border: 1px solid rgba(99,102,241,0.25);

      background: rgba(15,23,42,0.6);

      border-radius: 8px;

      color: #cbd5e1;

      font-size: 13px;
    }

    .status {
      display: inline-flex;
      align-items: center;
      gap: 7px;
    }

    .status-dot {
      width: 9px;
      height: 9px;

      border-radius: 50%;

      background: var(--green);

      box-shadow:
        0 0 10px rgba(34,197,94,0.8);
    }

    /* =========================================================
       HERO VISUAL
    ========================================================= */

    .hero-visual {
      position: relative;

      display: flex;
      align-items: center;
      justify-content: center;

      min-height: 410px;

      overflow: hidden;

      background:
        radial-gradient(
          circle at center,
          rgba(124,58,237,0.2),
          transparent 48%
        );
    }

    .orb {
      position: absolute;

      width: 320px;
      height: 320px;

      border-radius: 50%;

      background:
        radial-gradient(
          circle at 35% 30%,
          #06b6d4,
          #312e81 45%,
          #0f172a 75%
        );

      box-shadow:
        0 0 25px #7c3aed,
        0 0 70px rgba(124,58,237,0.6),
        inset 0 0 60px rgba(0,245,255,0.25);

      opacity: 0.9;
    }

    .orb::before {
      content: "";

      position: absolute;

      inset: -15px;

      border-radius: 50%;

      border: 2px solid rgba(0,245,255,0.6);

      box-shadow:
        0 0 20px #00f5ff,
        inset 0 0 20px #7c3aed;

      animation: rotate 10s linear infinite;
    }

    .orb::after {
      content: "";

      position: absolute;

      inset: -32px;

      border-radius: 50%;

      border: 1px solid rgba(124,58,237,0.45);

      transform: rotate(45deg);
    }

    @keyframes rotate {
      to {
        transform: rotate(360deg);
      }
    }

    .avatar {
      position: relative;

      width: 255px;
      height: 255px;

      object-fit: cover;

      border-radius: 50%;

      border: 3px solid rgba(255,255,255,0.15);

      box-shadow:
        0 0 40px rgba(124,58,237,0.7);

      z-index: 2;
    }

    .terminal-box {
      position: absolute;

      right: 22px;
      bottom: 25px;

      width: 190px;

      padding: 13px;

      background: rgba(2,6,23,0.9);

      border: 1px solid rgba(0,245,255,0.3);

      border-radius: 9px;

      font-family: monospace;

      font-size: 10px;

      color: #a7f3d0;

      box-shadow: var(--glow-cyan);

      z-index: 3;
    }

    .terminal-box .keyword {
      color: var(--purple-light);
    }

    .terminal-box .function {
      color: var(--cyan);
    }

    .terminal-box .comment {
      color: #64748b;
    }

    /* =========================================================
       CAPABILITY STRIP
    ========================================================= */

    .capabilities {
      display: grid;

      grid-template-columns:
        repeat(5, 1fr);

      gap: 8px;

      padding: 16px;

      border-bottom: 1px solid var(--border);
    }

    .capability {
      text-align: center;

      padding: 14px 8px;

      border: 1px solid rgba(99,102,241,0.16);

      background: rgba(15,23,42,0.4);

      border-radius: 9px;

      transition: 0.2s ease;
    }

    .capability:hover {
      border-color: var(--purple);

      background: rgba(124,58,237,0.08);

      transform: translateY(-2px);
    }

    .capability-icon {
      font-size: 24px;

      margin-bottom: 5px;

      filter:
        drop-shadow(
          0 0 7px rgba(168,85,247,0.7)
        );
    }

    .capability span {
      display: block;

      font-size: 11px;

      font-weight: 700;

      letter-spacing: 0.5px;
    }

    /* =========================================================
       SECTION HEADER
    ========================================================= */

    .section {
      padding: 22px;
    }

    .section-title {
      display: flex;
      align-items: center;
      gap: 10px;

      margin-bottom: 18px;

      font-size: 18px;

      font-weight: 800;

      letter-spacing: 0.3px;
    }

    .section-title .icon {
      color: var(--purple-light);

      filter:
        drop-shadow(
          0 0 8px rgba(168,85,247,0.6)
        );
    }

    /* =========================================================
       TECH + BUILD GRID
    ========================================================= */

    .two-column {
      display: grid;

      grid-template-columns: 1fr 1.35fr;

      gap: 12px;

      margin-top: 12px;
    }

    .stack-row {
      display: grid;

      grid-template-columns: 105px 1fr;

      align-items: center;

      gap: 15px;

      padding: 13px 0;

      border-bottom: 1px solid rgba(148,163,184,0.1);
    }

    .stack-row:last-child {
      border-bottom: 0;
    }

    .stack-name {
      font-size: 13px;

      color: #cbd5e1;
    }

    .stack-icons {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .tech-icon {
      width: 42px;
      height: 42px;

      display: grid;
      place-items: center;

      border: 1px solid rgba(99,102,241,0.25);

      border-radius: 8px;

      background: rgba(15,23,42,0.8);

      font-size: 21px;

      transition: 0.2s ease;
    }

    .tech-icon:hover {
      border-color: var(--cyan);

      box-shadow:
        0 0 15px rgba(0,245,255,0.15);
    }

    /* =========================================================
       WHAT I BUILD
    ========================================================= */

    .build-layout {
      display: grid;

      grid-template-columns: 1fr 0.9fr;

      gap: 15px;
    }

    .build-list {
      display: flex;

      flex-direction: column;

      gap: 15px;
    }

    .build-item {
      display: grid;

      grid-template-columns: 40px 1fr;

      gap: 11px;
    }

    .build-icon {
      width: 40px;
      height: 40px;

      display: grid;
      place-items: center;

      border: 1px solid rgba(124,58,237,0.4);

      background: rgba(124,58,237,0.08);

      border-radius: 9px;

      color: var(--purple-light);

      font-size: 19px;
    }

    .build-item h3 {
      font-size: 13px;

      margin-bottom: 2px;
    }

    .build-item p {
      font-size: 11px;

      color: var(--muted);

      line-height: 1.5;
    }

    .architecture {
      min-height: 270px;

      display: grid;

      place-items: center;

      position: relative;

      overflow: hidden;

      border-radius: 12px;

      background:
        radial-gradient(
          circle,
          rgba(0,245,255,0.12),
          transparent 55%
        );
    }

    .brain {
      font-size: 105px;

      filter:
        drop-shadow(
          0 0 22px rgba(0,245,255,0.7)
        )
        drop-shadow(
          0 0 50px rgba(124,58,237,0.5)
        );
    }

    .architecture::before,
    .architecture::after {
      content: "";

      position: absolute;

      border: 1px solid rgba(0,245,255,0.18);

      border-radius: 50%;
    }

    .architecture::before {
      width: 230px;
      height: 110px;

      transform: rotate(25deg);
    }

    .architecture::after {
      width: 270px;
      height: 130px;

      transform: rotate(-30deg);
    }

    /* =========================================================
       PROJECTS
    ========================================================= */

    .projects {
      display: grid;

      grid-template-columns:
        repeat(4, 1fr);

      gap: 10px;
    }

    .project {
      position: relative;

      min-height: 260px;

      padding: 18px;

      display: flex;
      flex-direction: column;

      justify-content: flex-end;

      border: 1px solid rgba(99,102,241,0.22);

      border-radius: 11px;

      overflow: hidden;

      background:
        linear-gradient(
          180deg,
          rgba(15,23,42,0.2),
          rgba(3,7,18,0.98)
        );

      transition: 0.25s ease;
    }

    .project:hover {
      transform: translateY(-5px);

      border-color: var(--purple);

      box-shadow:
        0 15px 35px rgba(124,58,237,0.18);
    }

    .project-art {
      position: absolute;

      inset: 0;

      display: grid;

      place-items: center;

      font-size: 70px;

      opacity: 0.6;

      background:
        radial-gradient(
          circle at center,
          rgba(124,58,237,0.28),
          transparent 55%
        );
    }

    .project:nth-child(2) .project-art {
      background:
        radial-gradient(
          circle at center,
          rgba(6,182,212,0.2),
          transparent 55%
        );
    }

    .project:nth-child(3) .project-art {
      background:
        radial-gradient(
          circle at center,
          rgba(59,130,246,0.22),
          transparent 55%
        );
    }

    .project:nth-child(4) .project-art {
      background:
        radial-gradient(
          circle at center,
          rgba(16,185,129,0.18),
          transparent 55%
        );
    }

    .project-content {
      position: relative;

      z-index: 2;
    }

    .project h3 {
      font-size: 16px;

      margin-bottom: 7px;
    }

    .project p {
      color: var(--muted);

      font-size: 11px;

      margin-bottom: 12px;
    }

    .tags {
      display: flex;

      flex-wrap: wrap;

      gap: 5px;
    }

    .tag {
      padding: 4px 7px;

      border-radius: 5px;

      border: 1px solid rgba(124,58,237,0.25);

      color: #c4b5fd;

      background: rgba(124,58,237,0.09);

      font-family: monospace;

      font-size: 9px;
    }

    /* =========================================================
       GITHUB STATS
    ========================================================= */

    .stats-grid {
      display: grid;

      grid-template-columns: 1fr 1.5fr;

      gap: 12px;

      margin-top: 12px;
    }

    .stat-number {
      color: var(--cyan);

      font-size: 27px;

      font-weight: 800;
    }

    .stat-row {
      display: flex;

      justify-content: space-between;

      padding: 8px 0;

      border-bottom: 1px solid rgba(148,163,184,0.08);

      font-size: 12px;
    }

    .stat-row span:first-child {
      color: var(--muted);
    }

    .contribution-grid {
      display: grid;

      grid-template-columns:
        repeat(28, 10px);

      gap: 4px;

      margin-top: 20px;
    }

    .contribution {
      width: 10px;
      height: 10px;

      border-radius: 2px;

      background: #111827;
    }

    .contribution:nth-child(3n) {
      background: #312e81;
    }

    .contribution:nth-child(5n) {
      background: #7c3aed;
    }

    .contribution:nth-child(7n) {
      background: #06b6d4;
    }

    .contribution:nth-child(11n) {
      background: #22d3ee;
    }

    /* =========================================================
       CURRENTLY BUILDING
    ========================================================= */

    .building-grid {
      display: grid;

      grid-template-columns: 1fr 1fr;

      gap: 12px;

      margin-top: 12px;
    }

    .progress-item {
      margin-bottom: 13px;
    }

    .progress-label {
      display: flex;

      justify-content: space-between;

      font-size: 12px;

      margin-bottom: 5px;
    }

    .progress-label span:last-child {
      color: var(--muted);
    }

    .progress {
      height: 6px;

      background: #111827;

      border-radius: 99px;

      overflow: hidden;
    }

    .progress span {
      display: block;

      height: 100%;

      border-radius: inherit;

      background:
        linear-gradient(
          90deg,
          var(--purple),
          var(--cyan)
        );

      box-shadow:
        0 0 10px rgba(124,58,237,0.5);
    }

    /* =========================================================
       CONTACT
    ========================================================= */

    .contact {
      display: grid;

      grid-template-columns: 1fr 200px;

      gap: 20px;

      align-items: center;
    }

    .contact h2 {
      font-size: 25px;

      margin-bottom: 8px;
    }

    .contact p {
      color: var(--muted);

      font-size: 13px;

      margin-bottom: 17px;
    }

    .buttons {
      display: flex;

      flex-wrap: wrap;

      gap: 8px;
    }

    .button {
      padding: 9px 14px;

      border: 1px solid rgba(99,102,241,0.35);

      border-radius: 7px;

      font-size: 12px;

      background: rgba(15,23,42,0.7);

      transition: 0.2s ease;
    }

    .button:hover {
      border-color: var(--cyan);

      color: var(--cyan);

      box-shadow:
        0 0 15px rgba(0,245,255,0.12);
    }

    .qr {
      height: 160px;

      display: grid;

      place-items: center;

      border: 1px solid var(--border-bright);

      border-radius: 10px;

      background:
        radial-gradient(
          circle,
          rgba(124,58,237,0.18),
          rgba(2,6,23,0.8)
        );

      color: var(--cyan);

      font-family: monospace;

      text-align: center;
    }

    .qr-icon {
      font-size: 55px;
    }

    .qr small {
      color: var(--muted);
    }

    /* =========================================================
       FOOTER
    ========================================================= */

    .footer {
      margin-top: 12px;

      padding: 18px;

      text-align: center;

      border: 1px solid rgba(124,58,237,0.4);

      border-radius: 10px;

      background:
        linear-gradient(
          90deg,
          rgba(124,58,237,0.12),
          rgba(6,182,212,0.08),
          rgba(59,130,246,0.1)
        );

      color: #c4b5fd;

      font-family: monospace;

      font-size: 11px;

      letter-spacing: 3px;
    }

    .footer span {
      color: var(--cyan);
    }

    /* =========================================================
       RESPONSIVE
    ========================================================= */

    @media (max-width: 1000px) {

      .hero {
        grid-template-columns: 1fr;
      }

      .hero-visual {
        min-height: 360px;
      }

      .two-column,
      .stats-grid,
      .building-grid {
        grid-template-columns: 1fr;
      }

      .projects {
        grid-template-columns:
          repeat(2, 1fr);
      }

      .capabilities {
        grid-template-columns:
          repeat(3, 1fr);
      }
    }

    @media (max-width: 650px) {

      .container {
        width: min(
          100% - 16px,
          1180px
        );

        margin-top: 8px;
      }

      .hero-content {
        padding: 30px 22px;
      }

      .hero h1 {
        letter-spacing: -2px;
      }

      .hero-visual {
        min-height: 300px;
      }

      .orb {
        width: 220px;
        height: 220px;
      }

      .avatar {
        width: 175px;
        height: 175px;
      }

      .terminal-box {
        display: none;
      }

      .capabilities {
        grid-template-columns:
          repeat(2, 1fr);
      }

      .projects {
        grid-template-columns: 1fr;
      }

      .build-layout {
        grid-template-columns: 1fr;
      }

      .contribution-grid {
        grid-template-columns:
          repeat(20, 10px);
      }

      .contact {
        grid-template-columns: 1fr;
      }

      .qr {
        width: 160px;
      }

      .section {
        padding: 17px;
      }
    }
  </style>
</head>

<body>

  <div class="ambient one"></div>
  <div class="ambient two"></div>

  <main class="container">

    <!-- =====================================================
         TOP WINDOW BAR
    ====================================================== -->

    <div class="card">

      <div class="topbar">

        <div class="terminal">
          whoami
        </div>

        <div class="window-controls">
          <span></span>
          <span></span>
          <span></span>
        </div>

      </div>

      <!-- ===================================================
           HERO
      ==================================================== -->

      <section class="hero">

        <div class="hero-content">

          <div class="eyebrow">
            AI SYSTEMS / BACKEND / CLOUD
          </div>

          <h1>
            RAHUL THAKUR<span>.</span>
          </h1>

          <div class="role">
            AI Systems Architect · Backend Engineer · AI Builder
          </div>

          <div class="hero-description">

            I build production-grade AI systems
            that solve real problems and
            <strong>scale.</strong>

          </div>

          <div class="meta">

            <div class="meta-item">
              📍 India 🇮🇳
            </div>

            <div class="meta-item">
              ◫ 7+ Years
            </div>

            <div class="meta-item status">
              <span class="status-dot"></span>
              Open to Collaborate
            </div>

          </div>

        </div>

        <div class="hero-visual">

          <div class="orb"></div>

          <!-- Replace with your own professional photo if desired -->
          <img
            class="avatar"
            src="https://github.com/rahult017.png"
            alt="Rahul Thakur"
          />

          <div class="terminal-box">

            <span class="keyword">def</span>
            <span class="function">build_ai_system</span>():<br/>

            &nbsp;&nbsp;think_big()<br/>

            &nbsp;&nbsp;build_fast()<br/>

            &nbsp;&nbsp;ship_it()<br/>

            &nbsp;&nbsp;make_impact()<br/><br/>

            <span class="comment">
              # return legacy
            </span>

          </div>

        </div>

      </section>

      <!-- ===================================================
           CAPABILITIES
      ==================================================== -->

      <div class="capabilities">

        <div class="capability">
          <div class="capability-icon">🤖</div>
          <span>AI AGENTS</span>
        </div>

        <div class="capability">
          <div class="capability-icon">🧠</div>
          <span>LLMs</span>
        </div>

        <div class="capability">
          <div class="capability-icon">📚</div>
          <span>RAG</span>
        </div>

        <div class="capability">
          <div class="capability-icon">🔗</div>
          <span>MCP</span>
        </div>

        <div class="capability">
          <div class="capability-icon">☁️</div>
          <span>CLOUD NATIVE</span>
        </div>

      </div>

    </div>

    <!-- =====================================================
         TECH + WHAT I BUILD
    ====================================================== -->

    <div class="two-column">

      <!-- TECH STACK -->

      <section class="card section">

        <div class="section-title">
          <span class="icon">ϟ</span>
          TECH STACK
        </div>

        <div class="stack-row">

          <div class="stack-name">
            Languages
          </div>

          <div class="stack-icons">

            <div class="tech-icon">🐍</div>
            <div class="tech-icon">GO</div>
            <div class="tech-icon">TS</div>
            <div class="tech-icon">⌘</div>

          </div>

        </div>

        <div class="stack-row">

          <div class="stack-name">
            Backend
          </div>

          <div class="stack-icons">

            <div class="tech-icon">⚡</div>
            <div class="tech-icon">DJ</div>
            <div class="tech-icon">⚙</div>

          </div>

        </div>

        <div class="stack-row">

          <div class="stack-name">
            AI / LLM
          </div>

          <div class="stack-icons">

            <div class="tech-icon">◉</div>
            <div class="tech-icon">AI</div>
            <div class="tech-icon">🔗</div>
            <div class="tech-icon">🦜</div>

          </div>

        </div>

        <div class="stack-row">

          <div class="stack-name">
            Infra / DevOps
          </div>

          <div class="stack-icons">

            <div class="tech-icon">🐳</div>
            <div class="tech-icon">☸</div>
            <div class="tech-icon">🐧</div>
            <div class="tech-icon">◉</div>

          </div>

        </div>

        <div class="stack-row">

          <div class="stack-name">
            Databases
          </div>

          <div class="stack-icons">

            <div class="tech-icon">🐘</div>
            <div class="tech-icon">▰</div>
            <div class="tech-icon">🍃</div>
            <div class="tech-icon">◈</div>

          </div>

        </div>

      </section>

      <!-- WHAT I BUILD -->

      <section class="card section">

        <div class="section-title">
          <span class="icon">♧</span>
          WHAT I BUILD
        </div>

        <div class="build-layout">

          <div class="build-list">

            <div class="build-item">

              <div class="build-icon">♧</div>

              <div>
                <h3>Multi-Agent Systems</h3>
                <p>
                  Intelligent agents that collaborate
                  to solve complex tasks.
                </p>
              </div>

            </div>

            <div class="build-item">

              <div class="build-icon">♙</div>

              <div>
                <h3>Enterprise RAG</h3>
                <p>
                  Retrieval systems that turn data
                  into accurate answers.
                </p>
              </div>

            </div>

            <div class="build-item">

              <div class="build-icon">▣</div>

              <div>
                <h3>LLM Applications</h3>
                <p>
                  Scalable, reliable and
                  production-ready AI.
                </p>
              </div>

            </div>

            <div class="build-item">

              <div class="build-icon">⌁</div>

              <div>
                <h3>Backend & APIs</h3>
                <p>
                  High-performance APIs and
                  microservices.
                </p>
              </div>

            </div>

            <div class="build-item">

              <div class="build-icon">♧</div>

              <div>
                <h3>Cloud Native</h3>
                <p>
                  Containerized and orchestrated
                  systems built for scale.
                </p>
              </div>

            </div>

          </div>

          <div class="architecture">

            <div class="brain">
              🧠
            </div>

          </div>

        </div>

      </section>

    </div>

    <!-- =====================================================
         FEATURED PROJECTS
    ====================================================== -->

    <section class="card section" style="margin-top:12px">

      <div class="section-title">
        <span class="icon">🚀</span>
        FEATURED PROJECTS

        <span
          style="
            margin-left:auto;
            color:#64748b;
            font-size:11px;
            font-weight:400;
          "
        >
          View all repositories →
        </span>
      </div>

      <div class="projects">

        <!-- PROJECT 1 -->

        <a
          href="https://github.com/rahult017"
          class="project"
        >

          <div class="project-art">
            🤖
          </div>

          <div class="project-content">

            <h3>
              Multi-Agent Platform
            </h3>

            <p>
              Production-ready multi-agent
              platform with orchestration,
              tools and memory.
            </p>

            <div class="tags">

              <span class="tag">FastAPI</span>
              <span class="tag">LangGraph</span>
              <span class="tag">PostgreSQL</span>

            </div>

          </div>

        </a>

        <!-- PROJECT 2 -->

        <a
          href="https://github.com/rahult017"
          class="project"
        >

          <div class="project-art">
            📚
          </div>

          <div class="project-content">

            <h3>
              Enterprise RAG System
            </h3>

            <p>
              Advanced RAG architecture with
              hybrid search and citations.
            </p>

            <div class="tags">

              <span class="tag">OpenAI</span>
              <span class="tag">Qdrant</span>
              <span class="tag">FastAPI</span>

            </div>

          </div>

        </a>

        <!-- PROJECT 3 -->

        <a
          href="https://github.com/rahult017"
          class="project"
        >

          <div class="project-art">
            🚀
          </div>

          <div class="project-content">

            <h3>
              FastAPI Boilerplate
            </h3>

            <p>
              Production-grade backend foundation
              with authentication and observability.
            </p>

            <div class="tags">

              <span class="tag">FastAPI</span>
              <span class="tag">Docker</span>
              <span class="tag">Kubernetes</span>

            </div>

          </div>

        </a>

        <!-- PROJECT 4 -->

        <a
          href="https://github.com/rahult017"
          class="project"
        >

          <div class="project-art">
            GO
          </div>

          <div class="project-content">

            <h3>
              Go Microservices
            </h3>

            <p>
              High-performance Go services with
              clean architecture and observability.
            </p>

            <div class="tags">

              <span class="tag">Go</span>
              <span class="tag">gRPC</span>
              <span class="tag">PostgreSQL</span>

            </div>

          </div>

        </a>

      </div>

    </section>

    <!-- =====================================================
         GITHUB STATS
    ====================================================== -->

    <div class="stats-grid">

      <section class="card section">

        <div class="section-title">
          <span class="icon">▥</span>
          GITHUB STATS
        </div>

        <div class="stat-row">
          <span>Total Stars</span>
          <strong class="stat-number">1.2K+</strong>
        </div>

        <div class="stat-row">
          <span>Total Commits</span>
          <strong class="stat-number">8.5K+</strong>
        </div>

        <div class="stat-row">
          <span>Repositories</span>
          <strong class="stat-number">35+</strong>
        </div>

        <div class="stat-row">
          <span>Contributions</span>
          <strong style="color:#c084fc">
            Consistent
          </strong>
        </div>

      </section>

      <section class="card section">

        <div class="section-title">
          <span class="icon">⌁</span>
          CONTRIBUTION GRAPH
        </div>

        <div class="contribution-grid">

          <!-- Generated contribution cells -->

          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>

          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>

          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>
          <span class="contribution"></span>

        </div>

        <div
          style="
            margin-top:15px;
            text-align:center;
            color:#38bdf8;
            font-size:12px;
          "
        >
          Learn. Build. Ship. Repeat.
        </div>

      </section>

    </div>

    <!-- =====================================================
         CURRENTLY BUILDING + COLLABORATION
    ====================================================== -->

    <div class="building-grid">

      <section class="card section">

        <div class="section-title">
          <span class="icon">♧</span>
          CURRENTLY BUILDING
        </div>

        <div class="progress-item">

          <div class="progress-label">
            <span>AI Agents</span>
            <span>80%</span>
          </div>

          <div class="progress">
            <span style="width:80%"></span>
          </div>

        </div>

        <div class="progress-item">

          <div class="progress-label">
            <span>MCP Servers</span>
            <span>70%</span>
          </div>

          <div class="progress">
            <span style="width:70%"></span>
          </div>

        </div>

        <div class="progress-item">

          <div class="progress-label">
            <span>LangGraph Workflows</span>
            <span>60%</span>
          </div>

          <div class="progress">
            <span style="width:60%"></span>
          </div>

        </div>

        <div class="progress-item">

          <div class="progress-label">
            <span>Cloud Native AI</span>
            <span>75%</span>
          </div>

          <div class="progress">
            <span style="width:75%"></span>
          </div>

        </div>

        <div class="progress-item">

          <div class="progress-label">
            <span>Go Microservices</span>
            <span>65%</span>
          </div>

          <div class="progress">
            <span style="width:65%"></span>
          </div>

        </div>

      </section>

      <section class="card section">

        <div class="contact">

          <div>

            <div class="section-title">
              <span class="icon">♥</span>
              LET'S BUILD SOMETHING
            </div>

            <h2>
              Serious AI.
              <br/>
              Serious Engineering.
            </h2>

            <p>
              I'm always interested in ambitious
              AI products, infrastructure and
              open-source collaboration.
            </p>

            <div class="buttons">

              <a
                class="button"
                href="https://github.com/rahult017"
                target="_blank"
              >
                ◉ GitHub
              </a>

              <a
                class="button"
                href="https://linkedin.com/in/rahult016-52209a145"
                target="_blank"
              >
                in LinkedIn
              </a>

              <a
                class="button"
                href="mailto:rahult016@gmail.com"
              >
                ✉ Email
              </a>

            </div>

          </div>

          <div class="qr">

            <div>

              <div class="qr-icon">
                ▦
              </div>

              <small>
                Let's connect.
              </small>

            </div>

          </div>

        </div>

      </section>

    </div>

    <!-- =====================================================
         FOOTER
    ====================================================== -->

    <footer class="footer">

      ✦ &nbsp;
      BUILDING INTELLIGENT SYSTEMS
      &nbsp; · &nbsp;
      <span>SOLVING REAL PROBLEMS</span>
      &nbsp; · &nbsp;
      CREATING REAL IMPACT
      &nbsp; ✦

    </footer>

  </main>

</body>
</html>