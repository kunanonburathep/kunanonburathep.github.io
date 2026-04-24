---
layout: default
title: "Curriculum Vitae — Kunanon Burathep"
description: "CV of Kunanon Burathep, PhD Student at Durham University"
---

# Curriculum Vitae

**Kunanon Burathep** — Ph.D. Student in Computer Science, Durham University

<div class="contact-grid">
  <span>kunanon.burathep(at)durham.ac.uk</span>
  <span>k.burathep(at)gmail.com</span>
</div>
<div class="profile-links">
  <a href="https://scholar.google.com/citations?user=QmBGDF8AAAAJ&hl=en">Google Scholar</a>
  <a href="https://dblp.org/pid/325/6635.html">dblp</a>
  <a href="https://orcid.org/0009-0000-5262-9300">ORCID</a>
  <a href="https://github.com/kunanonburathep">GitHub</a>
  <a href="https://www.linkedin.com/in/kunanonburathep/">LinkedIn</a>
</div>
<p style="margin-top: 1em;"><a href="/assets/CV_Kunanon.pdf">Download CV as PDF</a></p>

---

## Education

{% for edu in site.data.education %}
<div class="edu-item">
  <div class="edu-period">{{ edu.period }}</div>
  <div class="edu-degree">{{ edu.degree }}</div>
  <div class="edu-institution">{{ edu.institution }}, {{ edu.country }}</div>
  {% if edu.supervisors %}
  <div class="edu-supervisors">
    Supervisor{% if edu.supervisors.size > 1 %}s{% endif %}:
    {% for sup in edu.supervisors %}
      <a href="{{ sup.url }}">{{ sup.name }}</a>{% unless forloop.last %} and {% endunless %}
    {% endfor %}
  </div>
  {% endif %}
</div>
{% endfor %}

## Talks & Presentations

{% for talk in site.data.talks %}
<div class="talk-item">
  <div class="talk-type">{{ talk.type }}</div>
  <div><strong>{{ talk.title }}</strong></div>
  <div style="color: var(--text-muted); font-size: 0.9rem;">
    {{ talk.event }}{% if talk.location %}, {{ talk.location }}{% endif %}{% if talk.date %} — {{ talk.date }}{% endif %}
  </div>
</div>
{% endfor %}


## Teaching Experience

{% for teach in site.data.teaching %}
<div class="teach-item">
  <div><span class="teach-role">{{ teach.role }}</span>, {{ teach.institution }}</div>
  <div class="teach-meta">{{ teach.period }}</div>
  <ul class="teach-courses">
    {% for course in teach.courses %}
    <li>{% if course.url %}<a href="{{ course.url }}">{{ course.name }}</a>{% else %}{{ course.name }}{% endif %}</li>
    {% endfor %}
  </ul>
</div>
{% endfor %}


<footer>
Last updated: {{ site.time | date: "%B %d, %Y" }}
</footer>
