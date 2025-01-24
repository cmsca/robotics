---
layout: default
title: Meeting Summaries
---

# Meeting Summaries

Below is a list of all meeting notes:

{% for file in site.pages %}
  {% if file.path contains 'meetings/' and file.path != 'meetings/index.md' %}
  - [{{ file.title }}](/robotics{{ file.url }})
  {% endif %}
{% endfor %}

[Back to Home](../index.md)
