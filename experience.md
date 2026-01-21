---
layout: default
title: experience
permalink: /experience/
---

## experience

{% for exp in site.data.experience %}
<span class="date">{{ exp.dates }}</span>  
[{{ exp.title }} at {{ exp.org }}](/experience/{{ exp.slug }})

{% endfor %}
