---
layout: archive
title: "Positions & Service"
permalink: /positions/
author_profile: true
description: "Positions, editorial roles and professional service of Shiva Khanal, including UNFCCC climate transparency reporting for Nepal."
---

<div class="entry-list">
{% for role in site.data.positions %}
<div class="entry entry--no-year">
  <div class="entry__body">
    <p class="entry__title"><strong>{{ role.title }}</strong>{% if role.organization != "" %}, {% if role.link %}<a href="{{ role.link }}">{{ role.organization }}</a>{% else %}{{ role.organization }}{% endif %}{% endif %}</p>
    {% if role.start != "" or role.end != "" %}<p class="entry__org">{{ role.start }}{% if role.start != "" and role.end != "" %} to {% endif %}{{ role.end }}</p>{% endif %}
    {% if role.description != "" %}<p class="entry__desc">{{ role.description }}</p>{% endif %}
  </div>
</div>
{% endfor %}
</div>
