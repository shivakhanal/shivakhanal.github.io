---
layout: archive
title: "Awards & Honors"
permalink: /awards/
author_profile: true
---

{% for award in site.data.awards %}
<div style="margin-bottom: 1.2em;">
  <strong>{{ award.title }}</strong> - {{ award.organization }}, {{ award.year }}
  {% if award.description %}<br><span style="color:#666;">{{ award.description }}</span>{% endif %}
</div>
{% endfor %}
