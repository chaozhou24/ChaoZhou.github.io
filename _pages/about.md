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
/* ===== Overall page style ===== */
.page__content {
  font-size: 17px;
  line-height: 1.8;
}

:root{
  --main-color: #7F6000;
  --accent-color: #b88a00;
  --soft-bg: #faf8f3;
  --card-bg: #ffffff;
  --text-main: #222;
  --text-light: #666;
  --border-light: #ece6d8;
  --shadow: 0 8px 24px rgba(0,0,0,0.08);
  --radius: 18px;
}

/* ===== Hero card ===== */
.hero-card{
  display:flex;
  flex-wrap:wrap;
  align-items:center;
  gap:28px;
  background: linear-gradient(135deg, #fffdf8 0%, #faf6ea 100%);
  border: 1px solid var(--border-light);
  border-radius: 24px;
  padding: 28px 30px;
  margin: 12px 0 28px 0;
  box-shadow: var(--shadow);
}

.hero-avatar img{
  width: 160px;
  height: 160px;
  object-fit: cover;
  border-radius: 50%;
  border: 4px solid #fff;
  box-shadow: 0 8px 22px rgba(0,0,0,0.12);
}

.hero-text{
  flex:1;
  min-width: 260px;
}

.hero-text h1{
  margin: 0 0 10px 0;
  font-size: 2rem;
  color: var(--text-main);
}

.hero-text p{
  margin: 8px 0;
  color: var(--text-main);
}

.hero-links{
  margin-top: 14px;
  display:flex;
  flex-wrap:wrap;
  gap:12px;
}

.hero-btn{
  display:inline-block;
  padding:8px 16px;
  border-radius:999px;
  text-decoration:none !important;
  font-weight:600;
  border:1px solid var(--border-light);
  background:#fff;
  color: var(--main-color) !important;
  transition: all 0.25s ease;
}

.hero-btn:hover{
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0,0,0,0.08);
  background: #fffaf0;
}

/* ===== Section title ===== */
.section-title{
  font-size: 1.55rem;
  font-weight: 800;
  margin-top: 34px;
  margin-bottom: 18px;
  color: var(--text-main);
  border-left: 5px solid var(--main-color);
  padding-left: 12px;
}

/* ===== Research cards ===== */
.research-grid{
  display:grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap:20px;
  margin-top: 10px;
}

.research-card{
  background: var(--card-bg);
  border:1px solid var(--border-light);
  border-radius: var(--radius);
  padding: 22px 20px;
  box-shadow: var(--shadow);
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.research-card:hover{
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0,0,0,0.10);
}

.research-card h3{
  margin-top:0;
  margin-bottom:12px;
  color: var(--main-color);
  font-size:1.15rem;
}

.research-card ul{
  margin:0;
  padding-left:20px;
}

.research-card li{
  margin:8px 0;
}

/* ===== News timeline ===== */
.news-timeline{
  position:relative;
  margin-top: 8px;
  padding-left: 24px;
  border-left: 3px solid #e7dcc2;
}

.news-item{
  position:relative;
  margin-bottom: 20px;
  padding: 2px 0 2px 10px;
}

.news-item::before{
  content:"";
  position:absolute;
  left:-32px;
  top:10px;
  width:14px;
  height:14px;
  border-radius:50%;
  background: var(--main-color);
  box-shadow: 0 0 0 4px #f6efe0;
}

.news-date{
  font-weight:700;
  color: var(--main-color);
  margin-right: 8px;
}

.news-text{
  color: var(--text-main);
}

/* ===== Service tags ===== */
.service-block{
  background:#fff;
  border:1px solid var(--border-light);
  border-radius: var(--radius);
  padding: 22px 20px;
  box-shadow: var(--shadow);
  margin-top: 10px;
}

.tag-group{
  margin-bottom: 18px;
}

.tag-group strong{
  display:block;
  margin-bottom: 10px;
  color: var(--text-main);
}

.tags{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
}

.tag{
  display:inline-block;
  padding:7px 14px;
  border-radius:999px;
  background:#fff8e8;
  border:1px solid #ecdcae;
  color:#7a5a00;
  font-size:0.95rem;
  font-weight:600;
}

/* ===== Link style ===== */
a{
  text-decoration: none;
}

a:hover{
  text-decoration: underline;
}

/* ===== Responsive ===== */
@media (max-width: 768px){
  .hero-card{
    padding: 22px 18px;
  }
  .hero-text h1{
    font-size: 1.7rem;
  }
}
</style>

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<div class="hero-card">
  <div class="hero-avatar">
    <img src="/images/bio-photo.jpg" alt="Chao Zhou">
  </div>

  <div class="hero-text">
    <h1>Hello 👋, I am Chao Zhou (周超)</h1>
    <p>
      I am a second-year Ph.D. student at <strong>Southern University of Science and Technology (SUSTech)</strong>, 
      advised by Prof. 
      <a href="https://www.sustech.edu.cn/en/faculties/changshengyou.html" target="_blank">
        Changsheng You
      </a>.
      I received the M.S. degree from Nanjing University of Posts and Telecommunications.
    </p>

    <p>
      My main research interests include <strong>Near-Field Communications</strong>, 
      <strong>Intelligent Antenna and Surface</strong>, and 
      <strong>Symbiotic Radio</strong>. I have published several papers in top international communication journals and conferences.
    </p>

    <p>
      If you are interested in collaboration, please feel free to contact me via email:
      <a href="mailto:zhouchao2024@mail.sustech.edu.cn">zhouchao2024@mail.sustech.edu.cn</a>
    </p>

    <div class="hero-links">
      <a class="hero-btn" href="mailto:zhouchao2024@mail.sustech.edu.cn">Email</a>
      <a class="hero-btn" href="#news">News</a>
      <a class="hero-btn" href="/publications/">Publications</a>
    </div>
  </div>
</div>

<div class="section-title">📖 Research Interests</div>

<div class="research-grid">
  <div class="research-card">
    <h3>Near-Field Communications (NFC)</h3>
    <ul>
      <li>Flexible Beamforming Design</li>
      <li>Mixed-field Communications</li>
    </ul>
  </div>

  <div class="research-card">
    <h3>Intelligent Antenna and Surface</h3>
    <ul>
      <li>Intelligent Reflecting Surface</li>
      <li>Intelligent Antenna (e.g., movable antennas and rotatable antennas)</li>
    </ul>
  </div>

  <div class="research-card">
    <h3>Backscatter Communications (Backcom)</h3>
    <ul>
      <li>Symbiotic Radio (SR)</li>
    </ul>
  </div>
</div>

<span class='anchor' id='news'></span>
<div class="section-title">🔥 News</div>

<div class="news-timeline">
  <div class="news-item">
    <span class="news-date">2026.01</span>
    <span class="news-text">🎉🎉 Three papers have been accepted by IEEE International Conference on Communications (ICC) 2026.</span>
  </div>

  <div class="news-item">
    <span class="news-date">2024.11</span>
    <span class="news-text">
      🎉🎉 I received the IEEE WCSP Best Paper Award for the paper 
      "<a href="https://scholar.google.com/scholar?hl=zh-CN&as_sdt=0%2C5&q=Channel+Estimation+for+XL-IRS+Assisted+Wireless+Systems+with+Double-sided+Visibility+Regions&btnG=" target="_blank">
      Channel Estimation for XL-IRS Assisted Wireless Systems with Double-sided Visibility Regions
      </a>".
    </span>
  </div>
</div>

<div class="section-title">📄 Academic Services</div>

<div class="service-block">
  <div class="tag-group">
    <strong>Reviewer for Journals</strong>
    <div class="tags">
      <span class="tag">IEEE JSAC</span>
      <span class="tag">IEEE TWC</span>
      <span class="tag">IEEE TMC</span>
      <span class="tag">IEEE TCOM</span>
      <span class="tag">IEEE TCCN</span>
      <span class="tag">IEEE TVT</span>
      <span class="tag">IEEE TGCN</span>
      <span class="tag">IEEE OJ-COMS</span>
      <span class="tag">IEEE WCL</span>
      <span class="tag">IEEE CL</span>
    </div>
  </div>

  <div class="tag-group">
    <strong>Reviewer for Conferences</strong>
    <div class="tags">
      <span class="tag">ICC 2025</span>
      <span class="tag">ICC 2026</span>
      <span class="tag">GLOBECOM 2025</span>
    </div>
  </div>
</div>
