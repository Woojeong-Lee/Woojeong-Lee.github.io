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
    <p>Empathy, the ability to understand and share others’ emotions, is essential for social interaction. While often associated with emotional resonance, effective empathy also requires a clear distinction between self and other. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure. Contemporary theories of pain empathy differentiate between automatic, bottom-up simulation and controlled, top-down regulation depending on context. These distinct components may rely on separable neural mechanisms. To address this, we apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, providing a more nuanced understanding of how self–other distinction contributes to empathic accuracy.</p>
  </details>

  <details class="project-item social">
    <summary>Group Conformity Without Minds</summary>
    <p>Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking, observing that participants' judgments of a target avatar’s viewpoint were biased toward the average viewpoint of surrounding avatars. This interpretation relies on the assumption that participants adopt the avatar’s perspective. However, such bias may alternatively arise from domain-general mechanisms, such as ensemble coding of directional information, without necessarily invoking social reasoning. To test this possibility, the present study replicates the original paradigm using non-social stimuli—specifically, replacing avatars with isosceles triangles. This manipulation is intended to eliminate any motivation for participants to attribute mental states to the stimuli, while preserving the directional cues present in the original task. If the effect is replicated under these non-social conditions, it would suggest that the observed bias reflects ensemble-based spatial coding, rather than social-cognitive processes.</p>
  </details>

  <details class="project-item social">
    <summary>The Influence of Situational Context and Observer Emotion on Ensemble Perception of Crowd Emotion</summary>
    <p>Using naturalistic stimuli, we investigate how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.</p>
  </details>

  <details class="project-item memory">
    <summary>Self-Prioritization Effects on Nonspatial Working Memory</summary>
    <p>Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. Although extensive studies have demonstrated the SPE on perception, findings regarding its effects on working memory (WM) remain inconsistent. Some studies reported improved WM speed and accuracy for self-associated items (Yin et al., 2019; Yin et al., 2019: Yin & Chen, 2024), while others failed to find such an effect (Constable et al., 2019). Investigating the SPE on WM is important for understanding egocentric biases in cognition, since maintaining and evaluating information in WM is fundamental to decision-making and cognitive control (Baddeley, 2003; D’Esposito & Postle, 2015). The current study examined the SPE on shape-based WM across two experiments. Participants associated themselves and others with specific colors and completed a delayed matched-to-sample task (Experiment 1) or a reproduction task (Experiment 2) for the shapes of objects presented in each color. Results revealed no difference in WM responses for shapes between the self and other conditions, but WM responses for colors were faster in the self condition than in the other. Therefore, the current study limits the scope of self-prioritization to self-associated features, rather than to entire objects that contain those features.</p>
  </details>

  <details class="project-item memory">
    <summary>Does Meaningfulness Enhance Working Memory Across Spatial Locations?</summary>
    <p>We examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.</p>
  </details>

  <details class="project-item neuro">
    <summary>Resting-State fMRI Predictors of Theory of Mind Capacity</summary>
    <p>I examined whether individual differences in perspective-taking ability can be predicted from whole-brain resting-state connectivity using HCP data and SVM modeling.</p>
  </details>

  <details class="project-item neuro">
    <summary>Voice Gender Effects on Consumer Preferences</summary>
    <p>We investigated how the gender and age of voices influence product evaluations and purchase decisions, using naturalistic stimuli, online behavioral tasks, and fNIRS neuroimaging.</p>
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

/* Project list */
.project-list {
  max-width: 860px;
  margin: 0 auto;
  padding: 0 1rem;
}

.project-item {
  border-bottom: 1px solid #ddd;
  padding: 0.8rem 0;
}

/* Title row with triangle icon */
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

/* Change icon when open */
.project-item[open] summary::before {
  content: '▼';
  transform: rotate(0deg);
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
