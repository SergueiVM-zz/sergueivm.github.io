---
title: Apuntes tecnológicos del día a día
layout: default
date: 2020-12-29T22:04:07.720Z
last_modified_at: 2020-12-29T22:04:07.720Z
---
Llevo mucho años dedicándome al desarrollo de software y a la tecnología, en este blog voy a ir dejando apuntes/artículos que me han servido para solucionar problemas que he ido encontrando y que creo que a alguien puede interesar.

Puedes encontrar desde como programar un patrón de software determinado en *Java* o *Python* hasta una utilidad que haya descubierto para instalar en Windows y que me ayude a mejorar mi rendimiento cuando trabajo. Desde pequeños trucos hasta los más grandes consejos que pueda darte. Todo tiene cabida en este blog, siempre que este relacionado con la tecnología.

Puedes comprobar cuales son las últimos artículos que he escrito:
{%for post in site.posts%}
- [{{post.title}}]({{post.url}}): {% if post.description %}{{ post.description | strip_newlines }}{%else%}{{ post.excerpt | truncatewords: 50 | strip_newlines | markdownify | strip_html }}{% endif %}
{%endfor%}
