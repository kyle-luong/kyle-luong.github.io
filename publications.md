---
layout: default
title: publications
permalink: /publications/
---

## publications

<ol class="pub-list">
{% for pub in site.data.publications %}
  <li>
    <div class="project-header">
      <span class="pub-title">{% if pub.url %}<a href="{{ pub.url }}" target="_blank" rel="noopener">{{ pub.title }}</a>{% else %}{{ pub.title }}{% endif %}</span>
      <span class="pub-venue">{{ pub.venue }} '{{ pub.year | slice: 2, 2 }}</span>
    </div>
    <div class="pub-authors">{{ pub.authors | replace: "Kyle Luong", '<span class="pub-self">Kyle Luong</span>' }}</div>
  </li>
{% endfor %}
</ol>

<p class="pub-footnote">* equal contribution</p>
