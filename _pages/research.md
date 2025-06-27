---
title: ""
layout: single
permalink: /research/
header:
  show_title: false
---

<p style="text-align:center; max-width: 800px; margin: 2rem auto;">
  While I have organized my projects into the domains of Social, Memory, and Neuro for clarity, they are often closely connected. Many of my projects lie at the intersection of two or more of these areas, and insights gained from one have frequently contributed to the development of others.
</p>

<div style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button" onclick="filterSelection('all')">All</button>
  <button class="filter-button" onclick="filterSelection('social')">Social</button>
  <button class="filter-button" onclick="filterSelection('memory')">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro')">Neuro</button>
</div>

<div class="project-cards">
  <div class="card social">
    <h3><a href="/projects/social/self-prioritization">Self-Prioritization Effects on Nonspatial Working Memory</a></h3>
    <p>Exploring how self-relevant cues influence working memory performance.</p>
  </div>
  <div class="card social">
    <h3><a href="/projects/social/meaningfulness">Meaningfulness in Working Memory</a></h3>
    <p>Investigating the role of meaningful stimuli in memory encoding and maintenance.</p>
  </div>
  <div class="card social">
    <h3><a href="/projects/social/group-bias">Group Bias on Perspective Taking in Non-Social Context</a></h3>
    <p>Understanding group-related cognitive bias in neutral contexts.</p>
  </div>

  <div class="card memory">
    <h3><a href="/projects/memory/context-emotion">Context Processing in Ensemble Emotion Perception</a></h3>
    <p>How situational context shapes the perception of crowd emotion using naturalistic stimuli.</p>
  </div>
  <div class="card memory">
    <h3><a href="/projects/memory/interaction-dimension">Dimension Underlying the Perception of Social Interaction</a></h3>
    <p>Identifying core dimensions in social interaction perception.</p>
  </div>

  <div class="card neuro">
    <h3><a href="/projects/neuro/predicting-empathy">Predicting Perspective-Taking Ability from Resting-State fMRI</a></h3>
    <p>Using brain network features to predict cognitive empathy capacity.</p>
  </div>
  <div class="card neuro">
    <h3><a href="/projects/neuro/voice-gender">The Effect of Voice Gender on Product Preference</a></h3>
    <p>Examining how gendered voice cues shape product evaluations.</p>
  </div>
</div>

<script>
function filterSelection(category) {
  const cards = document.querySelectorAll('.card');
  cards.forEach(card => {
    if (category === 'all' || card.classList.contains(category)) {
      card.style.display = 'block';
    } else {
      card.style.display = 'none';
    }
  });
}
filterSelection('all'); // Show all on load
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
}
.filter-button:hover {
  background: #e0e0e0;
}
.project-cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1.5rem;
  margin-top: 1.5rem;
}
.card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 1rem;
  max-width: 320px;
  width: 100%;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
}
.card h3 {
  font-size: 1.1rem;
  margin-bottom: 0.5rem;
}
.card p {
  font-size: 0.9rem;
  color: #555;
}
.card a {
  color: #007acc;
  text-decoration: none;
}
.card a:hover {
  text-decoration: underline;
}
</style>
