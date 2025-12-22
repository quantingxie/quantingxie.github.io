---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

You can download a PDF version here: [Resume.pdf](/files/Resume.pdf).

## Education

{% if site.data.education %}
{% for item in site.data.education %}
- **{{ item.position }}** — {{ item.institution }} ({{ item.time }})
{% endfor %}
{% endif %}

## Work experience

{% if site.data.work %}
{% for item in site.data.work %}
- **{{ item.position }}** — {{ item.institution }} ({{ item.time }})
{% endfor %}
{% endif %}

## Service

- Reviewer for CoRL, ICRA, RA-L, IROS

## Publications

<ul>
{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}
</ul>
