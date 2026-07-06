<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Jahangir Amiri — Data Science &amp; AI</title>
<meta name="description" content="Jahangir Amiri — Data Science & AI postgraduate diploma student. Background in economics, music and the development sector, now building in machine learning and forecasting.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#F1F3F0;
    --paper-raised:#FFFFFF;
    --ink:#1B2430;
    --ink-soft:#5B6472;
    --line:#D7DCD6;
    --teal:#2F6F6B;
    --teal-soft:#E4EEEC;
    --amber:#E2A33D;
    --coral:#C1554A;
    --radius:10px;
    --maxw:920px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    *{animation-duration:0.01ms !important; animation-iteration-count:1 !important; transition-duration:0.01ms !important;}
  }
  body{
    margin:0;
    background:
      linear-gradient(90deg, rgba(27,36,48,0.035) 1px, transparent 1px) 0 0/28px 28px,
      linear-gradient(rgba(27,36,48,0.035) 1px, transparent 1px) 0 0/28px 28px,
      var(--paper);
    color:var(--ink);
    font-family:'IBM Plex Sans', system-ui, sans-serif;
    line-height:1.55;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3{
    font-family:'Space Grotesk', sans-serif;
    letter-spacing:-0.01em;
    margin:0;
  }
  .mono{font-family:'IBM Plex Mono', monospace;}
  a{color:var(--teal);}
  .wrap{max-width:var(--maxw); margin:0 auto; padding:0 24px;}

  /* ---------- nav ---------- */
  nav{
    position:sticky; top:0; z-index:20;
    background:rgba(241,243,240,0.88);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--line);
  }
  nav .wrap{display:flex; align-items:center; justify-content:space-between; padding-top:14px; padding-bottom:14px;}
  .brand{font-family:'IBM Plex Mono', monospace; font-size:14px; color:var(--ink); text-decoration:none; font-weight:500;}
  .brand span{color:var(--teal);}
  .navlinks{display:flex; gap:22px; list-style:none; margin:0; padding:0;}
  .navlinks a{
    font-family:'IBM Plex Mono', monospace; font-size:12.5px; text-decoration:none; color:var(--ink-soft);
    text-transform:lowercase;
  }
  .navlinks a:hover{color:var(--teal);}
  @media (max-width:560px){ .navlinks{gap:14px;} .navlinks a{font-size:11px;} }

  /* ---------- notebook cell shell ---------- */
  .cell{
    max-width:var(--maxw); margin:0 auto; padding:0 24px;
  }
  .cell-inner{
    background:var(--paper-raised);
    border:1px solid var(--line);
    border-radius:var(--radius);
    padding:32px clamp(20px,4vw,44px);
    margin:22px 0;
  }
  .cell-tag{
    display:flex; align-items:center; gap:8px;
    font-family:'IBM Plex Mono', monospace;
    font-size:12px; color:var(--ink-soft);
    margin-bottom:14px;
  }
  .cell-tag .dot{width:7px; height:7px; border-radius:50%; background:var(--teal); display:inline-block;}
  .cell-tag.out .dot{background:var(--coral);}
  section{scroll-margin-top:70px;}
  .eyebrow{
    font-family:'IBM Plex Mono', monospace; font-size:12px; color:var(--teal);
    text-transform:uppercase; letter-spacing:0.08em; margin-bottom:8px; display:block;
  }

  /* ---------- hero ---------- */
  .hero-cell{padding-top:8px;}
  .hero-grid{display:grid; grid-template-columns:auto 1fr; gap:26px; align-items:center;}
  @media (max-width:640px){ .hero-grid{grid-template-columns:1fr; text-align:center;} .hero-grid .avatar{margin:0 auto;} }
  .avatar{
    width:104px; height:104px; border-radius:50%;
    object-fit:cover; border:2px solid var(--line);
    background:var(--teal-soft);
  }
  .avatar-fallback{
    width:104px; height:104px; border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    background:var(--teal-soft); color:var(--teal);
    font-family:'Space Grotesk',sans-serif; font-weight:700; font-size:34px;
    border:2px solid var(--line);
  }
  h1{font-size:clamp(28px,4vw,38px); font-weight:700;}
  .role{font-family:'IBM Plex Mono', monospace; color:var(--teal); font-size:14px; margin-top:6px;}
  .pitch{margin-top:12px; color:var(--ink-soft); max-width:56ch;}
  .chips{display:flex; flex-wrap:wrap; gap:8px; margin-top:16px;}
  @media (max-width:640px){ .chips{justify-content:center;} }
  .chip{
    font-family:'IBM Plex Mono', monospace; font-size:12px;
    border:1px solid var(--line); border-radius:999px;
    padding:5px 12px; color:var(--ink-soft); background:var(--paper);
  }

  /* ---------- timeline ---------- */
  .timeline{list-style:none; margin:20px 0 0; padding:0; border-left:2px solid var(--line);}
  .timeline li{position:relative; padding:0 0 22px 22px;}
  .timeline li:last-child{padding-bottom:0;}
  .timeline li::before{
    content:''; position:absolute; left:-6px; top:4px;
    width:10px; height:10px; border-radius:50%; background:var(--paper-raised);
    border:2px solid var(--teal);
  }
  .timeline li.current::before{background:var(--amber); border-color:var(--amber);}
  .t-date{font-family:'IBM Plex Mono', monospace; font-size:12px; color:var(--teal); display:block; margin-bottom:2px;}
  .timeline li.current .t-date{color:var(--amber);}
  .t-role{font-weight:600;}
  .t-desc{color:var(--ink-soft); font-size:14.5px; margin-top:2px;}

  /* ---------- education ---------- */
  .edu-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:12px; margin-top:16px;}
  .edu-item{
    border:1px solid var(--line); border-radius:8px; padding:14px 16px;
    background:var(--paper);
  }
  .edu-item .deg{font-weight:600; font-size:14.5px;}
  .edu-item .inst{font-family:'IBM Plex Mono', monospace; font-size:12px; color:var(--ink-soft); margin-top:3px;}

  /* ---------- skills ---------- */
  .skill-group{margin-top:22px;}
  .skill-group:first-of-type{margin-top:16px;}
  .skill-group h3{font-size:14px; font-family:'IBM Plex Mono', monospace; color:var(--ink-soft); font-weight:500; text-transform:uppercase; letter-spacing:0.05em; margin-bottom:10px;}
  .skill-row{display:flex; align-items:center; gap:12px; margin-bottom:9px;}
  .skill-name{width:150px; flex-shrink:0; font-size:14px;}
  .skill-bar{flex:1; height:8px; background:var(--line); border-radius:99px; overflow:hidden;}
  .skill-bar > span{display:block; height:100%; background:var(--teal); border-radius:99px;}
  .skill-bar > span.learning{background:var(--amber);}
  .skill-label{width:110px; text-align:right; font-family:'IBM Plex Mono', monospace; font-size:11px; color:var(--ink-soft); flex-shrink:0;}
  @media (max-width:560px){ .skill-name{width:100px; font-size:13px;} .skill-label{width:80px; font-size:10px;} }
  .legend{display:flex; gap:18px; margin-top:18px; flex-wrap:wrap;}
  .legend-item{display:flex; align-items:center; gap:6px; font-family:'IBM Plex Mono', monospace; font-size:11.5px; color:var(--ink-soft);}
  .legend-dot{width:9px; height:9px; border-radius:2px;}

  /* ---------- projects ---------- */
  .proj-grid{display:grid; grid-template-columns:1fr; gap:16px; margin-top:18px;}
  .proj{
    border:1px solid var(--line); border-radius:8px; padding:20px 22px;
    background:var(--paper); position:relative;
  }
  .proj.flagship{border-color:var(--teal); background:var(--teal-soft);}
  .proj-head{display:flex; justify-content:space-between; align-items:baseline; gap:10px; flex-wrap:wrap;}
  .proj-title{font-family:'Space Grotesk',sans-serif; font-weight:600; font-size:17px;}
  .proj-tag{font-family:'IBM Plex Mono', monospace; font-size:11px; color:var(--teal); border:1px solid var(--teal); border-radius:99px; padding:3px 10px;}
  .proj p{margin:8px 0 0; color:var(--ink-soft); font-size:14.5px;}
  .proj-meta{display:flex; flex-wrap:wrap; gap:8px; margin-top:10px;}
  .proj-meta span{
    font-family:'IBM Plex Mono', monospace; font-size:11px; color:var(--ink-soft);
    background:var(--paper-raised); border:1px solid var(--line); padding:3px 9px; border-radius:6px;
  }
  .proj-note{margin-top:10px; font-size:13px; color:var(--ink-soft); font-style:italic;}

  /* ---------- learning now ---------- */
  .learn-list{display:flex; flex-wrap:wrap; gap:10px; margin-top:16px;}
  .learn-pill{
    font-family:'IBM Plex Mono', monospace; font-size:12.5px;
    border:1px dashed var(--amber); color:#8a611f; background:#FCF3E3;
    padding:6px 13px; border-radius:99px;
  }

  /* ---------- hobbies ---------- */
  .hobby-list{display:flex; flex-wrap:wrap; gap:10px; margin-top:16px;}
  .hobby-pill{
    font-size:13.5px; border:1px solid var(--line); border-radius:99px;
    padding:6px 14px; background:var(--paper);
  }

  /* ---------- contact ---------- */
  .contact-grid{display:flex; flex-wrap:wrap; gap:12px; margin-top:18px;}
  .contact-link{
    display:inline-flex; align-items:center; gap:8px;
    border:1px solid var(--line); border-radius:8px; padding:10px 16px;
    text-decoration:none; color:var(--ink); background:var(--paper);
    font-size:14px; transition:border-color .15s, color .15s;
  }
  .contact-link:hover{border-color:var(--teal); color:var(--teal);}

  footer{
    text-align:center; padding:36px 24px 46px;
    font-family:'IBM Plex Mono', monospace; font-size:11.5px; color:var(--ink-soft);
  }

  ::selection{background:var(--teal); color:#fff;}

  /* focus visibility */
  a:focus-visible, button:focus-visible{outline:2px solid var(--teal); outline-offset:2px;}
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <a class="brand" href="#top">jahangir<span>.py</span></a>
    <ul class="navlinks">
      <li><a href="#background">background</a></li>
      <li><a href="#skills">skills</a></li>
      <li><a href="#projects">projects</a></li>
      <li><a href="#contact">contact</a></li>
    </ul>
  </div>
</nav>

<!-- ============ HERO ============ -->
<div class="cell" id="top">
  <div class="cell-inner hero-cell">
    <div class="cell-tag"><span class="dot"></span> In [1]: load_profile()</div>

    <div class="hero-grid">
      <!-- Replace Jahangir.jpg with your own photo in the same folder as this file -->
      <img class="avatar" src="Jahangir.jpg" alt="Jahangir Amiri"
           onerror="this.replaceWith(Object.assign(document.createElement('div'),{className:'avatar-fallback',textContent:'JA'}))">
      <div>
        <h1>Jahangir Amiri</h1>
        <div class="role">Data Science &amp; AI · Postgraduate Diploma, NED University</div>
        <p class="pitch">Coming to machine learning from economics, music and five years in the development sector —
          now building models, pipelines and small AI-powered tools as I go, one graded assignment and one side
          project at a time.</p>
        <div class="chips">
          <span class="chip">Karachi, PK</span>
          <span class="chip">Python · pandas · scikit-learn</span>
          <span class="chip">SQL · Power BI</span>
          <span class="chip">Currently: time-series forecasting</span>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- ============ BACKGROUND ============ -->
<section id="background">
  <div class="cell">
    <div class="cell-inner">
      <span class="eyebrow"># background</span>
      <h2>From economics and the field to models and notebooks</h2>
      <p style="color:var(--ink-soft); margin-top:10px; max-width:64ch;">
        I studied Economics through to a Master's, then trained formally as a musician at NAPA, and spent five years
        working across different roles in Pakistan's development sector — editing content, coordinating field
        operations, and supporting communities directly. Data science is the newest chapter: I'm currently a
        postgraduate diploma student in Data Science &amp; AI at NED University, working through machine learning
        and deep learning fundamentals and building small, honest projects along the way.
      </p>

      <ul class="timeline">
        <li>
          <span class="t-date">2011 – 2013</span>
          <div class="t-role">Website Editor</div>
          <div class="t-desc">Early hands-on exposure to the web and digital content.</div>
        </li>
        <li>
          <span class="t-date">2015 – 2018</span>
          <div class="t-role">Zonal Field Officer</div>
          <div class="t-desc">Field-based coordination and reporting in the development sector.</div>
        </li>
        <li>
          <span class="t-date">2020 – 2022</span>
          <div class="t-role">Community Support Specialist</div>
          <div class="t-desc">Direct community engagement and support work.</div>
        </li>
        <li class="current">
          <span class="t-date">Now</span>
          <div class="t-role">Postgraduate Diploma, Data Science &amp; AI — NED University, Karachi</div>
          <div class="t-desc">Machine learning, deep learning, and data tools, applied through weekly assignments and self-directed projects.</div>
        </li>
      </ul>

      <span class="eyebrow" style="margin-top:26px;">education &amp; certifications</span>
      <div class="edu-grid">
        <div class="edu-item"><div class="deg">Postgraduate Diploma, Data Science &amp; AI</div><div class="inst">NED University of Engineering &amp; Technology</div></div>
        <div class="edu-item"><div class="deg">MA Economics</div><div class="inst">University of Karachi</div></div>
        <div class="edu-item"><div class="deg">BA (Hons) Economics</div><div class="inst">University of Karachi</div></div>
        <div class="edu-item"><div class="deg">Diploma in Music</div><div class="inst">National Academy of Performing Arts</div></div>
        <div class="edu-item"><div class="deg">Project Management</div><div class="inst">Institute of Business Administration</div></div>
      </div>
    </div>
  </div>
</section>

<!-- ============ SKILLS ============ -->
<section id="skills">
  <div class="cell">
    <div class="cell-inner">
      <span class="eyebrow"># skills</span>
      <h2>What I use, honestly rated</h2>
      <p style="color:var(--ink-soft); margin-top:8px;">No inflated star ratings — this is roughly where each skill
        actually sits right now.</p>

      <div class="skill-group">
        <h3>Core toolkit</h3>
        <div class="skill-row"><span class="skill-name">Python (pandas, NumPy)</span><div class="skill-bar"><span style="width:70%"></span></div><span class="skill-label">applied</span></div>
        <div class="skill-row"><span class="skill-name">scikit-learn</span><div class="skill-bar"><span style="width:65%"></span></div><span class="skill-label">applied</span></div>
        <div class="skill-row"><span class="skill-name">SQL</span><div class="skill-bar"><span style="width:55%"></span></div><span class="skill-label">practicing</span></div>
        <div class="skill-row"><span class="skill-name">Power BI</span><div class="skill-bar"><span style="width:50%"></span></div><span class="skill-label">practicing</span></div>
      </div>

      <div class="skill-group">
        <h3>Machine learning</h3>
        <div class="skill-row"><span class="skill-name">Classification (RF, XGBoost)</span><div class="skill-bar"><span style="width:65%"></span></div><span class="skill-label">applied</span></div>
        <div class="skill-row"><span class="skill-name">Regression</span><div class="skill-bar"><span style="width:65%"></span></div><span class="skill-label">applied</span></div>
        <div class="skill-row"><span class="skill-name">Clustering (KNN, K-Means)</span><div class="skill-bar"><span style="width:55%"></span></div><span class="skill-label">practicing</span></div>
        <div class="skill-row"><span class="skill-name">sklearn Pipelines / PyCaret</span><div class="skill-bar"><span class="learning" style="width:35%"></span></div><span class="skill-label">learning now</span></div>
      </div>

      <div class="skill-group">
        <h3>Deep learning &amp; forecasting</h3>
        <div class="skill-row"><span class="skill-name">Perceptrons / MLPs</span><div class="skill-bar"><span style="width:55%"></span></div><span class="skill-label">practicing</span></div>
        <div class="skill-row"><span class="skill-name">RNNs / LSTMs / GRUs</span><div class="skill-bar"><span style="width:45%"></span></div><span class="skill-label">practicing</span></div>
        <div class="skill-row"><span class="skill-name">ARIMA / SARIMA</span><div class="skill-bar"><span class="learning" style="width:25%"></span></div><span class="skill-label">learning now</span></div>
      </div>

      <div class="legend">
        <span class="legend-item"><span class="legend-dot" style="background:var(--teal)"></span>practicing / applied</span>
        <span class="legend-item"><span class="legend-dot" style="background:var(--amber)"></span>currently learning</span>
      </div>
    </div>
  </div>
</section>

<!-- ============ PROJECTS ============ -->
<section id="projects">
  <div class="cell">
    <div class="cell-inner">
      <span class="eyebrow"># projects</span>
      <h2>Things I've actually built</h2>

      <div class="proj-grid">
        <div class="proj">
          <div class="proj-head"><span class="proj-title">Healthcare Disease Prediction System</span></div>
          <p>End-to-end pipeline: preprocessing, a Random Forest classifier, and a set of visualizations, built as a
            graded assignment.</p>
          <div class="proj-meta"><span>Random Forest</span><span>scikit-learn Pipeline</span><span>Coursework</span></div>
          <p class="proj-note">Trained on a synthetic dataset — noted transparently in the submission, not dressed up as real clinical data.</p>
        </div>

        <div class="proj">
          <div class="proj-head"><span class="proj-title">Bank Customer Churn Prediction</span></div>
          <p>Logistic regression model on a 10,000-customer dataset, packaged into an executive-style presentation
            built directly from the analysis notebook.</p>
          <div class="proj-meta"><span>Logistic Regression</span><span>10k rows</span><span>Executive deck</span></div>
        </div>

      </div>

      <span class="eyebrow" style="margin-top:30px;">currently learning</span>
      <div class="learn-list">
        <span class="learn-pill">Imputers</span>
        <span class="learn-pill">scikit-learn Pipelines</span>
        <span class="learn-pill">PyCaret</span>
        <span class="learn-pill">ARIMA</span>
        <span class="learn-pill">SARIMA</span>
      </div>
    </div>
  </div>
</section>

<!-- ============ HOBBIES ============ -->
<div class="cell">
  <div class="cell-inner">
    <span class="eyebrow"># off the clock</span>
    <div class="hobby-list">
      <span class="hobby-pill">🎸 Guitar</span>
      <span class="hobby-pill">🎤 Singing</span>
      <span class="hobby-pill">✈️ Traveling</span>
      <span class="hobby-pill">🏸 Badminton</span>
    </div>
  </div>
</div>

<!-- ============ CONTACT ============ -->
<section id="contact">
  <div class="cell">
    <div class="cell-inner">
      <span class="eyebrow"># contact</span>
      <h2>Get in touch</h2>
      <p style="color:var(--ink-soft); margin-top:8px;">Happy to talk about data science, internships, or music — reach out however suits you.</p>
      <div class="contact-grid">
        <a class="contact-link" href="mailto:jhngramiri@gmail.com">✉️ Email</a>
        <a class="contact-link" href="https://www.facebook.com/jahangir.k.aij" target="_blank" rel="noopener">Facebook</a>
        <a class="contact-link" href="https://www.instagram.com/here_amiri/?hl=en" target="_blank" rel="noopener">Instagram</a>
        <a class="contact-link" href="https://twitter.com/amirijahangir" target="_blank" rel="noopener">Twitter / X</a>
        <!-- Add your LinkedIn and GitHub here once set up, e.g.:
        <a class="contact-link" href="https://linkedin.com/in/your-handle" target="_blank" rel="noopener">LinkedIn</a>
        <a class="contact-link" href="https://github.com/your-handle" target="_blank" rel="noopener">GitHub</a> -->
      </div>
    </div>
  </div>
</section>

<footer>
  built with pandas, patience, and a little bit of guitar &nbsp;·&nbsp; Karachi
</footer>

</body>
</html>
