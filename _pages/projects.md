---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<!-- Filter Buttons -->
<div style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button active" onclick="filterSelection('all', this)">All</button>
  <button class="filter-button" onclick="filterSelection('social', this)">Social</button>
  <button class="filter-button" onclick="filterSelection('memory', this)">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro', this)">Neuro</button>
</div>

<div class="project-list">
  <!-- Example card with image -->
  <a href="/projects/plan-1" class="project-card social neuro">
    <img src="/assets/img/projects/SRE2_method1.png" alt="Neural mechanisms" class="project-img">
    <div class="project-info">
      <h3 class="project-title">(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</h3>
      <p class="project-text">How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective...</p>
    </div>
  </a>

  <!-- Example card without image -->
  <a href="/projects/meaningfulness-vwm-boundaries" class="project-card memory no-image">
    <div class="project-info">
      <h3 class="project-title">Meaningfulness &amp; Visual Working Memory Across Spatial Boundaries</h3>
      <p class="project-text">Do meaningful objects facilitate encoding of spatially distal features in VWM? We probe cross-boundary integration with meaningful vs. meaningless items...</p>
    </div>
  </a>
</div>

<script>
function filterSelection(category, el) {
  const items = document.querySelectorAll('.project-card');
  items.forEach(item => {
    item.style.display = (category === 'all' || item.classList.contains(category)) ? 'flex' : 'none';
  });
  document.querySelectorAll('.filter-button').forEach(btn => btn.classList.remove('active'));
  if (el) el.classList.add('active');
}
filterSelection('all', document.querySelector('.filter-button'));
</script>

<style>
.filter-button{padding:.5rem 1rem;margin:0 .3rem;background:#f0f0f0;border:none;border-radius:6px;cursor:pointer;font-weight:500;transition:background .2s}
.filter-button:hover{background:#e0e0e0}.filter-button.active{background:#007acc;color:#fff}

.project-list{max-width:2000px;margin:0 auto;padding:0 6rem;display:flex;flex-direction:column;gap:1.2rem}

.project-card{display:flex;align-items:center;gap:1.5rem;text-decoration:none;color:inherit;background:#fff;border:1px solid #eee;border-radius:12px;padding:1.2rem;box-shadow:0 1px 3px rgba(0,0,0,.05);transition:box-shadow .25s,transform .15s}
.project-card:hover{box-shadow:0 4px 14px rgba(0,0,0,.08);transform:translateY(-1px)}

.project-img{width:420px;height:250px;object-fit:cover;border-radius:10px;flex-shrink:0}
.no-image{padding-left:1.5rem}

.project-info{flex:1}
.project-title{font-size:1.65rem;font-weight:800;margin:0 0 .4rem;line-height:1.25}
.project-text{font-size:1.08rem;color:#444;line-height:1.6;margin:0;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}

@media (max-width:900px){
  .project-list{padding:0 1rem}
  .project-card{flex-direction:column;align-items:flex-start}
  .project-img{width:100%;height:auto}
  .project-title{font-size:1.3rem}
}
</style>
