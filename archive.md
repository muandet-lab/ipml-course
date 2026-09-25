---
layout: page
title: Course Archive
permalink: /archive/
---

<ul class="previous-offerings">
{% for course in site.data.offerings %}
  <li>
    <a href="{{ course.path | relative_url }}">{{ course.term }}</a>
    {% if course.university %}&mdash; {{ course.university }}{% endif %}
    {% if course.current %}<strong>(current offering)</strong>{% endif %}
  </li>
{% endfor %}
</ul>
