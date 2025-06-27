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
      <h3>Group Conformity Without Minds: Testing Visual Perspective Taking with Non-Social Stimuli</h3>
      <p>This study tests whether the group conformity effect in visual perspective taking depends on social reasoning or can be explained by ensemble coding. Non-social stimuli (triangles) replace avatars to isolate domain-general mechanisms.</p>
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
      <h3>Neural and Behavioral Effects of Voice Gender on Consumer Preferences</h3>
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
/* Filter Buttons */
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
  justify-content: space-between;
  gap: 1.5rem;
  margin-top: 1.5rem;
}

/* 카드 레이아웃 */
.card-link {
  width: 48%;
  text-decoration: none;
  color: inherit;
  transition: transform 0.2s, box-shadow 0.2s;
}
.card-link:hover .card {
  box-shadow: 0 6px 16px rgba(0, 123, 255, 0.25);
  transform: translateY(-3px);
}

/* 카드 디자인 */
.card {
  background: #f9fbff;
  border: 1px solid #cce0ff;
  border-radius: 12px;
  padding: 1.5rem;
  min-height: 260px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

/* 제목, 본문 */
.card h3 {
  font-size: 1.2rem;
  margin-bottom: 0.75rem;
  line-height: 1.3;
  color: #003366;
}

.card p {
  font-size: 0.95rem;
  color: #444;
  line-height: 1.5;
}

/* 모바일 대응 */
@media screen and (max-width: 768px) {
  .card-link {
    width: 100%;
    max-width: 95%;
  }
}
</style>
