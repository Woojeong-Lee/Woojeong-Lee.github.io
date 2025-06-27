---
title: ""
layout: single
permalink: /research/
header:
  show_title: false
---

<style>
  .tabs {
    display: flex;
    justify-content: center;
    margin: 2rem 0 1rem;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .tab-button {
    font-size: 1rem;
    padding: 0.4rem 1rem;
    border: 1px solid #ccc;
    background: #f5f5f5;
    border-radius: 6px;
    cursor: pointer;
  }

  .tab-button.active {
    background: #333;
    color: #fff;
    border-color: #333;
  }

  .project-list {
    margin-top: 2rem;
    line-height: 1.6;
  }

  .project-item {
    margin-bottom: 1.5rem;
  }

  .project-title {
    font-weight: bold;
    font-size: 1.05rem;
    margin-bottom: 0.25rem;
  }

  .hidden {
    display: none;
  }
</style>

<div class="tabs">
  <div class="tab-button active" onclick="switchTab('all')">All</div>
  <div class="tab-button" onclick="switchTab('social')">Social</div>
  <div class="tab-button" onclick="switchTab('memory')">Memory</div>
  <div class="tab-button" onclick="switchTab('neuro')">Neuro</div>
</div>

<!-- All -->
<div id="all" class="project-list">
  <div class="project-item">
    <div class="project-title"><a href="#">(2024) Predicting Empathy from fMRI</a></div>
    <div>Resting-state brain network data used to predict cognitive empathy scores.</div>
  </div>
  <div class="project-item">
    <div class="project-title"><a href="#">(2023) Self-prioritization in Working Memory</a></div>
    <div>How self-relevant information enhances nonspatial memory performance.</div>
  </div>
  <!-- 더 많은 프로젝트 추가 가능 -->
</div>

<!-- Social -->
<div id="social" class="project-list hidden">
  <div class="project-item">
    <div class="project-title"><a href="#">Self-prioritization in Working Memory</a></div>
    <div>Investigating the role of self-cues in memory processes.</div>
  </div>
</div>

<!-- Memory -->
<div id="memory" class="project-list hidden">
  <div class="project-item">
    <div class="project-title"><a href="#">Group Bias in Perspective Taking</a></div>
    <div>Memory-related bias and neutral contexts in social cognition.</div>
  </div>
</div>

<!-- Neuro -->
<div id="neuro" class="project-list hidden">
  <div class="project-item">
    <div class="project-title"><a href="#">Predicting Empathy from fMRI</a></div>
    <div>Resting-state network features used in neuro-based modeling.</div>
  </div>
</div>

<script>
  function switchTab(tabId) {
    document.querySelectorAll('.project-list').forEach(div => div.classList.add('hidden'));
    document.getElementById(tabId).classList.remove('hidden');

    document.querySelectorAll('.tab-button').forEach(btn => btn.classList.remove('active'));
    event.target.classList.add('active');
  }
</script>
