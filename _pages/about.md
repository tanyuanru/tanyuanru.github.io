---
permalink: /
title: ""
show_news: true
show_latest_posts: false
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<div class="home-landing">

<div class="about-body">

<h2>About Me</h2>

<p class="home-intro">
  Hi! I’m <strong>Yuanru Tan</strong> (“Yoo-en-roo”, close to Mandarin pinyin <em>Yuǎnrú</em>), a Ph.D. candidate in the Learning Sciences program at the University of Wisconsin–Madison, advised by <a href="https://edpsych.education.wisc.edu/fac-staff/williamson-shaffer-david/" target="_blank" rel="noopener noreferrer">Professor David Williamson Shaffer</a> in the <a href="https://www.epistemicanalytics.org/" target="_blank" rel="noopener noreferrer">Epistemic Analytics Lab</a>, part of the <a href="https://www.crct.center/" target="_blank" rel="noopener noreferrer">Center for Research on Complex Thinking</a>. Prior to this, I worked as a Learning Experience Designer for Accessibility at the <a href="https://ai.umich.edu/" target="_blank" rel="noopener noreferrer">Center for Academic Innovation</a> at the University of Michigan–Ann Arbor, under the mentorship of <a href="https://marsal.umich.edu/directory/faculty-staff/rebecca-quintana" target="_blank" rel="noopener noreferrer">Professor Rebecca Quintana</a>. I hold an M.A. in Educational Studies from the University of Michigan–Ann Arbor (advised by <a href="https://marsal.umich.edu/directory/faculty-staff/christopher-quintana" target="_blank" rel="noopener noreferrer">Professor Chris Quintana</a>) and a B.S. in Information Management Systems from Tianjin University of Technology in China.
</p>

<h2>My Research</h2>

<p>
  I develop methods! Specifically, I design and develop computational methods for educational research, with a focus on modeling learning processes. I believe that studying how people learn requires methods that are not only computationally rigorous and visually expressive, but also grounded in theories of learning. That’s why I situate my research at the intersection of learning sciences, statistics, and data visualization. Here are some highlights:
</p>

{% include home-research-highlights.html %}

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

</div>
