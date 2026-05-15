
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Nytrixx (Anubhav Singh) — premium animated portfolio for high-performance, futuristic web design." />
  <title>Nytrixx — Premium Portfolio</title>

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet" />

  <style>
    :root{
      --bg0:#070A12;
      --bg1:#0A0F22;
      --card: rgba(255,255,255,.06);
      --card2: rgba(255,255,255,.08);
      --stroke: rgba(255,255,255,.12);
      --text:#EAF0FF;
      --muted: rgba(234,240,255,.72);
      --gold:#F5C84B;
      --cyan:#35E7FF;
      --mag:#A78BFA;
      --good:#36F095;
      --shadow: 0 24px 80px rgba(0,0,0,.55);
      --radius: 18px;
      --radius2: 26px;
    }

    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family:"Space Grotesk",system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Cantarell,Helvetica,Arial;
      color:var(--text);
      background:
        radial-gradient(1000px 600px at 15% 10%, rgba(53,231,255,.18), transparent 55%),
        radial-gradient(900px 520px at 85% 20%, rgba(245,200,75,.15), transparent 55%),
        radial-gradient(750px 450px at 45% 80%, rgba(167,139,250,.12), transparent 60%),
        linear-gradient(180deg, var(--bg0), var(--bg1));
      overflow-x:hidden;
    }

    a{color:inherit;text-decoration:none}
    button{font-family:inherit}

    /* Subtle grid */
    .grid{
      position:fixed; inset:0; pointer-events:none; z-index:0;
      background:
        linear-gradient(to right, rgba(255,255,255,.045) 1px, transparent 1px),
        linear-gradient(to bottom, rgba(255,255,255,.045) 1px, transparent 1px);
      background-size: 46px 46px;
      mask-image: radial-gradient(closest-side at 50% 20%, rgba(0,0,0,1), rgba(0,0,0,.2) 60%, transparent 78%);
      opacity:.55;
    }

    /* Floating aurora blobs */
    .aurora{
      position:fixed; inset:-20vh -10vw; pointer-events:none; z-index:0;
      filter: blur(32px);
      opacity:.8;
      background:
        radial-gradient(420px 280px at 20% 20%, rgba(53,231,255,.22), transparent 60%),
        radial-gradient(480px 320px at 75% 25%, rgba(245,200,75,.18), transparent 62%),
        radial-gradient(420px 300px at 45% 70%, rgba(167,139,250,.16), transparent 62%);
      animation: drift 12s ease-in-out infinite;
    }
    @keyframes drift{
      0%,100%{transform:translate3d(0,0,0) scale(1)}
      50%{transform:translate3d(-2%,1.5%,0) scale(1.02)}
    }

    .wrap{position:relative; z-index:1}

    /* Header */
    header{
      position:sticky; top:0; z-index:30;
      backdrop-filter: blur(12px);
      background: rgba(7,10,18,.55);
      border-bottom: 1px solid rgba(255,255,255,.08);
    }
    .nav{
      max-width:1180px; margin:0 auto;
      display:flex; align-items:center; justify-content:space-between;
      padding: 14px 18px;
      gap:16px;
    }

    .brand{
      display:flex; align-items:center; gap:12px;
      min-width: 210px;
    }
    .logo{
      width:38px;height:38px;border-radius:12px;
      background:
        radial-gradient(circle at 30% 30%, rgba(53,231,255,.9), rgba(53,231,255,0) 55%),
        radial-gradient(circle at 70% 70%, rgba(245,200,75,.9), rgba(245,200,75,0) 55%),
        linear-gradient(145deg, rgba(255,255,255,.18), rgba(255,255,255,.04));
      border: 1px solid rgba(255,255,255,.14);
      box-shadow: 0 10px 30px rgba(0,0,0,.35);
      position:relative;
      overflow:hidden;
    }
    .logo::after{
      content:"";
      position:absolute; inset:-40%;
      background: conic-gradient(from 180deg, rgba(53,231,255,.0), rgba(53,231,255,.7), rgba(245,200,75,.7), rgba(167,139,250,.3), rgba(53,231,255,.0));
      animation: spin 5.5s linear infinite;
      opacity:.55;
    }
    @keyframes spin{to{transform:rotate(360deg)}}

    .brand h1{
      margin:0; font-size:14px; letter-spacing:.08em; text-transform:uppercase;
      color: rgba(234,240,255,.88);
    }
    .brand .name{
      font-size:16px; font-weight:700; letter-spacing:.02em;
      line-height:1.1;
    }
    .name span{
      color: var(--cyan);
      text-shadow: 0 0 20px rgba(53,231,255,.25);
    }

    nav ul{list-style:none; display:flex; gap:14px; padding:0; margin:0; align-items:center}
    nav a{
      display:inline-flex; align-items:center;
      padding:10px 12px;
      border-radius: 14px;
      border:1px solid transparent;
      color: rgba(234,240,255,.78);
      transition: transform .2s ease, background .2s ease, border-color .2s ease, color .2s ease;
      font-weight:500;
      font-size:13px;
      white-space:nowrap;
    }
    nav a:hover{
      transform: translateY(-1px);
      background: rgba(255,255,255,.05);
      border-color: rgba(255,255,255,.12);
      color: rgba(234,240,255,.95);
    }

    .navRight{display:flex; align-items:center; gap:12px}

    .ctaSmall{
      display:inline-flex; align-items:center; gap:10px;
      padding: 10px 14px;
      border-radius: 16px;
      border:1px solid rgba(255,255,255,.14);
      background: linear-gradient(180deg, rgba(255,255,255,.08), rgba(255,255,255,.03));
      box-shadow: 0 18px 40px rgba(0,0,0,.35);
      color: rgba(234,240,255,.92);
      transition: transform .2s ease, border-color .2s ease;
      font-weight:700; font-size:13px;
    }
    .ctaSmall:hover{transform: translateY(-1px); border-color: rgba(53,231,255,.35)}

    .hamburger{display:none}
    .mobileMenu{display:none}

    /* Sections */
    .section{
      max-width:1180px;
      margin:0 auto;
      padding: 72px 18px;
    }
    .sectionHeader{
      display:flex; align-items:flex-end; justify-content:space-between;
      gap:18px; margin-bottom: 24px;
    }
    .kicker{
      display:inline-flex; align-items:center; gap:10px;
      font-size:12px; letter-spacing:.18em; text-transform:uppercase;
      color: rgba(234,240,255,.7);
    }
    .kicker::before{
      content:"";
      width:10px; height:10px; border-radius:4px;
      background: linear-gradient(135deg, var(--cyan), var(--gold));
      box-shadow: 0 0 18px rgba(53,231,255,.3);
    }
    .sectionHeader h2{
      margin:0;
      font-size: 28px;
      letter-spacing:-.02em;
    }
    .sectionHeader p{
      margin:0;
      color: var(--muted);
      max-width: 420px;
      font-size: 14px;
      line-height:1.55;
    }

    /* Hero */
    .hero{
      padding: 48px 18px 20px;
      max-width:1180px; margin:0 auto;
    }
    .heroGrid{
      display:grid;
      grid-template-columns: 1.2fr .8fr;
      gap:22px;
      align-items:stretch;
    }
    .heroLeft{
      border-radius: var(--radius2);
      background: linear-gradient(180deg, rgba(255,255,255,.07), rgba(255,255,255,.03));
      border: 1px solid rgba(255,255,255,.10);
      box-shadow: var(--shadow);
      padding: 26px 22px;
      position:relative;
      overflow:hidden;
    }
    .heroLeft::before{
      content:"";
      position:absolute; inset:-2px;
      background: radial-gradient(900px 260px at 10% 0%, rgba(53,231,255,.18), transparent 60%),
                  radial-gradient(760px 240px at 90% 10%, rgba(245,200,75,.16), transparent 58%),
                  linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.0));
      pointer-events:none;
    }

    .heroTopRow{display:flex; align-items:center; gap:12px; position:relative}
    .badge{
      display:inline-flex; align-items:center; gap:10px;
      padding: 10px 12px;
      border-radius: 16px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(255,255,255,.04);
      color: rgba(234,240,255,.88);
      font-weight:600;
      font-size:13px;
    }
    .badge .dot{
      width:10px;height:10px;border-radius:999px;
      background: radial-gradient(circle at 30% 30%, rgba(53,231,255,.95), rgba(53,231,255,.0) 60%),
                  linear-gradient(135deg, var(--cyan), var(--gold));
      box-shadow: 0 0 18px rgba(53,231,255,.33);
    }

    .hero h2{
      position:relative;
      margin: 18px 0 12px;
      font-size: 44px;
      line-height:1.08;
      letter-spacing:-.03em;
    }
    .gradientText{
      background: linear-gradient(90deg, var(--gold), var(--cyan));
      -webkit-background-clip:text; background-clip:text;
      color: transparent;
      text-shadow: 0 0 26px rgba(245,200,75,.18);
    }

    .hero p{
      position:relative;
      margin:0;
      color: var(--muted);
      font-size: 15px;
      line-height:1.65;
      max-width: 650px;
    }

    .heroActions{
      margin-top: 18px;
      display:flex; gap:12px; flex-wrap:wrap;
      position:relative;
    }

    .btn{
      display:inline-flex; align-items:center; justify-content:center; gap:10px;
      padding: 12px 16px;
      border-radius: 18px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(255,255,255,.04);
      color: rgba(234,240,255,.92);
      font-weight:800;
      font-size: 14px;
      transition: transform .2s ease, border-color .2s ease, background .2s ease;
      cursor:pointer;
      user-select:none;
    }
    .btn:hover{transform: translateY(-2px); border-color: rgba(255,255,255,.22)}

    .btnPrimary{
      background: linear-gradient(135deg, rgba(53,231,255,.22), rgba(245,200,75,.20));
      border-color: rgba(53,231,255,.35);
      box-shadow: 0 18px 50px rgba(53,231,255,.10);
      position:relative;
      overflow:hidden;
    }
    .btnPrimary::after{
      content:"";
      position:absolute; inset:-50%;
      background: conic-gradient(from 180deg, rgba(53,231,255,0), rgba(53,231,255,.65), rgba(245,200,75,.55), rgba(53,231,255,0));
      opacity:.35;
      animation: spin 6.5s linear infinite;
    }
    .btnPrimary span{position:relative; z-index:1}

    .btnGhost{
      background: rgba(255,255,255,.03);
      border-color: rgba(255,255,255,.14);
    }

    .heroRight{
      border-radius: var(--radius2);
      border: 1px solid rgba(255,255,255,.10);
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      box-shadow: var(--shadow);
      padding: 18px;
      position:relative;
      overflow:hidden;
    }

    .statGrid{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:12px;
      margin-top: 10px;
    }

    .stat{
      border-radius: 18px;
      padding: 14px 12px;
      background: rgba(255,255,255,.04);
      border: 1px solid rgba(255,255,255,.10);
      transition: transform .25s ease, border-color .25s ease;
    }
    .stat:hover{transform: translateY(-3px); border-color: rgba(53,231,255,.28)}

    .stat .v{font-size: 18px; font-weight:900; letter-spacing:-.02em}
    .stat .l{font-size: 12px; color: var(--muted); margin-top: 6px; line-height:1.35}

    .orb{
      width: 190px; height:190px;
      border-radius: 50%;
      background: radial-gradient(circle at 30% 30%, rgba(53,231,255,.7), rgba(53,231,255,0) 55%),
                  radial-gradient(circle at 70% 70%, rgba(245,200,75,.55), rgba(245,200,75,0) 60%),
                  linear-gradient(135deg, rgba(255,255,255,.12), rgba(255,255,255,.02));
      border: 1px solid rgba(255,255,255,.12);
      box-shadow: 0 40px 120px rgba(0,0,0,.55);
      position:absolute; right:-52px; top:-52px;
      animation: floaty 6s ease-in-out infinite;
    }
    @keyframes floaty{0%,100%{transform:translate3d(0,0,0)}50%{transform:translate3d(-8px,10px,0)}}

    .spark{
      position:absolute; left: 16px; bottom: 18px;
      width: calc(100% - 32px);
      height: 110px;
      background: radial-gradient(closest-side at 10% 50%, rgba(53,231,255,.22), transparent 60%),
                  radial-gradient(closest-side at 90% 10%, rgba(245,200,75,.18), transparent 60%);
      opacity:.8;
      pointer-events:none;
    }

    /* About timeline & skills */
    .twoCol{
      display:grid; grid-template-columns: 1fr 1fr; gap: 18px;
    }

    .panel{
      border-radius: var(--radius2);
      border: 1px solid rgba(255,255,255,.10);
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      box-shadow: 0 18px 60px rgba(0,0,0,.35);
      padding: 18px;
      overflow:hidden;
      position:relative;
    }

    .timeline{position:relative; padding-left: 18px}
    .timeline::before{
      content:""; position:absolute; left: 7px; top: 18px; bottom: 18px;
      width:2px; background: linear-gradient(180deg, rgba(53,231,255,.7), rgba(245,200,75,.2));
      opacity:.75;
    }
    .tItem{position:relative; padding: 12px 0 12px 12px}
    .tDot{position:absolute; left:-8px; top: 20px; width: 14px; height:14px; border-radius:5px;
      background: linear-gradient(135deg, var(--cyan), var(--gold));
      border:1px solid rgba(255,255,255,.18);
      box-shadow: 0 0 18px rgba(53,231,255,.25);
    }
    .tItem h3{margin:0; font-size: 14px; letter-spacing:-.01em}
    .tItem p{margin:8px 0 0; color: var(--muted); font-size: 13px; line-height:1.55}
    
    .skillsList{display:flex; flex-direction:column; gap:12px}
    .skillRow{border:1px solid rgba(255,255,255,.10); background: rgba(255,255,255,.03); border-radius: 18px; padding: 12px}
    .skillTop{display:flex; justify-content:space-between; align-items:center; gap:10px}
    .skillTop .sName{font-weight:800; font-size: 13px}
    .skillTop .sPct{color: rgba(234,240,255,.78); font-weight:800; font-size: 13px}
    .bar{height: 10px; border-radius: 999px; background: rgba(255,255,255,.08); margin-top: 10px; overflow:hidden; border:1px solid rgba(255,255,255,.10)}
    .bar > i{display:block; height:100%; width:0%; background: linear-gradient(90deg, rgba(53,231,255,.9), rgba(245,200,75,.9)); border-radius: 999px; box-shadow: 0 0 20px rgba(53,231,255,.18)}

    /* Cards grids */
    .cards{display:grid; grid-template-columns: repeat(12, 1fr); gap: 14px}
    .card{grid-column: span 6; border-radius: var(--radius2); border:1px solid rgba(255,255,255,.10);
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      padding: 16px; position:relative; overflow:hidden;
      transition: transform .25s ease, border-color .25s ease;
      box-shadow: 0 18px 60px rgba(0,0,0,.28);
    }
    .card:hover{transform: translateY(-4px); border-color: rgba(53,231,255,.28)}
    .cardWide{grid-column: span 4}

    .card .tag{
      display:inline-flex; align-items:center; gap:10px;
      padding: 10px 12px; border-radius: 16px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.03);
      font-weight:900; font-size: 13px;
    }
    .tag i{width:10px;height:10px;border-radius:4px; background: linear-gradient(135deg, var(--cyan), var(--gold)); display:inline-block; box-shadow:0 0 18px rgba(53,231,255,.25)}

    .card h3{margin: 12px 0 8px; font-size: 18px}
    .price{font-size: 13px; color: var(--muted); line-height:1.5}
    .bullets{margin: 12px 0 0; padding:0; list-style:none; display:flex; flex-direction:column; gap:9px}
    .bullets li{display:flex; gap:10px; align-items:flex-start; color: rgba(234,240,255,.84); font-size: 13px; line-height:1.45}
    .check{
      width: 18px; height: 18px; border-radius: 7px;
      background: rgba(54,240,149,.12);
      border:1px solid rgba(54,240,149,.30);
      display:flex; align-items:center; justify-content:center;
      color: rgba(54,240,149,.95);
      font-weight:900; font-size: 12px;
      flex: 0 0 auto;
    }

    /* Projects */
    .project{
      grid-column: span 4;
      padding: 16px;
      border-radius: var(--radius2);
      border: 1px solid rgba(255,255,255,.10);
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      overflow:hidden;
      position:relative;
      transition: transform .25s ease, border-color .25s ease;
      box-shadow: 0 18px 60px rgba(0,0,0,.28);
      min-height: 210px;
    }
    .project:hover{transform: translateY(-4px); border-color: rgba(245,200,75,.28)}

    .project .thumb{
      height: 110px;
      border-radius: 18px;
      border:1px solid rgba(255,255,255,.10);
      background:
        radial-gradient(200px 140px at 20% 30%, rgba(53,231,255,.28), transparent 62%),
        radial-gradient(260px 160px at 80% 20%, rgba(245,200,75,.22), transparent 62%),
        linear-gradient(135deg, rgba(255,255,255,.08), rgba(255,255,255,.02));
      position:relative;
      overflow:hidden;
      transform: translateZ(0);
    }
    .thumb::after{
      content:"";
      position:absolute; inset:-40%;
      background: conic-gradient(from 180deg, rgba(53,231,255,0), rgba(53,231,255,.55), rgba(245,200,75,.5), rgba(167,139,250,.3), rgba(53,231,255,0));
      opacity:.35;
      animation: spin 10s linear infinite;
    }
    .project h3{margin: 12px 0 6px; font-size: 17px}
    .project p{margin:0; color: var(--muted); font-size: 13px; line-height:1.55}

    .project .mini{
      margin-top: 12px;
      display:flex; gap:10px; flex-wrap:wrap;
    }
    .pill{
      font-size: 12px;
      font-weight:900;
      padding: 8px 10px;
      border-radius: 999px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.03);
      color: rgba(234,240,255,.84);
    }

    /* Contact */
    .contactGrid{display:grid; grid-template-columns: 1.05fr .95fr; gap: 14px; align-items:stretch}
    .contactMeta{display:flex; flex-direction:column; gap: 12px}
    .metaRow{display:flex; gap:12px; align-items:flex-start; padding: 14px; border-radius: 20px; border:1px solid rgba(255,255,255,.10); background: rgba(255,255,255,.03)}
    .metaIcon{
      width: 38px; height:38px; border-radius: 16px;
      background: linear-gradient(135deg, rgba(53,231,255,.22), rgba(245,200,75,.18));
      border:1px solid rgba(255,255,255,.12);
      display:flex; align-items:center; justify-content:center;
      box-shadow: 0 18px 50px rgba(53,231,255,.08);
      flex: 0 0 auto;
      font-size: 16px;
    }
    .metaRow b{display:block; font-size: 13px}
    .metaRow a{color: rgba(234,240,255,.88)}
    .metaRow span{display:block; margin-top: 6px; color: var(--muted); font-size: 13px; line-height:1.45}

    form{display:flex; flex-direction:column; gap: 12px}
    .field{display:flex; flex-direction:column; gap: 8px}
    label{font-size: 13px; color: rgba(234,240,255,.86); font-weight:800}
    input, textarea{
      width:100%;
      padding: 12px 12px;
      border-radius: 18px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.03);
      color: var(--text);
      outline:none;
      transition: border-color .2s ease, transform .2s ease;
    }
    textarea{min-height: 120px; resize: vertical}
    input:focus, textarea:focus{border-color: rgba(53,231,255,.35)}

    .formActions{display:flex; gap: 12px; flex-wrap:wrap; align-items:center; justify-content:space-between}
    .hint{color: var(--muted); font-size: 12px}

    /* Footer */
    footer{
      border-top: 1px solid rgba(255,255,255,.08);
      padding: 24px 18px;
      color: rgba(234,240,255,.78);
      background: rgba(7,10,18,.35);
    }
    .footInner{max-width:1180px; margin:0 auto; display:flex; justify-content:space-between; gap: 14px; flex-wrap:wrap}
    .social{display:flex; gap:12px; flex-wrap:wrap; align-items:center}

    /* Animations on scroll */
    .reveal{opacity:0; transform: translateY(16px); transition: opacity .6s ease, transform .7s ease}
    .reveal.in{opacity:1; transform: translateY(0)}

    @media (prefers-reduced-motion: reduce){
      html{scroll-behavior:auto}
      .aurora, .orb, .btnPrimary::after, .thumb::after{animation:none !important}
      .reveal{transition:none; opacity:1; transform:none}
      .logo::after{animation:none}
    }

    /* Responsive */
    @media (max-width: 980px){
      .heroGrid{grid-template-columns: 1fr;}
      .twoCol{grid-template-columns: 1fr;}
      .contactGrid{grid-template-columns: 1fr;}
      nav ul{display:none}
      .hamburger{display:inline-flex}
      .mobileMenu{display:block}
      .project{grid-column: span 6}
      .card{grid-column: span 12}
      .cardWide{grid-column: span 12}
      .statGrid{grid-template-columns: 1fr 1fr}
    }

    @media (max-width: 560px){
      .hero h2{font-size: 34px}
      .project{grid-column: span 12}
      .statGrid{grid-template-columns: 1fr}
    }

    /* Mobile menu */
    .hamburgerBtn{
      border-radius: 16px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(255,255,255,.04);
      padding: 10px 12px;
      color: rgba(234,240,255,.92);
      cursor:pointer;
      font-weight:900;
    }

    .mobileDrawer{
      max-width:1180px; margin: 0 auto; padding: 0 18px 16px;
      display:none;
    }
    .mobileDrawer.open{display:block}
    .mobileDrawer a{
      display:block;
      padding: 12px 12px;
      border-radius: 18px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(255,255,255,.03);
      margin-top: 10px;
      color: rgba(234,240,255,.9);
      font-weight:900;
      font-size: 14px;
    }

  </style>
</head>
<body>
  <div class="grid"></div>
  <div class="aurora"></div>

  <div class="wrap">
    <header>
      <div class="nav">
        <div class="brand">
          <div class="logo" aria-hidden="true"></div>
          <div>
            <h1>Nytrixx <span>•</span> Portfolio</h1>
            <div class="name">Anubhav <span>Singh</span></div>
          </div>
        </div>

        <nav aria-label="Primary">
          <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#pricing">Pricing</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </nav>

        <div class="navRight">
          <a class="ctaSmall" href="#contact">
            <span>Hire Me</span>
            <span aria-hidden="true">→</span>
          </a>

          <div class="hamburger">
            <button class="hamburgerBtn" id="hamburger" aria-label="Open navigation">Menu</button>
          </div>
        </div>
      </div>

      <div class="mobileDrawer" id="mobileDrawer" role="navigation" aria-label="Mobile primary">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#projects">Projects</a>
        <a href="#pricing">Pricing</a>
        <a href="#contact">Contact</a>
      </div>
    </header>

    <!-- Hero -->
    <section class="hero" id="home">
      <div class="heroGrid">
        <div class="heroLeft reveal">
          <div class="heroTopRow">
            <div class="badge"><span class="dot" aria-hidden="true"></span><span>High-performance • Futuristic UI • Smooth animations</span></div>
          </div>

          <h2>
            <span class="gradientText">A new age of creative tricks, premium design, futuristic identity</span>
          </h2>

          <p>
            I’m <b>Anubhav Singh (Nytrixx)</b>, a 15-year-old developer from India crafting high-performance, visually stunning websites that drive results.
          </p>

          <div class="heroActions">
            <a class="btn btnPrimary" href="#contact"><span>Hire Me →</span></a>
            <a class="btn btnGhost" href="#projects"><span>View Projects ›</span></a>
          </div>
        </div>

        <aside class="heroRight reveal" aria-label="Highlights">
          <div class="orb" aria-hidden="true"></div>
          <div class="kicker">Trusted for speed & polish</div>
          <div class="statGrid" style="margin-top:14px">
            <div class="stat">
              <div class="v">15+ </div>
              <div class="l">Projects delivered with clean UI + animation focus</div>
            </div>
            <div class="stat">
              <div class="v">React + Animations</div>
              <div class="l">Modern frontend stacks for premium user experience</div>
            </div>
            <div class="stat">
              <div class="v">Fast Loading</div>
              <div class="l">Optimized layouts and performance-first design</div>
            </div>
            <div class="stat">
              <div class="v">Premium Aesthetic</div>
              <div class="l">Dark theme with gold/cyan identity accents</div>
            </div>
          </div>
          <div class="spark" aria-hidden="true"></div>
        </aside>
      </div>
    </section>

    <!-- About -->
    <section class="section" id="about">
      <div class="sectionHeader reveal">
        <div>
          <div class="kicker">About Me</div>
          <h2>Built for impact. Designed for wow.</h2>
        </div>
        <p>
          A timeline of growth and a skill matrix that shows what I can ship—fast, clean, and premium.
        </p>
      </div>

      <div class="twoCol">
        <div class="panel reveal">
          <div class="kicker" style="margin-bottom: 12px">Timeline</div>
          <div class="timeline">
            <div class="tItem">
              <div class="tDot" aria-hidden="true"></div>
              <h3>Started coding at 13</h3>
              <p>Learned fundamentals and built small projects to sharpen logic and UI instincts.</p>
            </div>
            <div class="tItem">
              <div class="tDot" aria-hidden="true"></div>
              <h3>First freelance client in 2024</h3>
              <p>Delivered real-world work, refined communication, and improved delivery speed.</p>
            </div>
            <div class="tItem">
              <div class="tDot" aria-hidden="true"></div>
              <h3>Expanded into React.js & animations</h3>
              <p>Focused on smooth micro-interactions, modern components, and performance.</p>
            </div>
            <div class="tItem">
              <div class="tDot" aria-hidden="true"></div>
              <h3>Delivered 15+ projects</h3>
              <p>From landing pages to e-commerce experiences—always with a premium finish.</p>
            </div>
          </div>
        </div>

        <div class="panel reveal">
          <div class="kicker" style="margin-bottom: 12px">Skills</div>
          <div class="skillsList">
            <div class="skillRow">
              <div class="skillTop"><div class="sName">HTML & CSS</div><div class="sPct">95%</div></div>
              <div class="bar" aria-hidden="true"><i data-pct="95"></i></div>
            </div>
            <div class="skillRow">
              <div class="skillTop"><div class="sName">JavaScript</div><div class="sPct">88%</div></div>
              <div class="bar" aria-hidden="true"><i data-pct="88"></i></div>
            </div>
            <div class="skillRow">
              <div class="skillTop"><div class="sName">React.js</div><div class="sPct">82%</div></div>
              <div class="bar" aria-hidden="true"><i data-pct="82"></i></div>
            </div>
            <div class="skillRow">
              <div class="skillTop"><div class="sName">Animations</div><div class="sPct">90%</div></div>
              <div class="bar" aria-hidden="true"><i data-pct="90"></i></div>
            </div>
            <div class="skillRow">
              <div class="skillTop"><div class="sName">Responsive Design</div><div class="sPct">93%</div></div>
              <div class="bar" aria-hidden="true"><i data-pct="93"></i></div>
            </div>
            <div class="skillRow">
              <div class="skillTop"><div class="sName">UI/UX</div><div class="sPct">80%</div></div>
              <div class="bar" aria-hidden="true"><i data-pct="80"></i></div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Services / Packages -->
    <section class="section" id="services">
      <div class="sectionHeader reveal">
        <div>
          <div class="kicker">Services / Packages</div>
          <h2>Pick your level. Get the premium finish.</h2>
        </div>
        <p>
          Transparent packages designed for speed, quality, and outcomes.
        </p>
      </div>

      <div class="cards">
        <article class="card reveal">
          <div class="tag"><i aria-hidden="true"></i><span>Basic</span></div>
          <h3>₹5,000 – ₹15,000</h3>
          <div class="price">Single-page websites that load fast and look premium.</div>
          <ul class="bullets">
            <li><span class="check">✓</span><span>Single page + responsive layout</span></li>
            <li><span class="check">✓</span><span>Basic animations & smooth effects</span></li>
            <li><span class="check">✓</span><span>Contact form included</span></li>
            <li><span class="check">✓</span><span>Fast loading performance</span></li>
            <li><span class="check">✓</span><span>1 revision</span></li>
          </ul>
        </article>

        <article class="card reveal">
          <div class="tag"><i aria-hidden="true"></i><span>Standard</span></div>
          <h3>₹15,000 – ₹40,000</h3>
          <div class="price">Multi-page, SEO-ready sites with growth features.</div>
          <ul class="bullets">
            <li><span class="check">✓</span><span>Multi-page structure</span></li>
            <li><span class="check">✓</span><span>SEO optimized (on-page best practices)</span></li>
            <li><span class="check">✓</span><span>CMS integration plan</span></li>
            <li><span class="check">✓</span><span>Social links & conversion-ready sections</span></li>
            <li><span class="check">✓</span><span>3 revisions</span></li>
          </ul>
        </article>

        <article class="card reveal">
          <div class="tag"><i aria-hidden="true"></i><span>Advanced</span></div>
          <h3>₹40,000 – ₹80,000</h3>
          <div class="price">Custom design with complex animations and powerful integrations.</div>
          <ul class="bullets">
            <li><span class="check">✓</span><span>Custom design & premium UI system</span></li>
            <li><span class="check">✓</span><span>Complex animations & interaction logic</span></li>
            <li><span class="check">✓</span><span>Admin panel & content management</span></li>
            <li><span class="check">✓</span><span>API integration</span></li>
            <li><span class="check">✓</span><span>Unlimited revisions</span></li>
          </ul>
        </article>

        <article class="card reveal">
          <div class="tag"><i aria-hidden="true"></i><span>E-commerce</span></div>
          <h3>₹80,000 – ₹1,50,000+</h3>
          <div class="price">Online stores with payments, inventory, tracking & analytics.</div>
          <ul class="bullets">
            <li><span class="check">✓</span><span>Online store + product pages</span></li>
            <li><span class="check">✓</span><span>Payment gateway integration</span></li>
            <li><span class="check">✓</span><span>Inventory & order tracking</span></li>
            <li><span class="check">✓</span><span>Analytics dashboard</span></li>
            <li><span class="check">✓</span><span>Priority support</span></li>
          </ul>
        </article>
      </div>
    </section>

    <!-- Projects Showcase -->
    <section class="section" id="projects">
      <div class="sectionHeader reveal">
        <div>
          <div class="kicker">Projects</div>
          <h2>Selected work with premium motion.</h2>
        </div>
        <p>
          Each project is designed for clarity, performance, and conversion.
        </p>
      </div>

      <div class="cards" style="gap: 14px">
        <div class="project reveal">
          <div class="thumb" aria-hidden="true"></div>
          <h3>RestaurantPro</h3>
          <p>Premium restaurant site with reservations & an animated hero experience.</p>
          <div class="mini">
            <span class="pill">Reservations</span>
            <span class="pill">Animated Hero</span>
          </div>
        </div>

        <div class="project reveal">
          <div class="thumb" aria-hidden="true"></div>
          <h3>FashionStore</h3>
          <p>Full e-commerce fashion platform with product grids and conversion UX.</p>
          <div class="mini">
            <span class="pill">E-commerce</span>
            <span class="pill">UI/UX</span>
          </div>
        </div>

        <div class="project reveal">
          <div class="thumb" aria-hidden="true"></div>
          <h3>TechStartup Landing</h3>
          <p>SaaS landing with 3D-style motion, futuristic sections, and CTA focus.</p>
          <div class="mini">
            <span class="pill">3D Motion</span>
            <span class="pill">SaaS</span>
          </div>
        </div>

        <div class="project reveal">
          <div class="thumb" aria-hidden="true"></div>
          <h3>EduPlatform</h3>
          <p>Online learning platform with video player layout and quiz interactions.</p>
          <div class="mini">
            <span class="pill">Video Player</span>
            <span class="pill">Quizzes</span>
          </div>
        </div>

        <div class="project reveal">
          <div class="thumb" aria-hidden="true"></div>
          <h3>CryptoTracker</h3>
          <p>Real-time crypto dashboard with live chart UI & data-friendly design.</p>
          <div class="mini">
            <span class="pill">Live Charts</span>
            <span class="pill">Dashboard</span>
          </div>
        </div>

        <div class="project reveal">
          <div class="thumb" aria-hidden="true"></div>
          <h3>AgencyWebsite</h3>
          <p>Creative agency portfolio with parallax effects and premium branding flow.</p>
          <div class="mini">
            <span class="pill">Parallax</span>
            <span class="pill">Branding</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing -->
    <section class="section" id="pricing">
      <div class="sectionHeader reveal">
        <div>
          <div class="kicker">Pricing</div>
          <h2>Simple payment structure. Zero confusion.</h2>
        </div>
        <p>
          Transparent payment: <b>50% advance</b> + <b>50% on completion</b>.
        </p>
      </div>

      <div class="cards">
        <article class="cardWide card reveal">
          <div class="tag"><i aria-hidden="true"></i><span>Basic</span></div>
          <h3>₹5,000 – ₹15,000</h3>
          <ul class="bullets">
            <li><span class="check">✓</span><span>Start: 50% advance</span></li>
            <li><span class="check">✓</span><span>Finish: 50% on completion</span></li>
          </ul>
          <div style="margin-top:14px">
            <a class="btn btnPrimary" href="#contact" role="button"><span>Start Project</span></a>
          </div>
        </article>

        <article class="cardWide card reveal">
          <div class="tag"><i aria-hidden="true"></i><span>Standard</span></div>
          <h3>₹15,000 – ₹40,000</h3>
          <ul class="bullets">
            <li><span class="check">✓</span><span>Start: 50% advance</span></li>
            <li><span class="check">✓</span><span>Finish: 50% on completion</span></li>
          </ul>
          <div style="margin-top:14px">
            <a class="btn btnPrimary" href="#contact" role="button"><span>Start Project</span></a>
          </div>
        </article>

        <article class="cardWide card reveal">
          <div class="tag"><i aria-hidden="true"></i><span>Advanced</span></div>
          <h3>₹40,000 – ₹80,000</h3>
          <ul class="bullets">
            <li><span class="check">✓</span><span>Start: 50% advance</span></li>
            <li><span class="check">✓</span><span>Finish: 50% on completion</span></li>
          </ul>
          <div style="margin-top:14px">
            <a class="btn btnPrimary" href="#contact" role="button"><span>Start Project</span></a>
          </div>
        </article>

        <article class="cardWide card reveal">
          <div class="tag"><i aria-hidden="true"></i><span>E-commerce</span></div>
          <h3>₹80,000 – ₹1,50,000+</h3>
          <ul class="bullets">
            <li><span class="check">✓</span><span>Start: 50% advance</span></li>
            <li><span class="check">✓</span><span>Finish: 50% on completion</span></li>
          </ul>
          <div style="margin-top:14px">
            <a class="btn btnPrimary" href="#contact" role="button"><span>Start Project</span></a>
          </div>
        </article>
      </div>
    </section>

    <!-- Contact -->
    <section class="section" id="contact">
      <div class="sectionHeader reveal">
        <div>
          <div class="kicker">Contact</div>
          <h2>Let’s build something premium.</h2>
        </div>
        <p>
          Response time: <b>under 24 hours</b>.
        </p>
      </div>

      <div class="contactGrid">
        <div class="panel reveal">
          <div class="contactMeta">
            <div class="metaRow">
              <div class="metaIcon" aria-hidden="true">☎</div>
              <div>
                <b>Phone</b>
                <a href="tel:+919456853697">+91 9456853697</a>
                <span>Call or WhatsApp for quick updates.</span>
              </div>
            </div>
            <div class="metaRow">
              <div class="metaIcon" aria-hidden="true">✉</div>
              <div>
                <b>Email</b>
                <a href="mailto:nytrixxofficial@gmail.com">nytrixxofficial@gmail.com</a>
                <span>Best for detailed project requirements.</span>
              </div>
            </div>
            <div class="metaRow">
              <div class="metaIcon" aria-hidden="true">⌁</div>
              <div>
                <b>Instagram</b>
                <a href="https://instagram.com/nytrixxofficial" target="_blank" rel="noopener noreferrer">@nytrixxofficial</a>
                <span>Behind-the-scenes design & animations.</span>
              </div>
            </div>
            <div class="metaRow">
              <div class="metaIcon" aria-hidden="true">💬</div>
              <div>
                <b>WhatsApp</b>
                <a href="https://wa.me/919456853697" target="_blank" rel="noopener noreferrer">Chat on WhatsApp</a>
                <span>Fastest way to start.</span>
              </div>
            </div>
          </div>
        </div>

        <div class="panel reveal">
          <div class="kicker" style="margin-bottom: 10px">Send a message</div>
          <form id="contactForm">
            <div class="field">
              <label for="name">Name</label>
              <input id="name" name="name" type="text" placeholder="Your name" required />
            </div>
            <div class="field">
              <label for="email">Email</label>
              <input id="email" name="email" type="email" placeholder="you@example.com" required />
            </div>
            <div class="field">
              <label for="message">Message</label>
              <textarea id="message" name="message" placeholder="Tell me about your project" required></textarea>
            </div>

            <div class="formActions">
              <button class="btn btnPrimary" type="submit"><span>Submit</span><span aria-hidden="true">→</span></button>
              <div class="hint">No backend needed for demo. This will open your email app.</div>
            </div>
          </form>
        </div>
      </div>
    </section>

    <footer>
      <div class="footInner">
        <div><b>Nytrixx © 2025.</b> All rights reserved.</div>
        <div class="social">
          <a class="ctaSmall" style="padding:10px 12px" href="https://instagram.com/nytrixxofficial" target="_blank" rel="noopener noreferrer">Instagram</a>
          <a class="ctaSmall" style="padding:10px 12px" href="https://wa.me/919456853697" target="_blank" rel="noopener noreferrer">WhatsApp</a>
          <a class="ctaSmall" style="padding:10px 12px" href="mailto:nytrixxofficial@gmail.com">Email</a>
        </div>
      </div>
    </footer>
  </div>

  <script>
    // Mobile menu
    const hamburger = document.getElementById('hamburger');
    const mobileDrawer = document.getElementById('mobileDrawer');
    if (hamburger && mobileDrawer) {
      hamburger.addEventListener('click', () => {
        mobileDrawer.classList.toggle('open');
      });
      mobileDrawer.querySelectorAll('a').forEach(a => {
        a.addEventListener('click', () => mobileDrawer.classList.remove('open'));
      });
    }

    // Scroll reveals
    const revealEls = document.querySelectorAll('.reveal');
    const io = new IntersectionObserver((entries)=>{
      for (const e of entries) {
        if (e.isIntersecting) {
          e.target.classList.add('in');
          io.unobserve(e.target);
        }
      }
    }, {threshold: .12});
    revealEls.forEach(el => io.observe(el));

    // Animate skill bars when visible
    const skillBars = document.querySelectorAll('.bar > i');
    const io2 = new IntersectionObserver((entries)=>{
      for (const e of entries) {
        if (e.isIntersecting) {
          const i = e.target;
          const pct = Number(i.getAttribute('data-pct') || '0');
          i.style.transition = 'width 1.1s ease';
          i.style.width = pct + '%';
          io2.unobserve(i);
        }
      }
    }, {threshold: .35});
    skillBars.forEach(b => io2.observe(b));

    // Contact form -> email compose
    const contactForm = document.getElementById('contactForm');
    if (contactForm) {
      contactForm.addEventListener('submit', (e)=>{
        e.preventDefault();
        const name = document.getElementById('name').value.trim();
        const email = document.getElementById('email').value.trim();
        const message = document.getElementById('message').value.trim();

        const subject = encodeURIComponent(`Project inquiry from ${name}`);
        const body = encodeURIComponent(
          `Name: ${name}\nEmail: ${email}\n\nMessage:\n${message}\n\n— Sent from Nytrixx portfolio contact form`
        );

        window.location.href = `mailto:nytrixxofficial@gmail.com?subject=${subject}&body=${body}`;
      });
    }
  </script>
</body>
</html>

