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
  <a href="/projects/plan-1" class="project-card social neuro">
    <div class="project-media">
      <img src="/assets/img/projects/SRE2_method1.png" alt="Neural mechanisms" class="project-img">
    </div>
    <div class="project-info">
      <h3 class="project-title">(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</h3>
      <p class="project-text">How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA was used to identify brain regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then evaluated cross-condition generalization, testing whether classifiers trained on self-related judgments could decode president-related judgments.</p>
    </div>
  </a>
  
  <!-- Repeat same structure for other projects -->
  <!-- ... -->
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
.filter-button { padding: .5rem 1rem; margin: 0 .3rem; background: #f0f0f0; border: none; border-radius: 6px; cursor: pointer; font-weight: 500; transition: background .2s; }
.filter-button:hover { background: #e0e0e0; }
.filter-button.active { background: #007acc; color: #fff; }

.project-list { max-width: 100%; margin: 0 auto; padding: 0 12rem; display: flex; flex-direction: column; gap: 3rem; }

.project-card { display: flex; align-items: center; gap: 4rem; text-decoration: none; color: inherit; background: #fff; border: 1px solid #eee; border-radius: 12px; padding: 2rem; box-shadow: 0 1px 3px rgba(0,0,0,.05); transition: box-shadow .25s, transform .15s; }
.project-card:hover { box-shadow: 0 4px 14px rgba(0,0,0,.08); transform: translateY(-1px); }

.project-media { flex: 0 0 50%; display: flex; justify-content: center; align-items: center; }
.project-img { width: 100%; max-width: 800px; height: auto; object-fit: cover; border-radius: 12px; }

.project-info { flex: 1; }
.project-title { font-size: 2.2rem; font-weight: 800; margin: 0 0 1rem; line-height: 1.25; }
.project-text { font-size: 1.2rem; color: #444; line-height: 1.8; margin: 0; }

@media (max-width: 900px) {
  .project-list { padding: 0 1rem; }
  .project-card { flex-direction: column; align-items: flex-start; }
  .project-media, .project-info { flex: 1 1 100%; }
  .project-img { width: 100%; max-width: none; }
  .project-title { font-size: 1.5rem; }
}
</style>
