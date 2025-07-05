---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<!-- Filter Buttons -->
<div style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button" onclick="filterSelection('all')">All</button>
  <button class="filter-button" onclick="filterSelection('social')">Social</button>
  <button class="filter-button" onclick="filterSelection('memory')">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro')">Neuro</button>
</div>

<!-- Project List -->
<div class="project-list">

  <!-- Example Project -->
  <div class="project-row social">
    <div class="project-title">
      <strong>How Self–Other Distinction Shapes Empathy</strong>
      <button onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="project-description">
      This study uses rTPJ stimulation and MPT modeling to separate intentional, unintentional empathy and bias, clarifying the role of self–other distinction in empathy.
    </div>
  </div>

  <div class="project-row social">
    <div class="project-title">
      <strong>Group Conformity Without Minds</strong>
      <button onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="project-description">
      Replicates avatar-based group bias study using triangles, testing whether effects reflect ensemble spatial coding rather than social cognition.
    </div>
  </div>

  <div class="project-row social">
    <div class="project-title">
      <strong>The Influence of Situational Context and Observer Emotion on Ensemble Perception of Crowd Emotion</strong>
      <button onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="project-description">
      Explores how context and emotion modulate perception of group facial affect using naturalistic images and ensemble coding.
    </div>
  </div>

  <div class="project-row memory">
    <div class="project-title">
      <strong>Self-Prioritization Effects on Nonspatial Working Memory</strong>
      <button onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="project-description">
      Tests whether self-association boosts working memory accuracy and speed, showing feature-specific rather than object-based self-prioritization.
    </div>
  </div>

  <div class="project-row memory">
    <div class="project-title">
      <strong>Does Meaningfulness Enhance Working Memory Across Spatial Locations?</strong>
      <button onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="project-description">
      Investigates whether semantic content enhances memory of spatially distributed features using diffeomorphic stimuli.
    </div>
  </div>

  <div class="project-row neuro">
    <div class="project-title">
      <strong>Resting-State fMRI Predictors of Theory of Mind Capacity</strong>
      <button onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="project-description">
      Uses SVM on HCP resting-state fMRI to predict individual differences in perspective-taking based on whole-brain connectivity.
    </div>
  </div>

  <div class="project-row neuro">
    <div class="project-title">
      <strong>Voice Gender Effects on Consumer Preferences</strong>
      <button onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="project-description">
      fNIRS and behavioral studies show how voice gender and age affect product evaluations and purchase intent.
    </div>
  </div>

</div>

<style>
.project-list {
  max-width: 750px;
  margin: 0 auto;
  padding: 0 1rem;
}
.project-row {
  border-bottom: 1px solid #ddd;
  padding: 1rem 0;
}
.project-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.project-title strong {
  font-size: 1rem;
  color: #333;
  flex: 1;
  margin-right: 1rem;
}
.project-title button {
  background: #f1f1f1;
  border: none;
  padding: 0.3rem 0.6rem;
  border-radius: 5px;
  cursor: pointer;
  font-size: 0.85rem;
}
.project-title button:hover {
  background: #e0e0e0;
}
.project-description {
  margin-top: 0.6rem;
  font-size: 0.93rem;
  color: #555;
  display: none;
}
.filter-button {
  padding: 0.5rem 1rem;
  margin: 0 0.4rem;
  background: #f0f0f0;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 500;
}
.filter-button:hover {
  background: #e0e0e0;
}
@media screen and (max-width: 600px) {
  .project-title {
    flex-direction: column;
    align-items: flex-start;
  }
  .project-title button {
    margin-top: 0.5rem;
  }
}
</style>

<script>
function toggleDescription(button) {
  const desc = button.closest('.project-row').querySelector('.project-description');
  const visible = desc.style.display === 'block';
  desc.style.display = visible ? 'none' : 'block';
  button.textContent = visible ? 'Show more' : 'Show less';
}

function filterSelection(category) {
  const rows = document.querySelectorAll('.project-row');
  rows.forEach(row => {
    row.style.display = (category === 'all' || row.classList.contains(category)) ? 'block' : 'none';
  });
}
filterSelection('all');
</script>
