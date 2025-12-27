---
layout: page
title: Research
permalink: /research/
---
[My Google Scholar](https://scholar.google.com/citations?hl=fr&view_op=list_works&authuser=1&gmla=AElLoL2f491W0PRRZH3hHOk8_kg_uk0KUjNrjEs3LCKCkIRz9x0a1AfY-9n0N-oDRzLx2CzwRLA9MEuDkc_T-cwrLb8&user=JfxzleYAAAAJ)

# Research

## Preprints

{% assign pubs = site.data.preprints | sort: "Year" | reverse %}
{% for p in pubs %}
- {% if p.Title and p.Title != "" %}**{{ p.Title }}**{% endif %}{% if p.Year and p.Year != "" %} ({{ p.Year }}){% endif %}  
  {% if p.Authors and p.Authors != "" %}
  {{ p.Authors | replace: "Braun, Adam", "**Braun, Adam**" | replace: "; ", ", " | replace: ";", "" }}
  {% endif %}
  {% if p.Status and p.Status != "" %}
  {{ p.Status }}{% if p.Link and p.Link != "" %} — [HAL]({{ p.Link }}){% endif %}
  {% endif %}
{% endfor %}


## Articles published in a peer-reviewed journal

{% assign pubs = site.data.citations | sort: "Year" | reverse %}
{% for p in pubs %}
- **{{ p.Title }}** ({{ p.Year }})  
  {{ p.Authors | replace: "Braun, Adam", "**Braun, Adam**" | replace: "; ", ", " | replace: ";", "" }}  
  *{{ p.Publication }}*{% if p.Publisher and p.Publisher != "" %} — {{ p.Publisher }}{% endif %}
  {% if p.HAL or p.Article %}
  <br>
  {% if p.HAL %}[HAL]({{ p.HAL }}){% endif %}{% if p.HAL and p.Article %} · {% endif %}{% if p.Article %}[Article]({{ p.Article }}){% endif %}
  {% endif %}
{% endfor %}




