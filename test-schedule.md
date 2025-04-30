---
title: Schedule
layout: page
---


{% assign csv_data = site.data.schedule-line %} 

<table>
  <thead>
    <tr>
      <th>Week</th>
      <th>Day</th>
      <th>Time</th>
      <th>Event</th>
    </tr>
  </thead>
  <tbody>
    {% for row in csv_data %}
      <tr {% if row.Event == "Coffee Break" %}style="background-color: #f0f8ff;"{% endif %}>
        <td>{{ row.Week }}</td>
        <td>{{ row.Day }}</td>
        <td>{{ row.Time }}</td>
        <td>{{ row.Event }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>