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
        <a href="{{ person.website }}">Website</a>
        <br>
        <div class="column is-one-fifth-desktop is-one-fifth-fullhd is-one-quarter-tablet">
            <figure class="image is-64x64">
                <img class="is-rounded" src="{{site.url}}{{site.baseurl}}{person.photo}}">
            </figure>
        </div>
    {% endfor %}
</div>