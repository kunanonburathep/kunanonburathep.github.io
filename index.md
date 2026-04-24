---
layout: default
title: "Kunanon Burathep"
description: "PhD student at Durham University working on learning-augmented online algorithms and approximation algorithms."
---

<!-- Profile Section -->
<div class="profile-section">
  <img src="/assets/img/mypic-04.jpg" class="profile-photo" alt="Kunanon Burathep">
  <div class="profile-info">
    <h1>Kunanon Burathep</h1>
    <div class="pronunciation">(Pronunciation: Ku-na-non Bu-ra-thep)</div>
    <div class="affiliation">PhD Student, Department of Computer Science<br>Durham University, United Kingdom</div>
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
  </div>
</div>

---

## About Me

I am a PhD student at Durham University, funded by an [EPSRC Doctoral Studentship](https://gtr.ukri.org/projects?ref=studentship-2919518). I am a member of [ACiD](https://algorithmscomplexity.webspace.durham.ac.uk) (Algorithms and Complexity in Durham) and [NESTiD](https://nestid.webspace.durham.ac.uk) (Network Engineering, Science and Theory in Durham).

My research focuses on **learning-augmented online algorithms**, with a specific focus on online bipartite matching. I also have a strong interest in **approximation algorithms** for graph connectivity problems.

<ul class="research-tags">
  <li class="research-tag">Learning-Augmented Algorithms</li>
  <li class="research-tag">Online Bipartite Matching</li>
  <li class="research-tag">Approximation Algorithms</li>
  <li class="research-tag">Graph Connectivity</li>
</ul>

---

## Selected Publications

{% for pub in site.data.publications %}
{% if pub.selected %}
<div class="pub-item">
  <div class="pub-title"><span class="venue-badge">{{ pub.venue_short }}</span>{{ pub.title }}</div>
  <div class="pub-authors">{{ pub.authors | markdownify | remove: '<p>' | remove: '</p>' }}</div>
  <div class="pub-venue">{{ pub.venue }}, {{ pub.year }}, {{ pub.pages }}</div>
  <div class="pub-links">
    {% if pub.doi %}<a href="{{ pub.doi }}">DOI</a>{% endif %}
    {% if pub.arxiv %}<a href="{{ pub.arxiv }}">arXiv</a>{% endif %}
    {% if pub.pdf %}<a href="{{ pub.pdf }}">PDF</a>{% endif %}
  </div>
</div>
{% endif %}
{% endfor %}

<p style="margin-top: 1em; font-size: 0.93rem;"><a href="/publications">View all publications &rarr;</a></p>


<footer>
Last updated: {{ site.time | date: "%B %d, %Y" }}
</footer>
