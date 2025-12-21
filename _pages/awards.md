---
layout: single
author_profile: true
permalink: /awards/
title: "Awards"
excerpt: "Grants, Awards and Honours"
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/banner3.jpg
  image_description: "Armourers and Brasiers' Postdoctoral Prize award in 2024."
last_modified_at: 2025-12-21
toc: false
---
Along my journey, I’ve been honoured to receive support and recognition from organisations and communities that shaped my work.
Here are some of the grants, awards, and honours that have played a meaningful role in that path.

{% assign awards = site.data.awards | sort: "year" | reverse %}

<table class="awards-table">
  <thead>
    <tr>
      <th>Year</th>
      <th>Award</th>
      <th>Body</th>
      <th>Ref</th>
      <th>Amount</th>
      <th>Type</th>
    </tr>
  </thead>
  <tbody>
  {% for award in awards %}
    <tr>
      <td>{{ award.year }}</td>
      <td>{{ award.title }}</td>
      <td>{{ award.award_body }}</td>
      <td>{{ award.reference }}</td>
      <td>{{ award.amount }}</td>
      <td>
        {% if award.type == "grant" %}
          <span class="badge badge--grant">💰 Grant</span>
        {% elsif award.type == "prize" %}
          <span class="badge badge--prize">🏅 Prize</span>
        {% elsif award.type == "honour" %}
          <span class="badge badge--honour">🎖️ Honour</span>
        {% else %}
          <span class="badge badge--other">📌 Other</span>
        {% endif %}
      </td>
    </tr>
  {% endfor %}
  </tbody>
</table>