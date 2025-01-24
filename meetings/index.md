---
layout: default
title: Meeting Summaries
---

# Meeting Summaries

Below is a list of all meeting notes:

{% assign meetings = site.pages | where_exp: "file", "file.path contains 'meetings/'" | sort: "date" %}
{% for file in meetings %}
  {% unless file.path contains 'meetings/index.md' %}
  - [{{ file.title }}]({{ site.baseurl }}{{ file.url }})
  {% endunless %}
{% endfor %}

[Back to Home]({{ site.baseurl }}/index.md)
