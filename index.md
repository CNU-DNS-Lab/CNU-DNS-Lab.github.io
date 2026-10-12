---
---

# CNU DNS Lab's Website

<p class="center">
Welcome to the website of DNS Lab at Chonnam National University. Here you can find projects conducted in our lab, papers published, members, and contact information.
{% include section.html %}
</p>


## Select Publications:
<div style="margin-left: 2rem; display: flow-root;">
{% include select_references.html data="citations" component="citation" filter="highlight.to_s =~ /front-page/i" limit="5"%}
</div>

## Recent Publications:
<div style="margin-left: 2rem; display: flow-root;">
{% include select_references.html data="citations" component="citation" limit="5"%}
</div>

## Recent News:
<div style="display: flow-root;">
  {% for post in site.posts limit: 5 %}
    {% include post-excerpt.html post=post %}
  {% endfor %}
</div>

## Current Projects:
{% capture col1 %}
<ul>
  {% for project in site.data.projects %}
    {% assign rem = forloop.index0 | modulo: 3 %}
    {% if rem == 0 %}
      <li>{{ project.title }}</li>
    {% endif %}
  {% endfor %}
</ul>
{% endcapture %}

{% capture col2 %}
<ul>
  {% for project in site.data.projects %}
    {% assign rem = forloop.index0 | modulo: 3 %}
    {% if rem == 1 %}
      <li>{{ project.title }}</li>
    {% endif %}
  {% endfor %}
</ul>
{% endcapture %}

{% capture col3 %}
<ul>
  {% for project in site.data.projects %}
    {% assign rem = forloop.index0 | modulo: 3 %}
    {% if rem == 2 %}
      <li>{{ project.title }}</li>
    {% endif %}
  {% endfor %}
</ul>
{% endcapture %}

{% include cols.html col1=col1 col2=col2 col3=col3 %}


## Highlights:

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
  image="images/tomato.jpg"
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
