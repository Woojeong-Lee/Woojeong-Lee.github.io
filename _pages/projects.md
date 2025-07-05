---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<!-- 필터 버튼 -->
<div style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button" onclick="filterSelection('all')">All</button>
  <button class="filter-button" onclick="filterSelection('social')">Social</button>
  <button class="filter-button" onclick="filterSelection('memory')">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro')">Neuro</button>
</div>

<!-- 연구 항목 리스트 -->
<div class="project-list">

  <!-- Example 1 -->
  <div class="project-item social">
    <div class="project-header">
      <h3>How Self–Other Distinction Shapes Empathy</h3>
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="description">
      This study uses rTPJ stimulation and multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias, revealing how self–other distinction contributes to empathic accuracy.
    </div>
  </div>

  <!-- Example 2 -->
  <div class="project-item social">
    <div class="project-header">
      <h3>Group Conformity Without Minds</h3>
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="description">
      Replicating prior visual perspective-taking tasks with non-social stimuli (triangles), this study tests whether group conformity effects arise from domain-general spatial coding rather than social mentalizing.
    </div>
  </div>

  <!-- Example 3 -->
  <div class="project-item social">
    <div class="project-header">
      <h3>The Influence of Situational Context and Observer Emotion on Ensemble Perception of Crowd Emotion</h3>
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="description">
      Using naturalistic facial crowds, we examined how context and observer emotions shape perceived ensemble emotions, revealing top-down modulation of group emotion perception.
    </div>
  </div>

  <!-- Example 4 -->
  <div class="project-item memory">
    <div class="project-header">
      <h3>Self-Prioritization Effects on Nonspatial Working Memory</h3>
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="description">
      Across two experiments, we found that self-association facilitates memory for color features but not for shapes, suggesting a feature-specific rather than object-level self-prioritization in working memory.
    </div>
  </div>

  <!-- Example 5 -->
  <div class="project-item memory">
    <div class="project-header">
      <h3>Does Meaningfulness Enhance Working Memory Across Spatial Locations?</h3>
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="description">
      This study tested whether meaningful object cues enhance memory for spatially separated features, using diffeomorphic stimuli and online experiments to isolate the effect of semantic content.
    </div>
  </div>

  <!-- Example 6 -->
  <div class="project-item neuro">
    <div class="project-header">
      <h3>Resting-State fMRI Predictors of Theory of Mind Capacity</h3>
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="description">
      We used HCP resting-state fMRI data and SVM modeling to identify connectivity patterns predictive of individual differences in perspective-taking ability, focusing on theory of mind regions.
    </div>
  </div>

  <!-- Example 7 -->
  <div class="project-item neuro">
    <div class="project-header">
      <h3>Voice Gender Effects on Consumer Preferences</h3>
      <button class="toggle-button" onclick="toggleDescription(this)">Show more</button>
    </div>
    <div class="description">
      Using naturalistic auditory stimuli and fNIRS, this study explored how voice gender and age modulate product evaluations and purchase intentions in consumer decision-making contexts.
    </div>
  </div>

</div>

<!-- CSS -->
<style>
.project-list {
  max-width: 800px;
  margin: 2rem auto;
  padding: 0 1rem;
}
.project-item {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  margin-bottom: 1rem;
  padding: 1rem 1.2rem;
  background-color: #fff;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
}
.project-item:hover {
  box-shadow: 0 3px 12px rgba(0, 0, 0, 0.08);
}
.project-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1rem;
}
.project-header h3 {
  margin: 0;
  font-size: 1.05rem;
  font-weight: 600;
  flex: 1;
  color: #333;
}
.toggle-button {
  font-size: 0.85rem;
  pad
