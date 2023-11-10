---
title: Prout prout
layout: page
---

# Prout prout 

## Prout prout prooooooout

Je prout prout!

<div class="column is-one-fifth-desktop is-one-fifth-tablet is-one-fifth-fullhd">
    <figure class="image">
    </figure>
</div>

{% for person in site.people %}

    <img class="is-rounded" src="{{ person.photo }}" alt="{{ person.name }}">
    <h2>{{ person.name }} - {{ person.position }}</h2>
    <p>{{ person.content | markdownify }}</p>

{% endfor %}