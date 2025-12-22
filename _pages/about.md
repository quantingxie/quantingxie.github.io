---
permalink: /
title: "About"
author_profile: true
---

Hello! I am Quanting Xie. I am a second-year PhD student at the [CLAW Lab](https://talkingtorobots.com/) at Carnegie Mellon University (CMU), advised by Prof. [Yonatan Bisk](https://yonatanbisk.com/). I have also had the opportunity to closely work with Prof. [Matthew Johnson-Roberson](https://www.ri.cmu.edu/ri-faculty/matt-johnson-roberson/) and Prof. [Chris Atkeson](http://www.cs.cmu.edu/~cga/).

I currently work on robot manipulation and developing novel hardware to reduce the embodiment gap and sim-to-real gaps in dexterous manipulation. Previously, I worked on LLM spatial reasoning.

## Quick links

- [CV (PDF)](/files/Resume.pdf)
- [Google Scholar](https://scholar.google.com/citations?user=je-4q10AAAAJ&hl=en)
- [GitHub](https://github.com/quantingxie)
- [Email](mailto:quantinx@andrew.cmu.edu)

## Work

{% if site.data.work %}
{% for item in site.data.work %}
- **{{ item.position }}** — {{ item.institution }} ({{ item.time }})
{% endfor %}
{% endif %}

## Education

{% if site.data.education %}
{% for item in site.data.education %}
- **{{ item.position }}** — {{ item.institution }} ({{ item.time }})
{% endfor %}
{% endif %}
