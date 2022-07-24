---
title: Home
layout: default
---

This site contains an archive of Spyglass sheets, updated daily at 10am UTC. Sheets are loaded with default Spyglass settings. Dates shown match those [provided by NationStates](https://www.nationstates.net/page=archive/folder=regions) and *not* necessarily those provided by Spyglass on your local machine.

Spyglass is open-source software originally released [here](https://github.com/Derpseh/Spyglass) and released under a [GPLv3](https://github.com/Derpseh/Spyglass/blob/master/LICENSE) license. This site uses a forked version of Spyglass, available [here](https://github.com/esfalsa/spyglass-archive/blob/main/Spyglass-cli.py) and also released under a [GPLv3](https://github.com/esfalsa/spyglass-archive/blob/main/LICENSE) license. The fork is functionally the same as the original, but defaults the length of major update to 3550 seconds, rather than the length of the last major update.

{% assign sheets = site.collections | where: "label", "sheets" | first %}
{% assign files = sheets.files | sort: "name" | reverse %}

{% for file in files %}

- [{{ file.name }}](sheets/{{ file.name }})

{% endfor %}
