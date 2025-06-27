---
title: ""
layout: single
permalink: /research/
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

<!-- Project Cards -->
<div class="project-cards">
  <!-- Example cards (repeat for all projects) -->
  <div class="card social">
    <h3><a href="/projects/social/empathy_rtpj">How Self–Other Distinction Shapes Empathy</a></h3>
    <p>Using rTPJ stimulation and multinomial processing tree modeling, this project dissociates intentional empathy, unintentional empathy, and response bias to examine how self–other distinction contributes to empathic accuracy.</p>
  </div>

  <div class="card social">
    <h3><a href="/projects/social/groupbias_perspectivetaking">Group Conformity Without Minds</a></h3>
    <p>This study tests whether the group conformity effect in visual perspective taking depends on social reasoning or can be explained by ensemble coding using non-social stimuli.</p>
  </div>

  <div class="card social">
    <h3><a href="/projects/social/cep">Context Processing in Ensemble Emotion Perception</a></h3>
    <p>Using naturalistic stimuli, this research shows how contextual background and induced affect reshape ensemble emotion perception in crowds.</p>
  </div>

  <div class="card memory">
    <h3><a href="/projects/memory/spe8vcs">Self-Prioritization in Nonspatial Working Memory</a></h3>
    <p>Explored whether self-prioritization effects arise in nonspatial working memory, given inconsistent findings in the literature.</p>
  </div>

  <div class="card memory">
    <h3><a href="/projects/memory/meaningfulness">Spatial Generalization of Object Meaningfulness</a></h3>
    <p>Investigated whether meaningful object representations facilitate the encoding of spatially distal features in visual working memory.</p>
  </div>

  <div class="card neuro">
    <h3><a href="/projects/neuro/predicting-empathy">Resting-State fMRI Predictors of Theory of Mind</a></h3>
    <p>Examined whether perspective-taking ability can be predicted from whole-brain resting-state connectivity using HCP data and SVM modeling.</p>
  </div>

  <div class="card neuro">
    <h3><a href="/projects/neuro/voice-gender">Voice Gender Effects on Consumer Preferences</a></h3>
    <p>Investigated how voice gender and age influence product evaluations, using naturalistic videos, online experiments, and fNIRS data.</p>
  </div>
</div>

<!-- Script: Filtering + Active Button -->
<script>
function filterSelection(category, el) {
  const cards = document.querySelectorAll('.card');
  cards.forEach(card => {
    card.style.display = (category === 'all' || card.classList.contains(category)) ? 'block' : 'none';
  });

  // Update active button style
  document.querySelectorAll('.filter-button').forEach(btn => btn.classList.remove('active'));
  if (el) el.classList.add('active');
}
filterSelection('all');
</script>

<!-- Style -->
<style>
/* Filter Buttons */
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

/* Card Layout */
.project-cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1.5rem;
  padding: 0 1rem;
}

.card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 1.2rem 1.5rem;
  width: calc(50% - 1rem);
  max-width: 500px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
}

.card h3 {
  font-size: 1.2rem;
  margin-bottom: 0.5rem;
}
.card p {
  font-size: 0.95rem;
  color: #555;
}
.card a {
  color: #007acc;
  text-decoration: none;
}
.card a:hover {
  text-decoration: underline;
}

/* Mobile: Single Column */
@media screen and (max-width: 768px) {
  .card {
    width: 100%;
    max-width: 95%;
    padding: 1rem;
  }
}
</style>
