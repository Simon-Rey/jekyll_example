---
layout: default
title: Team
---

# Our Team

<div class="team-grid">
  {% for member in site.data.team_data %}
    <div class="team-member">
      <h3>{{ member.name }}</h3>
      <p><strong>{{ member.role }}</strong></p>
      <p>{{ member.bio }}</p>
    </div>
  {% endfor %}
</div>