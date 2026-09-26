---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
description: "Curriculum vitae of Shiva Khanal, PhD: positions, education, publications, presentations, awards and service."
redirect_from:
  - /resume
---

{% include base_path %}

<p class="page__lead-note">A summary drawn from the pages of this site. For a full, current CV please <a href="mailto:{{ site.author.email }}">get in touch</a>.</p>

<section class="cv-section">
<h2 class="archive__subtitle">Current position</h2>
{% assign current = site.data.positions | first %}
<div class="cv-item">
  <p class="cv-item__title"><strong>{{ current.title }}</strong>, {{ current.organization }}</p>
  {% if current.description != "" %}<p class="cv-item__desc">{{ current.description }}</p>{% endif %}
</div>
</section>

<section class="cv-section">
<h2 class="archive__subtitle">Education</h2>
<div class="cv-item">
  <p class="cv-item__title"><strong>PhD</strong>, <a href="https://www.westernsydney.edu.au/hie/people/postgraduate-students/graduates/shiva-khanal">Western Sydney University</a></p>
  <p class="cv-item__desc">Hawkesbury Institute for the Environment. Thesis research: quantification of Nepal's forest carbon stocks.</p>
</div>
</section>

<section class="cv-section">
<h2 class="archive__subtitle">Publications</h2>
<ol class="cv-list" reversed>
{% for post in site.publications reversed %}
  <li>
    {% if post.citation %}{% include publication-citation.html pub=post %}{% else %}<p class="pub__citation"><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>. {% if post.venue %}<i>{{ post.venue }}</i>, {% endif %}{{ post.date | date: "%Y" }}.</p>{% endif %}
    {% if post.doi %}<a class="cv-doi" href="https://doi.org/{{ post.doi }}">doi:{{ post.doi }}</a>{% endif %}
  </li>
{% endfor %}
</ol>
</section>

<section class="cv-section">
<h2 class="archive__subtitle">Contributed reports</h2>
<ul class="cv-list">
{% for item in site.data.reports %}
  <li>{% if item.url %}<a href="{{ item.url }}">{{ item.title }}</a>{% elsif item.doi %}<a href="https://doi.org/{{ item.doi }}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}{% if item.publisher %}. {{ item.publisher }}{% endif %}, {% include fuzzy-date.html date=item.date %}.</li>
{% endfor %}
</ul>
</section>

<section class="cv-section">
<h2 class="archive__subtitle">Data</h2>
<ul class="cv-list">
{% for item in site.data.datasets %}
  <li>{% if item.doi %}<a href="https://doi.org/{{ item.doi }}">{{ item.title }}</a>{% elsif item.url %}<a href="{{ item.url }}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}{% if item.creators %}. {{ item.creators }}{% endif %}, {{ item.date | slice: 0, 4 }}.</li>
{% endfor %}
</ul>
</section>

<section class="cv-section">
<h2 class="archive__subtitle">Presentations</h2>
<ul class="cv-list">
{% for post in site.talks reversed %}
  <li><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>. {{ post.venue }}{% if post.location %}, {{ post.location }}{% endif %}, {{ post.date | date: "%Y" }}.</li>
{% endfor %}
</ul>
</section>

<section class="cv-section">
<h2 class="archive__subtitle">Awards &amp; fellowships</h2>
<ul class="cv-list">
{% for award in site.data.awards %}
  <li><strong>{{ award.title }}</strong>, {{ award.organization }}, {{ award.year }}.</li>
{% endfor %}
</ul>
</section>

<section class="cv-section">
<h2 class="archive__subtitle">Positions &amp; service</h2>
<ul class="cv-list">
{% for role in site.data.positions %}
  {% if role.organization != "" %}
  <li><strong>{{ role.title }}</strong>, {% if role.link %}<a href="{{ role.link }}">{{ role.organization }}</a>{% else %}{{ role.organization }}{% endif %}</li>
  {% endif %}
{% endfor %}
</ul>
</section>
