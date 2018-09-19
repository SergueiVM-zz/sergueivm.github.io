---
layout: post
title: "Diseño API Rest - Introducción"
tags:
  - API Design
categories:
  - articulos
---
El diseño  API puede parecer una ciencia oscura si lo miramos desde fuera, pero si nos fijamos un poco, el estándar HTTP nos da directamente unas buenas prácticas para aplicar al diseño.

En esta serie de articulos vamos intentar aclarar algunos aspectos de esta disciplina.

<!--more-->
## ¿Qué es un API REST?

Un API expone un conjunto de datos y funciones para facilitar las interacciones entre programas informáticos y permite intercambiar información. REST es un estilo arquitectónico que se aplica en el diseño de APIs para los servicios web modernos que se apoya en el protocolo HTTP.

Un API REST consiste en montar/ensamblar/interconectar recursos. Este conjunto de recursos es conocido como “Modelo de recursos del API REST” y permite que cualquier cliente que entienda HTTP puede utilizar estos recursos.

Una buena API REST sabe atraer clientes/desarrolladores, hoy en día hay un mercado de APIs.



## ¿Qué pretende un Diseño API REST?
Un diseño API pretende exponer __con calidad__ los recursos para que los clientes puedan utliizarlos. Remarcamos __calidad__ ya que es importante seguir unos criterios que hagan las APIs intuitivas.

Existen tres niveles de calidad que se recogen en un modelo llamado [Richardson Maturity Model](https://martinfowler.com/articles/richardsonMaturityModel.html) en honor a la persona que lo estableció, Leonard Richardson padre de la arquitectura orientada a recursos. 

Estos niveles son:

### Nivel 1: Uso correcto de URIs

Las URL, Uniform Resource Locator , son un tipo de URI, Uniform Resource Identifier, que además de permitir identificar de forma única el recurso, nos permite localizarlo para poder acceder a él o compartir su ubicación. Un diseño correcto de estas URIs nos permitirá usar el API de una manera intuitiva, es por eso que debemos prestar cuidado.
Si pensamos en Diseño de BBDD tradicional, seria como diseñar las entidades de la BBDD y sus relaciones.

### Nivel 2: HTTP

Conocer bien HTTP no es opcional, para diseñar APIs REST los aspectos claves que hay que dominar y tener claros son:
- Métodos HTTP
- Códigos de estado
- Aceptación de tipos de contenido

De esta manera sabremos como nos relacionaremos con los recursos (URIs) que hemos diseñado en el nivel anterior.

### Nivel 3: Hypermedia.
La finalidad que busca describir es bastante sencillo: conectar mediante vínculos las aplicaciones clientes con las APIs, permitiendo a dichos clientes despreocuparse por conocer de antemano del cómo acceder a los recursos.
Con Hypermedia básicamente añadimos información extra al recurso sobre su conexión a otros recursos relacionados con él.

## Conclusión
En siguientes artículos profuncizaremos en como conseguir los niveles que hemos hablado anteriormente. Para que al final podamos conseguir un diseño API que cumpla las expectativas de nuestro clientes y lo suficientemente aclaratorios para que los desarrolladores puedan hacer su trabajo.

## Referencias
- [Arquitecturas REST y sus niveles](https://www.arquitecturajava.com/arquitecturas-rest-y-sus-niveles){:target="_blank"}
- [Wikipedia: REST](https://es.wikipedia.org/REST){:target="_blank"}
- [Conceptos sobre APIs REST](http://asiermarques.com/2013/conceptos-sobre-apis-rest/){:target="_blank"}