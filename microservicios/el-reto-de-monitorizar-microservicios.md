---
ID: 591
post_title: El reto de monitorizar microservicios
author: Víctor Cuervo
post_date: 2015-11-05 09:00:55
post_excerpt: ""
layout: post
permalink: >
  http://www.arquitectoit.com/arquitectura/el-reto-de-monitorizar-microservicios/
published: true
gitfolder:
  - microservicios
yst_is_cornerstone:
  - ""
---
Interesante charla de <a title="Twitter de Adrian Cockcroft" href="https://twitter.com/adrianco" target="_blank" rel="noopener noreferrer">Adrian Cockcroft</a> sobre <strong>El reto de Monitorizar Microservicios <em> (Monitoring Microservices: A challenge!).</em></strong>

<a title="Twitter de Adrian Cockcroft" href="https://twitter.com/adrianco" target="_blank" rel="noopener noreferrer">Adrian Cockcroft</a> incide en que la propia definición de un microservicio "Loosely coupled service oriented architecture with bounded context" nos da dos de los puntos a tener en cuenta a la hora de monitorizar microservicios. Y es que al ser ligeramente acoplados y al tener su contexto acotado tendremos muchos microservicios que tendrán alguna relación entre sí.

En la monitorización de servicios serán importantes:

<strong>1. Velocidad</strong> - venimos desde datacenters que son auténticos silos, dónde se despliega en meses aplicaciones para toda la vida, pasando por entornos virtualizados, gestión de contenedores para hacer pruebas de test que duran minutos llegando al extremos de entornos que viven milisegundos para ejecutar un paso de un proceso como sucede en los entornos AWS Lambda Events.

<strong>2. Escalado</strong>, como crecer en máquinas para estos entornos tan altamente demandantes. ¿Cómo podemos saber qué uso de CPU tienen nuestros microservicios y cuanta demanda existe?

<strong>3. Flujo de los microservicios</strong>, se deberá de conocer el flujo de los microservicios. Pero dada la cantidad de microservicios que existen se generarán gráficos como el siguiente:

<a href="http://www.arquitectoit.com/wp-content/uploads/2015/03/MonitorizacionMicroServicios.jpg"><img class=" size-full wp-image-593 aligncenter" src="http://www.arquitectoit.com/wp-content/uploads/2015/03/MonitorizacionMicroServicios.jpg" alt="MonitorizacionMicroServicios" width="629" height="437" /></a>

<strong>4. Fallos</strong>, como definir una tolerancia a fallos y controlar las caidas de regiones de microservicios en nuestro sistema.

<strong>5. Testing</strong>, cómo realizar testing sobre los sistemas, sin que estas pruebas de test y simulación sean muy caras.

<strong>6. Simulación</strong>, cómo se pueden simular los diferentes tipos de arquitecturas de microservicios a tener y ver cual sería su comportamiento.

Para este diseño de los flujos, pruebas de test, detección de fallos en arquitecturas de microservicios, <a title="Twitter de Adrian Cockcroft" href="https://twitter.com/adrianco" target="_blank" rel="noopener noreferrer">Adrian Cockcroft</a> ha creado <a title="Spigo" href="https://github.com/adrianco/spigo" target="_blank" rel="noopener noreferrer">la herramienta Spigo</a>, la cual nos ayudará en la definición de este tipo de arquitecturas.

No os perdáis el vídeo sobre <strong>El reto de Monitorizar Microservicios<em> (Monitoring Microservices: A challenge!)</em></strong>

https://www.youtube.com/watch?v=smEuX-Hq6RI

Además os dejo la presentación que iba realizando:

http://www.slideshare.net/adriancockcroft/software-architecture-monitoring-microservices-a-challenge

&nbsp;