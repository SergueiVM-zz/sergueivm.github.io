---
layout: post
title: "Diseño API Rest - Diseñando URIs"
tags:
  - API Design
categories:
  - articulos
---
El diseño de URIs es la base de un API, en el incluimos los recursos que darán información sobre nuestros recursos, nuestra información de negocio.



<!--more-->
## Diseñando las URIs / los recursos.

Comenzamos con la pregunta del millón de €uros  ¿Qué es una URI (**U**niform **R**esource **I**dentifier)?
Y ponemos una cita para responder a la pregunta.

> The only thing you can use an identifier for is to refer to an object. When you are not dereferencing, you should not look at the contents of the URI string to gain other information
— [Tim Berners-Lee](https://www.w3.org/DesignIssues/Axioms.html){:target="_blank"}

La URI nos identifica los recursos y los recursos son la información que exponemos a los clientes o consumidores del API, por lo tanto un buen diseño de URIs nos facilita el acceso a dicha información.

Debemos seguir el paradigma de una web y trata las URIs como **identificadores opacos**. El cliente/usuario/desarrollador/consumidor no tiene porqué saber cómo se conforma, solo debe saber que es un identificador único y univoco de un recurso.

Formato de un URI:

{% highlight lineos %}

URI = schema “://” autoridad “/” path [“?” query][“#” fragmento]

{% endhighlight %}

Debemos tener en cuenta algunos aspectos
### El slash (“/”) debe usarse para indicar un relación jerárquica, al final de una URI no aporta nada y no se debe incluir.

Las convenciones de un API REST indican que cada parte del path corresponde con un recurso único en un modelo jerarquico.

{% highlight lineos%}
http://api.example.es/ligas/futbol/equipos/athletic-club-de-bilbao
http://api.example.es/ligas/futbol/equipos/fc-barcelona
http://api.example.es/ligas/futbol/equipos/real-madrid
http://api.example.es/ligas/baloncesto/equipos/bilbao-basket
http://api.example.es/ligas/baloncesto/equipos/fc-barcelona
http://api.example.es/ligas/baloncesto/equipos/real-madrid
{% endhighlight %}

Si mostramos esto de una manera más gráfica sería como vemos a continuación.

![Jerarquia de Recursos API](/assets/images/api-jerarquia-deportes.png)


### Se debe usar el guion medio (“-“) para mejorar la legibilidad y no se deben utilizar los guiones bajos (“_”).

### Las URIs deben utilizar las minúsculas para los paths.

Vamos a detenernos es este punto y ver unos ejemplos:

1. http://api.example.es/mi-carperta/mi-doc
  - Es una URI correcta según las reglas que hemos indicado anteriormente.
  
2. http://API.EXAMPLE.ES/mi-carpeta/mi-doc
  - El formato de la URI según la especificación RFC-3986 la considera idéntica a la URI anterior.

3. http://api.example.es/Mi-carpeta/Mi-doc
  - Es distinta a la número 1 y pueden causar confusión innecesaria, la parte _path_ es sensible a mayúsculas y minúsculas.


### Otro aspecto a tener en cuenta cuando diseñemos la URIs es que no se debe incluir las extensiones en las URIs

- http://api.example.es/mi-recurso/pepe
- http://api.example.es/mi-recurso/pepe.json

De esta manera desacoplamos el formato físico (json, xml, texto, etc) de la representación funcional. Más adelante veremos como vamos a solucionar este aspecto.





