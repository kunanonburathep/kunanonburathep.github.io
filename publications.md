---
layout: default
title: "Publications — Kunanon Burathep"
description: "Publications by Kunanon Burathep"
---

# Publications

{% for pub in site.data.publications %}
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
{% endfor %}


<footer>
Last updated: {{ site.time | date: "%B %d, %Y" }}
</footer>
