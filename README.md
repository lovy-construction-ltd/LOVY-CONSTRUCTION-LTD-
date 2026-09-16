<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LOVY Construction LTD — Design, Build, Consult</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --blueprint:#0F2A47;
    --blueprint-deep:#0A1E35;
    --line:#7FA8C9;
    --line-soft:rgba(127,168,201,0.35);
    --paper:#EDE6D5;
    --paper-2:#E3DBC6;
    --ink:#211C15;
    --ink-soft:#585044;
    --brass:#A2712B;
    --brass-light:#C79A52;
    --white:#F7F4EC;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.55;
    overflow-x:hidden;
  }
  img{max-width:100%;display:block;}
  a{color:inherit;}
  .wrap{max-width:1140px;margin:0 auto;padding:0 28px;}
  h1,h2,h3{font-family:'Fraunces', serif;font-weight:600;margin:0;letter-spacing:-0.01em;}
  .mono{font-family:'IBM Plex Mono', monospace;}

  /* ---------- NAV ---------- */
  header{
    position:sticky;top:0;z-index:50;
    background:rgba(237,230,213,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--paper-2);
  }
  .nav{display:flex;align-items:center;justify-content:space-between;padding:16px 28px;max-width:1140px;margin:0 auto;}
  .brand{display:flex;align-items:center;gap:10px;text-decoration:none;color:var(--ink);}
  .brand-mark{
    width:34px;height:34px;border:1.5px solid var(--ink);border-radius:2px;
    display:flex;align-items:center;justify-content:center;
    font-family:'Fraunces',serif;font-weight:700;font-size:15px;
    transform:rotate(0deg);
  }
  .brand-name{font-family:'Fraunces',serif;font-weight:600;font-size:18px;letter-spacing:0.01em;}
  .brand-name small{display:block;font-family:'IBM Plex Mono',monospace;font-weight:400;font-size:9.5px;letter-spacing:0.14em;color:var(--ink-soft);margin-top:1px;}
  nav.links{display:flex;gap:28px;font-size:14.5px;}
  nav.links a{text-decoration:none;position:relative;padding:4px 0;}
  nav.links a:hover{color:var(--brass);}
  .nav-phone{font-family:'IBM Plex Mono',monospace;font-size:13.5px;color:var(--ink-soft);white-space:nowrap;}
  .nav-mobile-hide{display:flex;align-items:center;gap:32px;}
  @media (max-width:760px){
    nav.links{display:none;}
  }

  /* ---------- HERO ---------- */
  .hero{
    position:relative;
    background:var(--blueprint);
    color:var(--white);
    overflow:hidden;
    padding:96px 0 64px;
  }
  .hero::before{
    content:"";
    position:absolute;inset:0;
    background-image:
      linear-gradient(var(--line-soft) 1px, transparent 1px),
      linear-gradient(90deg, var(--line-soft) 1px, transparent 1px);
    background-size:44px 44px;
    opacity:0.35;
    mask-image:radial-gradient(ellipse 80% 70% at 60% 30%, black 40%, transparent 90%);
  }
  .hero-inner{position:relative;z-index:2;}
  .hero-eyebrow{
    display:flex;align-items:center;gap:10px;
    font-family:'IBM Plex Mono',monospace;font-size:12.5px;letter-spacing:0.08em;
    color:var(--line);margin-bottom:26px;
  }
  .hero-eyebrow .rule{width:40px;height:1px;background:var(--line);}
  .hero h1{
    font-size:clamp(34px,5.4vw,58px);
    line-height:1.08;
    max-width:780px;
    color:var(--white);
  }
  .hero h1 em{font-style:normal;color:var(--brass-light);}
  .hero p.lede{
    max-width:520px;margin-top:22px;font-size:16.5px;color:#CBD8E3;
  }
  .hero-ctas{display:flex;gap:16px;margin-top:36px;flex-wrap:wrap;}
  .btn{
    font-family:'IBM Plex Sans',sans-serif;font-weight:500;font-size:14.5px;
    padding:13px 24px;border-radius:2px;text-decoration:none;
    display:inline-flex;align-items:center;gap:8px;
    border:1px solid transparent;transition:transform .15s ease, background .15s ease;
  }
  .btn-primary{background:var(--brass);color:var(--white);}
  .btn-primary:hover{background:var(--brass-light);}
  .btn-ghost{border-color:var(--line-soft);color:var(--white);}
  .btn-ghost:hover{border-color:var(--line);background:rgba(255,255,255,0.05);}

  .stat-strip{
    position:relative;z-index:2;
    margin-top:72px;
    display:grid;grid-template-columns:repeat(4,1fr);
    border-top:1px solid var(--line-soft);
  }
  .stat-strip div{padding:22px 0 0;border-left:1px solid var(--line-soft);padding-left:20px;}
  .stat-strip div:first-child{border-left:none;padding-left:0;}
  .stat-num{font-family:'Fraunces',serif;font-weight:600;font-size:30px;color:var(--white);}
  .stat-label{font-family:'IBM Plex Mono',monospace;font-size:11px;color:var(--line);letter-spacing:0.04em;margin-top:4px;}
  @media (max-width:700px){
    .stat-strip{grid-template-columns:repeat(2,1fr);row-gap:20px;}
    .stat-strip div:nth-child(3){border-left:none;padding-left:0;}
  }

  /* ---------- PHOTOS ---------- */
  .photo{width:100%;object-fit:cover;display:block;}
  .photo-hero{height:340px;margin-top:56px;border:1px solid var(--line-soft);}
  .photo-about{height:280px;margin-bottom:36px;border:1px solid var(--ink);}

  /* ---------- SECTION HEADERS ---------- */
  .section{padding:88px 0;}
  .section-head{display:flex;justify-content:space-between;align-items:flex-end;gap:24px;margin-bottom:48px;flex-wrap:wrap;}
  .section-tag{font-family:'IBM Plex Mono',monospace;font-size:12px;color:var(--brass);letter-spacing:0.06em;margin-bottom:10px;}
  .section-head h2{font-size:clamp(26px,3.4vw,38px);max-width:560px;}
  .section-head p{max-width:360px;color:var(--ink-soft);font-size:15px;margin:0;}

  /* ---------- ABOUT ---------- */
  .about{background:var(--paper);}
  .about-grid{display:grid;grid-template-columns:1.1fr 0.9fr;gap:60px;align-items:start;}
  .about-grid p{color:var(--ink-soft);font-size:16px;margin:0 0 16px;}
  .about-figure{
    border:1px solid var(--ink);position:relative;padding:26px;background:var(--white);
  }
  .about-figure .corner{position:absolute;width:9px;height:9px;border:1px solid var(--brass);}
  .about-figure .c1{top:-1px;left:-1px;border-right:none;border-bottom:none;}
  .about-figure .c2{top:-1px;right:-1px;border-left:none;border-bottom:none;}
  .about-figure .c3{bottom:-1px;left:-1px;border-right:none;border-top:none;}
  .about-figure .c4{bottom:-1px;right:-1px;border-left:none;border-top:none;}
  .about-figure h3{font-size:13px;font-family:'IBM Plex Mono',monospace;font-weight:500;letter-spacing:0.05em;color:var(--ink-soft);margin-bottom:18px;text-transform:uppercase;}
  .founded-row{display:flex;justify-content:space-between;padding:12px 0;border-top:1px solid var(--paper-2);font-size:14px;}
  .founded-row:first-of-type{border-top:none;}
  .founded-row span:first-child{color:var(--ink-soft);}
  .founded-row span:last-child{font-family:'IBM Plex Mono',monospace;}
  @media (max-width:820px){.about-grid{grid-template-columns:1fr;}}

  /* ---------- SERVICES ---------- */
  .services{background:var(--blueprint-deep);color:var(--white);}
  .services .section-tag{color:var(--line);}
  .services .section-head p{color:#B9C7D4;}
  .svc-index{border-top:1px solid var(--line-soft);}
  .svc-row{
    display:grid;grid-template-columns:70px 1fr 1fr;gap:24px;
    padding:26px 0;border-bottom:1px solid var(--line-soft);
    align-items:baseline;
  }
  .svc-row .n{font-family:'IBM Plex Mono',monospace;color:var(--brass-light);font-size:14px;}
  .svc-row h3{font-size:19px;color:var(--white);font-weight:500;}
  .svc-row p{margin:0;color:#AFC0CE;font-size:14.5px;}
  @media (max-width:720px){
    .svc-row{grid-template-columns:40px 1fr;}
    .svc-row p{grid-column:2;margin-top:6px;}
  }

  /* ---------- PROJECTS ---------- */
  .projects{background:var(--paper);}
  .sheet{
    border:1px solid var(--ink);
    background:var(--white);
    margin-bottom:34px;
  }
  .sheet-photo{width:100%;height:220px;object-fit:cover;display:block;border-bottom:1px solid var(--ink);}
  .sheet-body{display:grid;grid-template-columns:1fr 300px;}
  .sheet-main{padding:34px 36px;}
  .sheet-status{
    font-family:'IBM Plex Mono',monospace;font-size:11px;letter-spacing:0.06em;
    color:var(--brass);border:1px solid var(--brass);display:inline-block;
    padding:3px 9px;border-radius:2px;margin-bottom:16px;
  }
  .sheet-main h3{font-size:23px;max-width:480px;margin-bottom:8px;}
  .sheet-main .desc{color:var(--ink-soft);font-size:14.5px;max-width:480px;}
  .sheet-block{
    border-left:1px solid var(--paper-2);
    padding:34px 30px;
    background:var(--paper-2);
  }
  .sheet-field{margin-bottom:16px;}
  .sheet-field:last-child{margin-bottom:0;}
  .sheet-field .label{font-family:'IBM Plex Mono',monospace;font-size:10px;color:var(--ink-soft);letter-spacing:0.08em;text-transform:uppercase;margin-bottom:4px;}
  .sheet-field .value{font-size:13.8px;font-family:'IBM Plex Mono',monospace;line-height:1.5;}
  @media (max-width:720px){
    .sheet-body{grid-template-columns:1fr;}
    .sheet-block{border-left:none;border-top:1px solid var(--paper-2);}
  }

  /* ---------- CTA ---------- */
  .cta{
    background:var(--blueprint);color:var(--white);
    padding:90px 0;text-align:left;position:relative;overflow:hidden;
  }
  .cta::before{
    content:"";position:absolute;right:-80px;top:-80px;width:340px;height:340px;
    border:1px solid var(--line-soft);border-radius:50%;
  }
  .cta::after{
    content:"";position:absolute;right:20px;top:20px;width:220px;height:220px;
    border:1px solid var(--line-soft);border-radius:50%;
  }
  .cta-inner{max-width:560px;position:relative;z-index:2;}
  .cta h2{font-size:clamp(26px,3.6vw,40px);color:var(--white);margin-bottom:16px;}
  .cta p{color:#C7D5E1;font-size:16px;margin-bottom:30px;}
  .contact-lines{display:flex;flex-direction:column;gap:10px;margin-bottom:34px;font-family:'IBM Plex Mono',monospace;font-size:15px;}
  .contact-lines a{text-decoration:none;color:var(--white);}
  .contact-lines a:hover{color:var(--brass-light);}

  /* ---------- FOOTER ---------- */
  footer{background:var(--blueprint-deep);color:#8CA0B2;padding:30px 0;font-size:13px;}
  .foot-row{display:flex;justify-content:space-between;flex-wrap:wrap;gap:12px;}
  footer a{text-decoration:none;color:#8CA0B2;}
  footer a:hover{color:var(--white);}
</style>
</head>
<body>

<header>
  <div class="nav">
    <a href="#top" class="brand">
      <span class="brand-mark">L</span>
      <span class="brand-name">LOVY CONSTRUCTION<small>DESIGN · BUILD · CONSULT — RWANDA</small></span>
    </a>
    <div class="nav-mobile-hide">
      <nav class="links">
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav>
      <span class="nav-phone">+250 783 287 644</span>
    </div>
  </div>
</header>

<section class="hero" id="top">
  <div class="wrap hero-inner">
    <div class="hero-eyebrow"><span class="rule"></span> LOVY CONSTRUCTION LTD — EST. RWANDA</div>
    <h1>Structures engineered for the ground they stand on, <em>not the other way around.</em></h1>
    <p class="lede">LOVY Construction LTD is a Rwandan engineering and construction firm delivering structural audits, permitting, architectural design and specialised construction — from mining infrastructure to residential and institutional buildings.</p>
    <div class="hero-ctas">
      <a href="#projects" class="btn btn-primary">View our projects</a>
      <a href="#contact" class="btn btn-ghost">Start a project</a>
    </div>

    <div class="stat-strip">
      <div><div class="stat-num">8+</div><div class="stat-label">YEARS IN OPERATION</div></div>
      <div><div class="stat-num">40+</div><div class="stat-label">PROJECTS DELIVERED</div></div>
      <div><div class="stat-num">07</div><div class="stat-label">CORE SERVICE LINES</div></div>
      <div><div class="stat-num">RW</div><div class="stat-label">NATIONWIDE COVERAGE</div></div>
    </div>

    <img class="photo photo-hero" src="assets/hero.jpg" alt="LOVY Construction — site photo" onerror="this.remove()">
  </div>
</section>

<section class="about section" id="about">
  <div class="wrap">
    <img class="photo photo-about" src="assets/about.jpg" alt="LOVY Construction — team or site" onerror="this.remove()">
  </div>
  <div class="wrap about-grid">
    <div>
      <div class="section-tag">01 — WHO WE ARE</div>
      <h2 style="margin-bottom:22px;max-width:480px;">A construction and engineering partner built on technical rigor.</h2>
      <p>For more than eight years, LOVY Construction LTD has worked across Rwanda on projects that demand precision before they demand speed — geological and hydrological assessments for mining infrastructure, structural audits for existing buildings, and full design-to-completion work for residential, institutional and commercial clients.</p>
      <p>Our team brings together architecture, structural engineering and site management under one roof, so a project's feasibility study, permit request, construction and finishing are handled with a single, consistent standard from first survey to handover.</p>
    </div>
    <div class="about-figure">
      <span class="corner c1"></span><span class="corner c2"></span><span class="corner c3"></span><span class="corner c4"></span>
      <h3>Company Record</h3>
      <div class="founded-row"><span>Sector</span><span>Construction &amp; Engineering</span></div>
      <div class="founded-row"><span>Years active</span><span>8+</span></div>
      <div class="founded-row"><span>Projects completed</span><span>40+</span></div>
      <div class="founded-row"><span>Coverage</span><span>Rwanda, nationwide</span></div>
      <div class="founded-row"><span>Service lines</span><span>7</span></div>
      <div class="founded-row"><span>Contact</span><span>+250 783 287 644</span></div>
    </div>
  </div>
</section>

<section class="services section" id="services">
  <div class="wrap">
    <div class="section-head">
      <div>
        <div class="section-tag">02 — WHAT WE DO</div>
        <h2>Seven service lines, one point of accountability.</h2>
      </div>
      <p>From feasibility through finishing, each service can stand alone or fold into a full design-and-build engagement.</p>
    </div>

    <div class="svc-index">
      <div class="svc-row">
        <div class="n mono">01</div>
        <h3>Design &amp; Structural Audit</h3>
        <p>Architectural design and assessment of existing structures for safety, compliance and reinforcement needs.</p>
      </div>
      <div class="svc-row">
        <div class="n mono">02</div>
        <h3>Construction Permit Requests</h3>
        <p>Preparing and processing the technical documentation required to secure building permits from local authorities.</p>
      </div>
      <div class="svc-row">
        <div class="n mono">03</div>
        <h3>Building Completion &amp; Finishing</h3>
        <p>Interior and exterior finishing works that bring a structure from shell to handover-ready.</p>
      </div>
      <div class="svc-row">
        <div class="n mono">04</div>
        <h3>Specialized Construction Activities</h3>
        <p>Technical works including geological, hydrological and shaft-engineering support for industrial and mining sites.</p>
      </div>
      <div class="svc-row">
        <div class="n mono">05</div>
        <h3>Real Estate Activities</h3>
        <p>Support across property development, from land assessment to delivery of residential and commercial units.</p>
      </div>
      <div class="svc-row">
        <div class="n mono">06</div>
        <h3>Architectural &amp; Engineering Services</h3>
        <p>Full design services spanning concept, structural engineering, and construction documentation.</p>
      </div>
      <div class="svc-row">
        <div class="n mono">07</div>
        <h3>Technical Consultancy</h3>
        <p>Independent advisory support on feasibility, safety and construction strategy for clients and partners.</p>
      </div>
    </div>
  </div>
</section>

<section class="projects section" id="projects">
  <div class="wrap">
    <div class="section-head">
      <div>
        <div class="section-tag">03 — SELECTED WORK</div>
        <h2>Three projects, three different disciplines.</h2>
      </div>
      <p>A sample of engagements spanning industrial engineering, education and residential construction.</p>
    </div>

    <div class="sheet">
      <img class="sheet-photo" src="assets/project-mining.jpg" alt="Mining shaft feasibility project" onerror="this.remove()">
      <div class="sheet-body">
        <div class="sheet-main">
          <div class="sheet-status">2026 · COMPLETED</div>
          <h3>Feasibility Study for Geological, Hydrological &amp; Engineering Design — Safe Mining Operations at 100m (Blind Vertical Shaft)</h3>
          <p class="desc">A technical feasibility study covering geological and hydrological conditions and engineering design to support safe operation of a 100-metre blind vertical mining shaft.</p>
        </div>
        <div class="sheet-block">
          <div class="sheet-field"><div class="label">Client</div><div class="value">New Bugarama Mining Company Ltd</div></div>
          <div class="sheet-field"><div class="label">Location</div><div class="value">Burera District<br>Kagogo Sector, Nyamabuye Cell</div></div>
          <div class="sheet-field"><div class="label">Duration</div><div class="value">Jan 2026 – Apr 2026</div></div>
        </div>
      </div>
    </div>

    <div class="sheet">
      <img class="sheet-photo" src="assets/project-nursery.jpg" alt="Nursery school project" onerror="this.remove()">
      <div class="sheet-body">
        <div class="sheet-main">
          <div class="sheet-status">DESIGN</div>
          <h3>Proposed G+3 Nursery School</h3>
          <p class="desc">Architectural design for a ground-plus-three nursery school facility, planned for early childhood learning and daily classroom use.</p>
        </div>
        <div class="sheet-block">
          <div class="sheet-field"><div class="label">Client</div><div class="value">Wisdom School Runda</div></div>
          <div class="sheet-field"><div class="label">Building type</div><div class="value">G+3 Educational Facility</div></div>
          <div class="sheet-field"><div class="label">Scope</div><div class="value">Architectural design</div></div>
        </div>
      </div>
    </div>

    <div class="sheet">
      <img class="sheet-photo" src="assets/project-residential.jpg" alt="Residential building project" onerror="this.remove()">
      <div class="sheet-body">
        <div class="sheet-main">
          <div class="sheet-status">2025 · COMPLETED</div>
          <h3>Proposed Residential Building</h3>
          <p class="desc">Design and construction of a residential building, delivered from proposal through to completion.</p>
        </div>
        <div class="sheet-block">
          <div class="sheet-field"><div class="label">Location</div><div class="value">Gasabo District<br>Bumbogo Sector, Ngara Cell<br>Birembo Village</div></div>
          <div class="sheet-field"><div class="label">Duration</div><div class="value">Feb 2025 – Nov 2025</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="cta" id="contact">
  <div class="wrap">
    <div class="cta-inner">
      <div class="section-tag" style="color:var(--line);">04 — GET IN TOUCH</div>
      <h2>Have a site, a structure, or a permit to work through?</h2>
      <p>Tell us about the project — location, scope and timeline — and we'll follow up with next steps.</p>
      <div class="contact-lines">
        <a href="tel:+250783287644">+250 783 287 644</a>
        <a href="mailto:Lovyconstruction@gmail.com">Lovyconstruction@gmail.com</a>
      </div>
      <a href="mailto:Lovyconstruction@gmail.com" class="btn btn-primary">Email LOVY Construction</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap foot-row">
    <span>© 2026 LOVY Construction LTD. All rights reserved.</span>
    <span><a href="tel:+250783287644">+250 783 287 644</a> · <a href="mailto:Lovyconstruction@gmail.com">Lovyconstruction@gmail.com</a></span>
  </div>
</footer>

</body>
</html>

