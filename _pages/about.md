---
permalink: /
title: "Hao Xu"
excerpt: "Ph.D. Student at Zhejiang University focusing on 3D generation."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<section class="home-about">
  <h2 class="home-about__title">About Me</h2>

  <p class="home-about__intro">
    I am Hao Xu (&#24464;&#28009;), a Ph.D. student (since 2022) in the
    <a href="http://www.cad.zju.edu.cn/">State Key Lab of CAD&amp;CG</a> at
    <a href="https://www.zju.edu.cn/english/">Zhejiang University</a>,
    advised by Prof. <a href="http://www.cad.zju.edu.cn/home/jin">Xiaogang Jin</a>.
    I received my dual B.E. degrees in Mechatronic Engineering and Automation
    from Zhejiang University in 2022.
    My research focuses on <strong>3D generation</strong>.
  </p>

  <div class="home-about__contact">
    <div class="home-about__contact-item">
      <i class="fa-solid fa-envelope" aria-hidden="true"></i>
      <a href="mailto:xh38@zju.edu.cn">xh38@zju.edu.cn</a>
      <span class="home-about__sep">/</span>
      <a href="mailto:haoxu38@outlook.com">haoxu38@outlook.com</a>
    </div>
    <div class="home-about__contact-item">
      <i class="fa-solid fa-location-dot" aria-hidden="true"></i>
      Zijingang Campus, Zhejiang University, 866 Yuhangtang Rd, Hangzhou 310058, China
    </div>
    <div class="home-about__contact-item">
      <i class="fab fa-github" aria-hidden="true"></i>
      <a href="https://github.com/{{ site.author.github }}">{{ site.author.github }}</a>
      {% if site.author.googlescholar %}
        <span class="home-about__sep">|</span>
        <i class="ai ai-google-scholar" aria-hidden="true"></i>
        <a href="{{ site.author.googlescholar }}">Google Scholar</a>
      {% endif %}
    </div>
  </div>
</section>

## Selected Publications

<div class="publications-list home-selected-publications">
  {% assign selected_count = 0 %}
  {% assign sorted_publications = site.publications | sort: "date" | reverse %}
  {% for post in sorted_publications %}
    {% assign excerpt_text = post.excerpt | default: "" | strip %}
    {% assign first_author_token = excerpt_text | split: "," | first | strip %}
    {% assign is_first_author = false %}
    {% if first_author_token contains "**Hao Xu**" %}
      {% assign is_first_author = true %}
    {% endif %}

    {% assign is_siggraph_paper = false %}
    {% if post.venue %}
      {% assign venue_upcase = post.venue | upcase %}
      {% if venue_upcase contains "SIGGRAPH" %}
        {% assign is_siggraph_paper = true %}
      {% endif %}
    {% endif %}

    {% if is_first_author or is_siggraph_paper %}
      {% assign selected_count = selected_count | plus: 1 %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}

  {% if selected_count == 0 %}
    <p class="home-publications-empty">No publication currently matches this filter.</p>
  {% endif %}
</div>

## Work Experience

<div class="experience-list">
  <div class="experience-item">
    <div class="experience-item__header">
      <span class="experience-item__role">Research Intern</span>
      <span class="experience-item__date">Nov 2024 &ndash; Present</span>
    </div>
    <div class="experience-item__org">VAST &middot; Beijing / Remote</div>
    <p class="experience-item__desc">3D generation research</p>
  </div>
  <div class="experience-item">
    <div class="experience-item__header">
      <span class="experience-item__role">Development Intern</span>
      <span class="experience-item__date">Jul &ndash; Sept 2023</span>
    </div>
    <div class="experience-item__org">OPPO &middot; Shanghai</div>
    <p class="experience-item__desc">Audio rendering via path tracing</p>
  </div>
</div>

