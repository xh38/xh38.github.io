---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<div class="publications-intro">
  <p>
    (* denotes corresponding author. <span class="pub-legend pub-legend--first-author"></span> = first-author paper.)
    {% if site.author.googlescholar %}
      For complete records, see <a href="{{site.author.googlescholar}}">Google Scholar</a>.
    {% endif %}
  </p>
</div>

{% include base_path %}

{% assign sorted_pubs = site.publications | sort: "date" | reverse %}
{% assign current_year = "" %}

<div class="publications-list">
  {% for post in sorted_pubs %}
    {% assign pub_year = post.date | date: "%Y" %}
    {% if pub_year != current_year %}
      {% assign current_year = pub_year %}
      <h2 class="publications-year">{{ current_year }}</h2>
    {% endif %}
    {% include archive-single.html %}
  {% endfor %}
</div>
