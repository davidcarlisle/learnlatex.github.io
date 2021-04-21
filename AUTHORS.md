---
layout: "page"
lang: "en"
title: Contributors
permalink: /AUTHORS
---

111

{% if (page.path | split: "/" | first) == page.lang %}

{% for l in site.data.languages %}

{% if l["language-code"] != page.lang %}
<p>{{  l["language-code"] }}{{page.path | remove_first: page.lang}}</p>
{% endif %}

{% endfor %}

{% else %}

english-only

{% endif %}

222

The following people have made contributions to learnlatex.org:

- Barbara Beeton
- David Carlisle
- Paulo Roberto Massa Cereda
- Ulrike Fischer
- Jim Hefferon
- Jérémy Just
- Marcel Fabian Krüger
- Frank Mittelbach
- Phelype Oleinik
- Will Robertson
- Jonathan P. Spratte
- Moritz Wemheuer
- Joseph Wright
- Dung Vu
- Uwe Ziegenhagen
- Denis Bitouzé
- निरंजन
