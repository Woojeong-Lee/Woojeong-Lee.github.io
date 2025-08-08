---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<!-- 필터 버튼 -->
<div class="project-filters" style="text-align:center; margin-bottom: 2rem;">
  <button class="filter-button active" onclick="filterSelection('all', this)">All</button>
  <button class="filter-button" onclick="filterSelection('social', this)">Social</button>
  <button class="filter-button" onclick="filterSelection('memory', this)">Memory</button>
  <button class="filter-button" onclick="filterSelection('neuro', this)">Neuro</button>
</div>

<!-- 프로젝트 리스트 -->
<div class="projects">

  <!-- Plan 1 -->
  <section class="project-row social neuro">
    <div class="project-image">
      <a href="/projects/plan1">
        <img src="/assets/img/projects/SRE2_method1.png" alt="Plan 1 image">
      </a>
    </div>
    <div class="project-text">
      <h2><a href="/projects/plan1">(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</a></h2>
      <p>
        How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA identified regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then tested cross-condition generalization to see whether classifiers trained on self-related judgments decode president-related judgments.
      </p>
    </div>
  </section>

  <!-- Plan 2 -->
  <section class="project-row social neuro">
    <div class="project-image">
      <!-- 이미지 없으면 비워둬도 됨 -->
    </div>
    <div class="project-text">
      <h2><a href="/projects/plan2">(Plan 2) How Self–Other Distinction Shapes Empathy</a></h2>
      <p>
        We use multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias. We then examine how rTPJ stimulation modulates each component, refining how self–other distinction contributes to empathic accuracy.
      </p>
    </div>
  </section>

  <!-- Plan 3 -->
  <section class="project-row social">
    <div class="project-image">
      <a href="/projects/plan3">
        <img src="/assets/img/projects/triangle.png" alt="Plan 3 image">
      </a>
    </div>
    <div class="project-text">
      <h2><a href="/projects/plan3">(Plan 3) Group Conformity Without Minds</a></h2>
      <p>
        This study replicates the original group conformity paradigm in visual perspective taking, replacing avatars with non-social stimuli (isosceles triangles) to test whether effects arise from domain-general mechanisms like ensemble coding.
      </p>
    </div>
  </section>

</div>

<!-- JS -->
<script>
function filterSelection(category, el) {
  const items = document.querySelectorAll('.project-row');
  items.forEach(item => {
    item.style.display = (category === 'all' || item.classList.contains(category)) ? 'grid' : 'none';
  });
  document.querySelectorAll('.filter-button').forEach(btn => btn.classList.remove('active'));
  el.classList.add('active');
}
</script>

<!-- CSS -->
<style>
/* 필터 버튼 - 원래 스타일 */
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
.filter-button.active {
  background: #007acc;
  color: white;
}

/* 전체 컨테이너 - 여백 줄임 */
.projects {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 1rem; /* 좌우 여백 최소화 */
}

/* 프로젝트 행 */
.project-row {
  display: grid;
  grid-template-columns: 39% 61%; /* 이미지:글 비율 */
  gap: 1.5rem;
  padding: 1.25rem 0;
  border-bottom: 1px solid #e9edf3;
  align-items: start;
  transition: transform 0.15s ease, box-shadow 0.15s ease;
}
.project-row:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
}

/* 이미지 */
.project-image img {
  width: 100%;
  height: auto;
  object-fit: contain;
  border-radius: 6px;
}

/* 텍스트 */
.project-text h2 {
  margin: 0 0 .4rem;
  font-weight: 600;
  font-size: clamp(1rem, 0.55vw + 0.95rem, 1.2rem); /* 제목 조금 줄임 */
  line-height: 1.25;
}
.project-text a {
  text-decoration: none;
  color: inherit; /* hover 시 색상 안 바뀜 */
}
.project-text a:hover {
  text-decoration: underline;
}
.project-text p {
  margin-top: 0.5rem;
  font-size: 1.05rem;
  color: #444;
  line-height: 1.6;
}
</style>
