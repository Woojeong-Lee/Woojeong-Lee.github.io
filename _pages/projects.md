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

<!-- 모든 프로젝트 카드를 같은 컨테이너(.project-list) 안에 넣음 -->
<div class="project-list">

  <details class="project-item social neuro">
    <summary>(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</summary>
    <figure class="project-figure">
      <img
        src="/assets/img/projects/SRE2_method1.png"
        loading="lazy"
        style="max-width:100%; border-radius:6px;"
      >
    </figure>
    <p>
      How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA was used to identify brain regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then evaluated cross-condition generalization, testing whether classifiers trained on self-related judgments could decode president-related judgments.
    </p>
  </details>

  <details class="project-item social neuro">
    <summary>(Plan 2) How Self–Other Distinction Shapes Empathy</summary>
    <p>
      Empathy—the ability to understand and share others’ emotions—is essential for social interaction. Effective empathy requires a clear self–other distinction. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure. Contemporary theories of pain empathy differentiate between automatic, bottom-up simulation and controlled, top-down regulation depending on context. These distinct components may rely on separable neural mechanisms. To address this, we apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, providing a more nuanced understanding of how self–other distinction contributes to empathic accuracy.
    </p>
  </details>

  <details class="project-item social">
    <summary>(Plan 3) Group Conformity Without Minds</summary>
    <p>
      Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking, observing that participants' judgments of a target avatar’s viewpoint were biased toward the average viewpoint of surrounding avatars. This interpretation relies on the assumption that participants adopt the avatar’s perspective. However, such bias may alternatively arise from domain-general mechanisms, such as ensemble coding of directional information, without necessarily invoking social reasoning. To test this possibility, the present study replicates the original paradigm using non-social stimuli—specifically, replacing avatars with isosceles triangles.
    </p>
  </details>

  <details class="project-item social">
    <summary>The Influence of Situational Context and Observer Emotion on Ensemble Emotion Perception</summary>
    <figure class="project-figure">
      <img
        src="/assets/img/projects/CEP_method.png"
        loading="lazy"
        style="max-width:100%; border-radius:6px;"
      >
    </figure>
    <p>
      Using naturalistic stimuli, the study investigated how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.
    </p>
  </details>

  <details class="project-item social memory">
    <summary>Self-Prioritization Effects on Nonspatial Working Memory</summary>
    <p>
      Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. Although extensive studies have demonstrated the SPE on perception, findings regarding its effects on working memory (WM) remain inconsistent. Some studies reported improved WM speed and accuracy for self-associated items (Yin et al, 2019; Yin et al, 2019; Yin &amp; Chen, 2024), while others failed to find such an effect (Constable et al., 2019).
      <br>The current study examined the SPE on shape-based WM across two experiments. Participants associated themselves and others with specific colors and completed a delayed matched-to-sample task
      <a href="/data/analyzeSPE8VCS1.html" target="_blank" class="project-link">(Experiment 1)</a>
      or a reproduction task
      <a href="/data/analyzeSPE8VCS2.html" target="_blank" class="project-link">(Experiment 2)</a>.
      Results revealed that WM responses for colors were faster in the self condition than in the other, though no shape differences emerged.
    </p>
  </details>

  <details class="project-item memory">
    <summary>The Impact of Meaningfulness on Visual Working Memory Across Spatial Boundaries</summary>
    <p>
      The study examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.
    </p>
  </details>

  <details class="project-item neuro">
    <summary>The Influence of Speaker Gender and Age on Product Preference</summary>
    <p>
      The study investigated how the gender and age of speakers affect product evaluations and purchase decisions, using naturalistic video stimuli and fNIRS.
    </p>
  </details>

</div> <!-- ← 모든 details가 이 안에 들어있음 -->

<script>
function filterSelection(category, el) {
  const items = document.querySelectorAll('.project-item');
  items.forEach(item => {
    item.style.display = (category === 'all' || item.classList.contains(category)) ? 'block' : 'none';
  });

  document.querySelectorAll('.filter-button').forEach(btn => btn.classList.remove('active'));
  el.classList.add('active');
}
filterSelection('all', document.querySelector('.filter-button'));
</script>

<style>
.filter-button {
  padding: 0.5rem 1rem;
  margin: 0 0.3rem;
  background: #f0f0f0;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 500;
  transition: background 0.2s;
}
.filter-button:hover {
  background: #e0e0e0;
}
.filter-button.active {
  background: #007acc;
  color: white;
}

.project-link {
  color: #007acc;
  text-decoration: none;
}
.project-link:hover {
  text-decoration: underline;
}

.project-list {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* 카드(세부 항목) 공통 스타일 */
.project-item {
  border: 1px solid #eee;
  border-radius: 8px;
  padding: 1rem 1.2rem;
  margin-bottom: 0rem;
  background: #fff;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
  transition: background-color 0.3s, box-shadow 0.3s, transform 0.2s;
}

/* figure안 이미지가 카드 폭을 넘지 않도록 보강 */
.project-figure img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 6px; /* inline style과 동일하게 유지 */
}

.project-item:hover {
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
  transform: translateY(-1px);
}

.project-item[open] {
  background-color: #f0f7ff;
  border: 1px solid #cce5ff;
}

.project-item summary {
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  outline: none;
  list-style: none;
  display: flex;
  align-items: center;
  position: relative;
  padding-left: 1.2rem;
  margin-bottom: 0.6rem;
}
.project-item summary::before {
  content: '▶';
  position: absolute;
  left: 0;
  transition: transform 0.2s ease;
}
.project-item[open] summary::before {
  content: '▼';
  transform: rotate(0deg);
}
.project-item[open] summary {
  color: #007acc;
}

.project-item p {
  margin-top: 0.5rem;
  margin-left: 0.3rem;
  font-size: 1.05rem;
  color: #444;
  line-height: 1.8;
}

@media screen and (max-width: 768px) {
  .project-item summary {
    font-size: 0.95rem;
  }
  .project-item p {
    font-size: 0.95rem;
  }
}
</style>
