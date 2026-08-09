---
layout: page
title: Course Archive
permalink: /archive/
---

Every offering of the course keeps its own permanent address, so material stays
citable years after the semester ends.

<ul class="previous-offerings">
{% for course in site.data.offerings %}
  <li>
    <a href="{{ course.path | relative_url }}">{{ course.term }}</a>
    {% if course.university %}&mdash; {{ course.university }}{% endif %}
    {% if course.current %}<strong>(current offering)</strong>{% endif %}
  </li>
{% endfor %}
</ul>

The full history of the course, including the source of this website, is
available in the [GitHub repository]({{ site.github_repo }}).
