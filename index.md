---
layout: default
---
<h1>Índice</h1>
{% if site.posts.size > 0 %}
<div class="flex-grid">
<section class="col">
  <h1>... por fecha</h1>
  {%for post in site.posts%}
    <a href="{{post.url}}" class="article">
    <article>
      <h2>{{ post.title}} <small>({{post.date | date: "%d/%m/%Y"}})</small></h2>
      <p>{{ post.excerpt}}</p>
    </article>
    </a>
  {%endfor%}
</section>

<section class="col">
  <h1>... por temas</h1>
  {% for tag in site.tags %}
    <section>
      <a href="/{{tag[0]}}"><h2>{{tag[0] | capitalize}}</h2></a>
    
      {%for post in tag[1]%}
        <a href="{{post.url}}" class="article">
        <article>
          <h3>{{ post.title}} <small>({{post.date | date: "%d/%m/%Y"}})</small></h3>
          <p>{{ post.excerpt}}</p>
        </article>
        </a>
      {%endfor%}
    </section>
  {% endfor %}
</section>
</div>
{% else %}
  Hola.
  Estoy remodelando la página como puedes ver. Espero tenerla lista muy pronto.
  Por favor, disculpa las molestias.  
{% endif %}
