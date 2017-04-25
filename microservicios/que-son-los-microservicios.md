---
ID: 613
post_title: Qué son los Microservicios
author: Víctor Cuervo
post_date: 2016-03-08 10:00:55
post_excerpt: ""
layout: post
permalink: >
  http://www.arquitectoit.com/arquitectura/que-son-los-microservicios/
published: true
gitfolder:
  - microservicios
---
Una de las tendencias en Arquitectura de Software de las que más se viene hablando las últimas fechas (desde el 2014) son los <b>microservicios</b>. Pero, realmente, <em>¿qué son los microservicios? ¿Qué tiene que ver los microservicios con el SOA? ¿Qué nuevas capacidades nos ofrecen dentro del ámbito del desarrollo de </em>aplicaciones?

Quizás, para poderlo explicar deberemos de analizar la situación en la que nos encontrábamos del desarrollo del software y cual es el nuevo enfoque.
<h3><strong>Aplicaciones monolíticas y problemas que conllevan</strong></h3>
Si pensamos en aplicaciones de software uno de los enfoques de diseño es el de construir <strong>aplicaciones monolíticas</strong>. En este enfoque todo el software que desarrollamos de una aplicación se construye de manera conjunta, apoyándonos sobre diferentes librerías o frameworks y realizando un despliegue masivo de la aplicación.

El diseño de aplicaciones monolíticas trae consigo una serie de problemas o inconvenientes:
<ul>
 	<li>El tiempo invertido en realizar un pequeño cambio y desplegarlo en PRO</li>
 	<li>Capacidad de absorber nuevas necesidades en el software que se está desarrollando.</li>
 	<li>Ante un cambio, hay que probar toda la aplicación. Hay que tener arrancada toda la aplicación aunque hagas pruebas unitarias.</li>
 	<li>Ante un cambio hay que volver a desplegar toda la aplicación y rearrancarla.</li>
 	<li>Al ser un solo proceso se ejecuta una sola vez y el escalado deberá de ser detrás de un balanceador que escale de forma horizontal por varias instancias.</li>
 	<li>En los circuitos de desarrollo, cambios, despliegue y pruebas queda tan poco tiempo entre release y release que es complejo realizar la gestión de versiones/release llegando a complicar mucho la gestión del software.</li>
</ul>
<blockquote>Esto no quiere decir que el desarrollo de aplicaciones monolíticas no sea una solución. Hay casos en los que es una buena opción.</blockquote>
<h3><b>Nuevas tendencias en el desarrollo del software</b></h3>
Los <strong>microservicios</strong> no han llegado al diseño del software de la noche a la mañana, si no, que hay un conjunto de tendencias que han hecho que el escenario sea favorable.
<ul>
 	<li>Mejora en los procesos de integración continua y despliegue de software</li>
 	<li>Consolidación de los API mediante sistemas RESTful como sistemas de integración.</li>
 	<li>Necesidad de acometer nuevas tecnologías como el BigData</li>
 	<li>El cloud con la disponibilidad de entornos de ejecución autoaprovisionados.</li>
 	<li>Implantación de metodologías ágiles, dónde hay un desarrollo dirigido por el usuario en búsqueda de funcionalidad útiles, dentro de un proceso iterativo.</li>
 	<li>Abandono paulatino de los enfoques de factoría del desarrollo del software hacía un modelo más artesanal. Menos ingeniería y más creatividad.</li>
</ul>
<h3><strong>¿Qué resuelven los Microservicios?</strong></h3>
Los microservicios no vienen a resolver un nuevo problema, si no que nos ofrecen una forma diferente de enfocar el desarrollo de aplicaciones. La idea que subyace detrás de las arquitecturas de microservicios es el<em> “divide y vencerás”</em>. El nuevo modelo plantea dividir la aplicación en pequeñas funcionalidades o servicios para implementar la aplicación.

De esta forma podemos hablar de tres planos de la arquitectura de la aplicación:
<h4><b>Arquitectura y Desarrollo de la Aplicación</b></h4>
La aplicación se estructurará en un conjunto de servicios independientes entre sí. Cada uno de los servicios debe de cubrir una funcionalidad clara de negocio. Esta independencia y división permite que su implementación en cuanto a código y persistencia de datos pueda ser políglota.
<h4><b>Gobierno de los Servicios</b></h4>
Los servicios en los que dividamos la aplicación no necesitarán ser gobernados o se aplicará un pequeño gobierno (registro del servicio). Los servicios se comunicarán entre sí mediante protocolos ligeros que no contengan ninguna lógica.
<h4><b>Despliegue y Ejecución</b></h4>
Cada uno de los servicios se puede desplegar de forma independiente, sin afectar al resto. De esta manera se podrán realizar modificaciones del software aisladas en un menor periodo de tiempo. A la hora de ejecutarse los servicios, estos se ejecutarán en procesos diferentes. Buscando el escalado más adecuado para cada uno de los servicios.
<h3><strong>Definición de los Microservicios</strong></h3>
Con todo esto podríamos recurrir para responder a la pregunta de qué son los servicios a la <a href="http://martinfowler.com/microservices/#what">definición de James Lewis y Martin Fowler</a>, la cual nos dice que:
<blockquote><i>“Una Arquitectura de Microservicios ofrece un enfoque de desarrollar una aplicación como un <b>conjunto de pequeños servicios</b>, mediante un <b>enfoque políglota de programación</b> y con <b>diferente sistemas de almacenamiento</b>, que <b>se ejecutan en su propio proceso</b> y que <b>se comunican entre sí mediante mecanismos ligeros http/api, sin necesitar tener una gestión centralizada de los mismos</b>. Los servicios <b>representan capacidades de negocio</b> y <b>son desplegados de forma independiente.</b>"</i></blockquote>