---
layout: default
sitemap: false
---
# Índice
{% if site.posts.size > 0 %}
<div class="flex-grid">
<section class="col">
  <h1>... por orden inverso de publicación</h1>
  {%for post in site.posts%}
    <a href="{{post.url}}" class="article">
      <article>
        <h2>{{ post.title | markdownify }}</h2>
        <p>{{ post.excerpt | truncatewords: 50 | markdownify}}</p>
      </article>
    </a>
  {%endfor%}
</section>

<section class="col">
  <h1>... por temas</h1>
  <ul>
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
      <li><a href="/{{tag[0] | slugify | downcase }}"><strong>{{tag[0] | markdownify | capitalize}}</strong></a></li>
  {% endfor %}
  </ul>
</section>
</div>
{% else %}
Hola!!!

Como podras comprobar estoy remodelando la página por eso aún no hay contenido.

Espero tenerla lista muy pronto, por favor, disculpa las molestias.

Puedes seguirme en las redes sociales que tienes al pie de página o suscribirte al [feed Rss](/feed.xml) para enterarte cuando publico contenidos.
{% endif %}
