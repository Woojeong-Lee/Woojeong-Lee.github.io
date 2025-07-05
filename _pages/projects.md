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

<div class="project-cards">
  <a href="/projects/social/empathy_rtpj" class="card-link social">
    <div class="card">
      <h3>How Self–Other Distinction Shapes Empathy</h3>
      <p>Empathy, the ability to understand and share others’ emotions, is essential for social interaction. While often associated with emotional resonance, effective empathy also requires a clear distinction between self and other. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure. Contemporary theories of pain empathy differentiate between automatic, bottom-up simulation and controlled, top-down regulation depending on context. These distinct components may rely on separable neural mechanisms. To address this, we apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, providing a more nuanced understanding of how self–other distinction contributes to empathic accuracy.</p>
    </div>
  </a>

  <a href="/projects/social/groupbias_perspectivetaking" class="card-link social">
    <div class="card">
      <h3>Group Conformity Without Minds</h3>
      <p>Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking, observing that participants' judgments of a target avatar’s viewpoint were biased toward the average viewpoint of surrounding avatars. This interpretation relies on the assumption that participants adopt the avatar’s perspective. However, such bias may alternatively arise from domain-general mechanisms, such as ensemble coding of directional information, without necessarily invoking social reasoning. To test this possibility, the present study replicates the original paradigm using non-social stimuli—specifically, replacing avatars with isosceles triangles. This manipulation is intended to eliminate any motivation for participants to attribute mental states to the stimuli, while preserving the directional cues present in the original task. If the effect is replicated under these non-social conditions, it would suggest that the observed bias reflects ensemble-based spatial coding, rather than social-cognitive processes.</p>
    </div>
  </a>

  <a href="/projects/social/cep" class="card-link social">
    <div class="card">
      <h3>The Influence of Situational Context and Observer Emotion on Ensemble Perception of Crowd Emotion</h3>
      <p>Using naturalistic stimuli, we investigate how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.</p>
    </div>
  </a>

  <a href="/projects/memory/spe8vcs" class="card-link memory">
    <div class="card">
      <h3>Self-Prioritization Effects on Nonspatial Working Memory</h3>
      <p>Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. Although extensive studies have demonstrated the SPE on perception, findings regarding its effects on working memory (WM) remain inconsistent. Some studies reported improved WM speed and accuracy for self-associated items (Yin et al., 2019; Yin et al., 2019: Yin & Chen, 2024), while others failed to find such an effect (Constable et al., 2019). Investigating the SPE on WM is important for understanding egocentric biases in cognition, since maintaining and evaluating information in WM is fundamental to decision-making and cognitive control (Baddeley, 2003; D’Esposito & Postle, 2015).
The current study examined the SPE on shape-based WM across two experiments. Participants associated themselves and others with specific colors and completed a delayed matched-to-sample task (Experiment 1) or a reproduction task (Experiment 2) for the shapes of objects presented in each color. Results revealed no difference in WM responses for shapes between the self and other conditions, but WM responses for colors were faster in the self condition than in the other. Therefore, the current study limits the scope of self-prioritization to self-associated features, rather than to entire objects that contain those features.
</p>
    </div>
  </a>

  <a href="/projects/memory/meaningfulness" class="card-link memory">
    <div class="card">
      <h3>Does Meaningfulness Enhance Working Memory Across Spatial Locations?</h3>
      <p>We examined meaningful objects facilitate the encoding of spatially distal features in visual working memory.</p>
    </div>
  </a>

  <a href="/projects/neuro/predicting-empathy" class="card-link neuro">
    <div class="card">
      <h3>Resting-State fMRI Predictors of Theory of Mind Capacity</h3>
      <p>I examined whether individual differences in perspective-taking ability can be predicted from whole-brain resting-state connectivity using HCP data and SVM modeling.</p>
    </div>
  </a>

  <a href="/projects/neuro/voice-gender" class="card-link neuro">
    <div class="card">
      <h3>Voice Gender Effects on Consumer Preferences</h3>
      <p>We investigated how the gender and age of voices influence product evaluations and purchase decisions, using naturalistic stimuli, online behavioral tasks, and fNIRS neuroimaging.</p>
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

/* Card grid layout */
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

.card-link:hover h3,
.card-link:hover p {
  text-decoration: none;
  color: inherit;
}

.card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 0.8rem 1rem;
  height: 310px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  overflow: hidden;
}

.card h3 {
  font-size: 1.1rem;
  margin-bottom: 0.6rem;
  line-height: 1.35;
  word-break: break-word;
  overflow-wrap: break-word;
}

.card p {
  font-size: 0.95rem;
  color: #555;
  line-height: 1.4;
  display: -webkit-box;
  -webkit-line-clamp: 6;       /* 최대 줄 수 */
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: normal;
}

/* Mobile responsiveness */
@media screen and (max-width: 768px) {
  .card-link {
    width: 100%;
    max-width: 95%;
  }
}
</style>
