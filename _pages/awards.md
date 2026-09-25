---
layout: archive
title: "Awards & Honors"
permalink: /awards/
author_profile: true
description: "Awards, fellowships and research grants received by Shiva Khanal."
---

<div class="entry-list">
{% for award in site.data.awards %}
<div class="entry">
  <div class="entry__year">{{ award.year }}</div>
  <div class="entry__body">
    <p class="entry__title"><strong>{{ award.title }}</strong></p>
    <p class="entry__org">{{ award.organization }}</p>
    {% if award.description %}<p class="entry__desc">{{ award.description }}</p>{% endif %}
  </div>
</div>
{% endfor %}
</div>
