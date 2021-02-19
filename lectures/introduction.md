---
layout: lecture
title: Introduktion till kursen och C# refresh
lectureDate: Måndag den 1:a Mars 2021
permalink: /lectures/introduction
---


Denna lektion är en introduktion till kursen, samt dom första steg med projektet. Fastsällning av grupper.

Delta i diskussionen runt denna lektion: [C# refresh](https://github.com/PGBSNH20/PGBSNH20-dataatkomst/discussions/3)

## Lektionsplan
Lektion från kl. 8:30 till kl. 16:30

* 08:30 Introduktion till kursen
* 09:00 C# refresh

Lunch 12:00 till 13:00

* 16:00 Samling och slut på dag

## Lektionsteori
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

{% for topic in site.data.lecture_csharp_refresh.topics %}
### {{topic.topic}}

{% for mandatory in topic.literature %}
* [{{mandatory.title}}]({{mandatory.url}})
{% endfor %}

<details markdown="1">
<summary>Frivillig fördjupningslitteratur innom {{topic.topic}} (klicka för att visa)</summary>
{% for optional in topic.optionalLiterature %}
* [{{optional.title}}]({{optional.url}})
{% endfor %}
</details>

{% endfor %}


## Uppgift

blala