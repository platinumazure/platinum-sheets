---
layout: default
title: Tales of Symphonia - Last Battle (Decision)
sheet: Tales of Symphonia - Last Battle (Decision)
---
Before anything else, I would like to say "Welcome!" This is my first post, and I'm
glad you are here.

Today's lead sheet is from Tales of Symphonia. It is one of the themes of the final
dungeon, "Last Battle (Decision)", composed by Motoi Sakuraba. Basically, it's one of
the last things you hear before the climactic final confrontation. The strings and oboe
melody fit the somber nature of the final mission, and the arpeggiating piano and
persistent drums propel the tune (and your characters) onward.

{% assign sheet_pages = site.static_files | where: "sheet", "true" | where_exp: "item", "item.basename contains page.sheet" | sort: "basename" %}

{% for sheet_page in sheet_pages %}
![{{ page.sheet }}, Page {{ forloop.index }}]({{ sheet_page.path | relative_url }})
{% endfor %}
