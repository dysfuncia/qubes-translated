---
lang: de
layout: default
permalink: /de/research/
redirect_from:
- /de/de/de/doc/qubes-research/
- /de/de/de/doc/QubesResearch/
- /de/de/de/wiki/QubesResearch/
ref: 102
title: Research
translated: 'yes'
---

Here are links to various research papers, projects, and blog posts that relate
to Qubes OS.

{% for category in site.data.research.categories %}
  <h3>{{category.name}}</h3>
  <ul class="add-top more-bottom">
  {% for paper in site.data.research.papers %}
    {% if paper.category == category.slug %}
    <li>
      <a href="{{paper.url}}">{{paper.title}}</a> by {{paper.author}}{% if paper.date %}, {{paper.date}}{% endif %}
    </li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}