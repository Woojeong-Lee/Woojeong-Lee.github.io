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
      <h2>Neural Mechanisms of Simulating Others’ Mind</h2>
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
      <h2>The Influence of Situational Context and Observer Emotion on Ensemble Emotion Perception</h2>
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

  <!-- Meaningfulness in VWM (no image) -->
  <section class="project-row memory no-image">
    <div class="project-image" aria-hidden="true"></div>
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
/* ========= Filters ========= */
.project-filters {
  text-align: center;
  margin: 0 0 1.25rem;
}
.filter-button {
  padding: .5rem 1rem;
  margin: 0 .3rem;
  background: #f0f0f0;
  border: 0;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 500;
  transition: background .2s;
}
.filter-button:hover { background: #e6e6e6; }
.filter-button.active { background: #007acc; color: #fff; }

/* ========= Full-bleed container (break out of theme) ========= */
.projects {
  width: 100vw;
  margin-left: calc(50% - 50vw);
  margin-right: calc(50% - 50vw);
  padding: 0 1rem;
}
.page .page__inner-wrap { padding-left: 0; padding-right: 0; }

/* ========= Two-column layout: all items image-left / text-right ========= */
.project-row {
  display: grid;
  grid-template-columns: minmax(0, 40%) minmax(0, 60%);
  align-items: stretch;
  gap: 2rem;
  padding: 1rem 0 2rem;
}

/* 구분선으로 프로젝트 간 분리 */
.project-row + .project-row {
  border-top: 1px solid #e9edf3;
}

/* 이미지 영역 */
.project-image {
  display: flex;
  align-items: center;
  justify-content: center;
}
.project-image img {
  width: 100%;
  height: auto; /* 원본 비율 유지 */
  max-height: 100%; /* 너무 커지지 않게 */
  object-fit: contain; /* 잘리지 않고 축소/확대 */
  border-radius: 6px;
}

/* 이미지가 없는 항목: 플레이스홀더 패널 유지(정렬 통일) */
.project-row.no-image .project-image {
  min-height: 320px;
  background: linear-gradient(180deg, #f6f8fb 0%, #eef2f8 100%);
  border: 1px dashed #d7deea;
}

/* 텍스트 */
.project-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.project-text h2 {
  margin: 0 0 .5rem;
  font-size: clamp(1rem, 0.6vw + 0.9rem, 1.4rem);
  line-height: 1.25;
  letter-spacing: -0.01em;
  color: #111827;
}
.project-text p {
  margin: 0;
  font-size: clamp(0.98rem, 0.35vw + 0.9rem, 1.08rem);
  line-height: 1.85;
  color: #374151;
}
.project-link { color: #0a6cff; text-decoration: none; }
.project-link:hover { text-decoration: underline; }

/* ========= Responsive ========= */
@media (max-width: 960px) {
  .projects { margin-left: 0; margin-right: 0; width: 100%; padding: 0 .75rem; }
  .project-row { grid-template-columns: 1fr; gap: 1.25rem; }
  .project-image img,
  .project-row.no-image .project-image { min-height: 240px; }
}
</style>
