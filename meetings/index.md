---
layout: default
title: Meeting Summaries
---

# Meeting Summaries

Below is a list of all meeting notes:

{% assign meetings = site.pages | where_exp: "file", "file.path contains 'meetings/' and file.path != 'meetings/index.md'" | sort: "date" %}
{% for file in meetings %}
  - [{{ file.title }}]({{ site.baseurl }}{{ file.url }})
{% endfor %}

[Back to Home]({{ site.baseurl }}/index.md)
