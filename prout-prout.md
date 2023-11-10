---
title: Prout prout
layout: page
---

# Prout prout 

## Prout prout prooooooout

Je prout prout!

<div class="column is-one-fifth-desktop is-one-fifth-tablet is-one-fifth-fullhd">
    <figure class="image">
        <img class="is-rounded" src="{{site.author-image}}" alt="{{site.author-name}}">
    </figure>
</div>

{% for person in site.people %}
  <h2>{{ person.name }} - {{ person.position }}</h2>
  <p>{{ person.content | markdownify }}</p>
{% endfor %}