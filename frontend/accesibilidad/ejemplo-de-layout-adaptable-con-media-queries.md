---
ID: 262
post_title: Ejemplo de Layout Adaptable con Media Queries
author: juan.m.garcia.m
post_date: 2012-09-10 09:00:07
post_excerpt: ""
layout: post
permalink: http://www.arquitectoit.com/front-end/ejemplo-de-layout-adaptable-con-media-queries/
published: true
---
<h3>Ejemplo de Diseño Sensible</h3>
Para el desarrollo de este ejemplo, <a title="Layout Adaptable en Diseños “Sensibles”" href="http://www.arquitectoit.com/accesibilidad/layout-adaptable-en-disenos-sensibles/">tomamos el caso descrito en mi anterior articulo a modo de diseño</a>. De este modo, tenemos una página <strong>que va a adaptar su presentación de acuerdo al ancho del dispositivo que accede a ella</strong>.

Este es el Diagrama de Componentes de nuestro ejemplo:

<a href="http://www.arquitectoit.com/wp-content/uploads/2012/07/Diseño-Reponsable-Arquitectura.png"><img class="aligncenter size-full wp-image-168" src="http://www.arquitectoit.com/wp-content/uploads/2012/07/Diseño-Reponsable-Arquitectura.png" alt="Diagrama de clases del ejemplo" width="500" height="397" /></a>
<blockquote>Los estilos que son comunes, los vamos a definir en una hoja de estilos CSS (base.css), para ser empleada independientemente de la resolución que tenga el dispositivo con el que accede el usuario.</blockquote>
Como se puede observar en el diagrama, hemos decidido que nuestra aplicación <strong>va a realizar la adaptación de su contenido a dos tipos de resoluciones</strong>:
<ol>
	<li>Dispositivos con un ancho de <strong>resolución menor de 400 pixeles (px)</strong>, que visualizarán nuestra aplicación con un layout vertical, representando las distintas zonas cada una en una fila</li>
</ol>
<a href="http://www.arquitectoit.com/wp-content/uploads/2012/07/layoutlt400.png"><img class="aligncenter size-full wp-image-170" src="http://www.arquitectoit.com/wp-content/uploads/2012/07/layoutlt400.png" alt="Layout menor de 400 px" width="395" height="615" /></a>
<ol start="2">
	<li>Dispositivos con un ancho de <strong>resolución mayor a 400 pixeles (px)</strong>, que visualizarán nuestra aplicación con un layout que ubique el menú ppal a la izquierda del contenido principal</li>
</ol>
<a href="http://www.arquitectoit.com/wp-content/uploads/2012/07/layougt400.png"><img class="aligncenter size-full wp-image-169" src="http://www.arquitectoit.com/wp-content/uploads/2012/07/layougt400.png" alt="Ejemplo para Layout mayor de 400 px" width="606" height="529" /></a>
<blockquote>Este modo nos va a permitir, el soporte incluso para el mismo usuario en el caso que disponga de un dispositivo con el que pueda variar su orientación</blockquote>
Con el fin de comprobar el cambio en dicha página, la cabecera de dicha página cambiará de color como consecuencia del ancho del dispositivo que accede.

<a href="http://garciamanzanero.eu5.org/ArquitectoIt/DSArticulo1/DSEjemploArticulo1.xhtml" target="_blank">Puedes ver el funcionamiento del ejemplo que vamos a realizar.</a>
<h3>Áreas de la Pagina y su comportamiento</h3>
Nuestro ejemplo, presenta las siguientes secciones:
<ul>
	<li>Una sección que es la cabecera del sitio</li>
	<li>Una barra de menu, con enlaces a otras secciones.</li>
	<li>Una sección, donde los articulos son presentados</li>
	<li>Un pie de página, con un enlace para contactar con el creador de la página</li>
</ul>
Los cámbios que se van producir son los siguiente:
<ol>
	<li><strong>Dispositivos con un máximo de 400 px</strong>. En este caso, las distintas secciones se presentan de modo lineal, una tras la otra. La hoja de estilos, con el nombre Adaptlt400.css, dispone de los siguientes estilos:</li>
</ol>
<pre lang="css">#banner {
  color: black;
  font-size: 1em;
  text-align: center;
  background-color:white;
}</pre>
En este caso, como no queremos alterar las disposiciones de los elementos, cambiamos el color de fondo de la cabecera, a
<ol start="2">
	<li><strong>Dispositivos con un mínimo de 400px</strong>. Los dispositivos que cumplan con esta característica, reciben distinta presentación:</li>
</ol>
<ul>
	<li>La barra de menú se presenta a la izquierda, alineando los distintos enlaces</li>
	<li>La sección con el contenido, se presenta a la derecha del menú</li>
</ul>
Para conseguir ese efecto, creamos la hoja Adaptgt400.css, con los siguientes cambios:

Cambiamos los elementos del menú de navegación, para se presenten como una lista
<pre lang="css">ul
{
  text-align: left;
  list-style-type: none;
  padding: 0;
  margin: 0;
}
li {display: block}
#banner {
  color: white;
  font-size: 1em;
  text-align: center;
  background-color:blue;
}</pre>
Indicamos que queremos que la barra de navegación <strong>se ubique a la izquierda </strong>de la zona de contenidos.
<pre lang="css">#navMenu {
  padding: 0;
  display: block;
  float:left;
  width: 20%;
  height: 100%;
}</pre>
Indicamos que la sección con los artículos, también flote sobre el menú de navegación.
<pre lang="cxss">#workArea {
  float:left;
  width: 80%;
}</pre>
<h3>Aplicar Media Queries a la página</h3>
Para que se aplique la hoja de estilo correspondiente, debemos incluir en nuestra página el enlace a las hojas de estilos.

Para ello, empleamos la etiqueta “link”, añadiendo las dos hojas de estilos:
<pre lang="html4strict"><!-- Estilos-->


<!-- Fin Estilos--></pre>
Como se observa, a primera vista, tenemos un nuevo atributo “media” que es el que vamos a emplear para indicar cuando se debe aplicar cada una de las hojas de estilos.
<h3>Herramientas empleadas</h3>
Debido a mi “afición” al software libre, me siento obligado a enumerar las herramientas que he empleado para la realización de este artículo:
<ul>
	<li><strong>Diagramas</strong>. Para los diagramas, he empleado la herramienta <a href="http://projects.gnome.org/dia/" target="_blank">DIA</a>. Se puede descargar e instalar desde los repositorios por defecto, en Ubuntu.</li>
	<li><strong>Imágenes</strong>. Todas las imágenes han sido redimensionadas con <a href="http://www.gimp.org/" target="_blank">Gimp</a>.</li>
	<li><strong>Desarrollo HTML 5</strong>. Para el desarrollo de la página, he empleado <a title="Sitio de Bluegriffon" href="http://bluegriffon.org/">BlueGriffon</a>.</li>
</ul>
