---
layout: page
title: Research
permalink: /research/
---
[My Google Scholar](https://scholar.google.com/citations?hl=fr&view_op=list_works&authuser=1&gmla=AElLoL2f491W0PRRZH3hHOk8_kg_uk0KUjNrjEs3LCKCkIRz9x0a1AfY-9n0N-oDRzLx2CzwRLA9MEuDkc_T-cwrLb8&user=JfxzleYAAAAJ)

# Research

## Preprints 

{% assign pubs = site.data.preprints | sort: "year" | reverse %}
{% for p in pubs %}
- **{{ p.title }}** ({{ p.year }})  
  {{ p.authors | replace: ";", ", " }}  
  *{{ p.venue }}*  
  {% if p.link and p.link != "" %}[link]({{ p.link }}){% endif %}
{% endfor %}

## Articles published in a peer-reviewed journal

{% assign pubs = site.data.citations | sort: "year" | reverse %}
{% for p in pubs %}
- **{{ p.title }}** ({{ p.year }})  
  {{ p.authors | replace: ";", ", " }}  
  *{{ p.venue }}*  
  {% if p.link and p.link != "" %}[link]({{ p.link }}){% endif %}
{% endfor %}



