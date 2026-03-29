---
permalink: /
title: "Yuanru Tan"
show_news: true
show_latest_posts: true
selected_publications_limit: 2
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<style>
.home-landing .home-subtitle {
  font-size: 1.05rem;
  color: #555;
  margin: -0.25rem 0 1.25rem;
  line-height: 1.45;
}
.about-body {
  line-height: 1.5;
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
.home-post-list {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.95em;
}
.home-post-list li {
  margin-bottom: 0.5rem;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid rgba(0,0,0,0.06);
}
.home-post-list li:last-child {
  border-bottom: none;
  margin-bottom: 0;
  padding-bottom: 0;
}
.home-post-list .post-date {
  color: #666;
  font-size: 0.9em;
  margin-right: 0.5rem;
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

<p class="home-subtitle">Ph.D. candidate in Learning Sciences · University of Wisconsin–Madison</p>

<div class="about-body">

<p>
I’m <strong>Yuanru Tan</strong> (“Yoo-en-roo”, close to Mandarin pinyin <em>Yuǎnrú</em>). I believe that studying how people learn requires methods that are not only computationally rigorous and visually expressive, but also grounded in theories of learning. That’s why, as a methodologist-in-training, my research sits at the intersection of learning sciences, statistics, and data visualization. I develop methods that turn complex learning data into representations that tell faithful and meaningful stories about how people learn.
</p>

<p>
In my first three years as a Ph.D. student, I led the development of <strong>Ordered Network Analysis (ONA)</strong>, a method for quantifying how concepts co-occur in coded data and visualizing those relationships as weighted directed networks that support both visual and statistical comparison. Since its introduction, ONA has been adopted by researchers in various fields such as quantitative ethnography, learning analytics, AI in education, healthcare, and nursing education.
</p>

<p>
In my current work, I’m extending ONA to develop a new method that constructs learning trajectories from process data. Learning is a process of change over time, we can see behavior change, but not the underlying mechanisms that drive it. The method I’m developing traces those mechanisms from moment to moment, to recover learning as it actually unfolds.
</p>

<p>
I’m advised by <a href="https://edpsych.education.wisc.edu/fac-staff/williamson-shaffer-david/" target="_blank" rel="noopener noreferrer">Professor David Williamson Shaffer</a> in the <a href="https://www.epistemicanalytics.org/" target="_blank" rel="noopener noreferrer">Epistemic Analytics Lab</a>, part of the <a href="https://www.crct.center/" target="_blank" rel="noopener noreferrer">Center for Research on Complex Thinking</a>. Before my Ph.D., I worked as a Learning Experience Designer for Accessibility at the <a href="https://ai.umich.edu/" target="_blank" rel="noopener noreferrer">Center for Academic Innovation</a> at the University of Michigan–Ann Arbor, under the mentorship of <a href="https://marsal.umich.edu/directory/faculty-staff/rebecca-quintana" target="_blank" rel="noopener noreferrer">Professor Rebecca Quintana</a>. I hold an M.A. in Education from the University of Michigan–Ann Arbor (advised by <a href="https://marsal.umich.edu/directory/faculty-staff/christopher-quintana" target="_blank" rel="noopener noreferrer">Professor Chris Quintana</a>) and a B.S. in Information Management Systems from Tianjin University of Technology in China.
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

{% if page.show_latest_posts != false %}
  {% assign post_limit = 3 %}
  {% assign recent_posts = site.posts | where_exp: "post", "post.date <= site.time" | sort: "date" | reverse %}
  {% if recent_posts.size > 0 %}
<section class="home-section" aria-labelledby="home-posts-heading">
  <h2 id="home-posts-heading">Latest posts</h2>
  <ul class="home-post-list">
    {% for post in recent_posts limit: post_limit %}
    <li>
      <span class="post-date">{{ post.date | date: "%b %d, %Y" }}</span>
      <a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
  </ul>
</section>
  {% endif %}
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
