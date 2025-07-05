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
  <!-- 예시: Social 연구 항목 -->
  <div class="project-item social">
    <h3>How Self–Other Distinction Shapes Empathy
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </h3>
    <div class="description">
Empathy, the ability to understand and share others’ emotions, is essential for social interaction. While often associated with emotional resonance, effective empathy also requires a clear distinction between self and other. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure. Contemporary theories of pain empathy differentiate between automatic, bottom-up simulation and controlled, top-down regulation depending on context. These distinct components may rely on separable neural mechanisms. To address this, we apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, providing a more nuanced understanding of how self–other distinction contributes to empathic accuracy.
    </div>
  </div>

  <div class="project-item social">
    <h3>Group Conformity Without Minds
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </h3>
    <div class="description">
      To test whether visual perspective conformity arises from social cognition or domain-general mechanisms, this study replicates a group conformity task with non-social stimuli, using triangles instead of avatars to remove mentalizing cues.
    </div>
  </div>

  <div class="project-item social">
    <h3>The Influence of Situational Context and Observer Emotion on Ensemble Perception of Crowd Emotion
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </h3>
    <div class="description">
      Using naturalistic stimuli, we investigate how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.
    </div>
  </div>

  <div class="project-item memory">
    <h3>Self-Prioritization Effects on Nonspatial Working Memory
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </h3>
    <div class="description">
      This study examined whether self-prioritization enhances working memory for object features. Results revealed feature-specific benefits for self-associated colors but not for shape memory accuracy.
    </div>
  </div>

  <div class="project-item memory">
    <h3>Does Meaningfulness Enhance Working Memory Across Spatial Locations?
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </h3>
    <div class="description">
      We examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.
    </div>
  </div>

  <div class="project-item neuro">
    <h3>Resting-State fMRI Predictors of Theory of Mind Capacity
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </h3>
    <div class="description">
      We examined whether individual differences in perspective-taking ability can be predicted from whole-brain resting-state connectivity using HCP data and SVM modeling.
    </div>
  </div>

  <div class="project-item neuro">
    <h3>Voice Gender Effects on Consumer Preferences
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </h3>
    <div class="description">
      We investigated how the gender and age of voices influence product evaluations and purchase decisions, using naturalistic stimuli, online behavioral tasks, and fNIRS neuroimaging.
    </div>
  </div>
</div>

<script>
function filterSelection(category) {
  const items = document.querySelectorAll('.project-item');
  items.forEach(item => {
    item.style.display = (category === 'all' || item.classList.contains(category)) ? 'block' : 'none';
  });
}

function toggleDescription(button) {
  const desc = button.parentElement.nextElementSibling;
  const isVisible = desc.style.display === 'block';
  desc.style.display = isVisible ? 'none' : 'block';
  button.textContent = isVisible ? 'Show more' : 'Show less';
}

filterSelection('all');
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

.project-list {
  max-width: 800px;
  margin: 2rem auto;
}

.project-item {
  border-bottom: 1px solid #ccc;
  padding: 1rem 0;
}

.project-item h3 {
  font-size: 1.1rem;
  margin: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.toggle-button {
  margin-left: 1rem;
  font-size: 0.8rem;
  padding: 0.2rem 0.6rem;
  border: none;
  background: #eee;
  border-radius: 4px;
  cursor: pointer;
}
.toggle-button:hover {
  background: #ddd;
}

.description {
  display: none;
  margin-top: 0.5rem;
  color: #555;
  font-size: 0.95rem;
  line-height: 1.4;
}

/* Mobile */
@media screen and (max-width: 600px) {
  .project-item h3 {
    flex-direction: column;
    align-items: flex-start;
  }

  .toggle-button {
    margin-top: 0.5rem;
  }
}
</style>
