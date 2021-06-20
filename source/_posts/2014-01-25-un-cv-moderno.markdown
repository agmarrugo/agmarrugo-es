---
layout: post
title: "Un cv moderno"
date: 2014-02-17 23:04
author: Andres Marrugo
comments: true
published: true
categories: academia
---


Hace ya mucho tiempo que preparo mi *curriculum vit&aelig;* en LaTeX. Durante gran parte de ese tiempo lo he hecho con el [paquete CV][cv] que ayuda a producir un cv sobrio, bien estructurado y elegante. La gran ventaja de LaTeX es que no tienes que preocuparte por el formato, sólo tienes que introducir la información y LaTeX hace su magia al compilar. A continuación muestro un ejemplo

<!-- more -->

[cv]: http://www.ctan.org/tex-archive/macros/latex2e/contrib/cv

<div class="aic" style="width:460px"><img src="http://andresmarrugo.net/es/images/Screenshot%202014-01-25%2011.13.35.png" alt="" width="" height="" border="0" /><br>
*Curriculum vitæ* producido con el paquete CV.</div>

Indudablemente esto es *mucho mejor* que cualquier cv producido en MS Word o procesadores similares. Sin embargo, hace poco más de un año al estar culminando el doctorado, comencé a buscar trabajo y me parecía que era hora de cambiar un poco el estilo del cv. Entre los distintos paquetes disponibles para LaTeX hubo uno que me pareció muy bueno. Era capaz de producir un cv académico, elegante, pero a la vez mucho más estético y divertido. El paquete se llama [moderncv][cvlink], he aquí un ejemplo de mi cv (ahora actualizado)

<div class="aic" style="width:460px"><img src="http://andresmarrugo.net/es/images/Screenshot%202014-01-25%2013.37.05.png" alt="" width="" height="" border="0" /><br>
*Curriculum vitæ* producido con el paquete moderncv.</div>

## Personalización del cv ##

Por supuesto que el paquete permite personalizar muchos aspectos del cv. He aquí algunas opciones o configuraciones que he escogido.

* En mi caso me gusta el estilo azul clásico ``\moderncvtheme[blue]{classic}``.
* La versión en español tiene que ir precedida del paquete ``\usepackage[spanish]{babel}``. 
* Para separar las distintas publicaciones de artículos en revistas, proceedings de congresos, etc. Utilizo 

		\usepackage{multibib}
		\newcites{jour,proc,jourdiv}{{Art\'iculos en Revistas},{Actas en Congresos Revisadas por Pares},{Art\'iculos t\'ecnicos por Invitaci\'on}}

* Esto significa que después de compilar el archivo ``.tex``, debo ejecutar el commando ``bibtex`` independientemente para cada bibliografía (``jour.bbl, proc.bbl, jourdiv.bbl``).
* N.B.1 Sólo hay un archivo ``.bib``, el paquete ``multibib`` me permite producir varias bibliografías o referencias al final de un documento.
* N.B.2 A veces edito manualmente los archivos ``.bbl`` si una referencia no sale exactamente como quiero. Esto es util para cuando un artículo que ha sido aceptado, pero todavía no tiene número o año (bibtex no maneja bien referencias sin año). 
 

El repositorio de mi cv [está disponible en github][github] con todos los archivos necesarios para compilar y producir el cv. Espero que les resulte útil. 

[cvlink]: http://www.ctan.org/tex-archive/macros/latex2e/contrib/moderncv
[github]: https://github.com/agmarrugo/cv "agmarrugo/cv"