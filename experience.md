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
      <span class="project-name">{{ exp.title }}</span>
      <span class="exp-dates">{{ exp.dates }}</span>
    </div>
    <div class="exp-org">{{ exp.org }}</div>
    <div class="project-stack">{{ exp.stack }}</div>
  </li>
{% endfor %}
</ul>
