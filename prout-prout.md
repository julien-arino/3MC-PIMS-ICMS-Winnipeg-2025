---
title: Prout prout
layout: page
---

# Prout prout 

## Prout prout prooooooout

Je prout prout!


{% for person in site.people %}

    <h2>{{ person.name }} - {{ person.position }}</h2>
    <p>{{ person.content | markdownify }}</p>

    {% assign image = person.photo %}
    {% imagesize image:size?height=200 %}

{% endfor %}