---
ID: 83
post_title: Diseños Web Multimedia con Popcorn
author: Víctor Cuervo
post_date: 2012-06-20 09:00:32
post_excerpt: ""
layout: post
permalink: >
  http://www.arquitectoit.com/front-end/disenos-web-multimedia-con-popcorn/
published: true
enclosure:
  - |
    http://videos.mozilla.org/serv/webmademovies/popcornplug.mp4
    228128
    video/mp4
    
  - |
    http://videos.mozilla.org/serv/webmademovies/popcornplug.ogv
    41057
    video/ogg
    
  - |
    http://videos.mozilla.org/serv/webmademovies/popcornplug.webm
    116618
    video/webm
    
video_type:
  - youtube
video_id:
  - ""
video_poster:
  - ""
slide_template:
  - default
---
La aparición de los elementos <a title="Elemento video de HTML5" href="http://w3api.com/wiki/HTML5:VIDEO">VIDEO</a> y <a title="Elemento audio en HTML5" href="http://w3api.com/wiki/HTML5:AUDIO">AUDIO</a> en <strong>HTML5 ha simplificado la capacidad de insertar elementos multimedia en nuestros diseños webs</strong>. Si bien, el estado primigenio de la especificación HTML5 hace que sea complicado mantener la compatibilidad de código para diferentes navegadores.
<h3>Popcorn: Unificando el elemento VIDEO</h3>
<strong>Popcorn es un proyecto de Mozilla que pretende dar un interface unificado y sencillo para el tratamiento de los elementos multimedia en las páginas web</strong>.

De esta manera, lo primero que nos ofrece Popcorn es el <strong>framework Popcorn.js</strong>, el cual, mediante un sistema de eventos facilita la interacción con los elementos multimedia. Así Popcorn.js nos permite centrarnos en lo que realmente queremos hacer simplificandonos el control y gestión del vídeo.

<strong>Popcorn.js estandariza las propiedades del elemento <a title="Elemento DOM HTMLMediaElement" href="http://w3api.com/wiki/DOM:HTMLMediaElement">HTMLMediaElement</a></strong>. Ya que a día de hoy no tiene una implementación unificada en todos los navegadores. Cada versión del framework tiene unos 1400 test de regresión para asegurar la compatibilidad con los navegadores web.
<h3>Popcorn: Realizando mashups multimedia</h3>
Pero Popcorn no se queda en una simplificación de la gestión de vídeos, si no que su idea es el <strong>poder proporcionar una experiencia multimedia completa al usuario</strong>. De esta forma, el framework Popcorn.js cuenta con multiples funcionalidades para acceder a recursos multimedia: fotos, tweets, wikipedia,... los cuales iremos cargando, mostrando y ocultando en el avance del vídeo.

Alrededor del proyecto Popcorn han nacido un ecosistema de proyectos y librerías que complementan a este framework, dando la posibilidad de extender su uso.

Entre los plugins podemos encontrar: Twitter, Flickr, Lastfm, Linkedin, OpenMap, Wikipedia, Google Maps,...
<h3>A descargarse Popcorn</h3>
Si quieres trabajar con el framework Popcorn.js tienes que saber que la versión actual de Popcorn es <strong>Popcorn 1.2</strong>. Las librerías que necesitarás son:
<ul>
	<li><a title="Popcorn para desarrollo" href="http://popcornjs.org/code/dist/popcorn-complete.js">Librería Popcorn para desarrollo</a></li>
	<li><a title="Librería Popcorn para producción" href="http://popcornjs.org/code/dist/popcorn-complete.js">Librería Popcorn para producción</a></li>
</ul>
Otra opción es <a title="Personalizarse Popcorn mediante un builder" href="http://mozillapopcorn.org/build-tool/">personalizarse la librería de producción mediante un builder</a>.

Si te has descargado Popcorn es bueno que ahora le eches un vistazo a la <a title="Documentación de Popcorn, apis y demos" href="http://popcornjs.org/">documentación de popcorn, sus apis y demos</a>.
<h3>Algo de código con Popcorn</h3>
El uso del framework Popcorn.js es muy sencillo. Veamos algunas pequeñas líneas de código sobre lo que podemos hacer:

Cargando Popcorn:
<pre lang="html4strict"><script src="http://popcornjs.org/code/dist/popcorn-complete.min.js" type="text/javascript"></script><video id="ourvideo" src="http://videos.mozilla.org/serv/webmademovies/popcornplug.mp4" width="300" height="180"><source src="http://videos.mozilla.org/serv/webmademovies/popcornplug.ogv" /><source src="http://videos.mozilla.org/serv/webmademovies/popcornplug.webm" /><object id="ourvideo" width="300" height="180" classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="src" value="http://www.arquitectoit.com/wp-includes/js/tinymce/plugins/media/moxieplayer.swf" /><param name="flashvars" value="url=http%3A//videos.mozilla.org/serv/webmademovies/popcornplug.mp4&amp;poster=/wp-admin/" /><param name="allowfullscreen" value="true" /><param name="allowscriptaccess" value="true" /><embed id="ourvideo" width="300" height="180" type="application/x-shockwave-flash" src="http://www.arquitectoit.com/wp-includes/js/tinymce/plugins/media/moxieplayer.swf" flashvars="url=http%3A//videos.mozilla.org/serv/webmademovies/popcornplug.mp4&amp;poster=/wp-admin/" allowfullscreen="allowfullscreen" allowscriptaccess="true" /></object>    </video></pre>
<div id="footnote"></div>
Creando texto en un momento determinado del vídeo:
<pre lang="javascript">var popcorn = Popcorn( "#ourvideo" );

popcorn.footnote({
  start: 2,
  end: 5,
  target: "footnote",
  text: "Pop!"
});</pre>
Integrando Popcorn con las fotos de Flickr:
<pre lang="javascript">var pop = Popcorn( "#video" );

pop.flickr({
  start: 5,
  end: 15,
  userid: "35034346917@N01",
  target: "flickrdiv"
});</pre>
Integrando Popcorn con el timeline de Twitter:
<pre lang="javascript">pop.twitter({
  start: 5,
  end: 15,
  title: "Steve Song",
  src: "@stevesong",
  target: "twitterdiv",
});</pre>
<h3>Ejemplos de Webs hechas con Popcorn</h3>
Algunas de las demos que puedes visualizar con Popcorn son:
<ul>
	<li><a title="Know your exit" href="http://www.robmorrismusic.com/knowyourexit/" target="_blank">Know you exit</a> - un experimento musical con gente componiendo alrededor del mundo. La composición de música y vídeo queda integrada con tweets de Twitter y geolocalizaciones.</li>
	<li><a title="Zaragoza Public Spaces" href="http://www.samuelnegredo.com/zaragoza-public-spaces/gran-via.htm" target="_blank">Zaragoza Public Spaces</a>, vídeo que nos muestra sitios de interés de Zaragoza integrando localizaciones con Google Maps y texto anexo al vídeo.</li>
	<li><a title="Open Images, Open Data" href="http://rdbg.tuxic.nl:4444/apps/openbeelden" target="_blank">Open Images, Open Data</a> - una iniciativa holandesa que nos muestra como se puede enriquecer un vídeo con contenido multimedia diverso obtenido de Wikipedia, Google Maps, repositorios de los museos de Holanda,...</li>
	<li><a title="Color Tracker" href="http://anavallasuiza.com/popcorn/" target="_blank">Color Tracker</a>, como poder seguir un color dentro del vídeo y añadirle información.</li>
	<li>... <a title="Otras demos con Popcorn" href="http://popcornjs.org/demos" target="_blank">otras demos</a>.</li>
</ul>
<blockquote>Aunque hemos comentado que Mozilla Popcorn es un proyecto que soporta diferentes navegadores, es muy recomendable visualizarlo con Firefox. :-D</blockquote>
<h3>Popcorn Maker (proyecto Butter): editando nuestros vídeos</h3>
Adicionalmente al framework Popcorn.js el proyecto <strong>Popcorn está construyendo Popcorn Maker</strong>. Que es conocido como el proyetco Butter.

<strong>Popcorn Maker es un editor de vídeos en formato web</strong>. De esta forma el editor Popcorn Maker creará de forma dinámica el código del framework Popcorn.js en base a las acciones que definamos: insertar elementos en el vídeo, realizar overlaping,...

Todo <strong>el trabajo con Popcorn Maker se realiza de forma visual</strong>, sin tener que tirar ni una sola línea de código.

<img class="aligncenter size-full wp-image-93" title="popcorn-maker" src="http://www.arquitectoit.com/wp-content/uploads/2012/06/popcorn-maker.png" alt="" width="400" height="251" />

A día de hoy podemos probar la <a title="Preview de Popcorn Maker" href="http://mozillapopcorn.org/popcorn-maker/">Preview de Popcorn Maker</a> y habrá que esperar hasta noviembre 2012 para poder disponer de la primera versión de Popcorn Maker.

Adicionalmente podemos <a title="Código fuente de Popcorn Maker" href="https://github.com/mozilla/butter">bajarnos el código de Popcorn Maker</a>, realizar pruebas, reportar bugs, extenderlo,...

---

Más información sobre el proyecto en <strong><a title="Mozilla Popcorn" href="http://mozillapopcorn.org">Mozilla Popcorn</a></strong> y<strong> <a title="Proyecto Mozilla Popcorn en Twitter" href="https://twitter.com/popcornjs">@popcornjs</a></strong>