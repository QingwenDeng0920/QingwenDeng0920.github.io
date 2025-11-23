---
title: "Research"
layout: "single"
permalink: "/research/"
topics:
  - "Authoritarian Institutions"
  - "Environment & Health"
  - "Methods"
---

{% for topic in page.topics %}
## {{ topic }}
{% assign items = site.research | where: "topic", topic | sort: "year" | reverse %}
{% for p in items %}
- **{{ p.title }}**{% if p.coauthors %}, with {{ p.coauthors }}{% endif %}{% if p.status %} ({{ p.status }}){% endif %}
{% endfor %}

{% endfor %}
