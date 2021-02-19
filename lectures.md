---
layout: page
title: Schema
permalink: /lectures/
---

# Lektioner

<ul id="archive">
{% for week in site.data.schedule.weeks %}
      <b>Vecka</b>: {{week.week}}<br/>
      
      {% for day in week.days %}
            {% if day.activities %}
{% for activity in day.activities %}
{% if activity.activity == "lecture" %}
<li class="archiveposturl">
        <span class="postlower">{{ activity.start-full | date: "%F"}} - {{day.weekday}}</span><br>
        <span><a href="{{ activity.slug }}">{{ activity.title }}</a></span><br>
        {% if activity.discussion %}(<i class="fa fa-comments" aria-hidden="true"></i> <a href="{{activity.discussion}}">{{activity.title}}</a>)<br>{% endif %}
<span class = "postlower">
{{ activity.description }}</span>
      </li>
      {% endif %}
      {% endfor %}
            {% endif %}
      {% endfor %}
      
{% endfor %}
</ul>
