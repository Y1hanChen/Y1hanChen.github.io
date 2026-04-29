---
layout: page
title: Publications
permalink: /publications/
---

<div class="publications-page">
  <p class="publications-intro">
    My research focuses on improving the reliability and safety of large language models, 
    with applications in AIGC detection and model alignment.
  </p>

  <div class="publications-list">
    {% assign sorted_pubs = site.publications | sort: 'year' | reverse %}
    {% for pub in sorted_pubs %}
      <div class="publication-item">
        <h3 class="pub-title">{{ pub.title }}</h3>
        <p class="pub-authors">{{ pub.authors }}</p>
        <p class="pub-venue">
          <strong>{{ pub.venue }}</strong>
          {% if pub.year %} • {{ pub.year }}{% endif %}
          {% if pub.status %} • <span class="pub-status">{{ pub.status }}</span>{% endif %}
        </p>
        {% if pub.abstract %}
        <p class="pub-abstract">{{ pub.abstract }}</p>
        {% endif %}
        <div class="pub-links">
          {% if pub.pdf %}
          <a href="{{ pub.pdf }}" target="_blank" class="pub-link">
            <i class="fas fa-file-pdf"></i> PDF
          </a>
          {% endif %}
          {% if pub.code %}
          <a href="{{ pub.code }}" target="_blank" class="pub-link">
            <i class="fab fa-github"></i> Code
          </a>
          {% endif %}
          {% if pub.arxiv %}
          <a href="{{ pub.arxiv }}" target="_blank" class="pub-link">
            <i class="ai ai-arxiv"></i> arXiv
          </a>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  </div>
</div>
