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
    <p>Empathy, the ability to understand and share others’ emotions, is essential for social interaction. ...</p>
  </details>

  <details class="project-item social">
    <summary>Group Conformity Without Minds</summary>
    <p>Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking, observing that participants' judgments ...</p>
  </details>

  <details class="project-item social">
    <summary>The Influence of Situational Context and Observer Emotion on Ensemble Perception of Crowd Emotion</summary>
    <p>Using naturalistic stimuli, we investigate how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.</p>
  </details>

  <details class="project-item memory">
    <summary>Self-Prioritization Effects on Nonspatial Working Memory</summary>
    <p>Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. ...<br>
    Participants associated themselves and others with specific colors and completed a delayed matched-to-sample task 
    <a href="/data/analyzeSPE8VCS1.html" target="_blank">(Experiment 1)</a> or a reproduction task 
    <a href="/data/analyzeSPE8VCS2.html" target="_blank">(Experiment 2)</a> for the shapes of objects presented in each color. ...</p>
  </details>

  <details class="project-item memory">
    <summary>Does Meaningfulness Enhance Working Memory Across Spatial Locations?</summary>
    <p>We examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.</p>
  </details>

  <details class="project-item neuro">
    <summary>Predicting Perspective-Taking Ability from Resting-State fMRI</summary>
    <p>I examined whether individual differences in perspective-taking ability can be predicted from whole-brain resting-state connectivity ...</p>
  </details>

  <details class="project-item neuro">
    <summary>The Role of Speaker Gender and Age in Shaping Product Preference</summary>
    <p>We investigated how the gender and age of voices influence product evaluations and purchase decisions ...</p>
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

/* Project list layout (updated width) */
.project-list {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
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
  position: relative;
  padding-left: 1.2rem;
}
.project-item summary::before {
  content: '▶';
  position: absolute;
  left: 0;
  transition: transform 0.2s ease;
}
.project-item[open] summary::before {
  content: '▼';
}

.project-item p {
  margin-top: 0.6rem;
  margin-left: 1.2rem;
  font-size: 0.95rem;
  color: #444;
  line-height: 1.6;
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
