---
layout: default
title: experience
permalink: /experience/
---

## experience

<ul class="other-projects">
{% for exp in site.data.experience %}
  <li>
    <div class="project-header">
      <span class="project-name">{{ exp.title }} <span style="font-weight: normal; color: var(--link);">at</span> {{ exp.org }}</span>
      <span class="project-stack" style="text-align: right; color: var(--text); margin-bottom: 0;">{{ exp.dates }}</span>
    </div>
    <div class="project-links-inline">
      <span class="project-stack" style="margin-right: auto; color: var(--link);">{{ exp.stack }}</span>
      {% if exp.page %}<a href="/experience/{{ exp.slug }}">more</a>{% endif %}
      {% if exp.org_url %}<a href="{{ exp.org_url }}">org</a>{% endif %}
    </div>
  </li>
{% endfor %}
</ul>
