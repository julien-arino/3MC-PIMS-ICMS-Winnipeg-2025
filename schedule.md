---
title: Schedule
layout: page
---

{% assign csv_data = site.data.schedule-line %} 

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
            <td colspan="3"></td> <!-- Empty row between days -->
          </tr>
        {% endif %}
        <tr 
          {% if row.Event == "Coffee Break" %}style="background-color: #f0f8ff;"{% endif %}
          {% if row.Event == "Lunch" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event == "Dinner" %}style="background-color: #d3ffd3;"{% endif %}
          {% if row.Event == "Project" %}style="background-color: #f5f5dc;"{% endif %}
        >
          <td>
            {% if row.Day != current_day %}
              <strong>{{ row.Day }}</strong>
              {% assign current_day = row.Day %}
            {% endif %}
          </td>
          <td>{{ row.Time }}</td>
          <td>{{ row.Event }}</td>
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
            <td colspan="3"></td> <!-- Empty row between days -->
          </tr>
        {% endif %}
        <tr 
          {% if row.Event == "Coffee Break" %}style="background-color: #f0f8ff;"{% endif %}
          {% if row.Event == "Lunch" %}style="background-color: #ffe4b5;"{% endif %}
          {% if row.Event == "Dinner" %}style="background-color: #d3ffd3;"{% endif %}
          {% if row.Event == "Project" %}style="background-color: #f5f5dc;"{% endif %}
        >
          <td>
            {% if row.Day != current_day %}
              <strong>{{ row.Day }}</strong>
              {% assign current_day = row.Day %}
            {% endif %}
          </td>
          <td>{{ row.Time }}</td>
          <td>{{ row.Event }}</td>
        </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>