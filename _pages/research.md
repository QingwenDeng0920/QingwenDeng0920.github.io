---
title: "Research"
layout: single
permalink: /research/
topics:
  - "Authoritarian Institutions"
  - "Natural Resources, Environment and Health"
  - "Methodology"
---

{% raw %}
{% for topic in page.topics %}
## {{ topic }}
{% assign items = site.research | where: "topic", topic | sort: "year" | reverse %}
{% if items.size == 0 %}
*Coming soon.*
{% endif %}
{% for p in items %}
- **{{ p.title }}**{% if p.coauthors %}, with {{ p.coauthors }}{% endif %}{% if p.status %} ({{ p.status }}){% endif %}
{% endfor %}

{% endfor %}
{% endraw %}
