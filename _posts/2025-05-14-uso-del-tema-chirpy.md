---
title: Uso del tema Chirpy
author: Hcalmur
date: 2025-05-14 12:37:00 +0800
toc: true
categories: [ti, tech]
tags: [programming, ruby, jekyll, theme]
description: Uso del tema CHIRPY y mi primer post
render_with_liquid: false
---

## Crear el Sitio

Porque crear el sitio, por cuestiones de trabajo (este año puede ser que termine mi contrato laboral después de más de 20 años en MEJOREDU, institución gubernamental dependiente de la SEP), bueno y además para aprovechar los cursos y estudios que he estado adquiriendo para el futuro.

Investigando y aprendiendo, me encuentro con que con [github](https://github.com) me puede servir como host para mi página web (estática) y poder usarla como mi portafolio (aunque sinceramente trabajando en el gobierno, los proyectos no son tan visibles como uno quisiera, pero al menos el decir que se colabora en los proyectos es suficiente, creo).

Como decía, encontré que el uso de [Jekyll](https://jekyllrb.com/), me resultaría en una buena alternativa para desarrollar mi sitio web, de tal forma, que solo me preocupe por la escritura y no tanto en el desarrollo del mismo, aunque como se verá más adelante, es necesario contar con conocimientos técnicos mínimos para solventar algunas de las dificultades a las cuales me tuve que enfrentar y solucionar.


## ¿Por qué usar esta tecnología?

Me resultó mucho más fácil el uso de esta tecnología porque al estar estudiándola, me ofreció la confianza de solo crear el sitio a  partir de las plantilla obtenida de jekyllthemes.org, el colocarlas  en el repositorio personal y a partir de unos cuantos click's, el tener la página web lista y en línea.

Buscando una plantilla que me resultara agradable, elegí la plantilla [Chripy](https://github.com/cotes2020/chirpy-starter). A partir de esta plantilla se puede crear el sitio web de uso personal. Más adelante describiré el paso a paso de cómo lo fui configurando y saltando las pequeñas dificultades que se presentaron.

## Paso a Paso

El primer paso es dirigirnos a la dirección: [chirpy-starter](https://github.com/cotes2020/chirpy-starter), ahí elegiremos la opción  `Usar como plantilla`, una vez que eligamos esa opción nos dirigirá a una nueva página la cual creara el fork de la página hacía tu cuenta, de lo cuál tu debes de poner el nombre que quieras, creando el nuevo sitio en tu cuenta de Github.

![Paso 1](/assets/img/images/01 - Setup-inicial-chirpy.png){: width="700" height="400" }

Una vez concluido el fork del sitio chirpy-starter, el siguiente paso es clonar en tu equipo local para comezar a trabajar, con tu información, que al final de eso se trata el sitio de que solo te pongas a plasmar tus ideas y proyectos sin preocuparte sobre cuestiones técnicas del sitio es solo instalar levantar el servicio de manera local para ver como va tu sitio y tus post y publicarlos, asi de sencillo.

![Paso 2](/assets/img/images/02 - cli.webpage.hcalmur.png)

El siguiente paso es considero el más crucial, ya que para que el sitio web se muestre sin errores y que cuente con todas las librerías si se me permite el termino necesarios para un buen fucnionamiento y es aplicar la instrucción a nivel raíz del proyecto de la instrucción `bundle`, como se muestra en la imagen

![Paso 3](/assets/img/images/03 - Bundle.png)

Una vez concluido el punto anterior, es necesario probarlo a nivel local antes de subir cualquier cambio a nuestro repositorio en Github, para ello debemos de aplicar la siguiente instrucción.

```bash
~/Projects/<username>.github.io/bundle exec jekyll serve
```
A partir de estos simples puntos podremos comenzar a realizar ya nuestro trabajo que es el final lo que buscamos y que es publicar nuestros aprendizajes y vivencias del día a día dentro de nuestro campo que es este caso es el de la #Ciberseguridad.

## Problemas

Eh encontrado algunos problemas que se han presentado, ya trabajando con el proyecto, pero nada que no se pueda solucionar.

1. Es muy importante aplicar esta instrucción nivel raíz del sitio, porque esto lo que va a hacer es compilar el sitio y crear una carpeta denominada `_site` que es el resultado de aplicar la instrucción anterior, y porque es importante realizar esto a nivel raíz del proyecto, porque si lo hacer en cualquier otra carpeta creara la carpeta `_site` dentro esa carpeta y eso no es lo que queremos, además de que podría arruinar la vista del sitio, eso no quiere decir que es un error de Jekyll es un error del ususario por levantar el sitio en la carpeta que no es, como se muestra a continuación.

### Error al levantar el servidor en una carpeta que no es
 ```bash
 ~/Projects/<username>.github.io/**_posts**/bundle exec jekyll serve
```

2. Al momento de clonar el sitio en tu equipo puede ser que al momento de empujar tus cambios al repositorio te encuentres con problemas de que no acepta tu password, esto es fácil de solucionar ya que lo único que tienes que hacer es crear un `tokern personal` este se puede crear en la configuración de tu sitio en la parte que dice desarrollo y ahí elegir la creación del toker personal, es importante elegir la opción de `token clasico` una vez generado, podremos realizar la misma operación de hacer `push` a nuestro sitio y al momento de pedirnos el password colocar ahí el token generado en nuestro repositorio, entiendo que solo se pedira una sola vez en ese equipo, obvio, ese **token no se comparte**.

## Conclusión

El uso de esta tecnología me resulta bastante fácil para personas con pocos conocimientos técnicoas acerca de la creación de sitios web, y que permite que te centres en la creación de contenido.

> - Seguir el [manual de como generar tú primer post](https://chirpy.cotes.page/posts/write-a-new-post/), y como aplicar el _lenguaje de marcado_ aka **Markdown**[¹] en la creación de tu primer publicación, es **bastante sencillo**.
> - La etapa de aprendizaje sobre el uso de toda la herramienta, es considerablemente sencilla.
> - La instalación es completamente transparente.
> - Tal vez si no cuentas con algunos conocimientos sobre el uso de de Github y de la línea de comando puede parecer algo complicado, pero no es así con un curso básico se puede solventar ese tema, al final solo se necesitan unas cuantas línea de comando para usar y publicar tu sitio web **estático**.

---
[¹] Aunque en realidad Markdown también se considera un lenguaje que tiene la finalidad de permitir crear contenido de una manera sencilla de escribir, y que en todo momento mantenga un diseño legible, así que para simplificar puedes considerar Markdown como un método de escritura.
