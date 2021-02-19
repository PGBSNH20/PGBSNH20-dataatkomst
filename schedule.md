---
layout: page
title: Schema
permalink: /schedule/
---

Start: {{ site.course-start}}, slut: {{ site.course-end}}


Vecka|Måndag|Tisdag|Onsdag|Torsdag|Fredag
-----|-------|-------|------{% for week in site.data.schedule.weeks %}
{{week.week}}{%- for day in week.days -%}|{% if day.lectures %}**{{ day.lectures[0].start-full | date: "%F"}}**{%- for lecture in day.lectures -%}<br /><br />{{ lecture.start-full | date: "%R"}} - {{ lecture.end-full | date: "%R"}}<br />{{lecture.number}}: [{{lecture.lecture}}]({{ lecture.slug | prepend: site.baseurl }}){%- endfor -%}{% endif %}{%- endfor -%}
{% endfor %}



## Alla lektioner
<ul id="archive">
{% for week in site.data.schedule.weeks %}
      <b>Vecka</b>: {{week.week}}<br/>
      
      {% for day in week.days %}
            {% if day.lectures %}
{% for lecture in day.lectures %}
<li class="archiveposturl">
        <span class="postlower">{{ lecture.start-full | date: "%F"}} - {{day.weekday}}</span><br>
        <span><a href="{{ lecture.slug }}">{{ lecture.lecture }}</a></span><br>
<span class = "postlower">
{{ lecture.description }}</span>
      </li>
      {% endfor %}
            {% endif %}
      {% endfor %}
      
{% endfor %}
</ul>
