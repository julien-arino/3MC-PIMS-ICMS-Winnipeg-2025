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
        <a href="mailto:{{ person.email }}">Email</a>
        <br>
        <a href="{{ person.website }}">website</a>
        <br>
        {{ person.photo }}
    {% endfor %}
</div>