---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<div class="project-list">

  <div class="project-item social neuro">
    <div class="project-image">
      <img src="/assets/img/projects/SRE2_method1.png" alt="Plan 1 image">
    </div>
    <div class="project-text">
      <h3>(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</h3>
      <p>
        How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA was used to identify brain regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then evaluated cross-condition generalization, testing whether classifiers trained on self-related judgments could decode president-related judgments.
      </p>
    </div>
  </div>

  <div class="project-item social neuro">
    <div class="project-text">
      <h3>(Plan 2) How Self–Other Distinction Shapes Empathy</h3>
      <p>
        Empathy—the ability to understand and share others’ emotions—is essential for social interaction. Effective empathy requires a clear self–other distinction. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure. Contemporary theories of pain empathy differentiate between automatic, bottom-up simulation and controlled, top-down regulation depending on context. These distinct components may rely on separable neural mechanisms. To address this, we apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, providing a more nuanced understanding of how self–other distinction contributes to empathic accuracy.
      </p>
    </div>
  </div>

  <div class="project-item social">
    <div class="project-text">
      <h3>(Plan 3) Group Conformity Without Minds</h3>
      <p>
        Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking, observing that participants' judgments of a target avatar’s viewpoint were biased toward the average viewpoint of surrounding avatars. This interpretation relies on the assumption that participants adopt the avatar’s perspective. However, such bias may alternatively arise from domain-general mechanisms, such as ensemble coding of directional information, without necessarily invoking social reasoning. To test this possibility, the present study replicates the original paradigm using non-social stimuli—specifically, replacing avatars with isosceles triangles.
      </p>
    </div>
  </div>

  <div class="project-item social">
    <div class="project-image">
      <img src="/assets/img/projects/CEP_method.png" alt="Ensemble Emotion Perception">
    </div>
    <div class="project-text">
      <h3>The Influence of Situational Context and Observer Emotion on Ensemble Emotion Perception</h3>
      <p>
        Using naturalistic stimuli, the study investigated how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.
      </p>
    </div>
  </div>

  <div class="project-item social memory">
    <div class="project-image">
      <img src="/assets/img/projects/SPE_method.png" alt="Self-Prioritization Effects">
    </div>
    <div class="project-text">
      <h3>Self-Prioritization Effects on Nonspatial Working Memory</h3>
      <p>
        Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. Although extensive studies have demonstrated the SPE on perception, findings regarding its effects on working memory (WM) remain inconsistent. Some studies reported improved WM speed and accuracy for self-associated items (Yin et al, 2019; Yin et al, 2019; Yin &amp; Chen, 2024), while others failed to find such an effect (Constable et al., 2019).
        <br>The current study examined the SPE on shape-based WM across two experiments. Participants associated themselves and others with specific colors and completed a delayed matched-to-sample task
        <a href="/data/analyzeSPE8VCS1.html" target="_blank" class="project-link">(Experiment 1)</a>
        or a reproduction task
        <a href="/data/analyzeSPE8VCS2.html" target="_blank" class="project-link">(Experiment 2)</a>.
        Results revealed that WM responses for colors were faster in the self condition than in the other, though no shape differences emerged.
      </p>
    </div>
  </div>

  <div class="project-item memory">
    <div class="project-text">
      <h3>The Impact of Meaningfulness on Visual Working Memory Across Spatial Boundaries</h3>
      <p>
        The study examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.
      </p>
    </div>
  </div>

  <div class="project-item neuro">
    <div class="project-text">
      <h3>The Influence of Speaker Gender and Age on Product Preference</h3>
      <p>
        The study investigated how the gender and age of speakers affect product evaluations and purchase decisions, using naturalistic video stimuli and fNIRS.
      </p>
    </div>
  </div>

</div>

<style>
.project-list {
  max-width: 100%;
  margin: 0 auto;
  padding: 0 1rem; /* 좌우 여백 최소화 */
}

.project-item {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  gap: 1.5rem;
  margin-bottom: 2rem;
  border: 1px solid #eee;
  border-radius: 8px;
  padding: 1rem;
  background: #fff;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
}

.project-image img {
  max-width: 320px;
  width: 100%;
  height: auto;
  border-radius: 6px;
  display: block;
}

.project-text {
  flex: 1;
  min-width: 250px;
}

.project-text h3 {
  margin: 0 0 0.5rem;
  font-size: 1.2rem;
  font-weight: 600;
  color: #007acc;
}

.project-text p {
  font-size: 1.05rem;
  color: #444;
  line-height: 1.6;
}

.project-link {
  color: #007acc;
  text-decoration: none;
}
.project-link:hover {
  text-decoration: underline;
}

@media screen and (max-width: 768px) {
  .project-item {
    flex-direction: column;
    align-items: center;
  }
  .project-image img {
    max-width: 100%;
  }
}
</style>
