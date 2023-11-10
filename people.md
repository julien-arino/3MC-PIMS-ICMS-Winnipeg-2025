---
title: People
layout: page
---

<div>
    <table>
    {% for person in site.people %}
        <tr>
            <td>
                <div class="column is-one-fifth-desktop is-one-fifth-fullhd is-one-quarter-tablet">
                    <figure class="image is-64x64">
                        <img class="is-rounded" src="{{site.url}}{{site.baseurl}}{{person.photo}}">
                    </figure>
                </div>
            </td>
            <td>
                <h2>{{ person.name }} </h2>
                {{ person.position_in_MM }}
                <br>
                {{ person.university }}
                <br>
                <a href="mailto:{{ person.email }}">Email</a>
                <br>
                <a href="{{ person.website }}">Website</a>
            </td>
        </tr>
    {% endfor %}
    </table>
</div>