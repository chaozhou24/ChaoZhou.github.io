---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
:root{
  --main-color:#8c6a12;
  --main-dark:#5f4700;
  --main-light:#b8922e;
  --accent-blue:#1f5fae;
  --accent-blue-soft:#eef4ff;

  --soft-bg:#f7f4ee;
  --card-bg:rgba(255,255,255,0.88);
  --card-solid:#ffffff;
  --hero-bg-1:#fffdf8;
  --hero-bg-2:#f7efdf;
  --hero-bg-3:#f3ead7;

  --border-light:rgba(222,212,187,0.75);
  --border-mid:rgba(211,196,157,0.95);

  --text-main:#1f1f1f;
  --text-soft:#5e5e5e;
  --text-faint:#7a7a7a;

  --shadow-soft:0 10px 30px rgba(30,30,30,0.06);
  --shadow-mid:0 16px 40px rgba(40,30,10,0.10);
  --shadow-hover:0 24px 50px rgba(40,30,10,0.14);

  --radius-xl:30px;
  --radius-lg:24px;
  --radius-md:18px;
  --radius-sm:14px;
}

html{
  scroll-behavior:smooth;
}

body{
  background:
    radial-gradient(circle at top right, rgba(184,146,46,0.10), transparent 20%),
    linear-gradient(180deg, #fcfbf8 0%, #f7f3eb 100%);
}

.page__content{
  font-size:17px;
  line-height:1.85;
  color:var(--text-main);
}

.page__content a{
  color:var(--accent-blue);
  text-decoration:none;
  transition:all 0.22s ease;
}

.page__content a:hover{
  text-decoration:none;
  opacity:0.88;
}

/* ===== overall spacing ===== */
.home-wrapper{
  display:flex;
  flex-direction:column;
  gap:22px;
}

/* ===== Hero ===== */
.hero-shell{
  position:relative;
  overflow:hidden;
  border-radius:var(--radius-xl);
  border:1px solid var(--border-light);
  background:
    linear-gradient(135deg, var(--hero-bg-1) 0%, var(--hero-bg-2) 52%, var(--hero-bg-3) 100%);
  box-shadow:var(--shadow-mid);
  padding:34px;
}

.hero-shell::before{
  content:"";
  position:absolute;
  width:340px;
  height:340px;
  right:-120px;
  top:-120px;
  border-radius:50%;
  background:radial-gradient(circle, rgba(184,146,46,0.18) 0%, rgba(184,146,46,0.05) 48%, rgba(184,146,46,0) 72%);
  pointer-events:none;
}

.hero-shell::after{
  content:"";
  position:absolute;
  width:260px;
  height:260px;
  left:-80px;
  bottom:-100px;
  border-radius:50%;
  background:radial-gradient(circle, rgba(31,95,174,0.10) 0%, rgba(31,95,174,0.03) 52%, rgba(31,95,174,0) 75%);
  pointer-events:none;
}

.hero-grid{
  position:relative;
  z-index:1;
  display:grid;
  grid-template-columns:1.35fr 0.78fr;
  gap:24px;
  align-items:stretch;
}

.hero-main,
.hero-side{
  background:rgba(255,255,255,0.52);
  backdrop-filter:blur(8px);
  -webkit-backdrop-filter:blur(8px);
  border:1px solid rgba(255,255,255,0.65);
  border-radius:24px;
  box-shadow:0 8px 24px rgba(0,0,0,0.04);
}

.hero-main{
  padding:30px 30px 26px 30px;
}

.hero-side{
  padding:24px 24px 20px 24px;
  display:flex;
  flex-direction:column;
  justify-content:space-between;
}

.hero-badge{
  display:inline-flex;
  align-items:center;
  gap:8px;
  margin-bottom:16px;
  padding:7px 14px;
  border-radius:999px;
  background:#fff7e8;
  border:1px solid #ead7a1;
  color:var(--main-dark);
  font-size:0.94rem;
  font-weight:800;
  letter-spacing:0.2px;
}

.hero-title{
  margin:0 0 14px 0;
  font-size:2.45rem;
  line-height:1.18;
  font-weight:850;
  letter-spacing:-0.02em;
  color:var(--text-main);
}

.hero-title strong{
  color:var(--main-dark);
}

.hero-intro{
  font-size:1.04rem;
  color:var(--text-soft);
  margin:0 0 14px 0;
}

.hero-intro strong{
  color:var(--text-main);
}

.hero-email{
  font-weight:800;
  color:var(--main-dark);
}

.hero-quick{
  display:flex;
  flex-wrap:wrap;
  gap:12px;
  margin-top:20px;
}

.hero-btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:10px 18px;
  border-radius:999px;
  border:1px solid var(--border-mid);
  background:#ffffff;
  color:var(--main-color) !important;
  font-weight:750;
  text-decoration:none !important;
  box-shadow:0 4px 12px rgba(0,0,0,0.04);
  transition:all 0.22s ease;
}

.hero-btn:hover{
  transform:translateY(-2px);
  background:#fff8e7;
  border-color:#d9c28d;
  box-shadow:0 12px 24px rgba(0,0,0,0.08);
}

.hero-btn.primary{
  background:linear-gradient(135deg, #9b7515 0%, #7f6000 100%);
  color:#fff !important;
  border-color:#86640f;
}

.hero-btn.primary:hover{
  background:linear-gradient(135deg, #ad8420 0%, #8a6705 100%);
}

.mini-panel-title{
  margin:0 0 14px 0;
  font-size:0.98rem;
  font-weight:800;
  color:var(--text-main);
}

.profile-mini{
  display:flex;
  flex-direction:column;
  gap:14px;
}

.profile-stat{
  display:flex;
  align-items:flex-start;
  gap:12px;
  padding:12px 14px;
  border-radius:16px;
  background:rgba(255,255,255,0.72);
  border:1px solid rgba(231,222,200,0.9);
}

.profile-stat .icon{
  flex:0 0 38px;
  width:38px;
  height:38px;
  border-radius:12px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:#fff5da;
  color:var(--main-dark);
  font-size:1rem;
  font-weight:800;
}

.profile-stat .meta{
  line-height:1.55;
}

.profile-stat .meta strong{
  display:block;
  color:var(--text-main);
  font-size:0.98rem;
}

.profile-stat .meta span{
  color:var(--text-faint);
  font-size:0.92rem;
}

/* ===== section header ===== */
.section-title{
  display:flex;
  align-items:center;
  gap:12px;
  font-size:1.48rem;
  font-weight:850;
  color:var(--text-main);
  margin:6px 0 4px 0;
}

.section-title::before{
  content:"";
  width:6px;
  height:24px;
  border-radius:999px;
  background:linear-gradient(180deg, var(--main-light), var(--main-dark));
  box-shadow:0 2px 8px rgba(127,96,0,0.18);
}

.section-subtitle{
  margin:-4px 0 8px 18px;
  color:var(--text-faint);
  font-size:0.96rem;
}

/* ===== Research ===== */
.research-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit, minmax(260px, 1fr));
  gap:22px;
}

.research-card{
  position:relative;
  overflow:hidden;
  background:linear-gradient(180deg, rgba(255,255,255,0.92) 0%, rgba(255,255,255,0.84) 100%);
  border:1px solid var(--border-light);
  border-radius:var(--radius-lg);
  padding:24px 22px 20px 22px;
  box-shadow:var(--shadow-soft);
  transition:all 0.25s ease;
}

.research-card::after{
  content:"";
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:4px;
  background:linear-gradient(90deg, #a67d14 0%, #d0b25d 100%);
}

.research-card:hover{
  transform:translateY(-5px);
  box-shadow:var(--shadow-hover);
  border-color:#decea2;
}

.research-card h3{
  margin:0 0 14px 0;
  color:var(--main-color);
  font-size:1.16rem;
  line-height:1.4;
}

.research-card ul{
  margin:0;
  padding-left:20px;
}

.research-card li{
  margin:10px 0;
  color:var(--text-soft);
}

.research-card li::marker{
  color:var(--main-light);
}

/* ===== News ===== */
.news-board{
  background:linear-gradient(180deg, rgba(255,255,255,0.9) 0%, rgba(255,255,255,0.82) 100%);
  border:1px solid var(--border-light);
  border-radius:var(--radius-lg);
  padding:24px 24px 10px 24px;
  box-shadow:var(--shadow-soft);
}

.news-timeline{
  position:relative;
  margin-top:4px;
  padding-left:28px;
  border-left:2px solid #e9dfcb;
}

.news-item{
  position:relative;
  margin-bottom:22px;
  padding:0 0 0 12px;
}

.news-item::before{
  content:"";
  position:absolute;
  left:-37px;
  top:8px;
  width:14px;
  height:14px;
  border-radius:50%;
  background:linear-gradient(135deg, var(--main-light), var(--main-dark));
  box-shadow:0 0 0 5px #f9f3e7;
}

.news-date{
  display:inline-flex;
  align-items:center;
  padding:4px 10px;
  border-radius:999px;
  margin-right:10px;
  background:#fff7e7;
  border:1px solid #eadbb2;
  font-weight:800;
  color:var(--main-dark);
  font-size:0.92rem;
}

.news-item p{
  display:inline;
  margin:0;
  color:var(--text-main);
}

.news-item a{
  font-weight:700;
}

/* ===== Services ===== */
.service-block{
  background:linear-gradient(180deg, rgba(255,255,255,0.92) 0%, rgba(255,255,255,0.84) 100%);
  border:1px solid var(--border-light);
  border-radius:var(--radius-lg);
  padding:24px;
  box-shadow:var(--shadow-soft);
}

.service-group + .service-group{
  margin-top:22px;
  padding-top:20px;
  border-top:1px dashed #e6dbc0;
}

.service-heading{
  display:flex;
  align-items:center;
  gap:10px;
  margin:0 0 14px 0;
  font-size:1rem;
  color:var(--text-main);
  font-weight:800;
}

.service-heading::before{
  content:"";
  width:10px;
  height:10px;
  border-radius:50%;
  background:var(--main-color);
}

.tags{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
}

.tag{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:8px 14px;
  border-radius:999px;
  background:linear-gradient(180deg, #fff9ea 0%, #fff4d7 100%);
  border:1px solid #ecdcae;
  color:#6f5400;
  font-size:0.92rem;
  font-weight:700;
  transition:all 0.22s ease;
}

.tag:hover{
  transform:translateY(-2px);
  box-shadow:0 10px 20px rgba(0,0,0,0.06);
}

/* ===== small highlight row ===== */
.highlight-row{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
}

.highlight-pill{
  display:inline-flex;
  align-items:center;
  padding:7px 13px;
  border-radius:999px;
  background:#fffaf0;
  border:1px solid #eadab0;
  color:var(--main-dark);
  font-size:0.92rem;
  font-weight:750;
}

/* ===== Responsive ===== */
@media (max-width: 900px){
  .hero-grid{
    grid-template-columns:1fr;
  }

  .hero-shell{
    padding:22px;
  }

  .hero-main,
  .hero-side{
    padding:22px;
  }

  .hero-title{
    font-size:2rem;
  }
}

@media (max-width: 768px){
  .page__content{
    font-size:16px;
  }

  .hero-title{
    font-size:1.8rem;
  }

  .section-title{
    font-size:1.3rem;
  }

  .news-board,
  .service-block,
  .research-card{
    padding:20px;
  }
}
</style>

<div class="home-wrapper">

  <div class="hero-shell">
    <div class="hero-grid">
      <div class="hero-main">
        <div class="hero-badge">🎓 Ph.D. Student @ SUSTech</div>

        <h1 class="hero-title">
          Hello 👋, I am <strong>Chao Zhou (周超)</strong>
        </h1>

        <p class="hero-intro">
          I am a second-year <strong>Ph.D. student at Southern University of Science and Technology (SUSTech)</strong>,
          advised by Prof.
          <a href="https://www.sustech.edu.cn/en/faculties/changshengyou.html" target="_blank">
            Changsheng You
          </a>.
          I received the <strong>M.S. degree from Nanjing University of Posts and Telecommunications</strong>.
        </p>

        <p class="hero-intro">
          My research interests include <strong>Near-Field Communications</strong>,
          <strong>Intelligent Antenna and Surface</strong>, and
          <strong>Symbiotic Radio</strong>. I have published several papers in top international
          communication journals and conferences.
        </p>

        <p class="hero-intro" style="margin-bottom:0;">
          For research discussion or collaboration, please contact me via email:
          <span class="hero-email">zhouchao2024@mail.sustech.edu.cn</span>
        </p>

        <div class="hero-quick">
          <a class="hero-btn primary" href="mailto:zhouchao2024@mail.sustech.edu.cn">Email Me</a>
          <a class="hero-btn" href="https://scholar.google.com/citations?user=o5Sqh2MAAAAJ&hl=zh-CN&oi=sra" target="_blank">Google Scholar</a>
          <a class="hero-btn" href="/Publications.html">Publications</a>
          <a class="hero-btn" href="/Photos.html">Photos</a>
          <a class="hero-btn" href="#news">News</a>
        </div>
      </div>

      <div class="hero-side">
        <div>
          <p class="mini-panel-title">Academic Snapshot</p>

          <div class="profile-mini">
            <div class="profile-stat">
              <div class="icon">📍</div>
              <div class="meta">
                <strong>Affiliation</strong>
                <span>Southern University of Science and Technology</span>
              </div>
            </div>

            <div class="profile-stat">
              <div class="icon">🔬</div>
              <div class="meta">
                <strong>Focus</strong>
                <span>Near-field communications, intelligent antenna and surface, symbiotic radio</span>
              </div>
            </div>

            <div class="profile-stat">
              <div class="icon">🤝</div>
              <div class="meta">
                <strong>Looking for</strong>
                <span>Academic collaboration, research exchange, and related opportunities</span>
              </div>
            </div>
          </div>
        </div>

        <div class="highlight-row" style="margin-top:18px;">
          <span class="highlight-pill">Wireless Communications</span>
          <span class="highlight-pill">Near-Field Beamforming</span>
          <span class="highlight-pill">Intelligent Surfaces</span>
        </div>
      </div>
    </div>
  </div>

  <div>
    <div class="section-title">Research Interests</div>
    <div class="section-subtitle">Main topics and current academic directions</div>

    <div class="research-grid">
      <div class="research-card">
        <h3>Near-Field Communications</h3>
        <ul>
          <li>Flexible Beamforming Design</li>
          <li>Mixed-field Communications</li>
        </ul>
      </div>

      <div class="research-card">
        <h3>Intelligent Antenna and Surface</h3>
        <ul>
          <li>Intelligent Reflecting Surface</li>
          <li>Reconfigurable Antenna</li>
        </ul>
      </div>

      <div class="research-card">
        <h3>Backscatter Communications</h3>
        <ul>
          <li>Symbiotic Radio</li>
        </ul>
      </div>
    </div>
  </div>

  <span id="news"></span>

  <div>
    <div class="section-title">News</div>
    <div class="section-subtitle">Selected updates and recent milestones</div>

    <div class="news-board">
      <div class="news-timeline">
        <div class="news-item">
          <p>
            <span class="news-date">2026.01</span>
            Three papers have been accepted by the IEEE International Conference on Communications (ICC) 2026.
          </p>
        </div>

        <div class="news-item">
          <p>
            <span class="news-date">2024.11</span>
            I received the IEEE WCSP Best Paper Award for paper
            <a href="https://scholar.google.com/scholar?hl=zh-CN&as_sdt=0%2C5&q=Channel+Estimation+for+XL-IRS+Assisted+Wireless+Systems+with+Double-sided+Visibility+Regions&btnG=" target="_blank">
              Channel Estimation for XL-IRS Assisted Wireless Systems with Double-sided Visibility Regions
            </a>.
          </p>
        </div>

        <div class="news-item">
          <p>
            <span class="news-date">2024.10</span>
            I received China Institute of Communications Master's Thesis Incentive Program (Only 7 recipients nationwide), 2024.
          </p>
        </div>

        <div class="news-item">
          <p>
            <span class="news-date">2023.10</span>
            I received the National Scholarship for Master's Students (Top 2%), 2023.
          </p>
        </div>

        <div class="news-item">
          <p>
            <span class="news-date">2022.10</span>
            I received the National Scholarship for Master's Students (Top 2%), 2022.
          </p>
        </div>
      </div>
    </div>
  </div>

  <div>
    <div class="section-title">Academic Services</div>
    <div class="section-subtitle">Reviewing activities for journals and conferences</div>

    <div class="service-block">
      <div class="service-group">
        <p class="service-heading">Reviewer for Journals</p>
        <div class="tags">
          <span class="tag">IEEE JSAC</span>
          <span class="tag">IEEE TWC</span>
          <span class="tag">IEEE TMC</span>
          <span class="tag">IEEE TCOM</span>
          <span class="tag">IEEE TCCN</span>
          <span class="tag">IEEE TVT</span>
          <span class="tag">IEEE TGCN</span>
          <span class="tag">IEEE JSTEAP</span>
          <span class="tag">IEEE OJ-COMS</span>
          <span class="tag">IEEE WCL</span>
          <span class="tag">IEEE CL</span>
          <span class="tag">IEEE ChinaCom</span>
        </div>
      </div>

      <div class="service-group">
        <p class="service-heading">Reviewer for Conferences</p>
        <div class="tags">
          <span class="tag">ICC 2026</span>
          <span class="tag">WCNC 2026</span>
          <span class="tag">ICC 2025</span>
          <span class="tag">GLOBECOM 2025</span>
          <span class="tag">ICCC 2025</span>
          <span class="tag">GLOBECOM 2024</span>
          <span class="tag">WCSP 2024</span>
          <span class="tag">PIMRC 2024</span>
          <span class="tag">WCNC 2024</span>
        </div>
      </div>
    </div>
  </div>

</div>
