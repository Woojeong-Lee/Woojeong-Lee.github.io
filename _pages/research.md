---
title: ""
layout: single
permalink: /research/
header:
  show_title: false
---

<div style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button" onclick="filterSelection('all')">All</button>
  <button class="filter-button" onclick="filterSelection('social')">Social</button>
  <button class="filter-button" onclick="filterSelection('memory')">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro')">Neuro</button>
</div>

<div class="project-cards">
  <div class="card social">
    <h3><a href="/projects/social/empathy_rtpj">How Self–Other Distinction Shapes Empathy</a></h3>
    <p>Using rTPJ stimulation and multinomial processing tree modeling, this project dissociates intentional empathy, unintentional empathy, and response bias to examine how self–other distinction contributes to empathic accuracy.</p>
  </div>
  <div class="card social">
    <h3><a href="/projects/social/groupbias_perspectivetaking">Group Conformity Without Minds: Testing Visual Perspective Taking with Non-Social Stimuli</a></h3>
    <p>This study tests whether the group conformity effect in visual perspective taking depends on social reasoning or can be explained by ensemble coding. We replicate Sun et al.'s (2024) paradigm with non-social stimuli (triangles), removing cues that evoke mentalizing. A persistent bias would suggest a domain-general mechanism underlying the original effect.</p>
  </div>
  <div class="card social">
    <h3><a href="/projects/social/cep">Context Processing in Ensemble Emotion Perception</a></h3>
    <p>Using naturalistic stimuli, this research shows how contextual background and induced affect reshape ensemble emotion perception in crowds.</p>
  </div>

<div class="card memory">
  <h3><a href="/projects/memory/spe8vcs">Self-Prioritization Effects on Nonspatial Working Memory</a></h3>
  <p>Explored whether self-prioritization effects arise in nonspatial working memory, given inconsistent findings in the literature.</p>
</div>
  </div>
<div class="card memory">
  <h3><a href="/projects/memory/meaningfulness">Spatial Generalization of Object Meaningfulness in Working Memory</a></h3>
  <p>Investigated whether meaningful object representations facilitate the encoding of spatially distal features in visual working memory.</p>
</div>

<div class="card neuro">
  <h3><a href="/projects/neuro/predicting-empathy">Resting-State fMRI Predictors of Theory of Mind Capacity</a></h3>
  <p>Examined whether individual differences in perspective-taking ability can be predicted from whole-brain resting-state connectivity using HCP data and SVM modeling.</p>
<div class="card neuro">
  <h3><a href="/projects/neuro/voice-gender">Neural and Behavioral Effects of Voice Gender on Consumer Preferences</a></h3>
  <p>Investigated how the gender and age of voices influence product evaluations and purchase decisions, using naturalistic stimuli, online behavioral tasks, and fNIRS neuroimaging.</p>
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
