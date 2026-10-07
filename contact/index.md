---
title: Contact
nav:
  order: 5
  tooltip: Email, address, and location
---

# {% include icon.html icon="fa-regular fa-envelope" %}Contact

<p class="center">
For any questions, inquiries, or collaboration requests, etc. feel free to contact DNS Lab through one of the options below.
</p>

{%
  include button.html
  type="email"
  text="kyungbaekkim@jnu.ac.kr"
  link="kyungbaekkim@jnu.ac.kr"
%}
{%
  include button.html
  type="phone"
  text="+82-62-530-3438"
  link="+82-62-530-3438"
%}
{%
  include button.html
  type="address"
  tooltip="Our location on Google Maps for easy navigation"
  link="https://maps.app.goo.gl/PYjDM7a6x5no42HW7"
%}

{% include section.html %}

{% capture col1 %}

{%
  include figure.html
  image="images/photo.jpg"
  caption="Lorem ipsum"
%}

{% endcapture %}

{% capture col2 %}

{%
  include figure.html
  image="images/photo.jpg"
  caption="Lorem ipsum"
%}

{% endcapture %}
