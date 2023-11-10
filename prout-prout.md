---
title: Prout prout
layout: page
---

# Prout prout 

## Prout prout prooooooout

Je prout prout!


{% for person in site.people %}
    <h2>{{ person.name }} - {{ person.position }}</h2>
    <div class="column is-one-fifth-desktop is-one-fifth-tablet is-one-fifth-fullhd">
        <figure class="image">
            <img class="is-rounded" src="{{ person.photo }}" alt="{{ person.name }}">
        </figure>
    </div>
    <!-- <p>{{ person.content | markdownify }}</p> -->
{% endfor %}