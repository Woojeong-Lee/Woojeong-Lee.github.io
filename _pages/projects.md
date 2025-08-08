---
title: ""
layout: single
permalink: /projects/
header:
  show_title: false
---

<div class="projects">

  <!-- Plan 1: 이미지 왼쪽 / 글 오른쪽 -->
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

  <!-- Plan 2: 이미지 없이 텍스트만 (필요시 그림 추가 가능) -->
  <section class="project-row text-only">
    <div class="project-text">
      <h2>(Plan 2) How Self–Other Distinction Shapes Empathy</h2>
      <p>
        Empathy—the ability to understand and share others’ emotions—is essential for social interaction. Effective empathy requires a clear self–other distinction. The right temporoparietal junction (rTPJ) has been shown to modulate empathic responses. We apply multinomial processing tree (MPT) modeling to dissociate intentional empathy, unintentional empathy, and response bias, and test how rTPJ stimulation modulates each component.
      </p>
    </div>
  </section>

  <!-- Plan 3: 위치를 바꾸고 싶으면 .reverse 추가 -->
  <section class="project-row reverse">
    <div class="project-image">
      <!-- 이미지가 없으면 div 자체를 지우면 되고, 있으면 이렇게 크게 씁니다 -->
      <img src="/assets/img/projects/placeholder-triangle.png" alt="Group Conformity Without Minds (triangle stimuli)">
    </div>
    <div class="project-text">
      <h2>(Plan 3) Group Conformity Without Minds</h2>
      <p>
        Sun, Wang, and Geng (2024) reported a group conformity effect in visual perspective taking. We test whether the bias can emerge from domain-general mechanisms (e.g., ensemble coding of directions) by replacing avatars with isosceles triangles.
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
        Self-prioritization effect (SPE) refers to the tendency to process self-associated items more quickly and accurately. We examined the SPE on shape-based working memory across two experiments:
        <a href="/data/analyzeSPE8VCS1.html" target="_blank" class="project-link">(Experiment 1)</a>,
        <a href="/data/analyzeSPE8VCS2.html" target="_blank" class="project-link">(Experiment 2)</a>.
        Responses for colors were faster in the self condition than in the other, though no shape differences emerged.
      </p>
    </div>
  </section>

  <!-- Meaningfulness in VWM (텍스트만) -->
  <section class="project-row text-only">
    <div class="project-text">
      <h2>The Impact of Meaningfulness on Visual Working Memory Across Spatial Boundaries</h2>
      <p>
        The study examined whether meaningful objects facilitate the encoding of spatially distal features in visual working memory.
      </p>
    </div>
  </section>

  <!-- fNIRS study (텍스트만) -->
  <section class="project-row text-only">
    <div class="project-text">
      <h2>The Influence of Speaker Gender and Age on Product Preference</h2>
      <p>
        The study investigated how the gender and age of speakers affect product evaluations and purchase decisions, using naturalistic video stimuli and fNIRS.
      </p>
    </div>
  </section>

</div>

<style>
/* 페이지를 거의 꽉 채우기 */
.projects {
  max-width: 100%;
  padding: 0 1rem; /* 최소 안전 여백 */
}

/* 2열: 이미지(큼) / 텍스트(조금) */
.project-row {
  display: grid;
  grid-template-columns: minmax(0, 58%) minmax(0, 42%);
  align-items: stretch;
  gap: 2rem;
  margin: 0 0 3rem 0;
}

/* 좌우 반전용 (원하면 섹션에 .reverse 추가) */
.project-row.reverse {
  grid-template-columns: minmax(0, 42%) minmax(0, 58%);
}
.project-row.reverse .project-image { order: 2; }
.project-row.reverse .project-text  { order: 1; }

/* 이미지: 섹션 높이를 꽉 채우도록 크게 */
.project-image {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
}
.project-image img {
  display: block;
  width: 100%;
  height: 100%;
  min-height: 420px;      /* 이미지가 시원하게 커 보이도록 */
  object-fit: cover;      /* 자르더라도 꽉 채우기 */
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
  font-size: clamp(1.25rem, 1vw + 1rem, 2rem);
  line-height: 1.2;
  letter-spacing: -0.01em;
}
.project-text p {
  font-size: clamp(1rem, 0.4vw + 0.9rem, 1.125rem);
  line-height: 1.8;
  color: #333;
  margin: 0;
}
.project-link {
  color: #0a6cff;
  text-decoration: none;
}
.project-link:hover { text-decoration: underline; }

/* 이미지가 없는 섹션은 텍스트가 전체 폭 사용 */
.project-row.text-only {
  grid-template-columns: 1fr;
}

/* 반응형: 모바일에서는 위/아래로 쌓기 */
@media (max-width: 900px) {
  .project-row,
  .project-row.reverse {
    grid-template-columns: 1fr;
  }
  .project-row.reverse .project-image { order: 0; }
  .project-row.reverse .project-text  { order: 0; }

  .project-image img {
    min-height: 240px;
  }
}

/* 아주 넓은 화면에서는 좌우 여백 조금만 더 */
@media (min-width: 1600px) {
  .projects {
    padding: 0 1.5rem;
  }
}
</style>
