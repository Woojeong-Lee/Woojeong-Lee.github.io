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

<!-- ====== FULL-BLEED OUTER + CENTERED INNER with small gutters ====== -->
<div class="projects-outer">
  <div class="projects"><!-- centered inner -->

    <!-- Plan 1 -->
    <a href="/projects/plan1" class="project-link-wrapper">
      <section class="project-row social neuro">
        <div class="project-image">
          <img src="/assets/img/projects/SRE2_method1.png" alt="Plan 1 image">
        </div>
        <div class="project-text">
          <h2>(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</h2>
          <p>
            How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA identified regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then tested cross-condition generalization to see whether classifiers trained on self-related judgments decode president-related judgments.
          </p>
        </div>
      </section>
    </a>

    <!-- Plan 2 (text only) -->
    <a href="/projects/plan2" class="project-link-wrapper">
      <section class="project-row social neuro no-image">
        <div class="project-image" aria-hidden="true"></div>
        <div class="project-text">
          <h2>(Plan 2) How Self–Other Distinction Shapes Empathy</h2>
          <p>
            We use multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias, and test how rTPJ stimulation modulates each component to refine how self–other distinction contributes to empathic accuracy.
          </p>
        </div>
      </section>
    </a>

    <!-- Plan 3 -->
    <a href="/projects/plan3" class="project-link-wrapper">
      <section class="project-row social">
        <div class="project-image">
          <img src="/assets/img/projects/placeholder-triangle.png" alt="Group Conformity Without Minds">
        </div>
        <div class="project-text">
          <h2>(Plan 3) Group Conformity Without Minds</h2>
          <p>
            A reported conformity effect in visual perspective taking may reflect domain-general ensemble coding rather than social reasoning. We replicate the paradigm with non-social isosceles triangles to test this possibility.
          </p>
        </div>
      </section>
    </a>

    <!-- Ensemble Emotion Perception -->
    <a href="/projects/ensemble-emotion" class="project-link-wrapper">
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
    </a>

    <!-- SPE -->
    <a href="/projects/spe-vwm" class="project-link-wrapper">
      <section class="project-row social memory">
        <div class="project-image">
          <img src="/assets/img/projects/SPE_method.png" alt="Self-Prioritization Effects">
        </div>
        <div class="project-text">
          <h2>Self-Prioritization Effects on Nonspatial Working Memory</h2>
          <p>
            We tested SPE on shape-based WM across two experiments:
            <a href="/data/analyzeSPE8VCS1.html" target="_blank">Experiment 1</a>,
            <a href="/data/analyzeSPE8VCS2.html" target="_blank">Experiment 2</a>.
            WM responses for colors were faster in the self condition than the other; no shape differences emerged.
          </p>
        </div>
      </section>
    </a>

    <!-- Meaningfulness in VWM (text only) -->
    <a href="/projects/meaningfulness-vwm" class="project-link-wrapper">
      <section class="project-row memory no-image">
        <div class="project-image" aria-hidden="true"></div>
        <div class="project-text">
          <h2>The Impact of Meaningfulness on Visual Working Memory Across Spatial Boundaries</h2>
          <p>
            We test whether meaningful objects facilitate encoding of spatially distal features in visual working memory.
          </p>
        </div>
      </section>
    </a>

    <!-- fNIRS (text only) -->
    <a href="/projects/fnirs-product-pref" class="project-link-wrapper">
      <section class="project-row neuro no-image">
        <div class="project-image" aria-hidden="true"></div>
        <div class="project-text">
          <h2>The Influence of Speaker Gender and Age on Product Preference</h2>
          <p>
            How do speaker gender and age shape product evaluations and purchase decisions? We test this using naturalistic video stimuli and fNIRS.
          </p>
        </div>
      </section>
    </a>

  </div>
</div>

<!-- ====== Filter logic ====== -->
<script>
function filterSelection(category, btn) {
  const rows = document.querySelectorAll('.project-row');
  rows.forEach(row => {
    const show = (category === 'all') || row.classList.contains(category);
    row.parentElement.style.display = show ? '' : 'none'; // hide <a> wrapper
  });
  document.querySelectorAll('.filter-button').forEach(b => b.classList.remove('active'));
  if (btn) btn.classList.add('active');
}
filterSelection('all', document.querySelector('.filter-button'));
</script>

<style>
/* ========= Filters ========= */
.project-filters{
  text-align:center;
  margin: .25rem 0 1rem;
}
.filter-button{
  padding:.45rem .9rem;
  margin:0 .3rem;
  background:#f1f5f9;
  border:0;
  border-radius:999px;
  cursor:pointer;
  font-weight:500;
  transition:background .2s;
}
.filter-button:hover{ background:#e6edf5; }
.filter-button.active{ background:#0a66c2; color:#fff; }

/* ========= Full-bleed escape (outer), centered inner with small gutters ========= */
.projects-outer{
  width:100vw;
  margin-left:calc(50% - 50vw);
  margin-right:calc(50% - 50vw);
}
.projects{
  width:100%;
  max-width:1400px;    /* 전체 최대 폭 */
  margin:0 auto;       /* 가운데 정렬 */
  padding:0 2rem;      /* 양 끝에 '조금' 여백 */
}

/* ========= Clickable wrapper ========= */
.project-link-wrapper{
  display:block;
  text-decoration:none;
  color:inherit;
}
.project-link-wrapper:hover .project-row{
  background:#f9fafb;
}

/* ========= Grid: 이미지 39% / 텍스트 61%, 위쪽 정렬 ========= */
.project-row{
  display:grid;
  grid-template-columns:minmax(0,39%) minmax(0,61%);
  align-items:start;
  gap:1.75rem;
  padding:1.25rem 0 2rem;
  transition:background .2s ease;
}
.project-row + .project-row{ border-top:1px solid #e9edf3; }

/* ========= 이미지: 비율 유지, 잘림 없음 ========= */
.project-image{ display:flex; align-items:flex-start; justify-content:center; }
.project-image img{
  width:100%;
  height:auto;            /* 원본 비율 유지 */
  object-fit:contain;     /* 잘리지 않게 */
  max-height:420px;       /* 통일된 최대 높이 (원하면 360~480으로 조절) */
  border-radius:6px;
}

/* ========= 텍스트 ========= */
.project-text{ display:flex; flex-direction:column; justify-content:flex-start; }
.project-text h2{
  margin:0 0 .4rem;
  font-weight:600;
  font-size:clamp(1rem, 0.55vw + 0.95rem, 1.28rem); /* 제목 살짝 작게 */
  line-height:1.25;
  letter-spacing:-0.01em;
  color:#0f172a;
}
.project-text p{
  margin:0;
  max-width:60ch;         /* 가독성 좋은 줄길이 */
  line-height:1.85;
  font-size:clamp(.98rem, 0.35vw + .9rem, 1.08rem);
  color:#374151;
}
.project-text a{ color:#0a6cff; text-decoration:underline; }

/* ========= 모바일 ========= */
@media (max-width: 960px){
  .projects{ padding:0 1rem; }
  .project-row{ grid-template-columns:1fr; gap:1rem; }
  .project-image img{ max-height:280px; }
  .project-text p{ max-width:65ch; }
}

/* ========= (선택) 다크 모드 대비 ========= */
@media (prefers-color-scheme: dark){
  .project-row + .project-row{ border-top:1px solid #2a2f3a; }
  .project-link-wrapper:hover .project-row{ background:#161a22; }
  .project-text h2{ color:#e5e7eb; }
  .project-text p{ color:#cbd5e1; }
  .filter-button{ background:#1f2937; color:#e5e7eb; }
  .filter-button.active{ background:#2563eb; color:#fff; }
}
</style>
