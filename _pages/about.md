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

<div class="home-landing">

<p class="home-open">
  Welcome! I work at the intersection of <strong>learning sciences</strong>, <strong>computational methods</strong>, and <strong>data visualization</strong> — building tools to model <strong>learning processes</strong> and <strong>process data</strong>. Ph.D. candidate at the <a href="https://www.wisc.edu/" target="_blank" rel="noopener noreferrer">University of Wisconsin–Madison</a>, advised by <a href="https://edpsych.education.wisc.edu/fac-staff/williamson-shaffer-david/" target="_blank" rel="noopener noreferrer">David Williamson Shaffer</a> (<a href="https://www.epistemicanalytics.org/" target="_blank" rel="noopener noreferrer">Epistemic Analytics Lab</a>, <a href="https://www.crct.center/" target="_blank" rel="noopener noreferrer">CRCT</a>).
</p>

<p class="home-where" aria-label="Profile links">
  <strong>Where to find me:</strong>
  <a href="{{ site.author.googlescholar }}" target="_blank" rel="noopener noreferrer">Google Scholar</a><span class="home-dot" aria-hidden="true"> · </span><a href="{{ site.author.orcid }}" target="_blank" rel="noopener noreferrer">ORCID</a><span class="home-dot" aria-hidden="true"> · </span><a href="https://github.com/{{ site.author.github }}" target="_blank" rel="noopener noreferrer">GitHub</a><span class="home-dot" aria-hidden="true"> · </span><a href="https://www.linkedin.com/in/{{ site.author.linkedin }}" target="_blank" rel="noopener noreferrer">LinkedIn</a><span class="home-dot" aria-hidden="true"> · </span><a href="mailto:{{ site.author.email }}">Email</a>
</p>

<p class="home-market-note">On the academic job market (2025–26).</p>

<div class="home-actions" role="navigation" aria-label="Documents">
  <a class="home-btn home-btn--primary" href="{{ site.cv_pdf_url }}" target="_blank" rel="noopener noreferrer">Download CV (PDF)</a>
  <a class="home-btn" href="{{ base_path }}/research/">Research</a>
  <a class="home-btn" href="{{ base_path }}/teaching/">Teaching &amp; mentoring</a>
</div>

<div class="about-body">

<h2 class="home-theme-head">Learning, methods, representation</h2>

<p>
<strong>Yuanru Tan</strong> (“Yoo-en-roo”; Mandarin <em>Yuǎnrú</em>). My training bridges learning sciences, statistics, and visualization — with prior experience as a Learning Experience Designer for Accessibility at the <a href="https://ai.umich.edu/" target="_blank" rel="noopener noreferrer">Center for Academic Innovation</a>, University of Michigan–Ann Arbor (<a href="https://marsal.umich.edu/directory/faculty-staff/rebecca-quintana" target="_blank" rel="noopener noreferrer">Rebecca Quintana</a>). M.A. in Educational Studies, Michigan (advisor <a href="https://marsal.umich.edu/directory/faculty-staff/christopher-quintana" target="_blank" rel="noopener noreferrer">Chris Quintana</a>); B.S. in Information Management Systems, Tianjin University of Technology.
</p>

<h2>Research</h2>

<p class="home-section-lead">
  I develop methods that help researchers represent and reason about learning from complex qualitative and process data — work that should be <em>computationally sound</em>, <em>visually clear</em>, and <em>theoretically grounded</em>.
</p>

<ul class="research-highlights">
  <li><strong>Ordered Network Analysis (ONA).</strong> A signature method for temporal network structure in coded data; in use across quantitative ethnography, learning analytics, AI in education, healthcare, and nursing education since 2023 (<a href="https://scholar.google.com/scholar?oi=bibs&amp;hl=en&amp;cites=10712429113643550992&amp;as_sdt=5" target="_blank" rel="noopener noreferrer">citing works</a>).</li>
  <li><strong>Dissertation.</strong> Extending this line of work toward methods for <strong>learning trajectories</strong> from process data — more soon.</li>
  <li><strong>Goal.</strong> Representations that support faithful, meaningful accounts of how people learn — not only summaries of behavior.</li>
</ul>

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

{% assign pub_count = site.publications | size %}
{% if pub_count > 0 %}
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
    <p class="home-pub-links"><a href="{{ pub.paperurl }}" target="_blank" rel="noopener noreferrer">Paper</a></p>
    {% endif %}
  </article>
  {% endfor %}
  <p class="home-more"><a href="{{ base_path }}/research/">All research →</a></p>
</section>
{% endif %}

</div>
