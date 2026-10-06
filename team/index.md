---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# {% include icon.html icon="fa-solid fa-users" %}Team

Meet our Professor, current students in DNS Lab, as well as alumni that worked at DNS Lab during their studies at CNU.
{% include section.html %}

## Professor

{% include list.html data="members" component="portrait" filter="role == 'professor'" %}

## Current Students
### PhD
{% include list.html data="members" component="portrait" filter="role == 'phd' and group != 'alum'" style="phd" %}
### Master
{% include list.html data="members" component="portrait" filter="role == 'master' and group != 'alum'" style="master" %}
### Undergraduate
{% include list.html data="members" component="portrait" filter="role == 'undergrad' and group != 'alum'" style="undergrad" %}

## Alumni

{% include list.html data="members" component="portrait" filter="group == 'alum'" style="alum" %}

{% include section.html %}

{% capture content %}

{% include figure.html image="images/group1.jpg" %}
{% include figure.html image="images/group2.jpg" %}
{% include figure.html image="images/group3.jpg" %}

{% endcapture %}

{% include grid.html style="square" content=content %}
