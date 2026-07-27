---
layout: archive
title: "Positions & Service"
permalink: /positions/
author_profile: true
---

{% for role in site.data.positions %}
<div style="margin-bottom: 1.2em;">
  <strong>{{ role.title }}</strong>, {{ role.organization }}
  <br><span style="color:#666;">{{ role.start }} - {{ role.end }}</span>
  {% if role.description %}<br>{{ role.description }}{% endif %}
</div>
{% endfor %}
