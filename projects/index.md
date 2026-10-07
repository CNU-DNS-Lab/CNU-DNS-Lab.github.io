---
title: Projects
nav:
  order: 2
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Projects

Current Projects carried out at DNS Lab include:

{% capture col1 %}
- KISA DNS-Based DID Resolution
- Digital Agricultire
- GITRC-Mobility AI
{% endcapture %}
{% capture col2 %}
- BEMS-MARL
- SLAM
{% endcapture %}
{% capture col3 %}
- Glocal LAB
- Fed-Med
{% endcapture %}

{%
  include cols.html
  col1=col1
  col2=col2
  col3=col3
%}

{% include section.html %}


Here we link to open source repositories and datasets provided by our lab.

{% include tags.html tags="publication, resource, software, dataset" %}

{% include search-info.html %}

{% include section.html %}

## Open-Source

{% include list.html component="card" data="projects" style="small" %}
