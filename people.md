---
title: People
layout: page
---

<div>
    {% for person in site.people %}
        <h2>{{ person.name }} - {{ person.position }}</h2>
    {% endfor %}
</div>