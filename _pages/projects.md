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
    <div class="project-content">
      <p><strong>Summary:</strong> Empathy, the ability to understand and share others’ emotions, is essential for social interaction. While often associated with emotional resonance, effective empathy also requires a clear distinction between self and other. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure. Contemporary theories of pain empathy differentiate between automatic, bottom-up simulation and controlled, top-down regulation depending on context. These distinct components may rely on separable neural mechanisms. To address this, we apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, providing a more nuanced understanding of how self–other distinction contributes to empathic accuracy.</p>
    </div>
  </details>

  <details class="project-item social">
    <summary>Group Conformity Without Minds</summary>
    <div class="project-content">
      <p><strong>Summary:</strong> Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking, observing that participants' judgments of a target avatar’s viewpoint were biased toward the average viewpoint of surrounding avatars. This interpretation relies on the assumption that participants adopt the avatar’s perspective. However, such bias may alternatively arise from domain-general mechanisms, such as ensemble coding of directional information, without necessarily invoking social reasoning. To test this possibility, the present study replicates the original paradigm using non-social stimuli—specifically, replacing avatars with isosceles triangles. This manipulation is intended to eliminate any motivation for participants to attribute mental states to the stimuli, while preserving the directional cues present in the original task.</p>
    </div>
  </details>

  <details class="project-item memory">
    <summary>Self-Prioritization Effects on Nonspatial Working Memory</summary>
    <div class="project-content">
      <p><strong>Summary:</strong> Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. Although extensive studies have demonstrated the SPE on perception, findings regarding its effects on working memory (WM) remain inconsistent. Some studies reported improved WM speed and accuracy for self-associated items (Yin et al., 2019; Yin et al., 2019: Yin &amp; Chen, 2024), while others failed to find such an effect (Constable et al., 2019). Investigating the SPE on WM is important for understanding egocentric biases in cognition, since maintaining and evaluating information in WM is fundamental to decision-making and cognitive control (Baddeley, 2003; D’Esposito &amp; Postle, 2015).</p>

      <p>The current study examined the SPE on shape-based WM across two experiments. Participants associated themselves and others with specific colors and completed a delayed matched-to-sample task 
      <a href="/data/analyzeSPE8VCS1.html" target="_blank">(Experiment 1)</a> 
      or a reproduction task 
      <a href="/data/analyzeSPE8VCS2.html" target="_blank">(Experiment 2)</a> 
      for the shapes of objects presented in each color. Results revealed no difference in WM responses for shapes between the self and other conditions, but WM responses for colors were faster in the self condition than in the other.</p>
    </div>
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
/* Buttons */
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

/* Layout */
.project-list {
  max-width: 800px;
  margin: 0 auto;
  padding: 0 1rem;
}
.project-item {
  border-bottom: 1px solid #ddd;
  padding: 1rem 0;
}

/* Summary */
.project-item summary {
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  display: flex;
  align-items: center;
  padding-left: 1.2rem;
  position: relative;
}
.project-item summary::before {
  content: '▶';
  position: absolute;
  left: 0;
  transition: transform 0.2s ease;
}
.project-item[open] summary::before {
  content: '▼';
}

/* Paragraphs */
.project-content p {
  margin-top: 0.6rem;
  margin-left: 1.2rem;
  font-size: 0.95rem;
  color: #444;
  line-height: 1.6;
}

/* Links */
.project-content a {
  color: #007acc;
  text-decoration: none;
}
.project-content a:hover {
  text-decoration: underline;
}
</style>
