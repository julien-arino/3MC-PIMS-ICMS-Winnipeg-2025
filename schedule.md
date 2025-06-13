---
title: Schedule
layout: page
---

{% assign csv_data = site.data.schedule-line %}
{% assign instructors = site.people | where: "position_in_school", "Instructor" %}

<h2>Week 1</h2>
<table>
  <thead>
    <tr>
      <th>Day</th>
      <th>Time</th>
      <th>Event</th>
    </tr>
  </thead>
  <tbody>
    {% assign current_day = "" %}
    {% for row in csv_data %}
      {% if row.Week == "Week 1" %}
        {% if row.Day != current_day and current_day != "" %}
          <tr>
            <td colspan="3"></td>
          </tr>
        {% endif %}
        <tr
          {% if row.Event contains "Coffee Break" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event contains "Breakfast" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event contains "Brunch" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event contains "Lunch" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event contains "Dinner" %}style="background-color:  #ffe4b5;"{% endif %}
          {% if row.Event contains "Reception" %}style="background-color:  #ffe4b5;"{% endif %}
          {% if row.Event contains "Project" %}style="background-color:rgb(194, 207, 209);"{% endif %}
          {% if row.Event contains "Supervised Project" %}style="background-color:rgb(175, 202, 206);"{% endif %}
          {% if row.Event contains "Lecture" %}style="background-color:rgb(226, 239, 241);"{% endif %}
        >
          <td>
            {% if row.Day != current_day %}
              <strong>{{ row.Day }}</strong>
              {% assign current_day = row.Day %}
            {% endif %}
          </td>
          <td>{{ row.Time }}</td>
          <td>
            {% assign linked = false %}
            {% for instructor in instructors %}
              {% assign last_name = instructor.last_name %}
              {% if row.Event contains last_name %}
                <a href="{{ site.baseurl }}{{ instructor.url }}">{{ row.Event }}</a>
                {% assign linked = true %}
                {% break %}
              {% endif %}
            {% endfor %}
            {% unless linked %}
              {{ row.Event }}
            {% endunless %}
          </td>
        </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>

<h2>Week 2</h2>
<table>
  <thead>
    <tr>
      <th>Day</th>
      <th>Time</th>
      <th>Event</th>
    </tr>
  </thead>
  <tbody>
    {% assign current_day = "" %}
    {% for row in csv_data %}
      {% if row.Week == "Week 2" %}
        {% if row.Day != current_day and current_day != "" %}
          <tr>
            <td colspan="3"></td>
          </tr>
        {% endif %}
        <tr
         {% if row.Event contains "Coffee Break" %}style="background-color: #ffe4b5;"{% endif %}
         {% if row.Event contains "Brunch" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event contains "Breakfast" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event contains "Lunch" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event contains "Dinner" %}style="background-color:  #ffe4b5;"{% endif %}
          {% if row.Event contains "Reception" %}style="background-color:  #ffe4b5;"{% endif %}
          {% if row.Event contains "Project" %}style="background-color:rgb(194, 207, 209);"{% endif %}
          {% if row.Event contains "Supervised Project" %}style="background-color:rgb(175, 202, 206);"{% endif %}
          {% if row.Event contains "Lecture" %}style="background-color:rgb(226, 239, 241);"{% endif %}
        >
          <td>
            {% if row.Day != current_day %}
              <strong>{{ row.Day }}</strong>
              {% assign current_day = row.Day %}
            {% endif %}
          </td>
          <td>{{ row.Time }}</td>
          <td>
            {% assign linked = false %}
            {% for instructor in instructors %}
              {% assign last_name = instructor.last_name %}
              {% if row.Event contains last_name %}
                <a href="{{ site.baseurl }}{{ instructor.url }}">{{ row.Event }}</a>
                {% assign linked = true %}
                {% break %}
              {% endif %}
            {% endfor %}
            {% unless linked %}
              {{ row.Event }}
            {% endunless %}
          </td>
        </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>