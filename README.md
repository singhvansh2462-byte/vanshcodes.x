<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>| Premium Web Developer</title>
  <meta name="description" content="Portfolio of Nytrixx, a 15-year-old premium web developer from India specializing in stunning, high-performance websites." />
  <meta name="robots" content="index, follow" />
  <meta property="og:title" content="Nytrixx | Premium Web Developer" />
  <meta property="og:description" content="I build premium websites that drive results." />
  <meta property="og:type" content="website" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #f8fafc;
      --fg: #0f172a;
      --card: #ffffff;
      --border: #e2e8f0;
      --muted: #f1f5f9;
      --muted-fg: #64748b;
      --primary: #c59a00;
      --primary-fg: #ffffff;
      --accent: #0099cc;
      --input-bg: #f8fafc;
    }

    html.dark {
      --bg: #060c18;
      --fg: #e8f0fe;
      --card: #0d1526;
      --border: #1e2d4a;
      --muted: #111827;
      --muted-fg: #94a3b8;
      --primary: #f4c542;
      --primary-fg: #060c18;
      --accent: #00d8ff;
      --input-bg: #0a1120;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--fg);
      min-height: 100vh;
      transition: background 0.3s, color 0.3s;
      -webkit-font-smoothing: antialiased;
    }

    h1, h2, h3, h4 { font-family: 'Space Grotesk', sans-serif; }

    /* Scrollbar */
    ::-webkit-scrollbar { width: 5px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: var(--primary); border-radius: 3px; opacity: 0.5; }

    /* Utility */
    .gold-text {
      background: linear-gradient(135deg, #f4c542, #ffd700, #f4c542);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
    }
    .gradient-text {
      background: linear-gradient(135deg, #f4c542 0%, #00d8ff 100%);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
    }
    .glow-gold { box-shadow: 0 0 20px rgba(244,197,66,0.5), 0 0 40px rgba(244,197,66,0.2); }
    .glow-gold:hover { box-shadow: 0 0 30px rgba(244,197,66,0.7), 0 0 60px rgba(244,197,66,0.3); }

    /* Grid background */
    .grid-bg {
      background-image:
        linear-gradient(rgba(244,197,66,0.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(244,197,66,0.04) 1px, transparent 1px);
      background-size: 60px 60px;
    }

    /* ── NAVBAR ── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      height: 64px; display: flex; align-items: center;
      padding: 0 24px;
      transition: background 0.3s, border-color 0.3s, box-shadow 0.3s;
    }
    nav.scrolled {
      background: color-mix(in srgb, var(--bg) 80%, transparent);
      backdrop-filter: blur(20px);
      border-bottom: 1px solid var(--border);
      box-shadow: 0 4px 24px rgba(0,0,0,0.15);
    }
    .nav-inner {
      max-width: 1100px; width: 100%; margin: 0 auto;
      display: flex; align-items: center; justify-content: space-between;
    }
    .nav-logo {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 1.5rem; font-weight: 700;
      background: linear-gradient(135deg, #f4c542, #ffd700);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
      cursor: pointer; border: none; background-color: transparent;
      letter-spacing: -0.02em;
    }
    .nav-links { display: flex; gap: 32px; }
    .nav-links a {
      font-size: 0.875rem; font-weight: 500; color: var(--muted-fg);
      text-decoration: none; transition: color 0.2s; cursor: pointer;
    }
    .nav-links a:hover { color: var(--primary); }
    .nav-right { display: flex; align-items: center; gap: 12px; }
    .theme-btn {
      width: 36px; height: 36px; border-radius: 50%;
      border: 1px solid var(--border); background: transparent;
      cursor: pointer; display: flex; align-items: center; justify-content: center;
      color: var(--primary); transition: border-color 0.2s, background 0.2s;
      font-size: 16px;
    }
    .theme-btn:hover { border-color: var(--primary); background: var(--muted); }
    .hamburger {
      display: none; background: transparent; border: none;
      cursor: pointer; color: var(--fg); font-size: 20px; padding: 4px;
    }
    .mobile-menu {
      display: none; flex-direction: column; gap: 16px;
      padding: 16px 24px 20px;
      background: color-mix(in srgb, var(--bg) 95%, transparent);
      backdrop-filter: blur(20px);
      border-bottom: 1px solid var(--border);
    }
    .mobile-menu.open { display: flex; }
    .mobile-menu a { font-size: 0.875rem; color: var(--muted-fg); text-decoration: none; cursor: pointer; }
    .mobile-menu a:hover { color: var(--primary); }

    /* ── HERO ── */
    #home {
      min-height: 100vh; display: flex; align-items: center; justify-content: center;
      position: relative; overflow: hidden; padding: 80px 24px 40px;
    }
    .hero-orb {
      position: absolute; border-radius: 50%; pointer-events: none; filter: blur(80px); opacity: 0.12;
    }
    .hero-orb-1 { width: 400px; height: 400px; background: var(--primary); top: 20%; left: 15%; }
    .hero-orb-2 { width: 320px; height: 320px; background: var(--accent); bottom: 20%; right: 15%; }
    .hero-content { position: relative; z-index: 1; text-align: center; max-width: 800px; }
    .hero-badge {
      display: inline-flex; align-items: center; gap: 8px;
      border: 1px solid color-mix(in srgb, var(--primary) 30%, transparent);
      border-radius: 999px; padding: 6px 16px; margin-bottom: 32px;
      font-size: 0.75rem; font-weight: 500; color: var(--primary);
      background: color-mix(in srgb, var(--primary) 5%, transparent);
      animation: fadeUp 0.6s ease both;
    }
    .hero-badge-dot {
      width: 8px; height: 8px; border-radius: 50%; background: var(--primary);
      animation: pulse 2s infinite;
    }
    @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.6;transform:scale(0.9)} }
    .hero-headline {
      font-size: clamp(2.5rem, 7vw, 5rem);
      font-weight: 700; line-height: 1.1; margin-bottom: 24px;
      animation: fadeUp 0.7s 0.1s ease both;
    }
    .cursor {
      display: inline-block; width: 3px; height: 0.85em;
      background: var(--primary); margin-left: 4px;
      animation: blink 1s step-end infinite; vertical-align: middle;
    }
    @keyframes blink { 50% { opacity: 0; } }
    .hero-sub {
      font-size: clamp(1rem, 2.5vw, 1.25rem); color: var(--muted-fg);
      max-width: 600px; margin: 0 auto 40px; line-height: 1.7;
      animation: fadeUp 0.6s 0.3s ease both;
    }
    .hero-btns {
      display: flex; gap: 16px; justify-content: center; flex-wrap: wrap;
      animation: fadeUp 0.6s 0.5s ease both;
    }
    .btn-primary {
      padding: 14px 32px; background: var(--primary); color: var(--primary-fg);
      border: none; border-radius: 10px; font-size: 0.875rem; font-weight: 600;
      cursor: pointer; display: flex; align-items: center; gap: 8px;
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .btn-primary:hover { transform: scale(1.05); }
    .btn-outline {
      padding: 14px 32px; background: transparent; color: var(--fg);
      border: 1px solid var(--border); border-radius: 10px; font-size: 0.875rem; font-weight: 600;
      cursor: pointer; display: flex; align-items: center; gap: 8px;
      transition: transform 0.2s, border-color 0.2s, color 0.2s;
    }
    .btn-outline:hover { transform: scale(1.05); border-color: var(--primary); color: var(--primary); }
    .scroll-indicator {
      position: absolute; bottom: 40px; left: 50%; transform: translateX(-50%);
      display: flex; flex-direction: column; align-items: center; gap: 8px;
      color: var(--muted-fg); font-size: 0.7rem;
      animation: fadeIn 1s 1.5s ease both;
    }
    .scroll-box {
      width: 20px; height: 32px; border: 1px solid var(--border);
      border-radius: 10px; display: flex; align-items: flex-start;
      justify-content: center; padding: 4px;
    }
    .scroll-dot {
      width: 4px; height: 8px; background: var(--primary); border-radius: 2px;
      animation: scrollBounce 1.5s ease-in-out infinite;
    }
    @keyframes scrollBounce { 0%,100%{transform:translateY(0)} 50%{transform:translateY(12px)} }
    @keyframes fadeUp { from{opacity:0;transform:translateY(24px)} to{opacity:1;transform:translateY(0)} }
    @keyframes fadeIn { from{opacity:0} to{opacity:1} }

    /* ── SECTIONS COMMON ── */
    section { padding: 96px 24px; }
    .section-inner { max-width: 1100px; margin: 0 auto; }
    .section-label {
      font-size: 0.75rem; font-weight: 600; text-transform: uppercase;
      letter-spacing: 0.12em; color: var(--primary);
    }
    .section-title {
      font-size: clamp(1.75rem, 4vw, 2.5rem); font-weight: 700; margin-top: 12px;
    }
    .section-sub { color: var(--muted-fg); margin-top: 16px; max-width: 500px; line-height: 1.7; }
    .section-header { text-align: center; margin-bottom: 64px; }
    .section-header .section-sub { margin: 16px auto 0; }
    .fade-in { opacity: 0; transform: translateY(32px); transition: opacity 0.6s ease, transform 0.6s ease; }
    .fade-in.visible { opacity: 1; transform: translateY(0); }

    /* ── ABOUT ── */
    #about { background: transparent; }
    .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: start; }
    .about-text p { color: var(--muted-fg); line-height: 1.8; margin-bottom: 16px; font-size: 1.05rem; }
    .about-text p span { color: var(--fg); font-weight: 600; }
    .about-tags { display: flex; flex-wrap: wrap; gap: 10px; margin: 24px 0; }
    .tag {
      padding: 4px 14px; border-radius: 999px;
      border: 1px solid color-mix(in srgb, var(--primary) 30%, transparent);
      color: var(--primary); font-size: 0.75rem; font-weight: 500;
      background: color-mix(in srgb, var(--primary) 5%, transparent);
    }
    .timeline { margin-top: 24px; }
    .timeline-label { font-size: 0.75rem; font-weight: 600; text-transform: uppercase; letter-spacing: 0.1em; color: var(--muted-fg); margin-bottom: 20px; }
    .timeline-item { display: flex; gap: 16px; margin-bottom: 16px; }
    .timeline-year { font-size: 0.7rem; font-weight: 700; color: var(--primary); width: 36px; margin-top: 4px; flex-shrink: 0; }
    .timeline-dot-wrap { display: flex; align-items: flex-start; padding-top: 6px; }
    .timeline-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--primary); flex-shrink: 0; }
    .timeline-event { font-size: 0.875rem; color: var(--muted-fg); padding-left: 12px; line-height: 1.5; }
    .skills-label { font-size: 0.75rem; font-weight: 600; text-transform: uppercase; letter-spacing: 0.1em; color: var(--muted-fg); margin-bottom: 28px; }
    .skill { margin-bottom: 20px; }
    .skill-header { display: flex; justify-content: space-between; margin-bottom: 6px; }
    .skill-name { font-size: 0.875rem; font-weight: 500; }
    .skill-pct { font-size: 0.875rem; color: var(--primary); font-weight: 600; }
    .skill-track { height: 6px; background: var(--muted); border-radius: 3px; overflow: hidden; }
    .skill-fill {
      height: 100%; border-radius: 3px;
      background: linear-gradient(90deg, var(--primary), var(--accent));
      width: 0; transition: width 1.2s ease;
    }

    /* ── SERVICES ── */
    #services { background: var(--muted); }
    html.dark #services { background: color-mix(in srgb, var(--bg) 60%, var(--muted)); }
    .cards-4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; }
    .card {
      background: var(--card); border: 1px solid var(--border);
      border-radius: 16px; padding: 24px; position: relative;
      transition: border-color 0.3s, transform 0.2s; height: 100%;
      display: flex; flex-direction: column;
    }
    .card:hover { border-color: color-mix(in srgb, var(--primary) 50%, transparent); }
    .card.popular {
      border: 1px solid transparent;
      background: linear-gradient(var(--card), var(--card)) padding-box,
                  linear-gradient(135deg, #f4c542, #00d8ff) border-box;
    }
    .popular-badge {
      position: absolute; top: -14px; left: 50%; transform: translateX(-50%);
      padding: 4px 14px; background: var(--primary); color: var(--primary-fg);
      border-radius: 999px; font-size: 0.7rem; font-weight: 700; white-space: nowrap;
    }
    .card-tier { font-size: 1.1rem; font-weight: 700; margin-bottom: 4px; }
    .card-price { font-size: 0.875rem; color: var(--primary); font-weight: 600; margin-bottom: 20px; }
    .card-features { list-style: none; flex: 1; margin-bottom: 24px; }
    .card-features li {
      display: flex; align-items: flex-start; gap: 8px;
      font-size: 0.875rem; color: var(--muted-fg); margin-bottom: 10px; line-height: 1.4;
    }
    .check { color: var(--primary); flex-shrink: 0; margin-top: 2px; font-size: 13px; }
    .card-btn {
      width: 100%; padding: 10px; border-radius: 10px; font-size: 0.875rem;
      font-weight: 600; cursor: pointer; transition: transform 0.2s, color 0.2s, border-color 0.2s;
    }
    .card-btn:hover { transform: scale(1.04); }
    .card-btn.primary-btn { background: var(--primary); color: var(--primary-fg); border: none; }
    .card-btn.outline-btn { background: transparent; color: var(--fg); border: 1px solid var(--border); }
    .card-btn.outline-btn:hover { border-color: var(--primary); color: var(--primary); }

    /* ── PROJECTS ── */
    #projects { background: transparent; }
    .cards-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
    .project-card {
      background: var(--card); border: 1px solid var(--border);
      border-radius: 16px; overflow: hidden; position: relative;
      transition: border-color 0.3s, transform 0.2s;
    }
    .project-card:hover { border-color: color-mix(in srgb, var(--primary) 50%, transparent); }
    .project-thumb {
      height: 176px; display: flex; align-items: center; justify-content: center;
      position: relative; overflow: hidden;
    }
    .project-thumb-title {
      font-family: 'Space Grotesk', sans-serif;
      color: #fff; font-size: 1.2rem; font-weight: 700;
      text-shadow: 0 2px 8px rgba(0,0,0,0.4); z-index: 1;
    }
    .project-overlay {
      position: absolute; inset: 0; background: color-mix(in srgb, var(--bg) 92%, transparent);
      display: flex; align-items: center; justify-content: center; gap: 12px;
      opacity: 0; transition: opacity 0.3s;
    }
    .project-card:hover .project-overlay { opacity: 1; }
    .overlay-btn {
      padding: 8px 16px; border-radius: 8px; font-size: 0.8rem; font-weight: 600;
      cursor: pointer; display: flex; align-items: center; gap: 6px;
      transition: transform 0.2s;
    }
    .overlay-btn:hover { transform: scale(1.05); }
    .overlay-btn.primary { background: var(--primary); color: var(--primary-fg); border: none; }
    .overlay-btn.outline { background: transparent; border: 1px solid var(--border); color: var(--fg); }
    .overlay-btn.outline:hover { border-color: var(--primary); color: var(--primary); }
    .project-body { padding: 20px; }
    .project-title { font-weight: 700; margin-bottom: 8px; }
    .project-desc { font-size: 0.875rem; color: var(--muted-fg); line-height: 1.6; margin-bottom: 12px; }
    .tech-tags { display: flex; flex-wrap: wrap; gap: 6px; }
    .tech-tag {
      font-size: 0.7rem; padding: 2px 10px; border-radius: 6px;
      background: color-mix(in srgb, var(--primary) 10%, transparent);
      color: var(--primary);
      border: 1px solid color-mix(in srgb, var(--primary) 20%, transparent);
    }

    /* ── PRICING ── */
    #pricing { background: var(--muted); }
    html.dark #pricing { background: color-mix(in srgb, var(--bg) 60%, var(--muted)); }
    .stats-row {
      display: grid; grid-template-columns: repeat(4, 1fr); gap: 24px;
      background: var(--card); border: 1px solid var(--border);
      border-radius: 16px; padding: 40px 32px; margin: 48px 0;
    }
    .stat-item { text-align: center; }
    .stat-number { font-size: 2.5rem; font-weight: 700; font-family: 'Space Grotesk', sans-serif; }
    .stat-label { font-size: 0.8rem; color: var(--muted-fg); margin-top: 4px; }
    .payment-note {
      display: flex; align-items: center; justify-content: center; gap: 12px;
      max-width: 400px; margin: 0 auto 48px;
      padding: 16px; border-radius: 12px;
      border: 1px solid color-mix(in srgb, var(--primary) 30%, transparent);
      background: color-mix(in srgb, var(--primary) 5%, transparent);
      font-size: 0.875rem;
    }
    .payment-note span { color: var(--primary); font-weight: 600; }
    .payment-note .sep { color: var(--muted-fg); }

    /* ── CONTACT ── */
    #contact { background: transparent; }
    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 48px; }
    .contact-info h3 { font-size: 1.1rem; font-weight: 700; margin-bottom: 32px; }
    .contact-item {
      display: flex; align-items: center; gap: 16px;
      margin-bottom: 24px; text-decoration: none; color: inherit;
    }
    .contact-icon {
      width: 48px; height: 48px; border-radius: 12px;
      border: 1px solid var(--border); background: var(--card);
      display: flex; align-items: center; justify-content: center;
      font-size: 18px; color: var(--muted-fg);
      transition: border-color 0.2s, background 0.2s, color 0.2s;
    }
    .contact-item:hover .contact-icon {
      border-color: var(--primary);
      background: color-mix(in srgb, var(--primary) 10%, transparent);
      color: var(--primary);
    }
    .contact-item:hover .contact-val { color: var(--primary); }
    .contact-lbl { font-size: 0.7rem; color: var(--muted-fg); }
    .contact-val { font-size: 0.95rem; font-weight: 500; transition: color 0.2s; }
    .contact-note {
      margin-top: 32px; padding: 20px; border-radius: 12px;
      background: color-mix(in srgb, var(--muted) 50%, transparent);
      border: 1px solid var(--border); font-size: 0.875rem; color: var(--muted-fg); line-height: 1.8;
    }
    .contact-note strong { color: var(--fg); }
    .contact-form-wrap {
      background: var(--card); border: 1px solid var(--border);
      border-radius: 16px; padding: 28px;
    }
    .form-group { margin-bottom: 16px; }
    .form-label { font-size: 0.8rem; color: var(--muted-fg); margin-bottom: 6px; display: block; }
    .form-input, .form-textarea {
      width: 100%; padding: 12px 16px;
      background: var(--input-bg); border: 1px solid var(--border);
      border-radius: 10px; font-size: 0.875rem; color: var(--fg);
      font-family: 'Inter', sans-serif; outline: none;
      transition: border-color 0.2s;
    }
    .form-input:focus, .form-textarea:focus { border-color: var(--primary); }
    .form-textarea { resize: none; height: 120px; }
    .submit-btn {
      width: 100%; padding: 14px; background: var(--primary); color: var(--primary-fg);
      border: none; border-radius: 10px; font-size: 0.875rem; font-weight: 600;
      cursor: pointer; transition: transform 0.2s, box-shadow 0.2s;
      font-family: 'Inter', sans-serif;
    }
    .submit-btn:hover { transform: scale(1.02); }
    .toast {
      position: fixed; top: 24px; right: 24px; z-index: 9999;
      background: #1a2640; color: #fff;
      border: 1px solid rgba(244,197,66,0.3); border-radius: 12px;
      padding: 16px 20px; font-size: 0.875rem;
      box-shadow: 0 8px 32px rgba(0,0,0,0.3);
      transform: translateX(120%); transition: transform 0.4s ease;
      display: flex; align-items: center; gap: 10px;
    }
    .toast.show { transform: translateX(0); }
    .toast-icon { color: #4ade80; font-size: 18px; }

    /* ── FOOTER ── */
    footer {
      border-top: 1px solid var(--border); padding: 32px 24px;
    }
    .footer-inner {
      max-width: 1100px; margin: 0 auto;
      display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 16px;
    }
    .footer-logo {
      font-family: 'Space Grotesk', sans-serif; font-size: 1.25rem; font-weight: 700;
      background: linear-gradient(135deg, #f4c542, #ffd700);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
    }
    .footer-copy { font-size: 0.8rem; color: var(--muted-fg); }
    .footer-links { display: flex; gap: 16px; }
    .footer-links a {
      color: var(--muted-fg); text-decoration: none; font-size: 18px;
      transition: color 0.2s;
    }
    .footer-links a:hover { color: var(--primary); }
    .footer-links a.wa:hover { color: #25D366; }

    /* ── WHATSAPP FLOATING ── */
    .wa-float {
      position: fixed; bottom: 24px; right: 24px; z-index: 500;
      width: 56px; height: 56px; border-radius: 50%;
      background: #25D366; display: flex; align-items: center; justify-content: center;
      text-decoration: none; font-size: 26px; color: #fff;
      box-shadow: 0 0 20px rgba(37,211,102,0.5);
      transition: transform 0.3s;
    }
    .wa-float:hover { transform: scale(1.1); }

    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      .cards-4, .cards-3 { grid-template-columns: repeat(2, 1fr); }
      .about-grid, .contact-grid { grid-template-columns: 1fr; }
      .stats-row { grid-template-columns: repeat(2, 1fr); }
    }
    @media (max-width: 640px) {
      .cards-4, .cards-3 { grid-template-columns: 1fr; }
      .stats-row { grid-template-columns: repeat(2, 1fr); }
      .nav-links { display: none; }
      .hamburger { display: block; }
      section { padding: 72px 20px; }
    }

    /* Tilt */
    .tilt { transform-style: preserve-3d; transition: transform 0.2s ease; }
  </style>
</head>
<body>

<!-- Toast -->
<div class="toast" id="toast">
  <span class="toast-icon">✓</span>
  <span>Message sent! I'll get back to you soon.</span>
</div>

<!-- NAVBAR -->
<nav id="navbar">
  <div class="nav-inner">
    <button class="nav-logo" onclick="scrollToSection('home')">Nytrixx</button>
    <div class="nav-links">
      <a onclick="scrollToSection('home')">Home</a>
      <a onclick="scrollToSection('about')">About</a>
      <a onclick="scrollToSection('services')">Services</a>
      <a onclick="scrollToSection('projects')">Projects</a>
      <a onclick="scrollToSection('pricing')">Pricing</a>
      <a onclick="scrollToSection('contact')">Contact</a>
    </div>
    <div class="nav-right">
      <button class="theme-btn" id="themeBtn" onclick="toggleTheme()" aria-label="Toggle theme">☀</button>
      <button class="hamburger" id="hamburger" onclick="toggleMenu()" aria-label="Toggle menu">☰</button>
    </div>
  </div>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <a onclick="scrollToSection('home')">Home</a>
  <a onclick="scrollToSection('about')">About</a>
  <a onclick="scrollToSection('services')">Services</a>
  <a onclick="scrollToSection('projects')">Projects</a>
  <a onclick="scrollToSection('pricing')">Pricing</a>
  <a onclick="scrollToSection('contact')">Contact</a>
</div>

<!-- HERO -->
<section id="home" class="grid-bg">
  <div class="hero-orb hero-orb-1"></div>
  <div class="hero-orb hero-orb-2"></div>
  <div class="hero-content">
    <div class="hero-badge">
      <span class="hero-badge-dot"></span>
      Available for freelance projects
    </div>
    <h1 class="hero-headline">
      <span class="gradient-text" id="typedText"></span><span class="cursor"></span>
    </h1>
    <p style="font-size:0.75rem;letter-spacing:0.15em;text-transform:uppercase;color:var(--accent);font-weight:600;margin-bottom:20px;font-family:'Space Grotesk',sans-serif;">
      A new age of creative tricks, premium design, aur futuristic identity
    </p>
    <p class="hero-sub">
      I'm <strong style="color:var(--fg)">Anubhav Singh</strong>, known as <strong style="background:linear-gradient(135deg,#f4c542,#ffd700);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;">Nytrixx</strong> — a 15-year-old developer from India crafting high-performance, visually stunning websites that drive results.
    </p>
    <div class="hero-btns">
      <button class="btn-primary glow-gold" onclick="scrollToSection('contact')">
        Hire Me &nbsp;→
      </button>
      <button class="btn-outline" onclick="scrollToSection('projects')">
        View Projects &nbsp;›
      </button>
    </div>
  </div>
  <div class="scroll-indicator">
    <span>Scroll down</span>
    <div class="scroll-box"><div class="scroll-dot"></div></div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-inner">
    <div class="section-header fade-in">
      <div class="section-label">About Me</div>
      <h2 class="section-title">The Developer Behind the Work</h2>
    </div>
    <div class="about-grid">
      <div class="fade-in" style="transition-delay:0.1s">
        <div class="about-text">
          <p>I'm <span>Anubhav Singh</span>, known as <span style="background:linear-gradient(135deg,#f4c542,#ffd700);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;font-weight:700;">Nytrixx</span> — only 15, a passionate web developer from India. I started coding at 13 and haven't stopped since. I specialize in building premium, high-performance websites that don't just look good — they convert.</p>
          <p>From landing pages to full e-commerce platforms, I bring precision and creativity to every project. My clients get more than just a website — they get a digital asset built to last.</p>
        </div>
        <div class="about-tags">
          <span class="tag">15 Years Old</span>
          <span class="tag">India</span>
          <span class="tag">2+ Years Coding</span>
          <span class="tag">15+ Projects</span>
        </div>
        <div class="timeline">
          <div class="timeline-label">Experience Timeline</div>
          <div class="timeline-item">
            <span class="timeline-year">2023</span>
            <div class="timeline-dot-wrap"><div class="timeline-dot"></div></div>
            <div class="timeline-event">Started learning HTML, CSS &amp; JavaScript</div>
          </div>
          <div class="timeline-item">
            <span class="timeline-year">2024</span>
            <div class="timeline-dot-wrap"><div class="timeline-dot"></div></div>
            <div class="timeline-event">First freelance client — restaurant website</div>
          </div>
          <div class="timeline-item">
            <span class="timeline-year">2024</span>
            <div class="timeline-dot-wrap"><div class="timeline-dot"></div></div>
            <div class="timeline-event">Expanded to React.js and advanced animations</div>
          </div>
          <div class="timeline-item">
            <span class="timeline-year">2025</span>
            <div class="timeline-dot-wrap"><div class="timeline-dot"></div></div>
            <div class="timeline-event">15+ projects delivered across multiple industries</div>
          </div>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.2s">
        <div class="skills-label">Skills &amp; Expertise</div>
        <div class="skill">
          <div class="skill-header"><span class="skill-name">HTML &amp; CSS</span><span class="skill-pct">95%</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="95"></div></div>
        </div>
        <div class="skill">
          <div class="skill-header"><span class="skill-name">JavaScript</span><span class="skill-pct">88%</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="88"></div></div>
        </div>
        <div class="skill">
          <div class="skill-header"><span class="skill-name">React.js</span><span class="skill-pct">82%</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="82"></div></div>
        </div>
        <div class="skill">
          <div class="skill-header"><span class="skill-name">Animations &amp; Motion</span><span class="skill-pct">90%</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="90"></div></div>
        </div>
        <div class="skill">
          <div class="skill-header"><span class="skill-name">Responsive Design</span><span class="skill-pct">93%</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="93"></div></div>
        </div>
        <div class="skill">
          <div class="skill-header"><span class="skill-name">UI/UX Design</span><span class="skill-pct">80%</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="80"></div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="section-inner">
    <div class="section-header fade-in">
      <div class="section-label">Services</div>
      <h2 class="section-title">What I Offer</h2>
      <p class="section-sub">Premium web development packages tailored to every stage of your business journey.</p>
    </div>
    <div class="cards-4">
      <div class="fade-in" style="transition-delay:0.05s">
        <div class="card tilt">
          <div class="card-tier">Basic</div>
          <div class="card-price">₹5,000 – ₹15,000</div>
          <ul class="card-features">
            <li><span class="check">✓</span> Single page website</li>
            <li><span class="check">✓</span> Responsive design</li>
            <li><span class="check">✓</span> Basic animations</li>
            <li><span class="check">✓</span> Contact form</li>
            <li><span class="check">✓</span> Fast loading</li>
            <li><span class="check">✓</span> 1 revision</li>
          </ul>
          <button class="card-btn outline-btn" onclick="scrollToSection('contact')">Get Started</button>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.1s">
        <div class="card tilt">
          <div class="card-tier">Standard</div>
          <div class="card-price">₹15,000 – ₹40,000</div>
          <ul class="card-features">
            <li><span class="check">✓</span> Multi-page website</li>
            <li><span class="check">✓</span> SEO optimized</li>
            <li><span class="check">✓</span> Smooth animations</li>
            <li><span class="check">✓</span> CMS integration</li>
            <li><span class="check">✓</span> Social media links</li>
            <li><span class="check">✓</span> 3 revisions</li>
          </ul>
          <button class="card-btn outline-btn" onclick="scrollToSection('contact')">Get Started</button>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.15s">
        <div class="card popular tilt">
          <span class="popular-badge">Most Popular</span>
          <div class="card-tier">Advanced</div>
          <div class="card-price">₹40,000 – ₹80,000</div>
          <ul class="card-features">
            <li><span class="check">✓</span> Custom design</li>
            <li><span class="check">✓</span> Complex animations</li>
            <li><span class="check">✓</span> Admin panel</li>
            <li><span class="check">✓</span> API integration</li>
            <li><span class="check">✓</span> Performance audit</li>
            <li><span class="check">✓</span> Unlimited revisions</li>
          </ul>
          <button class="card-btn primary-btn glow-gold" onclick="scrollToSection('contact')">Get Started</button>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.2s">
        <div class="card tilt">
          <div class="card-tier">E-commerce</div>
          <div class="card-price">₹80,000 – ₹1,50,000+</div>
          <ul class="card-features">
            <li><span class="check">✓</span> Online store</li>
            <li><span class="check">✓</span> Payment gateway</li>
            <li><span class="check">✓</span> Inventory management</li>
            <li><span class="check">✓</span> Order tracking</li>
            <li><span class="check">✓</span> Analytics dashboard</li>
            <li><span class="check">✓</span> Priority support</li>
          </ul>
          <button class="card-btn outline-btn" onclick="scrollToSection('contact')">Get Started</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-inner">
    <div class="section-header fade-in">
      <div class="section-label">Portfolio</div>
      <h2 class="section-title">Projects Showcase</h2>
      <p class="section-sub">A selection of websites and applications I've built for real clients.</p>
    </div>
    <div class="cards-3">
      <div class="fade-in" style="transition-delay:0.05s">
        <div class="project-card tilt">
          <div class="project-thumb" style="background:linear-gradient(135deg,#f59e0b,#ea580c)">
            <span class="project-thumb-title">RestaurantPro</span>
            <div class="project-overlay">
              <button class="overlay-btn primary">&#8599; Live Demo</button>
              <button class="overlay-btn outline">&#60;/&#62; Code</button>
            </div>
          </div>
          <div class="project-body">
            <div class="project-title">RestaurantPro</div>
            <p class="project-desc">A premium restaurant website with online reservations, menu showcase, and animated hero section.</p>
            <div class="tech-tags"><span class="tech-tag">HTML</span><span class="tech-tag">CSS</span><span class="tech-tag">JS</span></div>
          </div>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.1s">
        <div class="project-card tilt">
          <div class="project-thumb" style="background:linear-gradient(135deg,#ec4899,#e11d48)">
            <span class="project-thumb-title">FashionStore</span>
            <div class="project-overlay">
              <button class="overlay-btn primary">&#8599; Live Demo</button>
              <button class="overlay-btn outline">&#60;/&#62; Code</button>
            </div>
          </div>
          <div class="project-body">
            <div class="project-title">FashionStore</div>
            <p class="project-desc">Full e-commerce fashion platform with product filtering, cart system, and smooth checkout flow.</p>
            <div class="tech-tags"><span class="tech-tag">React</span><span class="tech-tag">CSS</span><span class="tech-tag">JS</span></div>
          </div>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.15s">
        <div class="project-card tilt">
          <div class="project-thumb" style="background:linear-gradient(135deg,#06b6d4,#2563eb)">
            <span class="project-thumb-title">TechStartup</span>
            <div class="project-overlay">
              <button class="overlay-btn primary">&#8599; Live Demo</button>
              <button class="overlay-btn outline">&#60;/&#62; Code</button>
            </div>
          </div>
          <div class="project-body">
            <div class="project-title">TechStartup Landing</div>
            <p class="project-desc">SaaS landing page with 3D animations, feature comparisons, and integrated waitlist form.</p>
            <div class="tech-tags"><span class="tech-tag">React</span><span class="tech-tag">Framer</span></div>
          </div>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.2s">
        <div class="project-card tilt">
          <div class="project-thumb" style="background:linear-gradient(135deg,#22c55e,#059669)">
            <span class="project-thumb-title">EduPlatform</span>
            <div class="project-overlay">
              <button class="overlay-btn primary">&#8599; Live Demo</button>
              <button class="overlay-btn outline">&#60;/&#62; Code</button>
            </div>
          </div>
          <div class="project-body">
            <div class="project-title">EduPlatform</div>
            <p class="project-desc">Online learning platform with course catalog, video player, progress tracking, and quizzes.</p>
            <div class="tech-tags"><span class="tech-tag">React</span><span class="tech-tag">JS</span><span class="tech-tag">CSS</span></div>
          </div>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.25s">
        <div class="project-card tilt">
          <div class="project-thumb" style="background:linear-gradient(135deg,#a855f7,#7c3aed)">
            <span class="project-thumb-title">CryptoTracker</span>
            <div class="project-overlay">
              <button class="overlay-btn primary">&#8599; Live Demo</button>
              <button class="overlay-btn outline">&#60;/&#62; Code</button>
            </div>
          </div>
          <div class="project-body">
            <div class="project-title">CryptoTracker</div>
            <p class="project-desc">Real-time crypto dashboard with live charts, portfolio management, and price alerts.</p>
            <div class="tech-tags"><span class="tech-tag">React</span><span class="tech-tag">JS</span><span class="tech-tag">API</span></div>
          </div>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.3s">
        <div class="project-card tilt">
          <div class="project-thumb" style="background:linear-gradient(135deg,#eab308,#d97706)">
            <span class="project-thumb-title">AgencyWebsite</span>
            <div class="project-overlay">
              <button class="overlay-btn primary">&#8599; Live Demo</button>
              <button class="overlay-btn outline">&#60;/&#62; Code</button>
            </div>
          </div>
          <div class="project-body">
            <div class="project-title">AgencyWebsite</div>
            <p class="project-desc">High-end creative agency portfolio with parallax effects, case studies, and team showcase.</p>
            <div class="tech-tags"><span class="tech-tag">HTML</span><span class="tech-tag">CSS</span><span class="tech-tag">JS</span></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PRICING -->
<section id="pricing">
  <div class="section-inner">
    <div class="section-header fade-in">
      <div class="section-label">Pricing</div>
      <h2 class="section-title">Transparent Pricing</h2>
      <p class="section-sub">No hidden fees. Clear pricing, premium delivery.</p>
    </div>
    <div class="stats-row fade-in">
      <div class="stat-item">
        <div class="stat-number gold-text" data-target="15" data-suffix="+">0</div>
        <div class="stat-label">Projects Delivered</div>
      </div>
      <div class="stat-item">
        <div class="stat-number gold-text" data-target="100" data-suffix="%">0</div>
        <div class="stat-label">Client Satisfaction</div>
      </div>
      <div class="stat-item">
        <div class="stat-number gold-text" data-target="5" data-suffix="+">0</div>
        <div class="stat-label">Technologies</div>
      </div>
      <div class="stat-item">
        <div class="stat-number gold-text" data-target="2" data-suffix="+">0</div>
        <div class="stat-label">Years Experience</div>
      </div>
    </div>
    <div class="payment-note fade-in">
      <span>50% advance</span>
      <span class="sep">+</span>
      <span>50% on completion</span>
    </div>
    <div class="cards-4">
      <div class="fade-in" style="transition-delay:0.05s">
        <div class="card tilt">
          <div class="card-tier">Basic</div>
          <div style="font-size:1.75rem;font-weight:700;font-family:'Space Grotesk',sans-serif" class="gold-text">₹5,000</div>
          <div class="card-price" style="font-size:0.75rem;color:var(--muted-fg);margin-top:2px">₹5,000 – ₹15,000</div>
          <ul class="card-features">
            <li><span class="check">✓</span> Single page website</li>
            <li><span class="check">✓</span> Responsive design</li>
            <li><span class="check">✓</span> Basic animations</li>
            <li><span class="check">✓</span> Contact form</li>
            <li><span class="check">✓</span> Fast loading</li>
            <li><span class="check">✓</span> 1 revision</li>
          </ul>
          <button class="card-btn outline-btn" onclick="scrollToSection('contact')">Start Project</button>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.1s">
        <div class="card tilt">
          <div class="card-tier">Standard</div>
          <div style="font-size:1.75rem;font-weight:700;font-family:'Space Grotesk',sans-serif" class="gold-text">₹15,000</div>
          <div class="card-price" style="font-size:0.75rem;color:var(--muted-fg);margin-top:2px">₹15,000 – ₹40,000</div>
          <ul class="card-features">
            <li><span class="check">✓</span> Multi-page website</li>
            <li><span class="check">✓</span> SEO optimized</li>
            <li><span class="check">✓</span> Smooth animations</li>
            <li><span class="check">✓</span> CMS integration</li>
            <li><span class="check">✓</span> Social media links</li>
            <li><span class="check">✓</span> 3 revisions</li>
          </ul>
          <button class="card-btn outline-btn" onclick="scrollToSection('contact')">Start Project</button>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.15s">
        <div class="card popular tilt">
          <span class="popular-badge">Best Value</span>
          <div class="card-tier">Advanced</div>
          <div style="font-size:1.75rem;font-weight:700;font-family:'Space Grotesk',sans-serif" class="gold-text">₹40,000</div>
          <div class="card-price" style="font-size:0.75rem;color:var(--muted-fg);margin-top:2px">₹40,000 – ₹80,000</div>
          <ul class="card-features">
            <li><span class="check">✓</span> Custom design</li>
            <li><span class="check">✓</span> Complex animations</li>
            <li><span class="check">✓</span> Admin panel</li>
            <li><span class="check">✓</span> API integration</li>
            <li><span class="check">✓</span> Performance audit</li>
            <li><span class="check">✓</span> Unlimited revisions</li>
          </ul>
          <button class="card-btn primary-btn glow-gold" onclick="scrollToSection('contact')">Start Project</button>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.2s">
        <div class="card tilt">
          <div class="card-tier">E-commerce</div>
          <div style="font-size:1.75rem;font-weight:700;font-family:'Space Grotesk',sans-serif" class="gold-text">₹80,000</div>
          <div class="card-price" style="font-size:0.75rem;color:var(--muted-fg);margin-top:2px">₹80,000 – ₹1,50,000+</div>
          <ul class="card-features">
            <li><span class="check">✓</span> Online store</li>
            <li><span class="check">✓</span> Payment gateway</li>
            <li><span class="check">✓</span> Inventory management</li>
            <li><span class="check">✓</span> Order tracking</li>
            <li><span class="check">✓</span> Analytics dashboard</li>
            <li><span class="check">✓</span> Priority support</li>
          </ul>
          <button class="card-btn outline-btn" onclick="scrollToSection('contact')">Start Project</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-inner">
    <div class="section-header fade-in">
      <div class="section-label">Contact</div>
      <h2 class="section-title">Let's Build Together</h2>
      <p class="section-sub">Ready to start your project? Reach out and let's talk.</p>
    </div>
    <div class="contact-grid">
      <div class="fade-in" style="transition-delay:0.1s">
        <div class="contact-info">
          <h3>Get in touch</h3>
          <a href="tel:+919456853697" class="contact-item">
            <div class="contact-icon">📞</div>
            <div>
              <div class="contact-lbl">Phone</div>
              <div class="contact-val">+91 9456853697</div>
            </div>
          </a>
          <a href="mailto:nytrixxofficial@gmail.com" class="contact-item">
            <div class="contact-icon">✉</div>
            <div>
              <div class="contact-lbl">Email</div>
              <div class="contact-val">nytrixxofficial@gmail.com</div>
            </div>
          </a>
          <a href="https://l.instagram.com/?u=https%3A%2F%2Fsinghvansh2462-byte.github.io%2Fvanshcodes.x%2F%3Futm_source%3Dig%26utm_medium%3Dsocial%26utm_content%3Dlink_in_bio" target="_blank" rel="noopener noreferrer" class="contact-item">
            <div class="contact-icon">📸</div>
            <div>
              <div class="contact-lbl">Instagram</div>
              <div class="contact-val">@nytrixxofficial</div>
            </div>
          </a>
          <div class="contact-note">
            Typical response time: <strong>under 24 hours</strong><br>
            Available for projects starting at <strong style="color:var(--primary)">₹5,000</strong>
          </div>
        </div>
      </div>
      <div class="fade-in" style="transition-delay:0.2s">
        <div class="contact-form-wrap">
          <form id="contactForm" onsubmit="handleFormSubmit(event)">
            <div class="form-group">
              <label class="form-label">Your Name</label>
              <input class="form-input" type="text" name="name" placeholder="John Doe" required />
            </div>
            <div class="form-group">
              <label class="form-label">Email Address</label>
              <input class="form-input" type="email" name="email" placeholder="you@example.com" required />
            </div>
            <div class="form-group">
              <label class="form-label">Message</label>
              <textarea class="form-textarea" name="message" placeholder="Tell me about your project..." required></textarea>
            </div>
            <button type="submit" class="submit-btn glow-gold">Send Message</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <span class="footer-logo">Nytrixx</span>
    <span class="footer-copy">© 2025 Nytrixx. All rights reserved.</span>
    <div class="footer-links">
      <a href="https://l.instagram.com/?u=https%3A%2F%2Fsinghvansh2462-byte.github.io%2Fvanshcodes.x%2F%3Futm_source%3Dig%26utm_medium%3Dsocial%26utm_content%3Dlink_in_bio" target="_blank" rel="noopener noreferrer" title="Instagram">📸</a>
      <a href="https://wa.me/919456853697" target="_blank" rel="noopener noreferrer" class="wa" title="WhatsApp">💬</a>
      <a href="mailto:nytrixxofficial@gmail.com" title="Email">✉</a>
    </div>
  </div>
</footer>

<!-- WhatsApp Float -->
<a href="https://wa.me/919456853697" target="_blank" rel="noopener noreferrer" class="wa-float" title="Chat on WhatsApp">💬</a>

<script>
  // ── THEME ──
  const html = document.documentElement;
  const themeBtn = document.getElementById('themeBtn');
  let dark = localStorage.getItem('theme') !== 'light';

  function applyTheme() {
    html.classList.toggle('dark', dark);
    themeBtn.textContent = dark ? '☀' : '🌙';
  }
  applyTheme();

  function toggleTheme() {
    dark = !dark;
    localStorage.setItem('theme', dark ? 'dark' : 'light');
    applyTheme();
  }

  // ── NAVBAR SCROLL ──
  const navbar = document.getElementById('navbar');
  window.addEventListener('scroll', () => {
    navbar.classList.toggle('scrolled', window.scrollY > 20);
  });

  // ── MOBILE MENU ──
  const mobileMenu = document.getElementById('mobileMenu');
  const hamburger = document.getElementById('hamburger');
  function toggleMenu() {
    mobileMenu.classList.toggle('open');
    hamburger.textContent = mobileMenu.classList.contains('open') ? '✕' : '☰';
  }

  // ── SMOOTH SCROLL ──
  function scrollToSection(id) {
    document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' });
    mobileMenu.classList.remove('open');
    hamburger.textContent = '☰';
  }

  // ── TYPING EFFECT ──
  const strings = [
    'I build premium websites',
    'I craft digital experiences',
    'I turn ideas into reality',
    'I build your vision',
  ];
  let sIdx = 0, cIdx = 0, deleting = false;
  const typedEl = document.getElementById('typedText');

  function type() {
    const cur = strings[sIdx];
    if (!deleting && cIdx < cur.length) {
      typedEl.textContent = cur.slice(0, ++cIdx);
      setTimeout(type, 80);
    } else if (!deleting && cIdx === cur.length) {
      setTimeout(() => { deleting = true; type(); }, 2000);
    } else if (deleting && cIdx > 0) {
      typedEl.textContent = cur.slice(0, --cIdx);
      setTimeout(type, 40);
    } else {
      deleting = false;
      sIdx = (sIdx + 1) % strings.length;
      setTimeout(type, 200);
    }
  }
  type();

  // ── FADE IN ON SCROLL ──
  const fades = document.querySelectorAll('.fade-in');
  const obs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) { e.target.classList.add('visible'); obs.unobserve(e.target); }
    });
  }, { threshold: 0.1, rootMargin: '-60px' });
  fades.forEach(el => obs.observe(el));

  // ── SKILL BARS ──
  const skillObs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('.skill-fill').forEach(bar => {
          bar.style.width = bar.dataset.width + '%';
        });
        skillObs.unobserve(e.target);
      }
    });
  }, { threshold: 0.3 });
  document.querySelectorAll('.about-grid').forEach(el => skillObs.observe(el));

  // ── COUNT UP ──
  const countObs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('[data-target]').forEach(el => {
          const target = parseInt(el.dataset.target);
          const suffix = el.dataset.suffix || '';
          let cur = 0;
          const step = Math.max(1500 / target, 15);
          const timer = setInterval(() => {
            cur = Math.min(cur + 1, target);
            el.textContent = cur + suffix;
            if (cur >= target) clearInterval(timer);
          }, step);
        });
        countObs.unobserve(e.target);
      }
    });
  }, { threshold: 0.5 });
  document.querySelectorAll('.stats-row').forEach(el => countObs.observe(el));

  // ── 3D TILT ──
  document.querySelectorAll('.tilt').forEach(el => {
    el.addEventListener('mousemove', (e) => {
      const rect = el.getBoundingClientRect();
      const x = ((e.clientX - rect.left) - rect.width / 2) / (rect.width / 2);
      const y = ((e.clientY - rect.top) - rect.height / 2) / (rect.height / 2);
      el.style.transform = `perspective(800px) rotateX(${y * -7}deg) rotateY(${x * 7}deg) scale(1.02)`;
    });
    el.addEventListener('mouseleave', () => {
      el.style.transform = 'perspective(800px) rotateX(0) rotateY(0) scale(1)';
    });
  });

  // ── CONTACT FORM ──
  function handleFormSubmit(e) {
    e.preventDefault();
    e.target.reset();
    const toast = document.getElementById('toast');
    toast.classList.add('show');
    setTimeout(() => toast.classList.remove('show'), 3500);
  }
</script>
</body>
</html>
