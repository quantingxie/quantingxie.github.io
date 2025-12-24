---
permalink: /
title:
author_profile: false
classes: wide
---

{% include base_path %}

<div class="kz-home">
<div class="kz-shell">
  <aside class="kz-sidebar">
    <img class="kz-avatar" src="{{ base_path }}/images/profile.jpg" alt="Quanting Xie">
    <h1 class="kz-side-name">Quanting Xie</h1>
    <p class="kz-side-subtitle">PhD student @ Carnegie Mellon University</p>

    <ul class="kz-side-meta">
      {% if site.author.location %}
      <li><i class="fas fa-fw fa-location-dot" aria-hidden="true"></i><span>{{ site.author.location }}</span></li>
      {% endif %}
      <li><i class="fas fa-fw fa-link" aria-hidden="true"></i><a href="{{ site.url }}{{ site.baseurl }}">{{ site.url | remove: "https://" | remove: "http://" }}</a></li>
      {% if site.author.email %}
      <li><i class="fas fa-fw fa-envelope" aria-hidden="true"></i><a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a></li>
      {% endif %}
      {% if site.author.twitter %}
      <li><i class="fab fa-fw fa-x-twitter" aria-hidden="true"></i><a href="https://x.com/{{ site.author.twitter }}">Twitter</a></li>
      {% endif %}
      {% if site.author.github %}
      <li><i class="fab fa-fw fa-github" aria-hidden="true"></i><a href="https://github.com/{{ site.author.github }}">GitHub</a></li>
      {% endif %}
      {% if site.author.googlescholar %}
      <li><i class="ai ai-google-scholar ai-fw" aria-hidden="true"></i><a href="{{ site.author.googlescholar }}">Google Scholar</a></li>
      {% endif %}
      <li><i class="fas fa-fw fa-file-lines" aria-hidden="true"></i><a href="#cv">CV</a></li>
    </ul>
  </aside>

  <main class="kz-main">

<h2 id="about">About</h2>

<p>I’m a second-year PhD student at the <a href="https://talkingtorobots.com/">CLAW Lab</a> at Carnegie Mellon University (CMU), advised by Prof. <a href="https://yonatanbisk.com/">Yonatan Bisk</a>. I have also had the opportunity to closely work with Prof. <a href="https://www.ri.cmu.edu/ri-faculty/matt-johnson-roberson/">Matthew Johnson-Roberson</a> and Prof. <a href="http://www.cs.cmu.edu/~cga/">Chris Atkeson</a>.</p>

<p><strong>I research robot manipulation and novel hardware to reduce the embodiment gap and sim-to-real gaps in dexterous manipulation.</strong> Previously, I worked on LLM spatial reasoning.</p>

<h2 id="news">News and Olds</h2>

{% if site.data.news %}
<ul class="kz-news">
{% for item in site.data.news %}
  <li><strong>{{ item.date }}</strong>: {{ item.text }}</li>
{% endfor %}
</ul>
{% endif %}

<h2 id="research">Research</h2>

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

<h2 id="experience">Experience</h2>

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

<h2 id="service">Professional Service</h2>

{% if site.data.service %}
<ul>
{% for s in site.data.service %}
  <li>{{ s }}</li>
{% endfor %}
</ul>
{% endif %}

<h2 id="cv">CV</h2>

<p><a href="{{ base_path }}/files/Resume.pdf">Download CV (PDF)</a></p>

<h3>Education</h3>
{% if site.data.education %}
<ul>
{% for item in site.data.education %}
  <li><strong>{{ item.position }}</strong> — {{ item.institution }} ({{ item.time }})</li>
{% endfor %}
</ul>
{% endif %}

<h3>Work</h3>
{% if site.data.work %}
<ul>
{% for item in site.data.work %}
  <li><strong>{{ item.position }}</strong> — {{ item.institution }} ({{ item.time }})</li>
{% endfor %}
</ul>
{% endif %}

<h2 id="misc">Misc</h2>

{% if site.data.misc %}
<ul>
{% for m in site.data.misc %}
  <li>{{ m }}</li>
{% endfor %}
</ul>
{% endif %}

  </main>
</div>
</div>
