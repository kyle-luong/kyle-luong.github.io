---
layout: default
title: projects
permalink: /projects/
---

## projects

I've completed a few projects that showcase foundational development skills, but I'm now focused on building tools and applications that provide real-world utility and solve meaningful problems for others.

---

### highlighted project(s)

<div class="project-grid">
{% for project in site.data.projects %}
{% if project.highlighted %}
  <div class="project-card">
    <img src="/assets/images/{{ project.image }}" alt="{{ project.title }}">
    <h3>{{ project.title }}</h3>
    <p class="project-stack">{{ project.stack }}</p>
    <p>{{ project.description }}</p>
    <div class="project-links">
      {% if project.page %}<a href="/projects/{{ project.slug }}">read more</a>{% endif %}
      {% if project.website %}<a href="{{ project.website }}">website</a>{% endif %}
      {% if project.github %}<a href="{{ project.github }}">github</a>{% endif %}
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
    <div class="project-header">
      <span class="project-name">{{ project.title }}</span>
      <div class="project-links-inline">
        {% if project.page %}<a href="/projects/{{ project.slug }}">more</a>{% endif %}
        {% if project.website %}<a href="{{ project.website }}">site</a>{% endif %}
        {% if project.github %}<a href="{{ project.github }}">github</a>{% endif %}
      </div>
    </div>
    <div class="project-stack">{{ project.stack }}</div>
  </li>
{% endunless %}
{% endfor %}
</ul>
