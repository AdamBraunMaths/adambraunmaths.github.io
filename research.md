---
layout: page
title: Research
permalink: /research/
---


# Research

## Articles published in a peer-reviewed journal
## Publications

{% assign pubs = site.data.citations | sort: "year" | reverse %}
{% for p in pubs %}
- **{{ p.title }}** ({{ p.year }})  
  {{ p.authors | replace: ";", ", " }}  
  *{{ p.venue }}*  
  {% if p.link and p.link != "" %}[link]({{ p.link }}){% endif %}
{% endfor %}



