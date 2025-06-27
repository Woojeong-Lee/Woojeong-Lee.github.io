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

  <a href="/projects/social/empathy_rtpj" class="card-link social">
    <div class="card">
      <h3>How Self–Other Distinction Shapes Empathy</h3>
      <p>Using rTPJ stimulation and multinomial processing tree modeling, this project dissociates intentional empathy, unintentional empathy, and response bias to examine how self–other distinction contributes to empathic accuracy.</p>
    </div>
  </a>

  <a href="/projects/social/groupbias_perspectivetaking" class="card-link social">
    <div class="card">
      <h3>Group Conformity Without Minds</h3>
      <p>This study tests whether the group conformity effect in visual perspective taking depends on social reasoning or can be explained by ensemble coding.</p>
    </div>
  </a>

  <a href="/projects/social/cep" class="card-link social">
    <div class="card">
      <h3>Context Processing in Ensemble Emotion Perception</h3>
      <p>Using naturalistic stimuli, this research shows how contextual background and induced affect reshape ensemble emotion perception in crowds.</p>
    </div>
  </a>

  <a href="/projects/memory/spe8vcs" class="card-link memory">
    <div class="card">
      <h3>Self-Prioritization Effects on Nonspatial Working Memory</h3>
      <p>Explored whether self-prioritization effects arise in nonspatial working memory, given inconsistent findings in the literature.</p>
    </div>
  </a>

  <a href="/projects/memory/meaningfulness" class="card-link memory">
    <div class="card">
      <h3>Spatial Generalization of Object Meaningfulness in Working Memory</h3>
      <p>Investigated whether meaningful object representations facilitate the encoding of spatially distal features in visual working memory.</p>
    </div>
  </a>

  <a href="/projects/neuro/predicting-empathy" class="card-link neuro">
    <div class="card">
      <h3>Resting-State fMRI Predictors of Theory of Mind Capacity</h3>
      <p>Examined whether individual differences in perspective-taking ability can be predicted from whole-brain resting-state connectivity using HCP data and SVM modeling.</p>
    </div>
  </a>

  <a href="/projects/neuro/voice-gender" class="card-link neuro">
    <div class="card">
      <h3>Voice Gender Effects on Consumer Preferences</h3>
      <p>Investigated how the gender and age of voices influence product evaluations and purchase decisions, using naturalistic stimuli, online behavioral tasks, and fNIRS neuroimaging.</p>
    </div>
  </a>

</div>

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
filterSelection('all');
</script>

<style>
/* 버튼 */
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

/* 카드 레이아웃 */
.project-cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  margin-top: 1.5rem;
}

.card-link {
  text-decoration: none;
  color: inherit;
  width: 48%;
  transition: transform 0.2s, box-shadow 0.2s;
}

.card-link:hover .card {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transform: translateY(-2px);
}

.card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 1.5rem;
  height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  overflow: hidden;
}

.card h3 {
  font-size: 1.1rem;
  margin-bottom: 0.6rem;
  line-height: 1.3;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.card p {
  font-size: 0.95rem;
  color: #555;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 6;
  -webkit-box-orient: vertical;
}

/* 모바일 대응 */
@media screen and (max-width: 768px) {
  .card-link {
    width: 100%;
    max-width: 95%;
  }
}
</style>
