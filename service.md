---
layout: page
permalink: /service/
title: Service
class: talks
---

{:.hidden}
# Services

{% assign servicetitles = site.data.service | group_by:"title" %}
{% for title in servicetitles %}
{:.service-title}
### {{ title.name }}
{% assign sorted_services = title.items | sort: 'date' | reverse %}
{% for service in sorted_services  %}
  {% include service.html service=service %}
{% endfor %}
{% endfor %}
