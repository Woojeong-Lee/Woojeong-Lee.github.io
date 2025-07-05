---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<div style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button active" onclick="filterSelection('all', this)">All</button>
  <button class="filter-button" onclick="filterSelection('social', this)">Social</button>
  <button class="filter-button" onclick="filterSelection('memory', this)">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro', this)">Neuro</button>
</div>

<div class="project-list">
  <details class="project-item social">
    <summary><span class="arrow"></span> How Self–Other Distinction Shapes Empathy</summary>
    <div class="project-content">
      <p>Empathy, the ability to understand and share others’ emotions, is essential for social interaction. While often associated with emotional resonance, effective empathy also requires a clear distinction between self and other. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure...</p>
    </div>
  </details>

  <details class="project-item memory">
    <summary><span class="arrow"></span> Self-Prioritization Effects on Nonspatial Working Memory</summary>
    <div class="project-content">
      <p>Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately...<br>
      The current study examined...<a href="/data/analyzeSPE8VCS1.html" target="_blank">(Experiment 1)</a> or <a href="/data/analyzeSPE8VCS2.html" target="_blank">(Experiment 2)</a> for the shapes...</p>
    </div>
  </details>

  <!-- More details here -->
</div>

<script>
function filterSelection(category, button) {
  const items = document.querySelectorAll('.project-item');
  items.forEach(item => {
    item.style.display = (category === 'all' || item.classList.contains(category)) ? 'block' : 'none';
  });
  document.querySelectorAll('.filter-button').forEach(btn => btn.classList.remove('active'));
  if (button) button.classList.add('active');
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
  transition: background 0.2s, color 0.2s;
}
.filter-button:hover, .filter-button.active {
  background: #007acc;
  color: white;
}

.project-list {
  max-width: 860px;
  margin: 0 auto;
  padding: 0 1rem;
}

.project-item {
  border-bottom: 1px solid #ddd;
  padding: 0.8rem 0;
}

.project-item summary {
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  outline: none;
  list-style: none;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.project-item summary::marker {
  content: "";
}

.arrow {
  display: inline-block;
  width: 0.6em;
  height: 0.6em;
  border-right: 2px solid #555;
  border-bottom: 2px solid #555;
  transform: rotate(45deg);
  transition: transform 0.3s ease;
}

.project-item[open] .arrow {
  transform: rotate(135deg);
}

.project-content {
  background: #f9f9f9;
  border-radius: 8px;
  padding: 1rem;
  margin-top: 0.5rem;
  border: 1px solid #eee;
}

.project-content p {
  margin: 0;
  font-size: 0.95rem;
  color: #444;
  line-height: 1.5;
}

@media screen and (max-width: 768px) {
  .project-item summary {
    font-size: 0.95rem;
  }
  .project-content p {
    font-size: 0.9rem;
  }
}
</style>
