<style>
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
  margin-bottom: 3rem;
}

.project-card {
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 0.75rem;
  padding: 1.25rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 6px 18px rgba(0,0,0,0.08);
}

.project-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: #0077aa;
  text-decoration: none;
}

.project-title:hover {
  text-decoration: underline;
}

.project-domain {
  font-size: 0.85rem;
  color: #777;
  margin-bottom: 0.5rem;
}

.project-desc {
  font-size: 0.95rem;
  color: #333;
  line-height: 1.4;
}
</style>

<div class="project-grid">

  <div class="project-card">
    <div class="project-domain">Social</div>
    <a href="/projects/social/self-prioritization" class="project-title">
      Self-prioritization effects on Nonspatial Working Memory
    </a>
    <p class="project-desc">
      Exploring how self-relevant cues influence working memory performance.
    </p>
  </div>

  <div class="project-card">
    <div class="project-domain">Memory</div>
    <a href="/projects/memory/group-bias" class="project-title">
      Group Bias on Perspective Taking in Non-Social Context
    </a>
    <p class="project-desc">
      Understanding group-related cognitive bias in neutral contexts.
    </p>
  </div>

  <div class="project-card">
    <div class="project-domain">Neuro</div>
    <a href="/projects/neuro/predicting-perspective" class="project-title">
      Predicting Perspective-Taking from Resting-State fMRI
    </a>
    <p class="project-desc">
      Using brain network features to predict cognitive empathy capacity.
    </p>
  </div>

</div>
