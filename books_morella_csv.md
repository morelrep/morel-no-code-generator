---
layout: default_csv
title: all books
---
{% capture text_with_newlines %}
Line one
Line two
{% endcapture %}

{{ text_with_newlines | newline_to_br }}

{% capture text_with_newlines %}{% for book in site.books %}{% if book.nacionalidad == "Venezuela" %} ,book,{{ book.year }},{{ book.author }}{% if book.author 2%};{{ book.author2 }}{% endif %}{% if book.author3 %};{{ book.author3}}{% endif %},{{ book.title }},,,,,{{ book.descarga }},,,,,,,,,,,,,,,,,{{ book. Editorial }},{{ book.ciudad }},es,,,{{ book.repositorio }},{{ book.repurl }},{{ book.biblioteca }},,"genre:{{ book.genero}},nacionalidad:{{book.nacionalidad }}","{{ book.content }}",../assets/img/{{book.img}},,,,,,,,,,,,,,,,,,,,,,,{{ book.edicion }},,,,,,,,,,,,,,,,,,,,,,,,,,
{% endif %}{% endfor %}{% endcapture %}

<code>{{ text_with_newlines | newline_to_br }}</code>
