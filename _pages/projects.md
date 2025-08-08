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
    <img src="/assets/img/projects/SRE2_method1.png" alt="Neural mechanisms" class="project-img">
    <div class="project-info">
      <h3 class="project-title">(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</h3>
      <p class="project-text">How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA was used to identify brain regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then evaluated cross-condition generalization, testing whether classifiers trained on self-related judgments could decode president-related judgments.</p>
    </div>
  </a>

  <a href="/projects/plan-2" class="project-card social neuro">
    <img src="/assets/img/projects/CEP_method.png" alt="Self–Other distinction" class="project-img">
    <div class="project-info">
      <h3 class="project-title">(Plan 2) How Self–Other Distinction Shapes Empathy</h3>
      <p class="project-text">Empathy—the ability to understand and share others’ emotions—is essential for social interaction. Effective empathy requires a clear self–other distinction. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure. Contemporary theories of pain empathy differentiate between automatic, bottom-up simulation and controlled, top-down regulation depending on context. These distinct components may rely on separable neural mechanisms. To address this, we apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, providing a more nuanced understanding of how self–other distinction contributes to empathic accuracy.</p>
    </div>
  </a>

  <a href="/projects/plan-3" class="project-card social no-image">
    <div class="project-info">
      <h3 class="project-title">(Plan 3) Group Conformity Without Minds</h3>
      <p class="project-text">Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking, observing that participants' judgments of a target avatar’s viewpoint were biased toward the average viewpoint of surrounding avatars. This interpretation relies on the assumption that participants adopt the avatar’s perspective. However, such bias may alternatively arise from domain-general mechanisms, such as ensemble coding of directional information, without necessarily invoking social reasoning. To test this possibility, the present study replicates the original paradigm using non-social stimuli—specifically, replacing avatars with isosceles triangles.</p>
    </div>
  </a>

  <a href="/projects/ensemble-emotion-context" class="project-card social">
    <img src="/assets/img/projects/CEP_method.png" alt="Ensemble emotion perception" class="project-img">
    <div class="project-info">
      <h3 class="project-title">The Influence of Situational Context and Observer Emotion on Ensemble Emotion Perception</h3>
      <p class="project-text">Using naturalistic stimuli, the study investigated how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.</p>
    </div>
  </a>

  <a href="/projects/self-prioritization-wm" class="project-card social memory">
    <img src="/assets/img/projects/SPE_method.png" alt="Self-prioritization working memory" class="project-img">
    <div class="project-info">
      <h3 class="project-title">Self-Prioritization Effects on Nonspatial Working Memory</h3>
      <p class="project-text">Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. Although extensive studies have demonstrated the SPE on perception, findings regarding its effects on working memory (WM) remain inconsistent. Some studies reported improved WM speed and accuracy for self-associated items (Yin et al, 2019; Yin et al, 2019; Yin &amp; Chen, 2024), while others failed to find such an effect (Constable et al., 2019). The current study examined the SPE on shape-based WM across two experiments. Participants associated themselves and others with specific colors and completed a delayed matched-to-sample task (Experiment 1) or a reproduction task (Experiment 2). Results revealed that WM responses for colors were faster in the self condition than in the other, though no shape differences emerged. <a href="/data/analyzeSPE8VCS1.html" target="_blank" class="project-link">Experiment 1</a> · <a href="/data/analyzeSPE8VCS2.html" target="_blank" class="project-link">Experiment 2</a></p>
    </div>
  </a>

  <a href="/projects/meaningfulness-vwm-boundaries" class="project-card memory no-image">
    <div class="project-info">
      <h3 class="project-title">The Impact of Meaningfulness on Visual Working Memory Across Spatial Boundaries</h3>
      <p class="project-text">The study examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.</p>
    </div>
  </a>

  <a href="/projects/speaker-gender-age-preference" class="project-card neuro no-image">
    <div class="project-info">
      <h3 class="project-title">The Influence of Speaker Gender and Age on Product Preference</h3>
      <p class="project-text">The study investigated how the gender and age of speakers affect product evaluations and purchase decisions, using naturalistic video stimuli and fNIRS.</p>
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
.filter-button { padding: .5rem 1rem; margin: 0 .3rem; background: #f0f0f0; border: none; border-radius: 6px; cursor: pointer; font-weight: 500; transition: background .2s; }
.filter-button:hover { background: #e0e0e0; }
.filter-button.active { background: #007acc; color: #fff; }

.project-list { max-width: 100%; margin: 0 auto; padding: 0 10rem; display: flex; flex-direction: column; gap: 2rem; }

.project-card { display: flex; align-items: center; gap: 3rem; text-decoration: none; color: inherit; background: #fff; border: 1px solid #eee; border-radius: 12px; padding: 2rem; box-shadow: 0 1px 3px rgba(0,0,0,.05); transition: box-shadow .25s, transform .15s; }
.project-card:hover { box-shadow: 0 4px 14px rgba(0,0,0,.08); transform: translateY(-1px); }

.project-img { width: 600px; height: 340px; object-fit: cover; border-radius: 12px; flex-shrink: 0; }
.no-image { padding-left: 1.5rem; }

.project-info { flex: 1; }
.project-title { font-size: 2rem; font-weight: 800; margin: 0 0 .8rem; line-height: 1.25; }
.project-text { font-size: 1.15rem; color: #444; line-height: 1.8; margin: 0; }

@media (max-width: 900px) {
  .project-list { padding: 0 1rem; }
  .project-card { flex-direction: column; align-items: flex-start; }
  .project-img { width: 100%; height: auto; }
  .project-title { font-size: 1.4rem; }
}
</style>
