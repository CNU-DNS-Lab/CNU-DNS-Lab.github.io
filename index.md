---
---

# CNU DNS Lab's Website

Welcome to the website of DNS Lab at Chonnam National University. Here you can find projects conducted in our lab, papers published, members, and contact information.
{% include section.html %}

## Highlights

{% capture text %}

Here you can find a list of select published research by our lab.

{%
  include button.html
  link="research"
  text="See our publications"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/papers.png"
  link="research"
  title="Our Research"
  text=text
%}

{% capture text %}

For projects, code, datasets and other resources check the projects page.

{%
  include button.html
  link="projects"
  text="Browse our projects"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="projects"
  title="Our Projects"
  flip=true
  style="bare"
  text=text
%}

{% capture text %}

Meet the DNS Lab team.

{%
  include button.html
  link="team"
  text="Meet our team"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/team.jpg"
  link="team"
  title="Our Team"
  text=text
%}
