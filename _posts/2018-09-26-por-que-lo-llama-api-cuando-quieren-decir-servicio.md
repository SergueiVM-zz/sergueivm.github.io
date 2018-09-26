---
layout: post
title: ¿Por qué lo llaman ~~amor~~ API cuando quieren decir ~~sexo~~ servicio?
tags:
  - reflexiones
categories:
  - articulos
---

Ultimamente se utiliza muy facilmente el término _API REST_, pero realmente queremos en un servicio que ejecute una acción sin más y nos liamos la manta a la cabeza para encajar lo que necesitamos con el término de moda.

<!--more-->

Un _API Rest_ trata de manejar recursos que tienen un modelado que no son puros verbos, sino que representan conceptos de negocio, normalmente son sustamtivos (en singular o en plural), aunque alguna vez nos vemos obligados a diseñar verbos como sustantivos para encajar acciones _determinadas_ que no tendrian cabida dentro de una logica de recursos puros, pero están más o menos _moralmente_ aceptadas.

Pero en otras ocasiones, solamente queremos un verbo, por ejemplo, _sumar_, _contratar_, _convertir_, etc. Son acciones, son verbos que no deben cuyo resultado no persistir en el tiempo, queremos unas _funciones puras_, que reciban unos parametros y devuelvan un resultado sin acciones colaterales.

Pero con la _APItitis_ actual, nos sentimos en la obligación crear un API a toda costa y eso no es sano porque desvirtuamos lo que realmente estamos diseñando.

> — Pero es que yo quiero utilizar REST
— dijo el desarrollador de turno.
>
> — ¿Por qué?
— pregunto yo
>
> — Porqué quiero usar JSON y verbos HTTP

¡¡¡Acabaramos!!! REST es un estandar que usar URIs como recursos y los verbos pero que sea REST no significa que sea API.

Hoy en día están los servicios serverless, acciones que se invocan que se levantan cuando el cliente requiere la operacion y se apagan para _ahorrar_ (tomad esto como una licencia poetica) pero que la forma de actuar pueder perfectamente con JSON y verbos HTTP.

Que quiero decir con esto, que **NO os compliqueis** la vida si quereis hacer un servicio, hacedlo, no necesita ser SOAP, podeis hacerlo REST pero llamadlo por su nombre **SERVICIO REST** un API conlleva un nivel más que en ocasiones entorpece en lugar de ayudar.
