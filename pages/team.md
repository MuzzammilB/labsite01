---
layout: page
title: TEAM
permalink: /team/
position: 2
hide: false
---

{% for member in site.data.members %}

<div class="member-card {% if member.profile %}clickable{% endif %}"
     {% if member.profile %}
     onclick="window.location='{{ member.profile | relative_url }}';"
     {% endif %}>

  <div class="member-photo-container">
    <img src="{{ member.image | relative_url }}" alt="{{ member.name }}">
  </div>

  <div class="member-info">

    <h3>{{ member.name }}</h3>

    <p class="member-position">{{ member.position }}</p>

    <p>{{ member.description }}</p>

  </div>

</div>

{% endfor %}


# Alumni

{% for alum in site.data.alumni %}

<div class="alumni-entry">

  <strong>{{ alum.name }}</strong><br>

  {{ alum.position }}

  {% if alum.duration %}
    <br><em>{{ alum.duration }}</em>
  {% endif %}

  {% if alum.current-position %}
    <br>Current position: {{ alum.current-position }}
  {% endif %}

</div>

{% endfor %}
