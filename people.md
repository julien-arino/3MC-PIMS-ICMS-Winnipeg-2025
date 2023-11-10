---
title: People
layout: page
---

<div>
    {% for person in site.people %}
        <h2>{{ person.name }} </h2>
        {{ person.position_in_MM }}
        <br>
        {{ person.university }}
        <br>
        {{ person.email }}
        <br>
        {{ person.website }}
        <br>
        {{ person.photo }}
    {% endfor %}
</div>