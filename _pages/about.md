---
permalink: /
title:
layout: single
author_profile: true
---

## About

I’m a second-year PhD student at the [CLAW Lab](https://talkingtorobots.com/) at Carnegie Mellon University (CMU), advised by Prof. [Yonatan Bisk](https://yonatanbisk.com/). I have also had the opportunity to closely work with Prof. [Matthew Johnson-Roberson](https://www.ri.cmu.edu/ri-faculty/matt-johnson-roberson/) and Prof. [Chris Atkeson](http://www.cs.cmu.edu/~cga/).

**I research robot manipulation and novel hardware to reduce the embodiment gap and sim-to-real gaps in dexterous manipulation.** Previously, I worked on LLM spatial reasoning.

## News and Olds

{% if site.data.news %}
{% for item in site.data.news %}
- **{{ item.date }}**: {{ item.text }}
{% endfor %}
{% endif %}

## Research

<div class="kz-toggle">
  <a href="javascript:void(0)" id="kz-show-selected">Show Selected</a> |
  <a href="javascript:void(0)" id="kz-show-all">Show All</a>
</div>
<div style="font-size: 0.9rem; color: #666; margin-bottom: 1rem;">
  (*equal contribution, †alphabetical/random authorship)
</div>

<div class="list__wrapper" id="kz-research-grid">
{% assign pubs = site.publications | sort: "date" | reverse %}
{% for post in pubs %}
  {% assign data_selected = "0" %}
  {% if post.selected %}{% assign data_selected = "1" %}{% endif %}
  {% include archive-single-external.html type="list" data_selected=data_selected %}
{% endfor %}
</div>

<script>
  (function () {
    function setMode(mode) {
      var rows = document.querySelectorAll('#kz-research-grid .list__item');
      rows.forEach(function (row) {
        var selected = row.getAttribute('data-selected') === '1';
        if (mode === 'selected' && !selected) row.classList.add('kz-hidden');
        else row.classList.remove('kz-hidden');
      });
      document.getElementById('kz-show-selected').style.fontWeight = (mode === 'selected' ? 'bold' : 'normal');
      document.getElementById('kz-show-all').style.fontWeight = (mode === 'all' ? 'bold' : 'normal');
    }
    var sel = document.getElementById('kz-show-selected');
    var all = document.getElementById('kz-show-all');
    if (sel) sel.addEventListener('click', function () { setMode('selected'); });
    if (all) all.addEventListener('click', function () { setMode('all'); });
    setMode('selected');
  })();
</script>

## Experience

{% if site.data.experience %}
{% for x in site.data.experience %}
<div class="experience-item">
  <div class="experience-info">
    <div class="experience-org">
      {% if x.org_url %}<a href="{{ x.org_url }}">{{ x.org }}</a>{% else %}{{ x.org }}{% endif %}, 
      <span class="experience-location">{{ x.location }}</span>
    </div>
    <div class="experience-role-time">
      {{ x.role }}, {{ x.time }}
    </div>
  </div>
  {% if x.icon %}
  <div class="experience-icon">
    <img src="{{ '/images/' | append: x.icon | relative_url }}" alt="{{ x.org }}">
  </div>
  {% endif %}
</div>
{% endfor %}
{% endif %}

## Professional Service

{% if site.data.service %}
{% for s in site.data.service %}
- {{ s }}
{% endfor %}
{% endif %}

## ☕ Misc

{% if site.data.misc %}
{% for m in site.data.misc %}
- {{ m }}
{% endfor %}
{% endif %}
