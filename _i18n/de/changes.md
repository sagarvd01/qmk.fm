---
title: "Letzte Änderungen in QMK"
layout: qmk-title
permalink: /de/changes/
---

{% for change in site.changes reversed %}
**<a href="{{ change.url }}">{{ change.title }}</a>**   
<a href="{{ change.url }}"><img src="https://img.shields.io/badge/date-{{ change.date | date: "%F" | replace:'-','--' }}-lightgrey.svg" /></a>
<a href="https://github.com/qmk/qmk_firmware/commit/{{ change.commit }}">
    <img src="https://img.shields.io/badge/commit-{{ change.commit }}-000000.svg" />
</a>
<a href="/changes/{{ change.category }}">
    <img src="https://img.shields.io/badge/category-{{ change.category }}-{{ site.data.categories[change.category].color }}.svg" />
</a>
{{ change.excerpt }}

{% endfor %}
