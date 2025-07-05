---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<div style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button" onclick="filterSelection('all')">All</button>
  <button class="filter-button" onclick="filterSelection('social')">Social</button>
  <button class="filter-button" onclick="filterSelection('memory')">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro')">Neuro</button>
</div>

<div class="project-list">
  <details class="project-item social">
    <summary>How Self–Other Distinction Shapes Empathy</summary>
    <p>Empathy, the ability to understand and share others’ emotions, is essential for social interaction... (생략)</p>
  </details>

  <details class="project-item social">
    <summary>Group Conformity Without Minds</summary>
    <p>Sun, Wang, and Geng (2024) reported a group conformity effect... (생략)</p>
  </details>

  <details class="project-item social">
    <summary>The Influence of Situational Context and Observer Emotion on Ensemble Perception of Crowd Emotion</summary>
    <p>Using naturalistic stimuli, we investigate how situational context and observer emotion shape perception of crowd emotion.</p>
  </details>

  <details class="project-item memory">
    <summary>Self-Prioritization Effects on Nonspatial Working Memory</summary>
    <p>Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly... (생략)</p>
  </details>

  <details class="project-item memory">
    <summary>Does Meaningfulness Enhance Working Memory Across Spatial Locations?</summary>
    <p>We examined meaningful objects facilitate the encoding of spatially distal features in visual working memory.</p>
  </details>

  <details class="project-item neuro">
    <summary>Resting-State fMRI Predictors of Theory of Mind Capacity</summary>
    <p>I examined whether individual differences in perspective-taking ability can be predicted... (생략)</p>
  </details>

  <details class="project-item neuro">
    <summary>Voice Gender Effects on Consumer Preferences</summary>
    <p>We investigated how the gender and age of voices influence product evaluations and purchase decisions.</p>
  </details>
</div>

<script>
function filterSelection(category) {
  const items = document.querySelectorAll('.project-item');
  items.forEach(item => {
    item.style.display = (category === 'all' || item.classList.contains(category)) ? 'block' : 'none';
  });
}
filterSelection('all');
</script>

<style>
/* Filter buttons */
.filter-button {
  padding: 0.5rem 1rem;
  margin: 0 0.3rem;
  background: #f0f0f0;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 500;
}
.filter-button:hover {
  background: #e0e0e0;
}

/* Project List Styles */
.project-list {
  max-width: 860px;
  margin: 0 auto;
  padding: 0 1rem;
}

.project-item {
  border-bottom: 1px solid #ddd;
  padding: 0.8rem 0;
}

.project-item summary {
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  outline: none;
  list-style: none;
  display: flex;
  align-items: center;
  transition: color 0.2s;
}

.project-item summary::marker,
.project-item summary::-webkit-details-marker {
  margin-right: 0.5rem;
  font-size: 1rem;
}

.project-item p {
  margin-top: 0.6rem;
  margin-left: 1.2rem;
  font-size: 0.95rem;
  color: #444;
  line-height: 1.5;
}

/* Mobile */
@media screen and (max-width: 768px) {
  .project-item summary {
    font-size: 0.95rem;
  }
  .project-item p {
    font-size: 0.9rem;
  }
}
</style>
