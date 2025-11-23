---
title: "Research"
layout: "single"
permalink: "/research/"
topics:
  - "Authoritarian Institutions"
  - "Natural Resources, Environment and Health"
  - "Methodology"
---

{% for topic in page.topics %}
## {{ topic }}
{% assign items = site.research | where: "topic", topic | sort: "year" | reverse %}
{% for p in items %}
- **{{ p.title }}** {% if p.status %} ({{ p.status }}){% endif %}
{% endfor %}

{% endfor %}
