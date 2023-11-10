---
title: People
layout: page
---

<div>
    {% for person in site.people %}
        {{ person.name }} - {{ person.position }}
    {% endfor %}
</div>