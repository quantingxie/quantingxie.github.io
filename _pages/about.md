---
permalink: /
title:
author_profile: false
classes: wide
---

<div class="kz-header">
  <h1 class="kz-name">Quanting Xie</h1>
  <p class="kz-subtitle">PhD student @ Carnegie Mellon University</p>
  <ul class="kz-meta">
    <li>{% if site.author.location %}{{ site.author.location }}{% endif %}</li>
    <li><a href="{{ site.url }}{{ site.baseurl }}">{{ site.url | remove: "https://" | remove: "http://" }}</a></li>
    <li><a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a></li>
    <li><a href="https://x.com/{{ site.author.twitter }}">Twitter</a></li>
    <li><a href="https://github.com/{{ site.author.github }}">GitHub</a></li>
    <li><a href="{{ site.author.googlescholar }}">Google Scholar</a></li>
    <li><a href="/cv/">CV</a></li>
  </ul>
</div>

## About

I’m a second-year PhD student at the [CLAW Lab](https://talkingtorobots.com/) at Carnegie Mellon University (CMU), advised by Prof. [Yonatan Bisk](https://yonatanbisk.com/). I have also had the opportunity to closely work with Prof. [Matthew Johnson-Roberson](https://www.ri.cmu.edu/ri-faculty/matt-johnson-roberson/) and Prof. [Chris Atkeson](http://www.cs.cmu.edu/~cga/).

**I research robot manipulation and novel hardware to reduce the embodiment gap and sim-to-real gaps in dexterous manipulation.** Previously, I worked on LLM spatial reasoning.

## News and Olds

{% if site.data.news %}
<ul class="kz-news">
{% for item in site.data.news %}
  <li><strong>{{ item.date }}</strong>: {{ item.text }}</li>
{% endfor %}
</ul>
{% endif %}

## Research

<div class="kz-toggle">
  <a href="javascript:void(0)" id="kz-show-selected">Show Selected</a> |
  <a href="javascript:void(0)" id="kz-show-all">Show All</a>
</div>

{% include research_table.html %}

<script>
  (function () {
    function setMode(mode) {
      var rows = document.querySelectorAll('#kz-research-table .kz-research-row');
      rows.forEach(function (row) {
        var selected = row.getAttribute('data-selected') === '1';
        if (mode === 'selected' && !selected) row.classList.add('kz-hidden');
        else row.classList.remove('kz-hidden');
      });
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
<ul>
{% for x in site.data.experience %}
  <li>
    {% if x.org_url %}<a href="{{ x.org_url }}"><strong>{{ x.org }}</strong></a>{% else %}<strong>{{ x.org }}</strong>{% endif %}
    {% if x.location %} — {{ x.location }}{% endif %}
    <em>({{ x.role }}, {{ x.time }})</em>
    {% if x.group %} — {% if x.group_url %}<a href="{{ x.group_url }}">{{ x.group }}</a>{% else %}{{ x.group }}{% endif %}{% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}

## Professional Service

{% if site.data.service %}
<ul>
{% for s in site.data.service %}
  <li>{{ s }}</li>
{% endfor %}
</ul>
{% endif %}

## Misc

{% if site.data.misc %}
<ul>
{% for m in site.data.misc %}
  <li>{{ m }}</li>
{% endfor %}
</ul>
{% endif %}
