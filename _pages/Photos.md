---
#title: "Photos"
permalink: /Photos.html
---

<style>
:root{
  --main-color:#7F6000;
  --main-dark:#5f4700;
  --soft-bg:#faf8f3;
  --card-bg:#ffffff;
  --hero-bg-start:#fffdf8;
  --hero-bg-end:#f7f1e6;
  --border-light:#ece6d8;
  --border-mid:#e4d7b7;
  --text-main:#222222;
  --text-soft:#666666;
  --shadow-soft:0 8px 24px rgba(0,0,0,0.06);
  --shadow-hover:0 18px 38px rgba(0,0,0,0.16);
  --radius-lg:22px;
  --radius-md:18px;
}

/* ===== overall ===== */
.page__content{
  font-size:17px;
  line-height:1.8;
  color:var(--text-main);
}

.page__content a{
  color:#1f5fae;
  text-decoration:none;
}

.page__content a:hover{
  text-decoration:underline;
}

/* ===== page hero ===== */
.photo-hero{
  position:relative;
  overflow:hidden;
  background:linear-gradient(135deg,var(--hero-bg-start) 0%,var(--hero-bg-end) 100%);
  border:1px solid var(--border-light);
  border-radius:24px;
  padding:28px 32px;
  margin-bottom:24px;
  box-shadow:var(--shadow-soft);
}

.photo-hero::after{
  content:"";
  position:absolute;
  right:-70px;
  top:-70px;
  width:210px;
  height:210px;
  border-radius:50%;
  background:radial-gradient(circle, rgba(184,138,0,0.10) 0%, rgba(184,138,0,0.03) 55%, rgba(184,138,0,0) 72%);
  pointer-events:none;
}

.photo-hero h1{
  margin:0 0 10px 0;
  font-size:2rem;
  font-weight:800;
  color:var(--text-main);
}

.photo-hero p{
  margin:0;
  color:var(--text-soft);
}

/* ===== jump nav ===== */
.photo-nav{
  display:flex;
  flex-wrap:wrap;
  gap:12px;
  margin:0 0 30px 0;
}

.photo-nav a{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:8px 16px;
  border-radius:999px;
  background:#fff;
  border:1px solid var(--border-mid);
  color:var(--main-color) !important;
  font-weight:700;
  text-decoration:none !important;
  box-shadow:0 3px 10px rgba(0,0,0,0.03);
  transition:all 0.22s ease;
}

.photo-nav a:hover{
  background:#fff7dd;
  border-color:#d8c38d;
  transform:translateY(-2px);
  box-shadow:0 10px 20px rgba(0,0,0,0.08);
}

/* ===== section card ===== */
.photo-section{
  background:var(--card-bg);
  border:1px solid var(--border-light);
  border-radius:22px;
  padding:22px 22px 18px 22px;
  margin-bottom:28px;
  box-shadow:var(--shadow-soft);
}

.photo-section h2{
  margin:0 0 18px 0;
  font-size:1.38rem;
  font-weight:800;
  color:var(--text-main);
  padding-bottom:10px;
  border-bottom:1px solid #efe8d9;
}

/* ===== photo grid ===== */
/* 固定每张卡片宽度一致，图片高度一致 */
.photo-gallery{
  display:grid;
  grid-template-columns:repeat(auto-fill, minmax(300px, 300px));
  gap:22px;
  justify-content:start;
}

/* 响应式 */
@media (max-width: 980px){
  .photo-gallery{
    grid-template-columns:repeat(auto-fit, minmax(280px, 1fr));
  }
}

/* ===== photo item ===== */
.photo-item{
  position:relative;
  display:flex;
  flex-direction:column;
  background:#fffdfa;
  border:1px solid #f0e8d7;
  border-radius:18px;
  padding:12px 12px 14px 12px;
  box-shadow:0 6px 16px rgba(0,0,0,0.04);
  transition:transform 0.22s ease, box-shadow 0.22s ease, border-color 0.22s ease;
  overflow:visible;
}

.photo-item:hover{
  transform:translateY(-3px);
  box-shadow:0 12px 28px rgba(0,0,0,0.08);
  border-color:#e6d5ab;
  z-index:5;
}

/* ===== image wrapper ===== */
/* 固定显示框，确保所有照片视觉尺寸一致 */
.photo-thumb{
  position:relative;
  width:100%;
  height:200px;
  border-radius:14px;
  overflow:visible; /* 允许 hover 放大溢出 */
  display:flex;
  align-items:center;
  justify-content:center;
}

/* ===== image ===== */
.photo-item img{
  width:100%;
  height:200px;
  object-fit:cover;
  border-radius:14px;
  cursor:pointer;
  transition:transform 0.35s ease, box-shadow 0.35s ease;
  position:relative;
  z-index:1;
  display:block;
  background:#f5f5f5;
}

/* 悬停放大 + 高级阴影 */
.photo-item img:hover{
  transform:scale(1.7);
  box-shadow:0 24px 60px rgba(0,0,0,0.40);
  z-index:20;
}

/* ===== caption ===== */
.photo-caption{
  margin-top:12px;
  text-align:center;
  font-size:14px;
  color:var(--text-soft);
  line-height:1.45;
  min-height:40px;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:0 4px;
}

/* ===== lightbox ===== */
#lightbox{
  display:none;
  position:fixed;
  z-index:9999;
  left:0;
  top:0;
  width:100%;
  height:100%;
  background:rgba(0,0,0,0.92);
  justify-content:center;
  align-items:center;
  padding:20px;
  box-sizing:border-box;
}

#lightbox img{
  max-width:92%;
  max-height:88%;
  border-radius:14px;
  box-shadow:0 24px 70px rgba(0,0,0,0.55);
  animation:zoomIn 0.28s ease;
}

#lightbox-close{
  position:absolute;
  top:22px;
  right:34px;
  font-size:42px;
  line-height:1;
  color:white;
  cursor:pointer;
  user-select:none;
}

@keyframes zoomIn{
  from{transform:scale(0.82); opacity:0.6;}
  to{transform:scale(1); opacity:1;}
}

/* mobile */
@media (max-width: 768px){
  .photo-hero{
    padding:22px 18px;
  }

  .photo-hero h1{
    font-size:1.65rem;
  }

  .photo-section{
    padding:18px 16px 14px 16px;
  }

  .photo-item img,
  .photo-thumb{
    height:190px;
  }

  .photo-item img:hover{
    transform:scale(1.35);
  }

  #lightbox-close{
    right:20px;
    top:18px;
    font-size:38px;
  }
}
</style>

<div class="photo-hero">
  <h1>📷 Photos</h1>
  <p>Moments from academic activities, campus life, and personal travels.</p>
</div>

<div class="photo-nav">
  <a href="#phd">PhD (2024–Present)</a>
  <a href="#masters">Master's (2021–2024)</a>
  <a href="#personal">Personal</a>
</div>

<span id="phd"></span>
<div class="photo-section">
  <h2>PhD (2024–Present)</h2>

  <div class="photo-gallery">

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2602dinner.jpg" alt="PhD Photo 1">
      </div>
      <div class="photo-caption">[2026-02] Laboratory Dinner</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2511dongxichong.jpg" alt="PhD Photo 2">
      </div>
      <div class="photo-caption">[2025-11] Dongxiyong Hiking</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2507Dinner.jpg" alt="PhD Photo 3">
      </div>
      <div class="photo-caption">[2025-07] Laboratory Dinner</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2507TanglangMou.jpg" alt="PhD Photo 4">
      </div>
      <div class="photo-caption">[2025-07] Tanglang Mountain Hiking</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2503YangtaiMoun2.jpg" alt="PhD Photo 5">
      </div>
      <div class="photo-caption">[2025-03] Yangtai Mountain Hiking</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/DongxiCong1.jpg" alt="PhD Photo 6">
      </div>
      <div class="photo-caption">[2024-08] Dongxiyong Hiking</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2407TanglangMou.jpg" alt="PhD Photo 7">
      </div>
      <div class="photo-caption">[2024-07] Tanglang Mountain Hiking</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/MIMO.jpg" alt="PhD Photo 8">
      </div>
      <div class="photo-caption">[2024-07] MIMO Course at Tsinghua Uni.</div>
    </div>

  </div>
</div>

<span id="masters"></span>
<div class="photo-section">
  <h2>Master's (2021–2024)</h2>

  <div class="photo-gallery">

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2405Gra.jpg" alt="Master's Photo 1">
      </div>
      <div class="photo-caption">[2024-05] Graduation Photo</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2405Gra2.jpg" alt="Master's Photo 2">
      </div>
      <div class="photo-caption">[2024-05] Graduation Photo</div>
    </div>

  </div>
</div>

<span id="personal"></span>
<div class="photo-section">
  <h2>Personal</h2>

  <div class="photo-gallery">

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/Yantai.jpg" alt="Personal Photo 1">
      </div>
      <div class="photo-caption">[2026-02] Yantai Travel</div>
    </div>

    <div class="photo-item">
      <div class="photo-thumb">
        <img src="/images/2401eimen.jpg" alt="Personal Photo 2">
      </div>
      <div class="photo-caption">[2024-01] Xiamen Travel</div>
    </div>

  </div>
</div>

<div id="lightbox">
  <span id="lightbox-close">&times;</span>
  <img id="lightbox-img" alt="Enlarged photo">
</div>

<script>
const images = document.querySelectorAll(".photo-item img");
const lightbox = document.getElementById("lightbox");
const lightboxImg = document.getElementById("lightbox-img");
const closeBtn = document.getElementById("lightbox-close");

images.forEach(img => {
  img.addEventListener("click", function () {
    lightbox.style.display = "flex";
    lightboxImg.src = this.src;
    lightboxImg.alt = this.alt;
    document.body.style.overflow = "hidden";
  });
});

closeBtn.addEventListener("click", function () {
  lightbox.style.display = "none";
  document.body.style.overflow = "";
});

lightbox.addEventListener("click", function (e) {
  if (e.target === lightbox) {
    lightbox.style.display = "none";
    document.body.style.overflow = "";
  }
});

document.addEventListener("keydown", function(e){
  if(e.key === "Escape"){
    lightbox.style.display = "none";
    document.body.style.overflow = "";
  }
});
</script>
