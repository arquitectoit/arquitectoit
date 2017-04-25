---
ID: 583
post_title: Oracle Linux en el Docker Hub Registry
author: Víctor Cuervo
post_date: 2015-11-11 09:00:51
post_excerpt: ""
layout: post
permalink: >
  http://www.arquitectoit.com/cloud/oracle-linux-en-el-docker-hub-registry/
published: true
itrans_hidetitle:
  - "0"
itrans_show_slider:
  - "0"
itrans_hide_breadcrumb:
  - "0"
---
Parece que las grandes empresas se están dando cuenta de la relevancia de Docker como plataforma para la creación de contenedores y empaquetado de aplicaciones, así de cómo facilita el despliegue de estas.

El último caso ha sido Oracle, la cual ha subido las<strong> imágenes de Oracle Linux en el Docker Hub Registry. </strong>Dichas imágenes se pueden encontrar en el <a title="Proyecto Docker Oracle Linux" href="https://registry.hub.docker.com/_/oraclelinux/">proyecto Oracle Linux</a>. Ahora mismo se puede encontrar desde la versión 5 hasta la versión 7.1.

La información en detalle de las imágenes de Oracle Linux en el Docker Hub Repository se pueden encontrar dentro de la cuenta oficial de Oracle en Git, en el <a title="Proyecto GIT Docker Library Official Images" href="https://github.com/docker-library/official-images">proyecto Docker Library Official Images</a>.

Dentro de las imágenes de Oracle Linux encontramos un par de funcionalidades que ayudarán en su uso dentro del entorno Docker:
<ul>
	<li><strong>Tecnología Ksplice</strong>, la cual facilita la instalación de parches y actualizaciones en línea, sin necesidad de reiniciar el Kernel. De esta forma se reducen sustancialmente los periodos de inactividad del servicio.</li>
	<li><strong>Unbrekable Enterprise Kernel (UEK)</strong>, el cual permite indicar qué versión del kernel queremos arrancar (Linux 6 o Linux 7) de igual manera que permite mantener compatibilidad entre estas versiones de las aplicaciones desarrolladas.</li>
</ul>
El despliegue de las  imagenes de Oracle Linux en el Docker Hub Registry se suma a <a title="Imágenes Docker de MySQL" href="https://registry.hub.docker.com/_/mysql/">las imágenes, ya existentes, de MySQL</a>. Estas, aunque oficiales, no son mantenidas por Oracle, de momento.