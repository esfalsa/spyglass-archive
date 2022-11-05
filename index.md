---
title: Home
layout: default
---

This site contains an archive of Spyglass sheets, updated daily at 10am UTC. Sheets are generated for a minor update length of 3550 seconds and a major update length of 5350 seconds. Dates shown match those [provided by NationStates](https://www.nationstates.net/page=archive/folder=regions) and *not* necessarily those provided by Spyglass on your local machine.

Spyglass is [GPLv3](https://github.com/Derpseh/Spyglass/blob/master/LICENSE)-licensed software originally released [here](https://github.com/Derpseh/Spyglass).

{% assign sheets = site.collections | where: "label", "sheets" | first %}
{% assign files = sheets.files | sort: "name" | reverse %}

{% for file in files %} - [{{ file.name }}](sheets/{{ file.name }})
{% endfor %}
