---
title: ""
layout: single
permalink: /research/
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

<!-- Project Cards -->
<div class="project-cards">

  <a href="/projects/social/empathy_rtpj" class="card-link social">
    <div class="card">
      <h3>How Self–Other Distinction Shapes Empathy</h3>
      <p>Using rTPJ stimulation and multinomial processing tree modeling, this project dissociates intentional empathy, unintentional empathy, and response bias to examine how self–other distinction contributes to empathic accuracy.</p>
    </div>
  </a>

  <a href="/projects/social/groupbias_perspectivetaking" class="card-link social">
    <div class="card">
      <h3>Group Conformity Without Minds</h3>
      <p>This study replicates a visual perspective-taking task using non-social stimuli to test whether group conformity effects are due to social cognition or low-level ensemble coding.</p>
    </div>
  </a>

  <a href="/projects/social/cep" class="card-link social">
    <div class="card">
      <h3>Context Processing in Ensemble Emotion Perception</h3>
      <p>Using naturalistic stimuli, this research explores how contextual background and affective states reshape perception of crowd emotion.</p>
    </div>
  </a>

  <a href="/projects/memory/spe8vcs" class="card-link memory">
    <div class="card">
      <h3>Self-Prioritization in Nonspatial Working Memory</h3>
      <p>Investigated whether self-prioritization effects generalize to nonspatial working memory, addressing conflicting evidence in previous research.</p>
    </div>
  </a>

  <a href="/projects/memory/meaningfulness" class="card-link memory">
    <div class="card">
      <h3>Spatial Generalization of Object Meaningfulness</h3>
      <p>Tested whether meaningful object representations facilitate encoding of spatially distal features in visual working memory.</p>
    </div>
  </a>

  <a href="/projects/neuro/predicting-empathy" class="card-link neuro">
    <div class="card">
      <h3>Resting-State fMRI Predictors of Theory of Mind</h3>
      <p>Used whole-brain resting-state connectivity and machine learning models to predict individual differences in perspective-taking ability.</p>
    </div>
  </a>

  <a href="/projects/neuro/voice-gender" class="card-link neuro">
    <div class="card">
      <h3>Voice Gender Effects on Product Evaluation</h3>
      <p>Explored how voice gender and age modulate consumer preferences using behavioral experiments and fNIRS data.</p>
    </div>
  </a>

</div>

<!-- Filter Function -->
<script>
function filterSelection(category) {
  const links = document.querySelectorAll('.card-link');
  links.forEach(link => {
    if (category === 'all' || link.classList.contains(category)) {
      link.style.display = 'block';
    } else {
      link.style.display = 'none';
    }
  });
}
filterSelection('all'); // Show all on initial load
</script>

<!-- Style -->
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
  gap: 2rem 2rem;
  margin-top: 1.5rem;
}

.card-link {
  text-decoration: none;
  color: inherit;
  width: calc(50% - 1rem); /* 두 개씩 정렬 */
  transition: transform 0.2s, box-shadow 0.2s;
}

.card-link:hover .card {
  box-shadow: 0 4px 12px rgba(0, 122, 204, 0.2);
  transform: translateY(-2px);
}

.card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 1.5rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  min-height: 230px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.card h3 {
  font-size: 1.15rem;
  margin-bottom: 0.75rem;
  line-height: 1.3;
}

.card p {
  font-size: 0.95rem;
  color: #555;
  line-height: 1.4;
}

/* Responsive: 1 column on small screens */
@media screen and (max-width: 768px) {
  .card-link {
    width: 100%;
    max-width: 95%;
  }
}
</style>
