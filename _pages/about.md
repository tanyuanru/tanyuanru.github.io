---
permalink: /
title: ""
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

<p class="home-intro">
  Hi! I’m <strong>Yuanru Tan</strong> (“Yoo-en-roo”, close to Mandarin pinyin <em>Yuǎnrú</em>), a Ph.D. candidate in the Learning Sciences program at the University of Wisconsin–Madison, advised by <a href="https://edpsych.education.wisc.edu/fac-staff/williamson-shaffer-david/" target="_blank" rel="noopener noreferrer">Professor David Williamson Shaffer</a> in the <a href="https://www.epistemicanalytics.org/" target="_blank" rel="noopener noreferrer">Epistemic Analytics Lab</a>, part of the <a href="https://www.crct.center/" target="_blank" rel="noopener noreferrer">Center for Research on Complex Thinking</a>. Prior to this, I worked as a Learning Experience Designer for Accessibility at the <a href="https://ai.umich.edu/" target="_blank" rel="noopener noreferrer">Center for Academic Innovation</a> at the University of Michigan–Ann Arbor, under the mentorship of <a href="https://marsal.umich.edu/directory/faculty-staff/rebecca-quintana" target="_blank" rel="noopener noreferrer">Professor Rebecca Quintana</a>. I hold an M.A. in Educational Studies from the University of Michigan–Ann Arbor (advised by <a href="https://marsal.umich.edu/directory/faculty-staff/christopher-quintana" target="_blank" rel="noopener noreferrer">Professor Chris Quintana</a>) and a B.S. in Information Management Systems from Tianjin University of Technology in China.
</p>

<p class="home-where" aria-label="Profile links">
  <strong>Where to find me:</strong>
  <a href="{{ site.author.googlescholar }}" target="_blank" rel="noopener noreferrer">Google Scholar</a><span class="home-dot" aria-hidden="true"> · </span><a href="{{ site.author.orcid }}" target="_blank" rel="noopener noreferrer">ORCID</a><span class="home-dot" aria-hidden="true"> · </span><a href="https://github.com/{{ site.author.github }}" target="_blank" rel="noopener noreferrer">GitHub</a><span class="home-dot" aria-hidden="true"> · </span><a href="https://www.linkedin.com/in/{{ site.author.linkedin }}" target="_blank" rel="noopener noreferrer">LinkedIn</a>
</p>

<div class="about-body">

<h2>My Research</h2>

<p>
  I develop methods! Specifically, I design and develop computational methods for educational research, with a focus on modeling learning processes. I believe that studying how people learn requires methods that are not only computationally rigorous and visually expressive, but also grounded in theories of learning. That’s why I situate my research at the intersection of learning sciences, statistics, and data visualization. Here are some highlights:
</p>

<p>
  My first signature method, <strong>Ordered Network Analysis (ONA)</strong>, has been employed in 100+ published works across quantitative ethnography, learning analytics, AI in education, healthcare, and nursing education — since my colleagues and I introduced it in 2023 (<a href="https://link.springer.com/chapter/10.1007/978-3-031-31726-2_8" target="_blank" rel="noopener noreferrer">ONA method paper</a>).
</p>

<p>
  My current work focuses on developing a new method for modeling learning trajectories. Try my prototype app here! <em>(link coming soon)</em>
</p>

<p>
  I’m driven by the goal of developing methods that turn complex learning data into representations that help researchers tell faithful and meaningful stories about how people learn.
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
