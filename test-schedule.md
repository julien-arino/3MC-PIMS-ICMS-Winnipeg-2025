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
        <tr {% if row.Event == "Coffee Break" %}style="background-color: #f0f8ff;"{% endif %}>
          <td>
            {% if row.Day != current_day %}
              {{ row.Day }}
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
        <tr {% if row.Event == "Coffee Break" %}style="background-color: #f0f8ff;"{% endif %}>
          <td>
            {% if row.Day != current_day %}
              {{ row.Day }}
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