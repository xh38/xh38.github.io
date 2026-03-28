---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<div class="publications-intro">
  <p>
    Selected publications are listed below. For complete and updated records, please refer to
    {% if site.author.googlescholar %}
      <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.
    {% else %}
      the links provided in each publication card.
    {% endif %}
  </p>
</div>

{% include base_path %}

<div class="publications-list">
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
</div>
