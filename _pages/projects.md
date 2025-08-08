---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<!-- START: Projects (Full-bleed, Image Left / Text Right) -->
<div class="projects">

  <!-- Plan 1 -->
  <section class="project-row">
    <div class="project-image">
      <img src="/assets/img/projects/SRE2_method1.png" alt="Plan 1 image">
    </div>
    <div class="project-text">
      <h2>(Plan 1) Neural Mechanisms of Simulating Others’ Thoughts</h2>
      <p>
        How does the brain represent another person’s thoughts? Participants judged themselves and the president from both their own and a close friend’s perspective. Whole-brain searchlight RSA was used to identify brain regions whose activity patterns capture a friend’s mental perspective. ROI-based MVPA then evaluated cross-condition generalization, testing whether classifiers trained on self-related judgments could decode president-related judgments.
      </p>
    </div>
  </section>

  <!-- Plan 2 (text only) -->
  <section class="project-row text-only">
    <div class="project-text">
      <h2>(Plan 2) How Self–Other Distinction Shapes Empathy</h2>
      <p>
        Empathy—the ability to understand and share others’ emotions—is essential for social interaction. Effective empathy requires a clear self–other distinction. The right temporoparietal junction (rTPJ) has been shown to modulate empathic responses. However, prior work tends to treat empathy as a unitary process. We apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias, then examine how rTPJ stimulation modulates each component to clarify how self–other distinction contributes to empathic accuracy.
      </p>
    </div>
  </section>

  <!-- Plan 3 (reverse: image right / text left). 이미지가 준비되면 src 교체 -->
  <section class="project-row reverse">
    <div class="project-image">
      <img src="/assets/img/projects/placeholder-triangle.png" alt="Group Conformity Without Minds">
    </div>
    <div class="project-text">
      <h2>(Plan 3) Group Conformity Without Minds</h2>
      <p>
        Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking. We test whether the bias could arise from domain-general mechanisms—such as ensemble coding of directional information—by replacing avatars with isosceles triangles.
      </p>
    </div>
  </section>

  <!-- Ensemble Emotion Perception -->
  <section class="project-row">
    <div class="project-image">
      <img src="/assets/img/projects/CEP_method.png" alt="Ensemble Emotion Perception">
    </div>
    <div class="project-text">
      <h2>The Influence of Situational Context and Observer Emotion on Ensemble Emotion Perception</h2>
      <p>
        Using naturalistic stimuli, the study investigated how situational context and observer emotion shape the perception of a crowd’s ensemble emotion.
      </p>
    </div>
  </section>

  <!-- SPE -->
  <section class="project-row reverse">
    <div class="project-image">
      <img src="/assets/img/projects/SPE_method.png" alt="Self-Prioritization Effects">
    </div>
    <div class="project-text">
      <h2>Self-Prioritization Effects on Nonspatial Working Memory</h2>
      <p>
        Self-prioritization effect (SPE) is the tendency to process self-associated items more quickly and accurately. We examined SPE on shape-based working memory across two experiments:
        <a href="/data/analyzeSPE8VCS1.html" target="_blank" class="project-link">(Experiment 1)</a>,
        <a href="/data/analyzeSPE8VCS2.html" target="_blank" class="project-link">(Experiment 2)</a>.
        Responses for colors were faster in the self condition than in the other, though no shape differences emerged.
      </p>
    </div>
  </section>

  <!-- Meaningfulness in VWM (text only) -->
  <section class="project-row text-only">
    <div class="project-text">
      <h2>The Impact of Meaningfulness on Visual Working Memory Across Spatial Boundaries</h2>
      <p>
        The study examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.
      </p>
    </div>
  </section>

  <!-- fNIRS study (text only) -->
  <section class="project-row text-only">
    <div class="project-text">
      <h2>The Influence of Speaker Gender and Age on Product Preference</h2>
      <p>
        The study investigated how the gender and age of speakers affect product evaluations and purchase decisions, using naturalistic video stimuli and fNIRS.
      </p>
    </div>
  </section>

</div>
<!-- END: Projects -->

<style>
/* ---------- Full-bleed container (escape theme max-width) ---------- */
/* 화면 전체 폭(뷰포트)으로 확장하고, 가운데 본문 컨테이너의 제한을 탈출 */
.projects {
  width: 100vw;
  margin-left: calc(50% - 50vw);
  margin-right: calc(50% - 50vw);
  padding: 0 1rem;               /* 안전 여백. 완전 0을 원하면 0으로 바꿔도 됨 */
}

/* (선택) Minimal Mistakes 같은 테마의 본문 패딩이 너무 클 때 */
.page .page__inner-wrap { padding-left: 0; padding-right: 0; }

/* ---------- Two-column big-media layout ---------- */
.project-row {
  display: grid;
  grid-template-columns: minmax(0, 58%) minmax(0, 42%);
  align-items: stretch;
  gap: 2rem;
  margin: 0 0 3rem 0;
}

/* 좌우 반전: 이미지 오른쪽 / 텍스트 왼쪽 */
.project-row.reverse {
  grid-template-columns: minmax(0, 42%) minmax(0, 58%);
}
.project-row.reverse .project-image { order: 2; }
.project-row.reverse .project-text  { order: 1; }

/* 이미지가 크게 보이도록 섹션 높이에 맞춰 확장 */
.project-image {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
}
.project-image img {
  display: block;
  width: 100%;
  height: 100%;
  min-height: 420px;        /* 더 크게 보이고 싶으면 520~640px로 올려도 좋아 */
  object-fit: cover;        /* 자르더라도 꽉 채우기 */
  border-radius: 8px;
}

/* 텍스트 영역 */
.project-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.project-text h2 {
  margin: 0 0 0.75rem;
  font-size: clamp(1.35rem, 1vw + 1.1rem, 2.1rem);
  line-height: 1.2;
  letter-spacing: -0.01em;
}
.project-text p {
  margin: 0;
  font-size: clamp(1rem, 0.35vw + 0.95rem, 1.125rem);
  line-height: 1.8;
  color: #333;
}
.project-link { color: #0a6cff; text-decoration: none; }
.project-link:hover { text-decoration: underline; }

/* 이미지가 없는 섹션은 텍스트가 전체 폭 사용 */
.project-row.text-only {
  grid-template-columns: 1fr;
}

/* ---------- Responsive ---------- */
@media (max-width: 900px) {
  .projects {
    margin-left: 0;
    margin-right: 0;
    width: 100%;
    padding: 0 .75rem;
  }
  .project-row,
  .project-row.reverse {
    grid-template-columns: 1fr;
    gap: 1.25rem;
  }
  .project-row.reverse .project-image,
  .project-row.reverse .project-text { order: 0; }

  .project-image img { min-height: 240px; }
}
</style>
