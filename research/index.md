---
title: Research
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

<p class="center">
Here you can find published research conducted at DNS Lab.
</p>

{% include section.html %}

## All

{% include search-box.html %}

{% include search-info.html %}

{% include list.html data="citations" component="citation" filter="(id && !id.to_s.empty?) and (date && !date.to_s.empty?) and (authors && !authors.empty?) and (publisher && !publisher.to_s.empty?)" %}
