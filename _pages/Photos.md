---
#title: "Photos"
permalink: /Photos.html
---

<style>

/* 图片布局：使用 Grid 控制最多 3 列 */
.photo-gallery {
  display: grid;
  grid-template-columns: repeat(3, 300px);
  gap: 20px;
  justify-content: start; /* 整体靠左对齐，如果想居中可以改成 center */
}

/* 响应式：屏幕较小时自动减少列数，适配手机和平板 */
@media (max-width: 980px) {
  .photo-gallery {
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  }
}

/* 增加各个 Section 之间的间距 */
hr {
  margin-top: 80px; /* 明显增加章节上方的间隔 */
  margin-bottom: 40px; /* 章节下方的间隔 */
  border: none;
  border-top: 1px solid #eaeaea; /* 稍微淡化分割线，更显高级 */
}

h2 {
  margin-bottom: 25px; /* 标题和图片之间也稍微留点呼吸感 */
}

/* 图片容器 */
.photo-item {
  position: relative;
}

/* 图片样式 */
.photo-item img {
  width: 100%; /* 配合 grid 布局，宽度设为100%填满300px的格子 */
  height: 200px;
  object-fit: cover;

  border-radius: 12px;
  transition: transform 0.35s ease, box-shadow 0.35s ease;
  cursor: pointer;

  position: relative;
  z-index: 1;
}

/* 悬停放大 + 阴影 */
.photo-item img:hover {
  transform: scale(1.8); /* 稍微调小了一点放大比例，避免3列时放大遮挡太多 */
  box-shadow: 0 20px 50px rgba(0,0,0,0.6);
  z-index: 10;
}

/* Lightbox 背景 */
#lightbox {
  display: none;
  position: fixed;
  z-index: 9999;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.9);
  justify-content: center;
  align-items: center;
}

/* 弹出图片 */
#lightbox img {
  max-width: 90%;
  max-height: 90%;
  border-radius: 10px;
  box-shadow: 0 20px 60px rgba(0,0,0,0.7);
  animation: zoomIn 0.3s ease;
}

/* 关闭按钮 */
#lightbox-close {
  position: absolute;
  top: 25px;
  right: 40px;
  font-size: 40px;
  color: white;
  cursor: pointer;
}

/* 动画 */
@keyframes zoomIn {
  from {transform: scale(0.8);}
  to {transform: scale(1);}
}

</style>

# Photos

Jump to:
- [PhD (2024–Present)](#phd)
- [Master's (2021–2024)](#masters)
- [Personal](#personal)

---

<span id="phd"></span>
## PhD (2024–Present)

<div class="photo-gallery">

<div class="photo-item">
  <img src="/images/2602dinner.jpg" alt="PhD Photo 1">
</div>

<div class="photo-item">
  <img src="/images/2511dongxichong.jpg" alt="PhD Photo 2">
</div>

<div class="photo-item">
  <img src="/images/2507Dinner.jpg" alt="PhD Photo 3">
</div>

<div class="photo-item">
  <img src="/images/2507TanglangMou.jpg" alt="PhD Photo 4">
</div>

<div class="photo-item">
  <img src="/images/2503YangtaiMoun2.jpg" alt="PhD Photo 5">
</div>

<div class="photo-item">
  <img src="/images/DongxiCong1.jpg" alt="PhD Photo 6">
</div>

<div class="photo-item">
  <img src="/images/2407TanglangMou.jpg" alt="PhD Photo 7">
</div>

<div class="photo-item">
  <img src="/images/MIMO.jpg" alt="PhD Photo 8">
</div>

</div>

---

<span id="masters"></span>
## Master's (2021–2024)

<div class="photo-gallery">

<div class="photo-item">
  <img src="/images/2405Gra.jpg" alt="Master's Photo 1">
</div>

<div class="photo-item">
  <img src="/images/2405Gra2.jpg" alt="Master's Photo 2">
</div>

</div>

---

<span id="personal"></span>
## Personal

<div class="photo-gallery">

<div class="photo-item">
  <img src="/images/Yantai.jpg" alt="Personal Photo 1">
</div>

<div class="photo-item">
  <img src="/images/2401eimen.jpg" alt="Personal Photo 2">
</div>

</div>

---

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
  img.onclick = function(){
    lightbox.style.display = "flex";
    lightboxImg.src = this.src;
    lightboxImg.alt = this.alt;
  }
});

closeBtn.onclick = function(){
  lightbox.style.display = "none";
}

lightbox.onclick = function(e){
  if(e.target === lightbox){
    lightbox.style.display = "none";
  }
}

</script>
