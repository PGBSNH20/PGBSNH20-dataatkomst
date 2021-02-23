---
layout: page
title: Schema
permalink: /lectures/
---

<h1>Lektioner</h1>

<ul id="archive">
{% for week in site.data.schedule.weeks %}
  <li>
    <h2 class="mt-4"><strong>Vecka</strong>: {{week.week}}</h2>
    {% for day in week.days %}
      {% if day.activities %}
        {% for activity in day.activities %}
          {% if activity.activity == "lecture" %}
            <div class="archiveposturl mb-4">
              <h5 class="postlower">{{ activity.start-full | date: "%F"}} - {{day.weekday}}</h5>
              <span><a href="{{ activity.slug | prepend: site.baseurl }}">{{ activity.title }}</a></span><br>
              {% if activity.discussion %}
                (<i class="fa fa-comments" aria-hidden="true"></i>
                <a href="{{activity.discussion}}">{{activity.title}}</a>)<br>
              {% endif %}
              <span class = "postlower">
              {{ activity.description }}</span>
              </div>
          {% endif %}
        {% endfor %}
      {% endif %}
    {% endfor %}
  </li>  
{% endfor %}
</ul>
