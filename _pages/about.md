---
permalink: /
title: "Yuanru Tan"
show_news: true
show_latest_posts: false
selected_publications_limit: 2
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<style>
.home-landing .about-body > h2 {
  font-size: 1.15rem;
  font-weight: 600;
  margin: 1.75rem 0 0.65rem;
  padding-bottom: 0.35em;
  border-bottom: 1px solid var(--global-border-color, #ddd);
  font-family: 'IBM Plex Serif', serif !important;
}
.home-landing .about-body > h2:first-of-type {
  margin-top: 0;
}
.about-body {
  line-height: 1.55;
  font-size: 1em;
}
.about-body p {
  margin-bottom: 0.9em;
}
.about-body p:last-child {
  margin-bottom: 0;
}
.home-landing .home-section {
  margin-top: 2.25rem;
}
.home-landing .home-section:first-of-type {
  margin-top: 1.75rem;
}
.home-landing .home-section h2 {
  font-size: 1.2rem;
  font-weight: 600;
  margin: 0 0 0.75rem;
  padding-bottom: 0.35em;
  border-bottom: 1px solid var(--global-border-color, #ddd);
  font-family: 'IBM Plex Serif', serif !important;
}
.home-news-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.92em;
}
.home-news-table th,
.home-news-table td {
  text-align: left;
  vertical-align: top;
  padding: 0.45rem 0.65rem 0.45rem 0;
  border-bottom: 1px solid rgba(0,0,0,0.06);
}
.home-news-table th {
  width: 6.5rem;
  color: #666;
  font-weight: 500;
  white-space: nowrap;
}
.home-news-table tr:last-child th,
.home-news-table tr:last-child td {
  border-bottom: none;
}
.home-pub-card {
  border: 1px solid rgba(0,0,0,0.08);
  border-radius: 8px;
  padding: 1rem 1.15rem;
  background: #fafafa;
  margin-bottom: 0.85rem;
  font-size: 0.95em;
  line-height: 1.5;
}
.home-pub-card:last-of-type {
  margin-bottom: 0.5rem;
}
.home-pub-card .home-pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  margin: 0 0 0.35rem;
  font-family: 'IBM Plex Serif', serif !important;
}
.home-pub-card .home-pub-meta {
  color: #555;
  font-size: 0.9em;
  margin: 0 0 0.5rem;
}
.home-pub-card .home-pub-excerpt {
  margin: 0 0 0.5rem;
  font-size: 0.92em;
}
.home-landing .home-more {
  margin: 0.75rem 0 0;
  font-size: 0.95em;
}
</style>

<div class="home-landing">

<div class="about-body">

<h2>About Me</h2>

<p>
I’m <strong>Yuanru Tan</strong> (“Yoo-en-roo”, close to Mandarin pinyin <em>Yuǎnrú</em>), a Ph.D. candidate in the Learning Sciences program at the University of Wisconsin–Madison, advised by <a href="https://edpsych.education.wisc.edu/fac-staff/williamson-shaffer-david/" target="_blank" rel="noopener noreferrer">Professor David Williamson Shaffer</a> in the <a href="https://www.epistemicanalytics.org/" target="_blank" rel="noopener noreferrer">Epistemic Analytics Lab</a>, part of the <a href="https://www.crct.center/" target="_blank" rel="noopener noreferrer">Center for Research on Complex Thinking</a>. Prior to this, I worked as a Learning Experience Designer for Accessibility at the <a href="https://ai.umich.edu/" target="_blank" rel="noopener noreferrer">Center for Academic Innovation</a> at the University of Michigan–Ann Arbor, under the mentorship of <a href="https://marsal.umich.edu/directory/faculty-staff/rebecca-quintana" target="_blank" rel="noopener noreferrer">Professor Rebecca Quintana</a>. I hold an M.A. in Educational Studies from the University of Michigan–Ann Arbor (advised by <a href="https://marsal.umich.edu/directory/faculty-staff/christopher-quintana" target="_blank" rel="noopener noreferrer">Professor Chris Quintana</a>) and a B.S. in Information Management Systems from Tianjin University of Technology in China.
</p>

<h2>My Research</h2>

<p>
My research focuses on designing and developing computational methods for education, with a focus on modeling learning processes. My first signature method, <strong>Ordered Network Analysis (ONA)</strong>, has — since its introduction in 2023 — been employed in 100+ published works across quantitative ethnography, learning analytics, AI in education, healthcare, and nursing education (<a href="https://scholar.google.com/scholar?oi=bibs&amp;hl=en&amp;cites=10712429113643550992&amp;as_sdt=5" target="_blank" rel="noopener noreferrer">Google Scholar citation graph</a>). My dissertation project takes this further: a new method for modeling learning trajectories. More to come!
</p>

<p>
As a methodologist-in-training, I believe that studying how people learn requires methods that are not only computationally rigorous and visually expressive, but also grounded in theories of learning. That’s why I situate my research at the intersection of learning sciences, statistics, and data visualization. I’m driven by the goal of developing methods that turn complex learning data into representations that help researchers tell faithful and meaningful stories about how people learn.
</p>

</div>

{% if page.show_news != false and site.data.home_news.items and site.data.home_news.items.size > 0 %}
<section class="home-section" aria-labelledby="home-news-heading">
  <h2 id="home-news-heading">News</h2>
  <table class="home-news-table">
    <tbody>
      {% for item in site.data.home_news.items %}
      <tr>
        <th scope="row">{{ item.date }}</th>
        <td>{{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}</td>
      </tr>
      {% endfor %}
    </tbody>
  </table>
</section>
{% endif %}

{% if site.publications.size > 0 %}
<section class="home-section" aria-labelledby="home-pubs-heading">
  <h2 id="home-pubs-heading">Selected publications</h2>
  {% assign pub_limit = page.selected_publications_limit | default: 2 %}
  {% assign pubs_sorted = site.publications | sort: 'date' | reverse %}
  {% for pub in pubs_sorted limit: pub_limit %}
  <article class="home-pub-card">
    <h3 class="home-pub-title"><a href="{{ base_path }}{{ pub.url }}">{{ pub.title }}</a></h3>
    <p class="home-pub-meta">{% if pub.venue %}<i>{{ pub.venue }}</i>{% endif %}{% if pub.date and pub.venue %}, {% endif %}{% if pub.date %}{{ pub.date | date: "%Y" }}{% endif %}</p>
    {% if pub.excerpt %}
    <p class="home-pub-excerpt">{{ pub.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}</p>
    {% endif %}
    {% if pub.paperurl %}
    <p class="home-pub-links" style="margin:0;font-size:0.9em;"><a href="{{ pub.paperurl }}" target="_blank" rel="noopener noreferrer">Paper</a></p>
    {% endif %}
  </article>
  {% endfor %}
  <p class="home-more"><a href="{{ base_path }}/research/">View all research →</a></p>
</section>
{% endif %}

</div>
