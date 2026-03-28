---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<p>
I'm <strong>Yuanru Tan</strong> ("Yoo-en-roo", close to Mandarin pinyin <em>Yuǎnrú</em>), a Ph.D. candidate in the Learning Sciences program at the University of Wisconsin–Madison. I'm advised by <a href="https://edpsych.education.wisc.edu/fac-staff/williamson-shaffer-david/" target="_blank" rel="noopener noreferrer">Professor David Williamson Shaffer</a> in the <a href="https://www.epistemicanalytics.org/" target="_blank" rel="noopener noreferrer">Epistemic Analytics Lab</a>, part of the <a href="https://www.crct.center/" target="_blank" rel="noopener noreferrer">Center for Research on Complex Thinking</a>.
</p>
<p>
I'm a methodologist-in-training, working at the intersection of learning theories, data, and design. I led the development of <strong>Ordered Network Analysis (ONA)</strong>, a method available in R and as a web tool for quantifying directed connections in coded data and visualizing them as weighted directed networks. For my dissertation, I'm developing a new method that goes beyond ONA's capacity to summarize learning processes by describing learning processes as trajectories instead.
</p>
<p>
Before my Ph.D., I worked as a <em>Learning Experience Designer for Accessibility</em> at the <a href="https://ai.umich.edu/" target="_blank" rel="noopener noreferrer">Center for Academic Innovation</a> at the University of Michigan–Ann Arbor, under the mentorship of <a href="https://marsal.umich.edu/directory/faculty-staff/rebecca-quintana" target="_blank" rel="noopener noreferrer">Professor Rebecca Quintana</a>. I worked with <a href="https://www.youtube.com/watch?v=KDKdWDTVEzE&t=94s&ab_channel=CenterforAcademicInnovation" target="_blank" rel="noopener noreferrer">instructors</a> passionate about inclusive and accessible online learning, and contributed to research on learning experience design. One of my favorite projects explored how different forms of representation — <a href="https://dl.acm.org/doi/10.1145/3170427.3188650" target="_blank" rel="noopener noreferrer">beaded artifacts</a> and <a href="https://link.springer.com/article/10.1007/s11528-021-00592-x" target="_blank" rel="noopener noreferrer">digital visualizations</a> — can shape the way designers think. (P.S. Those beaded artifacts ended up on our desks, and it remains one of my favorite memories.)
</p>
<p>
I hold an M.A. in Education from the University of Michigan–Ann Arbor (advised by <a href="https://marsal.umich.edu/directory/faculty-staff/christopher-quintana" target="_blank" rel="noopener noreferrer">Professor Chris Quintana</a>) and a B.S. in Information Management Systems from Tianjin University of Technology in China.
</p>


---

<style>
/* ── Publication section styles ── */
.pub-section-label {
  font-size: 0.72em;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: #888;
  margin-bottom: 0.6em;
  margin-top: 2em;
}

/* Featured card */
.pub-featured {
  display: flex;
  gap: 24px;
  align-items: flex-start;
  padding: 20px;
  border-radius: 12px;
  border-left: 4px solid #61D04F;
  background: #f9fdf8;
  margin-bottom: 2em;
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}

.pub-featured:hover {
  box-shadow: 0 4px 16px rgba(0,0,0,0.08);
  transform: translateY(-2px);
}

/* Regular pub row */
.pub-row {
  display: flex;
  gap: 20px;
  align-items: flex-start;
  padding: 16px;
  border-radius: 10px;
  margin-bottom: 1.2em;
  transition: background-color 0.2s ease, box-shadow 0.2s ease, transform 0.2s ease;
}

.pub-row:hover {
  background-color: #f7f7f7;
  box-shadow: 0 3px 10px rgba(0,0,0,0.06);
  transform: translateY(-2px);
}

/* Thumbnails */
.pub-thumb {
  width: 120px;
  min-width: 120px;
  height: 88px;
  object-fit: cover;
  border-radius: 6px;
  background: #e8e8e8;
  flex-shrink: 0;
}

.pub-thumb-placeholder {
  width: 120px;
  min-width: 120px;
  height: 88px;
  border-radius: 6px;
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.65em;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: #fff;
}

/* Text block */
.pub-text {
  flex: 1;
  line-height: 1.5;
}

.pub-title {
  font-weight: 700;
  font-size: 1em;
  margin: 0 0 0.2em 0;
  line-height: 1.4;
}

.pub-authors {
  font-size: 0.88em;
  color: #555;
  margin: 0 0 0.2em 0;
}

.pub-authors .me {
  font-weight: 700;
  color: #222;
}

.pub-venue {
  font-size: 0.85em;
  color: #777;
  font-style: italic;
  margin: 0 0 0.25em 0;
}

.pub-citations {
  font-size: 0.8em;
  color: #aaa;
  margin: 0 0 0.5em 0;
}

.pub-abstract {
  font-size: 0.88em;
  color: #444;
  margin: 0.4em 0 0.7em 0;
  line-height: 1.55;
}

/* Pill links */
.pub-links {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 0.5em;
}

.pub-pill {
  display: inline-block;
  padding: 3px 12px;
  border-radius: 20px;
  border: 1.5px solid #61D04F;
  color: #61D04F;
  font-size: 0.8em;
  font-weight: 600;
  text-decoration: none;
  transition: background-color 0.15s ease, color 0.15s ease;
}

.pub-pill:hover {
  background-color: #61D04F;
  color: #fff;
  text-decoration: none;
}

.pub-pill.secondary {
  border-color: #aaa;
  color: #666;
}

.pub-pill.secondary:hover {
  background-color: #aaa;
  color: #fff;
}

/* Domain tag */
.pub-tag {
  display: inline-block;
  font-size: 0.72em;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: #888;
  background: #efefef;
  border-radius: 4px;
  padding: 2px 7px;
  margin-bottom: 0.4em;
}
</style>
<h2>Selected Publications</h2>
<!-- ── FEATURED ── -->
<p class="pub-section-label">Featured</p>
<div class="pub-featured">
  <!-- Replace src with: /images/pub-ona-method.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #61D04F, #3aad2e);">ONA</div>
  <div class="pub-text">
    <p class="pub-title">Ordered Network Analysis</p>
    <p class="pub-authors"><span class="me">Y Tan</span>, AR Ruis, C Marquart, Z Cai, MA Knowles, DW Shaffer</p>
    <p class="pub-venue">International Conference on Quantitative Ethnography, 2023</p>
    <p class="pub-citations">↗ [add citation count] citations</p>
    <p class="pub-abstract">I introduce ONA, a network technique to model, visualize, and statistically compare temporal structures in discourse data. Built on Epistemic Network Analysis (ENA), ONA has since been applied across education, healthcare, and other domains.</p>
    <div class="pub-links">
      <a class="pub-pill" href="https://link.springer.com/chapter/10.1007/978-3-031-31726-2_8" target="_blank" rel="noopener noreferrer">Paper</a>
      <a class="pub-pill secondary" href="https://link.springer.com/chapter/10.1007/978-3-031-54464-4_18" target="_blank" rel="noopener noreferrer">R Tutorial</a>
      <a class="pub-pill secondary" href="https://www.epistemicanalytics.org/our-projects/" target="_blank" rel="noopener noreferrer">Web Tool</a>
    </div>
  </div>
</div>
<!-- ── SELECTED PUBLICATIONS ── -->
<p class="pub-section-label">Other Publications</p>
<!-- 1. ONA Tutorial -->
<div class="pub-row">
  <!-- Replace src with: /images/pub-ona-tutorial.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #4db8a4, #2e8a78);">ENA / ONA</div>
  <div class="pub-text">
    <p class="pub-title">Epistemic Network Analysis and Ordered Network Analysis in Learning Analytics</p>
    <p class="pub-authors"><span class="me">Y Tan</span>, Z Swiecki, AR Ruis, DW Shaffer</p>
    <p class="pub-venue">Learning Analytics Methods and Tutorials: A Practical Guide Using R, 2024</p>
    <p class="pub-abstract">A detailed tutorial on conducting ENA and ONA in R, designed for learning analytics researchers and practitioners.</p>
    <div class="pub-links">
      <a class="pub-pill" href="PLACEHOLDER_URL" target="_blank" rel="noopener noreferrer">Book Chapter</a>
    </div>
  </div>
</div>
<!-- 2. Journal of Learning Analytics — Knowledge Building -->
<div class="pub-row">
  <!-- Replace src with: /images/pub-knowledge-building.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #7b9fd4, #4a72b0);">JLA</div>
  <div class="pub-text">
    <span class="pub-tag">Knowledge Building</span>
    <p class="pub-title">Temporal Network Analysis of Collaborative Prototyping from a Knowledge Creation Perspective</p>
    <p class="pub-authors">A Ohsaki, <span class="me">Y Tan</span>, B Eagan, DW Shaffer, Z Swiecki</p>
    <p class="pub-venue">Journal of Learning Analytics, 2026</p>
    <p class="pub-abstract">Applies ONA to examine how collaborative prototyping unfolds over time through a knowledge creation lens, revealing temporal patterns in student discourse.</p>
    <div class="pub-links">
      <a class="pub-pill" href="PLACEHOLDER_URL" target="_blank" rel="noopener noreferrer">Paper</a>
    </div>
  </div>
</div>
<!-- 3. Journal of Computer Assisted Learning — MOOCs -->
<div class="pub-row">
  <!-- Replace src with: /images/pub-mooc-tactics.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #d4a76b, #b07f3a);">JCAL</div>
  <div class="pub-text">
    <span class="pub-tag">Online Learning</span>
    <p class="pub-title">Dissecting Learning Tactics in MOOCs Using Ordered Network Analysis</p>
    <p class="pub-authors">Y Fan, <span class="me">Y Tan</span>, M Raković, Y Wang, Z Cai, DW Shaffer, D Gašević</p>
    <p class="pub-venue">Journal of Computer Assisted Learning, 2023, 39(1), 154–166</p>
    <p class="pub-abstract">Uses ONA to identify and compare temporal patterns in MOOC learning tactics, surfacing differences in how successful and struggling learners sequence their study behaviors.</p>
    <div class="pub-links">
      <a class="pub-pill" href="https://onlinelibrary.wiley.com/doi/full/10.1111/jcal.12735" target="_blank" rel="noopener noreferrer">Paper</a>
    </div>
  </div>
</div>
<!-- 4. Computers & Education — VR -->
<div class="pub-row">
  <!-- Replace src with: /images/pub-vr-attention.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #a87bd4, #7a4aaa);">C&E</div>
  <div class="pub-text">
    <span class="pub-tag">Virtual Reality</span>
    <p class="pub-title">Unveiling Joint Attention Dynamics: Examining Multimodal Engagement in an Immersive Collaborative Astronomy Simulation</p>
    <p class="pub-authors">J Kang, Y Zhou, RJ Rajarathinam, <span class="me">Y Tan</span>, DW Shaffer</p>
    <p class="pub-venue">Computers & Education, 213, 105002</p>
    <p class="pub-abstract">Applies ONA to multimodal data from an immersive VR simulation to examine how joint attention dynamics unfold during collaborative astronomy learning.</p>
    <div class="pub-links">
      <a class="pub-pill" href="PLACEHOLDER_URL" target="_blank" rel="noopener noreferrer">Paper</a>
    </div>
  </div>
</div>
<!-- 5. BMJ Open — Healthcare -->
<div class="pub-row">
  <!-- Replace src with: /images/pub-bmj-nursing.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #d47b7b, #aa4444);">BMJ</div>
  <div class="pub-text">
    <span class="pub-tag">Healthcare</span>
    <p class="pub-title">Applying Ordered Network Analysis to Video-Recorded Physician–Nurse Interactions to Examine Communication Patterns Associated with Shared Understanding in Inpatient Oncology</p>
    <p class="pub-authors">V Popov, <span class="me">Y Tan</span>, M Manojlovich</p>
    <p class="pub-venue">BMJ Open, 14(6), e084653</p>
    <p class="pub-abstract">Demonstrates ONA's cross-disciplinary reach by analyzing physician–nurse communication in oncology settings, identifying interaction patterns linked to shared clinical understanding.</p>
    <div class="pub-links">
      <a class="pub-pill" href="PLACEHOLDER_URL" target="_blank" rel="noopener noreferrer">Paper</a>
    </div>
  </div>
</div>
<!-- 6. AIED — Multimodal -->
<div class="pub-row">
  <!-- Replace src with: /images/pub-multimodal.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #7bd4c8, #3aaa9c);">AIED</div>
  <div class="pub-text">
    <span class="pub-tag">Multimodal Learning</span>
    <p class="pub-title">Analysing Verbal Communication in Embodied Team Learning Using Multimodal Data and Ordered Network Analysis</p>
    <p class="pub-authors">L Zhao, <span class="me">Y Tan</span>, D Gašević, DW Shaffer, L Yan, R Alfredo, X Li et al.</p>
    <p class="pub-venue">International Conference on Artificial Intelligence in Education (AIED), 2023, 242–254</p>
    <p class="pub-abstract">Combines ONA with multimodal data to analyze verbal communication patterns in embodied team learning, showing how physical and verbal channels interact during collaborative tasks.</p>
    <div class="pub-links">
      <a class="pub-pill" href="https://link.springer.com/chapter/10.1007/978-3-031-36272-9_20" target="_blank" rel="noopener noreferrer">Paper</a>
    </div>
  </div>
</div>
<!-- 7. Visual Design -->
<div class="pub-row">
  <!-- Replace src with: /images/pub-visual-design.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #d4c46b, #a89c3a);">ICQE</div>
  <div class="pub-text">
    <span class="pub-tag">Visualization</span>
    <p class="pub-title">On the Importance of Numerical and Visual Alignment: Comparing Transition Probability Matrices Visually Using Ordered Semantic Co-registration Layout and Modified Dot Layout</p>
    <p class="pub-authors"><span class="me">Y Tan</span>, Y Fan, DW Shaffer</p>
    <p class="pub-venue">International Conference on Quantitative Ethnography, 2023, 162–176</p>
    <p class="pub-abstract">Examines how different visual layouts for transition probability matrices affect interpretability, proposing design principles for communicating temporal network data more faithfully.</p>
    <div class="pub-links">
      <a class="pub-pill" href="PLACEHOLDER_URL" target="_blank" rel="noopener noreferrer">Paper</a>
    </div>
  </div>
</div>
<!-- 8. Early MOOC Work -->
<div class="pub-row">
  <!-- Replace src with: /images/pub-mooc-platforms.png once uploaded -->
  <div class="pub-thumb-placeholder" style="background: linear-gradient(135deg, #a0a0c8, #6868a0);">ICALN</div>
  <div class="pub-text">
    <span class="pub-tag">Learning Design</span>
    <p class="pub-title">What Can We Learn About Learner Interaction When One Course Is Hosted on Two MOOC Platforms</p>
    <p class="pub-authors"><span class="me">Y Tan</span>, RM Quintana</p>
    <p class="pub-venue">Companion Proceedings, International Conference on Learning Analytics & Knowledge, 2019</p>
    <p class="pub-abstract">Compares learner interaction patterns across two MOOC platforms hosting the same course, surfacing how platform design shapes learning behavior.</p>
    <div class="pub-links">
      <a class="pub-pill" href="PLACEHOLDER_URL" target="_blank" rel="noopener noreferrer">Paper</a>
    </div>
  </div>
</div>
