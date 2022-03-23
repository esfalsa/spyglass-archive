---
title: Home
layout: default
---

An archive of Spyglass sheets can be found below. Updated daily at 10am UTC. Sheets are loaded with default Spyglass settings. Dates shown match those [provided by NationStates](https://www.nationstates.net/page=archive/folder=regions), and *not* necessarily those provided by Spyglass on your local machine, which uses the current date you run the program instead.

{% assign sheets = site.collections | where: "label", "sheets" | first %}
{% assign files = sheets.files | sort: "modified_time" | reverse %}

{% for file in files %}

- [{{ file.name }}](sheets/{{ file.name }})

{% endfor %}
