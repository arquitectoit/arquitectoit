---
ID: 135
post_title: 'Layout Adaptable en Diseños &#8220;Sensibles&#8221;'
author: juan.m.garcia.m
post_date: 2012-08-12 19:36:03
post_excerpt: ""
layout: post
permalink: http://www.arquitectoit.com/front-end/layout-adaptable-en-disenos-sensibles/
published: true
---
<h3>Que tu diseño sea "Sensible" al contexto del usuario</h3>
Dentro del ámbito de la Accesibilidad, encontramos un punto muy importante, que todo arquitecto y desarrollador Web debería de tener en cuenta a la hora de plantear la Arquitectura de una nueva Aplicación Web. Me estoy refiriendo a la<strong> adaptación del contenido al dispositivo</strong> que emplea el usuario para acceder a dicha aplicación, tomando de modo adicional el contexto en el que se desenvuelve.

Cuando me refiero al contexto, principalmente, podemos centrarnos en la orientación del dispositivo, la resolución del mismo, etc...

A lo largo de los últimos años, <strong>ha surgido un nuevo paradigma denominado <a title="Definición diseño responsable en Wikipedia (ingles)" href="http://en.wikipedia.org/wiki/Responsive_Web_Design">Responsive Design</a>, que podemos traducir como Diseño Sensible</strong>. El planteamiento del Diseño Responsable se basa,  en tener en cuenta el Dispositivo y el contexto que el usuario emplea para acceder al contenido de modo que:
<ul>
	<li>Dicho contenido se adapte al dispositivo, siendo adaptable a las características del Viewport (espacio donde se muestra el contenido) y <strong>se evita que el usuario deba realizar scroll por nuestras páginas</strong>, impidiendo una experiencia de usuario correcta.</li>
	<li>De modo adicional, también <strong>debe adaptarse al modo de navegación del que dispone el usuario</strong> (si la navegación se va a realizar por teclado, por pantalla táctil, etc...)</li>
	<li><strong>Evitar la duplicidad de páginas</strong> para dar cábida a todos los dispositivos, de modo que <strong>no entremos en un mantenimiento costoso y pesado</strong></li>
	<li>Marcar las <strong>bases para la evolución de nuestra Aplicación Web</strong> a nuevos dispositivos, de un modo ágil</li>
</ul>
<blockquote>El diseño sensible presenta varios aspectos a tener en cuenta, pero en este articulo vamos a enfocarnos a la gestión de las distintas presentaciones (Layouts) de una Aplicación Web diseñada de este modo, siendo adaptadas al llamado Viewport (espacio en el que la página será presentada en el dispositivo que accede a ella).
Recomiendo la lectura, para aquellos que se encuentren cómodos con el ingles, <a title="Articulo Responsible Web Design" href="http://www.alistapart.com/articles/responsive-web-design/" target="_blank">del post de Ethan Marcotte</a></blockquote>
<h3>Distintos clientes, misma necesidad</h3>
Actualmente, nos encontramos con la siguiente necesidad.

<a href="http://www.arquitectoit.com/wp-content/uploads/2012/07/SDR-A1-Layout-Adaptable-Caso.png"><img class="aligncenter size-full wp-image-171" src="http://www.arquitectoit.com/wp-content/uploads/2012/07/SDR-A1-Layout-Adaptable-Caso.png" alt="Necesidad actual: representar contenido adaptado al dispositivo" width="725" height="436" /></a>

A dia de hoy, <strong>nos encontramos con multitud de dispositivos</strong>, que presentan distintas características a las que nuestra Aplicación Web debe tener en cuenta en su diseño:
<ul>
	<li>A nivel hardware, <strong>las pantallas presentan distintas resoluciones</strong>, en incluso algunos, como las tabletas pueden variarla de modo dinámico.</li>
	<li>Ciertos dispositivos son elegidos por usuarios que requieren desarrollar tareas “sobre la marcha” y de modo óptimo, para mejorar su acceso a Internet, por lo que estamos obligados a<strong> presentarle el contenido más importante de un modo accesible</strong></li>
	<li>Los dispositivos presentan distintos navegadores, con distinto soporte a lenguajes de marcas y tecnologías complementarias (javascript, soporte a lenguaje de marcas)</li>
</ul>
<h3>Media Queries, la solución a aplicar</h3>
Para ayudarnos en esta nueva tarea, disponemos de un mecanismo denominado <a href="http://www.w3.org/TR/2012/REC-css3-mediaqueries-20120619/" target="_blank">Media Queries</a>. El objetivo de esta tecnología, cumple con el objetivo que tenemos que cubrir.
<blockquote>Si queremos conocer el soporte actual de los navegadores, <a href="http://caniuse.com/css-mediaqueries" target="_blank">podemos encontrar aquí más información.</a></blockquote>
Por medio del uso de Media Queries, podemos establecer distintas hojas de estilo para lograr que nuestro ntenido se adapte a distintos tipos de medios. Si a este nivel equiparamos los distintos “tipos de medios” a los distintos tipos de dispositivos para los que deseamos que nuestra Aplicación Web, nos encontramos con el siguiente escenario:

<a href="http://www.arquitectoit.com/wp-content/uploads/2012/07/Diseño-Reponsable-Arquitectura.png"><img class="aligncenter size-full wp-image-168" src="http://www.arquitectoit.com/wp-content/uploads/2012/07/Diseño-Reponsable-Arquitectura.png" alt="Diagrama de clases del ejemplo" width="500" height="397" /></a>

Ya sea por el medio que sea, análisis de estadísticas de acceso de dispositivos en Internet, por las necesidades de nuestro cliente o de nuestra empresa; hemos decidido que nuestra aplicación va a realizar la adaptación de su contenido a dos tipos de resoluciones:
<ol>
	<li>Dispositivos con un ancho de resolución menor de 400 pixeles (px), que visualizarán nuestra aplicación con un layout vertical, representando las distintas zonas cada una en una fila</li>
</ol>
<a href="http://www.arquitectoit.com/wp-content/uploads/2012/07/layoutlt400.png"><img class="aligncenter size-full wp-image-170" src="http://www.arquitectoit.com/wp-content/uploads/2012/07/layoutlt400.png" alt="Layout menor de 400 px" width="395" height="615" /></a>
<ol start="2">
	<li>Dispositivos con un ancho de resolución mayor a 400 pixeles (px), que visualizarán nuestra aplicación con un layout que ubique el menú ppal a la izquierda del contenido principal</li>
</ol>
<a href="http://www.arquitectoit.com/wp-content/uploads/2012/07/layougt400.png"><img class="aligncenter size-full wp-image-169" src="http://www.arquitectoit.com/wp-content/uploads/2012/07/layougt400.png" alt="Ejemplo para Layout mayor de 400 px" width="606" height="529" /></a>

Los estilos que son comunes, los vamos a definir en una hoja de estilos CSS (base.css), para ser empleada independientemente de la resolución que tenga el dispositivo con el que accede el usuario.

Este enfoque, nos obliga a tener en cuenta a la hora de diseñar nuestra aplicación, de la importancia que tiene la definición de los estilos CSS y el mejor modo de agruparlo.

Como hemos comentado anteriormente, <strong>media Queries nos va a permitir aplicar una hoja de estilos u otra</strong>, dependiendo de las reglas que establezcamos. En nuestro caso, será el ancho mínimo el valor por el cual la CSS correspondiente será empleada.

Siempre queremos dar soporte a cualquier dispositivo, pero debemos tener en cuenta que el uso de media queries puede tener impacto en cuanto al rendimiento de nuestra Aplicación:
<ul>
	<li><strong>El navegador evalúa variaciones en el viewport</strong>, que provocar hacer el usuario, como cambio del tamaño de la ventana donde visualiza el contenido o variación en la orientación del dispositivo, redimensionar la ventana del navegador. Por esta razón, debemos establecer un límite a la hora de indicar el número de reglas, con el fin de no penalizar el rendimiento en la respuesta del navegador</li>
	<li><strong>Limitar los estilos de las hojas para el layout</strong>, sólo para posicionar contenido de nuestra página y no de presentación</li>
	<li>Si los estilos los tenemos en ficheros CSS, hay que tener en cuenta las peticiones que debe realizar el navegador para no sobrepasar el número optimo</li>
</ul>
<blockquote> Por norma general, las peticiones de recursos desde nuestra página debería de estar entre 6 y 8, contando con las peticiones para otros recursos, como las imágenes)</blockquote>
<h3>Resumen</h3>
Una vez visto el funcionamiento de Media Queries, podemos reconocer una herramienta a tener en cuenta si queremos adaptar la presentación del contenido de nuestras Aplicaciones Web a los distintos dispositivos que pueden emplear nuestros usuarios, y los que puedan aparecer en un futuro (más que próximo).

A la hora de aplicar Media Queries debemos tener en cuenta:
<ul>
	<li>El rendimiento. Hay que tener en cuenta que la modularización que supone su uso, implica añadir peticiones de nuestras páginas. Deberíamos tener siempre como meta, que no se superen las 8 peticiones por página, sobre todo si nuestros usuarios van a acceder con dispositivos móviles.</li>
	<li>Los estilos a incluir en las hojas de estilos. Debido a que el navegador reevalua cualquier cambio en el espacio donde se presenta nuestra página, el hecho de añadir cambios en la presentación de los elementos de nuestra página supone más tiempo de proceso del navegador para aplicarlos. Deberíamos, por tanto, añadir a las hojas de estilo cambios en la disposición de los elementos, e intentar centralizar en una hoja base la presentación de los mismos (color de fondo, fuentes, bordes, etc.)</li>
</ul>
<h3>Herramientas empleadas</h3>
Debido a mi “afición” al software libre, me siento obligado a enumerar las herramientas que he empleado para la realización de este artículo:
<ul>
	<li>Diagramas. Para los diagramas, he empleado la herramienta <a href="http://projects.gnome.org/dia/" target="_blank">DIA</a>. Se puede descargar e instalar desde los repositorios por defecto, en Ubuntu.</li>
	<li>Imágenes. Todas las imágenes han sido redimensionadas con <a href="http://www.gimp.org/" target="_blank">Gimp</a>.</li>
</ul>
