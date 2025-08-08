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
/* 1) 레이아웃 정리: 위쪽 정렬 + 칼럼 비율 고정 */
.project-row{
  display:grid;
  grid-template-columns:minmax(0,39%) minmax(0,61%);
  align-items:start;            /* ⬅ 가운데가 아니라 위쪽 정렬 */
  gap:1.75rem;
  padding:1.25rem 0 2rem;
}
.project-row + .project-row{ border-top:1px solid #e9edf3; }

/* 2) 이미지: 비율 유지(contain) + 최대 높이 통일 */
.project-image{ display:flex; align-items:flex-start; justify-content:center; }
.project-image img{
  width:100%;
  height:auto;                  /* 원본 비율 유지 */
  object-fit:contain;           /* 잘림 없음 */
  max-height:420px;             /* ⬅ 데스크톱 기준 통일 높이(원하면 360~480 조절) */
  border-radius:6px;
}

/* 3) 타이포: 제목 살짝 더 작고 가볍게, 본문 줄길이 제한 */
.project-text{ display:flex; flex-direction:column; justify-content:flex-start; }
.project-text h2{
  margin:0 0 .4rem;
  font-weight:600;              /* 700 -> 600 */
  font-size:clamp(1rem, 0.55vw + 0.95rem, 1.28rem);  /* 살짝 축소 */
  line-height:1.25;
  letter-spacing:-0.01em;
  color:#0f172a;
}
.project-text p{
  margin:0;
  max-width:60ch;               /* ⬅ 가독성 핵심 */
  line-height:1.85;
  font-size:clamp(.98rem, 0.35vw + .9rem, 1.08rem);
  color:#374151;
}

/* 4) 필터 바 살짝 업그레이드 + 상단 고정(옵션) */
.project-filters{
  position:sticky; top:64px; z-index:10; /* 네비바 높이에 맞춰 조절 */
  backdrop-filter:saturate(120%) blur(6px);
  background:rgba(255,255,255,.75);
  padding:.5rem .25rem 1rem;
  margin:0 0 .5rem;
  border-bottom:1px solid #eef2f7;
}
.filter-button{
  padding:.45rem .9rem; margin:0 .3rem;
  border-radius:999px;          /* pill 형태 */
  background:#f1f5f9;
}
.filter-button.active{ background:#0a66c2; color:#fff; }

/* 5) 모바일 */
@media (max-width: 960px){
  .project-row{ grid-template-columns:1fr; gap:1rem; }
  .project-image img{ max-height:280px; }
  .project-text p{ max-width:65ch; }      /* 모바일에선 조금 풀어줌 */
}

/* 6) 다크모드(선택) */
@media (prefers-color-scheme: dark){
  .project-row + .project-row{ border-top:1px solid #2a2f3a; }
  .project-text h2{ color:#e5e7eb; }
  .project-text p{ color:#cbd5e1; }
  .filter-button{ background:#1f2937; color:#e5e7eb; }
  .filter-button.active{ background:#2563eb; color:#fff; }
  .project-filters{ background:rgba(17,24,39,.75); border-bottom-color:#111827; }
}
</style>
