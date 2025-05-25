---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<div class="profile">
  <h2>About Me</h2>
  <p>I'm Xu Hao, a second-year (2022-now) Ph.D. student in State Key Lab of CAD&CG at Zhejiang University, advised by Prof. [Xiaogang Jin](http://www.cad.zju.edu.cn/home/jin). I obtained my bachelor degrees in Mechatronic Engineering and Automation from Zhejiang University in 2022.</p>
  
  <h3>Research Interest</h3>
  <p>3D generation.</p>
  
  <h3>Address</h3>
  <p>Zijingang Campus of Zhejiang University, 866 Yuhangtang Rd, Hangzhou 310058, P.R. China.</p>
  
  <h3>Contact</h3>
  <p>[xh38@zju.edu.cn](mailto:xh38@zju.edu.cn) / [haoxu38@outlook.com](mailto:haoxu38@outlook.com)</p>
</div>

## Publications

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}


