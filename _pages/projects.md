---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<!-- ====== Filters ====== -->
<div class="project-filters">
  <button class="filter-button active" onclick="filterSelection('all', this)">All</button>
  <button class="filter-button" onclick="filterSelection('social', this)">Social</button>
  <button class="filter-button" onclick="filterSelection('memory', this)">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro', this)">Neuro</button>
</div>

<!-- ====== Projects (full-bleed) ====== -->
<div class="projects">

  <!-- Plan 1 -->
  <section class="project-row social neuro">
    <div class="project-image">
      <img src="/assets/img/projects/SRE2_method1.png" alt="Plan 1 image">
    </div>
    <div class="project-text">
      <h2>Neural Mechanisms of Simulating Others' Mind</h2>
      <p>
        How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA identified regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then tested cross-condition generalization to see whether classifiers trained on self-related judgments decode president-related judgments.
      </p>
    </div>
  </section>

  <!-- Ensemble Emotion Perception -->
  <section class="project-row social">
    <div class="project-image">
      <img src="/assets/img/projects/CEP_method.png" alt="Ensemble Emotion Perception">
    </div>
    <div class="project-text">
      <h2>Contextual Effects on Ensemble Emotion Perception</h2>
      <p>
        Using naturalistic stimuli, we examine how situational context and observer emotion shape perceptions of a crowd’s ensemble emotion.
      </p>
    </div>
  </section>

  <!-- SPE -->
  <section class="project-row social memory">
    <div class="project-image">
      <img src="/assets/img/projects/SPE_method.png" alt="Self-Prioritization Effects">
    </div>
    <div class="project-text">
      <h2>Self-Prioritization Effects on Nonspatial Working Memory</h2>
      <p>
        We tested SPE on shape-based WM across two experiments:
        <a href="/data/analyzeSPE8VCS1.html" target="_blank" class="project-link">(Experiment 1)</a>,
        <a href="/data/analyzeSPE8VCS2.html" target="_blank" class="project-link">(Experiment 2)</a>.
        WM responses for colors were faster in the self condition than the other; no shape differences emerged.
      </p>
    </div>
  </section>

  <!-- Meaningfulness in VWM -->
  <section class="project-row memory">
    <div class="project-image">
      <img src="/assets/img/projects/Meaningfulness_method.png" alt="Meaningfulness Effects">
    </div>
    <div class="project-text">
      <h2>The Impact of Meaningfulness on Visual Working Memory Across Spatial Boundaries</h2>
      <p>
        We test whether meaningful objects facilitate encoding of spatially distal features in visual working memory.
      </p>
    </div>
  </section>

  <!-- fNIRS (no image) -->
  <section class="project-row neuro no-image">
    <div class="project-image" aria-hidden="true"></div>
    <div class="project-text">
      <h2>The Influence of Speaker Gender and Age on Product Preference</h2>
      <p>
        How do speaker gender and age shape product evaluations and purchase decisions? We test this using naturalistic video stimuli and fNIRS.
      </p>
    </div>
  </section>

</div>

<!-- ====== Filter logic ====== -->
<script>
function filterSelection(category, btn) {
  const rows = document.querySelectorAll('.project-row');
  rows.forEach(row => {
    const show = (category === 'all') || row.classList.contains(category);
    row.style.display = show ? '' : 'none';
  });
  document.querySelectorAll('.filter-button').forEach(b => b.classList.remove('active'));
  if (btn) btn.classList.add('active');
}
// 초기 상태: All
filterSelection('all', document.querySelector('.filter-button'));
</script>

<style>
/* ========= Filters (Underline Tabs) ========= */
.project-filters{
  text-align:center;
  margin: 0 0 1.25rem;
  border-bottom:1px solid #e5e7eb;
}
.filter-button{
  background:none;
  border:none;
  padding:.6rem 1rem;
  margin:0;
  font-size:1rem;
  font-weight:600;
  color:#6b7280;
  cursor:pointer;
  border-bottom:3px solid transparent; /* 밑줄 자리 확보 */
  transition:color .2s ease, border-bottom-color .2s ease;
}
.filter-button:hover{ color:#111827; }
.filter-button.active{
  color:#111827;
  border-bottom-color:#2563eb; /* 활성 탭 밑줄 */
}
/* 포커스 접근성 */
.filter-button:focus-visible{ outline:2px solid #2563eb; outline-offset:2px; }

/* ========= Full-bleed container (break out of theme) ========= */
.projects {
  width: 100vw;
  margin-left: calc(50% - 50vw);
  margin-right: calc(50% - 50vw);
  padding: 0 1rem;
}
.page .page__inner-wrap { padding-left: 0; padding-right: 0; }

/* ========= Two-column layout: image left / text right ========= */
.project-row {
  display: grid;
  grid-template-columns: minmax(0, 40%) minmax(0, 60%);
  align-items: stretch;
  gap: 5rem;
  padding: 2rem 3rem 2rem;

  border-radius: 8px;
  transition: box-shadow .18s ease, transform .18s ease;
}

/* 구분선 */
.project-row + .project-row { border-top: 2px solid #e9edf3; }

/* 이미지 */
.project-image {
  display: flex;
  align-items: center;
  justify-content: center;
  transition: box-shadow .18s ease, transform .18s ease;
}
.project-image img {
  width: 100%;
  height: auto;
  max-height: 100%;
  object-fit: contain;
  border-radius: 6px;
}

/* 이미지 없는 항목: Coming Soon 중앙 표시 */
.project-row.no-image .project-image{
  position:relative;
  min-height:320px;
  border:1px dashed #d7deea;
  background:#f8fafc;
  display:block;
}
.project-row.no-image .project-image::before{
  content:"Coming Soon";
  position:absolute; top:50%; left:50%;
  transform:translate(-50%,-50%);
  font-size:1.05rem; color:#9aa3af;
  font-weight:500; font-style:italic;
  white-space:nowrap; pointer-events:none; user-select:none;
}

/* 텍스트 */
.project-text{ display:flex; flex-direction:column; justify-content:center; }
.project-text h2{
  margin:0 0 .5rem;
  font-size:clamp(1rem, 0.6vw + 0.9rem, 1.4rem);
  line-height:1.3; letter-spacing:-0.01em; color:#111827;
}
.project-text h2:hover{ cursor:pointer; text-decoration:underline; }
.project-text p{
  margin:0;
  font-size:clamp(0.98rem, 0.35vw + 0.9rem, 1.08rem);
  line-height:1.85; color:#374151;
}
.project-link{ color:#0a6cff; text-decoration:none; }
.project-link:hover{ text-decoration:underline; }

/* ========= Responsive ========= */
@media (max-width: 960px) {
  .projects { margin-left: 0; margin-right: 0; width: 100%; padding: 0 .75rem; }
  .project-row { grid-template-columns: 1fr; gap: 1.25rem; }
  .project-image img,
  .project-row.no-image .project-image { min-height: 240px; }
}

/* Reduced motion */
@media (prefers-reduced-motion: reduce){
  .project-image, .project-row { transition: none; }
  .project-image:hover { transform:none; box-shadow:none; }
}
</style>
