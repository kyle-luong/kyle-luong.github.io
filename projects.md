---
layout: default
title: projects
permalink: /projects/
---

## projects

I've completed a few projects that showcase foundational development skills, but I'm now focused on building tools and applications that provide real-world utility and solve meaningful problems for others.

---

### work in progress
- A schedule routing app/extension
- More secret ideas...

---

### highlighted projects

<div class="project-grid">
{% for project in site.data.projects %}
{% if project.highlighted %}
  <div class="project-card">
    <img src="/assets/images/{{ project.image }}" alt="{{ project.title }}">
    <h3>{{ project.title }}</h3>
    <p class="project-stack">{{ project.stack }}</p>
    <p>{{ project.description }}</p>
    <div class="project-links">
      <a href="/projects/{{ project.slug }}">read more</a>
      {% if project.github %} · <a href="{{ project.github }}">github</a>{% endif %}
    </div>
  </div>
{% endif %}
{% endfor %}
</div>

---

### other projects

<ul class="other-projects">
{% for project in site.data.projects %}
{% unless project.highlighted %}
  <li>
    <a href="/projects/{{ project.slug }}">{{ project.title }}</a>
    <span class="project-stack">{{ project.stack }}</span>
  </li>
{% endunless %}
{% endfor %}
</ul>
