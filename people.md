---
title: People
layout: page
---

<div>
    <h1>Instructors</h1>
    <table>
    {% for person in site.people %}
        {% if person.position_in_school contains "Instructor" %}
                <tr>
                    <td>
                        <div class="column is-one-fifth-desktop is-one-fifth-fullhd is-one-quarter-tablet">
                            <figure class="image is-64x64">
                    {% if person.photo %}
                                    <img class="is-rounded" src="{{site.url}}{{site.baseurl}}{{person.photo}}">
                    {% endif %}
                            </figure>
                        </div>
                    </td>
                    <td>
                        <h2>{{ person.name }} </h2>
                        {{ person.position }} 
                        <br>
                        {{ person.university }}
                        <br>
                        <a href="mailto:{{ person.email }}">{{ person.email }}</a>
                        <br>
                        {% if person.website %}
                            <a href="{{ person.website }}">Website</a>
                            <br>
                        {% endif %}
                        {{ person.content | markdownify }}
                    </td>
                </tr>
        {% endif %}
    {% endfor %}
    </table>

    <h1>Organisation</h1>
    <table>
    {% for person in site.people %}
        {% if person.position_in_school contains "Organiser" %}
                <tr>
                    <td>
                        <div class="column is-one-fifth-desktop is-one-fifth-fullhd is-one-quarter-tablet">
                            <figure class="image is-64x64">
                    {% if person.photo %}
                                    <img class="is-rounded" src="{{site.url}}{{site.baseurl}}{{person.photo}}">
                    {% endif %}
                            </figure>
                        </div>
                    </td>
                    <td>
                        <h2>{{ person.name }} </h2>
                        {{ person.position }} 
                        <br>
                        {{ person.university }}
                        <br>
                        <a href="mailto:{{ person.email }}">{{ person.email }}</a>
                        <br>
                        {% if person.website %}
                            <a href="{{ person.website }}">Website</a>
                            <br>
                        {% endif %}
                        {{ person.content | markdownify }}
                    </td>
                </tr>
        {% endif %}
    {% endfor %}
    </table>
</div>
