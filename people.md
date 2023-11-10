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
                {{ person.university }}
                <br>
                <a href="mailto:{{ person.email }}">{{ person.email }}</a>
                <br>
                <a href="{{ person.website }}">Website</a>
                <br>
                {% if person.position_in_MM %}
                    Role in MMI : {{ person.position_in_MM }}
                    <br>
    q            {% endif %}   
                <br>
                {{ person.content | markdownify }}
            </td>
        </tr>
    {% endfor %}
    </table>
</div>