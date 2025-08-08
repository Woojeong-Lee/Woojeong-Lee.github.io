---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<!-- Filter Buttons -->
<div style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button active" onclick="filterSelection('all', this)">All</button>
  <button class="filter-button" onclick="filterSelection('social', this)">Social</button>
  <button class="filter-button" onclick="filterSelection('memory', this)">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro', this)">Neuro</button>
</div>

<!-- Cards in a 2-column responsive grid -->
<div class="project-grid">

  <!-- Card 1 -->
  <article class="project-card social neuro">
    <figure class="project-figure">
      <img
        src="/assets/img/projects/SRE2_method1.png"
        loading="lazy"
        alt="Neural mechanisms project illustration"
      >
    </figure>
    <h3 class="project-title">(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</h3>
    <p class="project-text">
      How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA was used to identify brain regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then evaluated cross-condition generalization, testing whether classifiers trained on self-related judgments could decode president-related judgments.
    </p>
    <div class="project-actions">
      <button class="read-more" onclick="toggleMore(this)">Read more</button>
    </div>
  </article>

  <!-- Card 2 -->
  <article class="project-card social neuro">
    <h3 class="project-title">(Plan 2) How Self–Other Distinction Shapes Empathy</h3>
    <p class="project-text">
      Empathy—the ability to understand and share others’ emotions—is essential for social interaction. Effective empathy requires a clear self–other distinction. The right temporoparietal junction (rTPJ), a region implicated in this distinction, has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process, overlooking its complex structure. Contemporary theories of pain empathy differentiate between automatic, bottom-up simulation and controlled, top-down regulation depending on context. These distinct components may rely on separable neural mechanisms. To address this, we apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, providing a more nuanced understanding of how self–other distinction contributes to empathic accuracy.
    </p>
    <div class="project-actions">
      <button class="read-more" onclick="toggleMore(this)">Read more</button>
    </div>
  </article>

  <!-- Card 3 -->
  <article class="project-card social">
    <h3 class="project-title">(Plan 3) Group Conformity Without Minds</h3>
    <p class="project-text">
      Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking, observing that participants' judgments of a target avatar’s viewpoint were biased toward the average viewpoint of surrounding avatars. This interpretation relies on the assumption that participants adopt the avatar’s perspective. However, such bias may alternatively arise from domain-general mechanisms, such as ensemble coding of directional information, without necessarily invoking social reasoning. To test this possibility, the present study replicates the original paradigm using non-social stimuli—specifically, replacing avatars with isosceles triangles.
    </p>
    <div class="project-actions">
      <button class="read-more" onclick="toggleMore(this)">Read more</button>
    </div>
  </article>

  <!-- Card 4 -->
  <article class="project-card social">
    <figure class="project-figure">
      <img
        src="/assets/img/projects/CEP_method.png"
        loading="lazy"
        alt="Context and observer emotion on ensemble perception"
      >
    </figure>
    <h3 class="project-title">The Influence of Situational Context and Observer Emotion on Ensemble Emotion Perception</h3>
    <p class="project-text">
      Using naturalistic stimuli, the study investigated how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.
    </p>
    <div class="project-actions">
      <button class="read-more" onclick="toggleMore(this)">Read more</button>
    </div>
  </article>

  <!-- Card 5 -->
  <article class="project-card social memory">
    <figure class="project-figure">
      <img
        src="/assets/img/projects/SPE_method.png"
        loading="lazy"
        alt="Self-prioritization effects on working memory"
      >
    </figure>
    <h3 class="project-title">Self-Prioritization Effects on Nonspatial Working Memory</h3>
    <p class="project-text">
      Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. Although extensive studies have demonstrated the SPE on perception, findings regarding its effects on working memory (WM) remain inconsistent. Some studies reported improved WM speed and accuracy for self-associated items (Yin et al, 2019; Yin et al, 2019; Yin &amp; Chen, 2024), while others failed to find such an effect (Constable et al., 2019). The current study examined the SPE on shape-based WM across two experiments. Participants associated themselves and others with specific colors and completed a delayed matched-to-sample task (Experiment 1) or a reproduction task (Experiment 2). Results revealed that WM responses for colors were faster in the self condition than in the other, though no shape differences emerged.
      <a href="/data/analyzeSPE8VCS1.html" target="_blank" class="project-link">Experiment 1</a>
      <span aria-hidden="true">·</span>
      <a href="/data/analyzeSPE8VCS2.html" target="_blank" class="project-link">Experiment 2</a>
    </p>
    <div class="project-actions">
      <button class="read-more" onclick="toggleMore(this)">Read more</button>
    </div>
  </article>

  <!-- Card 6 -->
  <article class="project-card memory">
    <h3 class="project-title">The Impact of Meaningfulness on Visual Working Memory Across Spatial Boundaries</h3>
    <p class="project-text">
      The study examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.
    </p>
    <div class="project-actions">
      <button class="read-more" onclick="toggleMore(this)">Read more</button>
    </div>
  </article>

  <!-- Card 7 -->
  <article class="project-card neuro">
    <h3 class="project-title">The Influence of Speaker Gender and Age on Product Preference</h3>
    <p class="project-text">
      The study investigated how the gender and age of speakers affect product evaluations and purchase decisions, using naturalistic video stimuli and fNIRS.
    </p>
    <div class="project-actions">
      <button class="read-more" onclick="toggleMore(this)">Read more</button>
    </div>
  </article>

</div>

<script>
function filterSelection(category, el) {
  const items = document.querySelectorAll('.project-card');
  items.forEach(item => {
    item.style.display = (category === 'all' || item.classList.contains(category)) ? 'block' : 'none';
  });
  document.querySelectorAll('.filter-button').forEach(btn => btn.classList.remove('active'));
  if (el) el.classList.add('active');
}

function toggleMore(btn) {
  const card = btn.closest('.project-card');
  const text = card.querySelector('.project-text');
  const expanded = text.classList.toggle('expanded');
  btn.textContent = expanded ? 'Show less' : 'Read more';
}

// Initialize
filterSelection('all', document.querySelector('.filter-button'));
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
  transition: background 0.2s;
}
.filter-button:hover { background: #e0e0e0; }
.filter-button.active { background: #007acc; color: white; }

.project-link { color: #007acc; text-decoration: none; }
.project-link:hover { text-decoration: underline; }

/* Grid: two cards per row, 1 on small screens */
.project-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1.2rem;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* Card style */
.project-card {
  border: 1px solid #eee;
  border-radius: 10px;
  padding: 0; /* we'll space inner elements separately */
  background: #fff;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
  transition: box-shadow 0.3s, transform 0.2s, background-color 0.3s;
}
.project-card:hover { box-shadow: 0 2px 8px rgba(0,0,0,0.08); transform: translateY(-1px); }

.project-figure { margin: 0; }
.project-figure img { width: 100%; height: auto; display: block; border-radius: 10px 10px 0 0; }

.project-title { font-size: 1.05rem; font-weight: 700; margin: 0.9rem 1rem 0.4rem; }

.project-text {
  margin: 0 1rem;
  color: #444;
  line-height: 1.7;
  font-size: 1.02rem;
  display: -webkit-box;
  -webkit-line-clamp: 3; /* show 3 lines by default */
  -webkit-box-orient: vertical;
  overflow: hidden;
  position: relative;
}
.project-text.expanded { -webkit-line-clamp: unset; overflow: visible; }

.project-actions { display: flex; justify-content: flex-end; padding: 0.6rem 1rem 1rem; }
.read-more {
  padding: 0.45rem 0.8rem;
  font-size: 0.9rem;
  background: #007acc;
  color: #fff;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
.read-more:hover { filter: brightness(0.95); }

@media screen and (max-width: 900px) {
  .project-grid { grid-template-columns: 1fr; }
}
</style>
