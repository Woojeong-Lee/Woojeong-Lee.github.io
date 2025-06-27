---
title: ""
layout: single
permalink: /research/
header:
  show_title: false
paginate: false
previous_next: false 
---

<div style="margin-top: 2em;">
  <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; margin-bottom: 2em;">
    <button class="tab-button" onclick="showTab('all')">All</button>
    <button class="tab-button" onclick="showTab('social')">Social</button>
    <button class="tab-button" onclick="showTab('memory')">Memory</button>
    <button class="tab-button" onclick="showTab('neuro')">Neuro</button>
  </div>

  <!-- All Tab -->
  <div class="tab-content" id="tab-all">
    <ul>
      <li><a href="/projects/self-prioritization">Self-Prioritization Effects on Nonspatial Working Memory</a></li>
      <li><a href="/projects/meaningfulness-memory">Meaningfulness in Working Memory</a></li>
      <li><a href="/projects/group-bias">Group Bias on Perspective Taking in Non-Social Context</a></li>
      <li><a href="/projects/context-emotion">Context Processing in Ensemble Emotion Perception</a></li>
      <li><a href="/projects/social-dimension">Dimension Underlying the Perception of Social Interaction</a></li>
      <li><a href="/projects/perspective-fmri">Predicting Perspective-Taking Ability from Resting-State fMRI</a></li>
      <li><a href="/projects/voice-gender">The Effect of Voice Gender on Product Preference</a></li>
    </ul>
  </div>

  <!-- Social Tab -->
  <div class="tab-content" id="tab-social" style="display:none;">
    <ul>
      <li><a href="/projects/self-prioritization">Self-Prioritization Effects on Nonspatial Working Memory</a></li>
      <li><a href="/projects/meaningfulness-memory">Meaningfulness in Working Memory</a></li>
      <li><a href="/projects/group-bias">Group Bias on Perspective Taking in Non-Social Context</a></li>
    </ul>
  </div>

  <!-- Memory Tab -->
  <div class="tab-content" id="tab-memory" style="display:none;">
    <ul>
      <li><a href="/projects/context-emotion">Context Processing in Ensemble Emotion Perception</a></li>
      <li><a href="/projects/social-dimension">Dimension Underlying the Perception of Social Interaction</a></li>
    </ul>
  </div>

  <!-- Neuro Tab -->
  <div class="tab-content" id="tab-neuro" style="display:none;">
    <ul>
      <li><a href="/projects/perspective-fmri">Predicting Perspective-Taking Ability from Resting-State fMRI</a></li>
      <li><a href="/projects/voice-gender">The Effect of Voice Gender on Product Preference</a></li>
    </ul>
  </div>
</div>

<script>
  function showTab(tabName) {
    const tabs = document.querySelectorAll(".tab-content");
    tabs.forEach(tab => tab.style.display = "none");

    const selected = document.getElementById("tab-" + tabName);
    if (selected) selected.style.display = "block";
  }

  // 초기 탭 설정
  document.addEventListener("DOMContentLoaded", function () {
    showTab("all");
  });
</script>

<style>
  .tab-button {
    background-color: #f0f0f0;
    border: none;
    padding: 0.6em 1em;
    cursor: pointer;
    font-size: 1em;
    border-radius: 6px;
  }
  .tab-button:hover {
    background-color: #e0e0e0;
  }
  .tab-content ul {
    list-style: none;
    padding-left: 0;
  }
  .tab-content li {
    margin-bottom: 0.75em;
  }
</style>
