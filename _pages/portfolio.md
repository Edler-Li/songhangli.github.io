---
layout: archive
title: "Portfolio"
permalink: /portfolio/
author_profile: true
redirect_from:
  - /portfolio
---

{% include base_path %}


Department of Physics and Astronomy, **Franklin & Marshall College** **一** **Lancaster, PA** <br />
_Teaching and Research Assistant_ Spring 2024 - Spring 2025 <br />
• Compared and contrasted two different textbooks and completed textbook exercises to help the professor
mark the key points of instruction for PHY321 Introduction to Electronics. <br />
• Experimented with different teaching kits chosen by the professor to facilitate in selecting a kit that is
more conducive to teaching and learning. <br />


{% for post in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}
