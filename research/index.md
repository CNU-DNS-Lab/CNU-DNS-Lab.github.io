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

<p class="center">
  <i>
    *Note that dates listed here might not perfectly reflect the actual publishing date, as some publisher do not provide full dates in their DOI lookup data. Months and dates might be filled in to complete missing information, and will be set to 01 if no data is given. Go to publisher page for full information.
  </i>
</p>
