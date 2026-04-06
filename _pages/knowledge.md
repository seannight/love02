---
layout: single
title: "知识库"
permalink: /knowledge/
author_profile: true
---

<style>
.knowledge-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  margin-top: 20px;
}

.category-bookmark {
  border-radius: 12px;
  padding: 20px;
  width: calc(50% - 10px);
  min-width: 260px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  cursor: pointer;
  transition: all 0.3s ease;
}

.category-bookmark:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

/* 统一色块 #F5E5E1 */
.category-bookmark.green {
  background: linear-gradient(135deg, #F5E5E1 0%, #E8D4CE 100%);
}

.category-bookmark.pink {
  background: linear-gradient(135deg, #F5E5E1 0%, #E8D4CE 100%);
}

.bookmark-icon {
  font-size: 2em;
  margin-bottom: 10px;
}

.bookmark-title {
  color: #333;
  font-size: 1.3em;
  font-weight: bold;
  margin-bottom: 8px;
}

.bookmark-count {
  color: #666;
  font-size: 0.9em;
}

.map-gallery {
  display: none;
  margin-top: 40px;
  padding: 30px;
  background: #fafafa;
  border-radius: 16px;
  border: 1px solid #eee;
}

.map-gallery.active {
  display: block;
}

.map-gallery-title {
  font-size: 1.4em;
  margin-bottom: 25px;
  padding-bottom: 15px;
  border-bottom: 2px solid #F5E5E1;
  color: #333;
}

.map-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 25px;
}

.map-item {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 15px rgba(0,0,0,0.06);
  transition: all 0.3s ease;
  border: 1px solid #eee;
}

.map-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}

.map-item img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  cursor: zoom-in;
  background: #f5f5f5;
}

.map-item-title {
  padding: 15px;
  font-weight: 500;
  text-align: center;
  color: #444;
  font-size: 0.95em;
}

.modal {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.92);
}

.modal-content {
  margin: auto;
  display: block;
  max-width: 95%;
  max-height: 95%;
  margin-top: 2%;
  border-radius: 8px;
}

.close {
  position: absolute;
  top: 15px;
  right: 30px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover { color: #F5E5E1; }

@media (max-width: 600px) {
  .category-bookmark { width: 100%; }
  .map-grid { grid-template-columns: 1fr; }
}
</style>

<div class="knowledge-container">
  <div class="category-bookmark green" onclick="showCategory('tencent-pm')">
    <div class="bookmark-icon">🎯</div>
    <div class="bookmark-title">腾讯产品经理创造营</div>
    <div class="bookmark-count">点击查看知识导图</div>
  </div>

  <div class="category-bookmark green" onclick="showCategory('vibe-coding')">
    <div class="bookmark-icon">💻</div>
    <div class="bookmark-title">Vibe Coding 初中级开发</div>
    <div class="bookmark-count">点击查看知识导图</div>
  </div>

  <div class="category-bookmark pink" onclick="showCategory('aigc')">
    <div class="bookmark-icon">🤖</div>
    <div class="bookmark-title">AIGC</div>
    <div class="bookmark-count">点击查看知识导图</div>
  </div>

  <div class="category-bookmark pink" onclick="showCategory('reading-notes')">
    <div class="bookmark-icon">📚</div>
    <div class="bookmark-title">读书笔记</div>
    <div class="bookmark-count">点击查看知识导图</div>
  </div>
</div>

<!-- 腾讯产品经理创造营 -->
<div id="tencent-pm" class="map-gallery">
  <h2 class="map-gallery-title">🎯 腾讯产品经理创造营</h2>
  <div class="map-grid">
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/01--产品启蒙.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品启蒙</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/02--课程框架.png" onclick="openModal(this.src)">
      <div class="map-item-title">课程框架</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/03 什么是产品？什么是产品经理？.png" onclick="openModal(this.src)">
      <div class="map-item-title">什么是产品？什么是产品经理？</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/04.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品思维</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/05 校对需求（找）.png" onclick="openModal(this.src)">
      <div class="map-item-title">校对需求（找）</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/06 预判需求和洞察趋势（找）.png" onclick="openModal(this.src)">
      <div class="map-item-title">预判需求和洞察趋势</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/07_找（闭坑指南）.png" onclick="openModal(this.src)">
      <div class="map-item-title">找（闭坑指南）</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/08 比 （向外看）分析市场竞争格局.png" onclick="openModal(this.src)">
      <div class="map-item-title">分析市场竞争格局</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/10. 确定产品的商业化模式（比）.png" onclick="openModal(this.src)">
      <div class="map-item-title">确定产品的商业化模式</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/11比（闭坑）.png" onclick="openModal(this.src)">
      <div class="map-item-title">比（闭坑）</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/12_做好需求规划.png" onclick="openModal(this.src)">
      <div class="map-item-title">做好需求规划</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/13把握需求管理节奏.png" onclick="openModal(this.src)">
      <div class="map-item-title">把握需求管理节奏</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/14_产品设计之美（试）.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品设计之美（试）</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/15_产品设计避免的弯路（试）.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品设计避免的弯路</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/16（试_设计篇）需求落地最后一公里.png" onclick="openModal(this.src)">
      <div class="map-item-title">需求落地最后一公里</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/18_(试 运营篇）运营拉动产品增长.png" onclick="openModal(this.src)">
      <div class="map-item-title">运营拉动产品增长</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/19（试运营篇）天下武功，唯快不破.png" onclick="openModal(this.src)">
      <div class="map-item-title">天下武功，唯快不破</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/20_（试_运营篇）产品风险管理.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品风险管理</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/20_精神篇_哪些品质助产品经理走得更远.png" onclick="openModal(this.src)">
      <div class="map-item-title">哪些品质助产品经理走得更远</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/21_腾讯Royal产品经理采访.png" onclick="openModal(this.src)">
      <div class="map-item-title">腾讯Royal产品经理采访</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/22_引爆内容型产品，搞定这5个问题就够了.png" onclick="openModal(this.src)">
      <div class="map-item-title">引爆内容型产品</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/23_优秀产品经理频出爆款的原因.png" onclick="openModal(this.src)">
      <div class="map-item-title">优秀产品经理频出爆款的原因</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/24_总结课--产品设计的方法与实践.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品设计的方法与实践</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/25_总结课--产品经理高效执行的攻略.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品经理高效执行的攻略</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/26_总结课--产品思维分享和应用.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品思维分享和应用</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/腾讯产品/进阶.png" onclick="openModal(this.src)">
      <div class="map-item-title">进阶</div>
    </div>
  </div>
</div>

<!-- Vibe Coding -->
<div id="vibe-coding" class="map-gallery">
  <h2 class="map-gallery-title">💻 Vibe Coding 初中级开发</h2>
  <div class="map-grid">
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/前端1.png" onclick="openModal(this.src)">
      <div class="map-item-title">前端1</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/前端2.png" onclick="openModal(this.src)">
      <div class="map-item-title">前端2</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/前端3.png" onclick="openModal(this.src)">
      <div class="map-item-title">前端3</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/前端4.png" onclick="openModal(this.src)">
      <div class="map-item-title">前端4</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/前端5.png" onclick="openModal(this.src)">
      <div class="map-item-title">前端5</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/后端1.png" onclick="openModal(this.src)">
      <div class="map-item-title">后端1</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/后端2.png" onclick="openModal(this.src)">
      <div class="map-item-title">后端2</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/后端3.png" onclick="openModal(this.src)">
      <div class="map-item-title">后端3</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/后端4.png" onclick="openModal(this.src)">
      <div class="map-item-title">后端4</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/后端5.png" onclick="openModal(this.src)">
      <div class="map-item-title">后端5</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/产品补充.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品补充</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/产品补充2.png" onclick="openModal(this.src)">
      <div class="map-item-title">产品补充2</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/vibe coding/开发APP.png" onclick="openModal(this.src)">
      <div class="map-item-title">开发APP</div>
    </div>
  </div>
</div>

<!-- AIGC -->
<div id="aigc" class="map-gallery">
  <h2 class="map-gallery-title">🤖 AIGC</h2>
  <div class="map-grid">
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/AI文字生成.png" onclick="openModal(this.src)">
      <div class="map-item-title">AI文字生成</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/MJ基础.png" onclick="openModal(this.src)">
      <div class="map-item-title">MJ基础</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/文生图基础.png" onclick="openModal(this.src)">
      <div class="map-item-title">文生图基础</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/垫图1.png" onclick="openModal(this.src)">
      <div class="map-item-title">垫图1</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/垫图2.png" onclick="openModal(this.src)">
      <div class="map-item-title">垫图2</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/垫图3.png" onclick="openModal(this.src)">
      <div class="map-item-title">垫图3</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/风格统一.png" onclick="openModal(this.src)">
      <div class="map-item-title">风格统一</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/主体一致.png" onclick="openModal(this.src)">
      <div class="map-item-title">主体一致</div>
    </div>
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/knowledge/AIGC/图片编辑.png" onclick="openModal(this.src)">
      <div class="map-item-title">图片编辑</div>
    </div>
  </div>
</div>

<!-- 读书笔记 -->
<div id="reading-notes" class="map-gallery">
  <h2 class="map-gallery-title">📚 读书笔记</h2>
  <div class="map-grid">
    <div class="map-item">
      <img src="{{ site.baseurl }}/assets/images/bio-photo.jpg" onclick="openModal(this.src)">
      <div class="map-item-title">待添加</div>
    </div>
  </div>
</div>

<div id="imageModal" class="modal" onclick="closeModal()">
  <span class="close">&times;</span>
  <img class="modal-content" id="modalImage">
</div>

<script>
function showCategory(categoryId) {
  document.querySelectorAll('.map-gallery').forEach(gallery => {
    gallery.classList.remove('active');
  });
  document.getElementById(categoryId).classList.add('active');
  document.getElementById(categoryId).scrollIntoView({ behavior: 'smooth', block: 'start' });
}

function openModal(imgSrc) {
  var modal = document.getElementById('imageModal');
  var modalImg = document.getElementById('modalImage');
  modal.style.display = 'block';
  modalImg.src = imgSrc;
}

function closeModal() {
  document.getElementById('imageModal').style.display = 'none';
}

document.addEventListener('keydown', function(event) {
  if (event.key === 'Escape') {
    closeModal();
  }
});
</script>
