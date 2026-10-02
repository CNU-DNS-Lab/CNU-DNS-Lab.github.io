---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# {% include icon.html icon="fa-solid fa-users" %}Team

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

{% include section.html %}

## Professor

{% include list.html data="members" component="portrait" filter="role == 'professor'" %}

## Current Students
### PhD
{% include list.html data="members" component="portrait" filter="role == 'phd'" %}
### Master
{% include list.html data="members" component="portrait" filter="role == 'master'" %}
### Undergraduate
{% include list.html data="members" component="portrait" filter="role == 'undergrad'" %}

## Alumni

{% include list.html data="members" component="portrait" filter="group == "'alum'" %}

{% include section.html %}

{% capture content %}

{% include figure.html image="images/group1.jpg" %}
{% include figure.html image="images/group2.jpg" %}
{% include figure.html image="images/group3.jpg" %}

{% endcapture %}

{% include grid.html style="square" content=content %}
