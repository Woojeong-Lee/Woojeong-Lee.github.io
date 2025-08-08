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

<!-- One-row horizontal cards. Left image, right text. Whole card is clickable. -->
<div class="project-list">

  <!-- Card 1 -->
  <a href="/projects/plan-1" class="project-card social neuro">
    <img src="/assets/img/projects/SRE2_method1.png" alt="Neural mechanisms" class="project-img">
    <div class="project-info">
      <h3 class="project-title">(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</h3>
      <p class="project-text">How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA identified regions encoding a friend’s perspective; ROI-based MVPA tested cross-condition generalization.</p>
    </div>
  </a>

  <!-- Card 2 -->
  <a href="/projects/plan-2" class="project-card social neuro">
    <img src="/assets/img/projects/CEP_method.png" alt="Self–Other distinction" class="project-img">
    <div class="project-info">
      <h3 class="project-title">(Plan 2) How Self–Other Distinction Shapes Empathy</h3>
      <p class="project-text">We dissociate intentional empathy, unintentional empathy, and response bias using MPT modeling, and test how rTPJ stimulation modulates each component to clarify the role of self–other distinction in empathic accuracy.</p>
    </div>
  </a>

  <!-- Card 3 -->
  <a href="/projects/plan-3" class="project-card social">
    <img src="/assets/img/projects/SPE_method.png" alt="Group conformity without minds" class="project-img">
    <div class="project-info">
      <h3 class="project-title">(Plan 3) Group Conformity Without Minds</h3>
      <p class="project-text">Replicating Sun, Wang, &amp; Geng (2024) with non-social stimuli (triangles) to test whether the conformity effect in visual perspective taking can be explained by ensemble coding of directions rather than adopting avatars’ minds.</p>
    </div>
  </a>

  <!-- Card 4 -->
  <a href="/projects/ensemble-emotion-context" class="project-card social">
    <img src="/assets/img/projects/CEP_method.png" alt="Ensemble emotion perception" class="project-img">
    <div class="project-info">
      <h3 class="project-title">Situational Context &amp; Observer Emotion in Ensemble Emotion Perception</h3>
      <p class="project-text">Using naturalistic stimuli, we test how situational context and the observer’s own emotion shape perceived crowd emotion.</p>
    </div>
  </a>

  <!-- Card 5 -->
  <a href="/projects/self-prioritization-wm" class="project-card social memory">
    <img src="/assets/img/projects/SPE_method.png" alt="Self-prioritization working memory" class="project-img">
    <div class="project-info">
      <h3 class="project-title">Self-Prioritization Effects on Nonspatial Working Memory</h3>
      <p class="project-text">Across two experiments (delayed match; reproduction), self-associated colors sped responses versus other-associated colors, with no shape advantage. <span class="inline-links"><a href="/data/analyzeSPE8VCS1.html" target="_blank" class="project-link">Experiment 1</a> · <a href="/data/analyzeSPE8VCS2.html" target="_blank" class="project-link">Experiment 2</a></span></p>
    </div>
  </a>

  <!-- Card 6 -->
  <a href="/projects/meaningfulness-vwm-boundaries" class="project-card memory">
    <img src="/assets/img/projects/CEP_method.png" alt="Meaningfulness and VWM" class="project-img">
    <div class="project-info">
      <h3 class="project-title">Meaningfulness &amp; Visual Working Memory Across Spatial Boundaries</h3>
      <p class="project-text">Do meaningful objects facilitate encoding of spatially distal features in VWM? We probe cross-boundary integration with meaningful vs. meaningless items.</p>
    </div>
  </a>

  <!-- Card 7 -->
  <a href="/projects/speaker-gender-age-preference" class="project-card neuro">
    <img src="/assets/img/projects/CEP_method.png" alt="Speaker gender/age and preference" class="project-img">
    <div class="project-info">
      <h3 class="project-title">Speaker Gender &amp; Age Effects on Product Preference</h3>
      <p class="project-text">Using naturalistic video and fNIRS, we examine how speaker gender and age shape product evaluations and purchase intent.</p>
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
// init
filterSelection('all', document.querySelector('.filter-button'));
</script>

<style>
/* Buttons */
.filter-button{padding:.5rem 1rem;margin:0 .3rem;background:#f0f0f0;border:none;border-radius:6px;cursor:pointer;font-weight:500;transition:background .2s}
.filter-button:hover{background:#e0e0e0}.filter-button.active{background:#007acc;color:#fff}

/* Wider layout */
.project-list{max-width:1680px;margin:0 auto;padding:0 5rem;display:flex;flex-direction:column;gap:1rem}

/* Card: one row, clickable */
.project-card{display:flex;align-items:center;gap:1.2rem;text-decoration:none;color:inherit;background:#fff;border:1px solid #eee;border-radius:12px;padding:1rem;box-shadow:0 1px 3px rgba(0,0,0,.05);transition:box-shadow .25s,transform .15s}
.project-card:hover{box-shadow:0 4px 14px rgba(0,0,0,.08);transform:translateY(-1px)}

/* Left image */
.project-img{width:300px;height:180px;object-fit:cover;border-radius:10px;flex-shrink:0}

/* Right text */
.project-info{flex:1}
.project-title{font-size:1.5rem;font-weight:800;margin:0 0 .35rem;line-height:1.25}
.project-text{font-size:1.05rem;color:#444;line-height:1.6;margin:0;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}

.inline-links a.project-link{color:#007acc;text-decoration:none}
.inline-links a.project-link:hover{text-decoration:underline}

/* Responsive */
@media (max-width:900px){
  .project-list{padding:0 1rem}
  .project-card{flex-direction:column;align-items:flex-start}
  .project-img{width:100%;height:auto}
  .project-title{font-size:1.25rem}
}
</style>
