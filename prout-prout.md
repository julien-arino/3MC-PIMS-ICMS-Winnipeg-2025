---
title: People
layout: page
---

{% for person in site.people %}
    {{ person.name }} - {{ person.position }}
{% endfor %}