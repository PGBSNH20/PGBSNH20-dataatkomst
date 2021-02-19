---
layout: page
title: Schema
permalink: /schedule/
---

# Schema

Start: {{ site.course-start}}, slut: {{ site.course-end}}


Vecka|Måndag|Tisdag|Onsdag|Torsdag|Fredag
-----|-------|-------|------{% for week in site.data.schedule.weeks %}
{{week.week}}{%- for day in week.days -%}|{% if day.activities %}**{{ day.activities[0].start-full | date: "%F"}}**{%- for activity in day.activities -%}<br /><br />{{ activity.start-full | date: "%R"}} - {{ activity.end-full | date: "%R"}}<br />{{activity.number}}: [{{activity.title}}]({{ activity.slug | prepend: site.baseurl }}){%- endfor -%}{% endif %}{%- endfor -%}
{% endfor %}


