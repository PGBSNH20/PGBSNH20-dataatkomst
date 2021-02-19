---
layout: page
title: Schema
permalink: /schedule/
---

Start: {{ site.course-start}}, slut: {{ site.course-end}}


Vecka|Måndag|Tisdag|Onsdag|Torsdag|Fredag
-----|-------|-------|------{% for week in site.data.schedule.weeks %}
{{week.week}}{%- for day in week.days -%}|{% if day.parts %}**{{ day.parts[0].start-full | date: "%F"}}**{%- for part in day.parts -%}<br /><br />{{ part.start-full | date: "%R"}} - {{ part.end-full | date: "%R"}}<br />{{part.number}}: [{{part.title}}]({{ part.slug | prepend: site.baseurl }}){%- endfor -%}{% endif %}{%- endfor -%}
{% endfor %}



## Alla lektioner
<ul id="archive">
{% for week in site.data.schedule.weeks %}
      <b>Vecka</b>: {{week.week}}<br/>
      
      {% for day in week.days %}
            {% if day.parts %}
{% for part in day.parts %}
<li class="archiveposturl">
        <span class="postlower">{{ part.start-full | date: "%F"}} - {{day.weekday}}</span><br>
        <span><a href="{{ lecture.slug }}">{{ part.title }}</a></span><br>
<span class = "postlower">
{{ part.description }}</span>
      </li>
      {% endfor %}
            {% endif %}
      {% endfor %}
      
{% endfor %}
</ul>
