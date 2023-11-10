---
title: People
layout: page
---

# People
{% for person in site.people %}
    <h2> {{ person.name }} - {{ person.position }} </h2>
{% endfor %}