&nbsp;

<strong>1. Componentizar vía servicios</strong>

Un componente es una unidad de software que es independientemente reemplazable y actualizable.

<span style="text-decoration: underline;">División de los componentes mediante servicios</span>

La forma de componentizar el software es dividiendolo mediante servicios.

Cada servicio tendrá su propio proceso y utilizarán mecanismos de invocaciones remotas o webservices para comunicarse. Al contrario que se hacía en las aplicaciones monolíticas dónde, al ser un único proceso, toda la información se compartía mediante llamadas a memoria.

Hay que tener cuidado como los dividimos y no llegar a una división extrema

&nbsp;

<span style="text-decoration: underline;">Definir el interface del servicio</span>

Al utilizar servicios deberemos de tener un interface del componente mejor definido y explicitado. Algo que con los lenguajes no tienen.

<span style="text-decoration: underline;">APIs de Grano grueso</span>

Como vamos a realizar muchas invocaciones entre los servicios el interface deberá de ser de grano grueso. No deberemos de realizar microservicios de una sola operación.

El coste de llamda en remoto será mayor que llamar por memoria.

<strong>2. Organizar los servicios alrededor de las capacidades de negocio</strong>

Los servicios se deberán de construir alrededor del una capacidad de negocio. Por lo tanto incluiran el interface de usuario, la capa de negocio y la capa de persistencia.

&nbsp;

<span style="text-decoration: underline;">Equipos Transversales</span>

Como el microservicio tiene todas las capas del software hará que el equipo que trabaje dentro del microservicio tenga todas las funcionalidades de desarrollo (y producción)

<strong>3. Productos, no proyectos</strong>

El desarrollo de un microservicio va desde su definición hasta puesta en PRO y mantenimiento.

En un circuito normal se construye y luego despliega otro equipo o lo mantiene otro.

Ya lo dice Amazon "You build, you run it".

Esto implica que el desarrollador esté en contacto con el producto a diario y con el comportamiento que este tiene en PRO.

De esta forma se ve el desarrollo más como un producto que como un proyecto.

Lo bueno de los microservicios es que es más fácil de implementar este modelo que con una aplicación monolítica.

<strong>4. EndPoint Inteligentes y Pipes Mudos</strong>

En integraciones normales se suelen utilizar ESB, la idea de los microservicios es que estén lo más desacoplados posible.

El microservicio recibirá una petición, aplicará una lógica y devolverá una respuesta.

La idea es utilizar peticiones/respuesta http con APIs de recursos y mensajería ligera.

<span style="text-decoration: underline;">Bus de mensajería ligera</span>

En el caso de necesitar un BUS de mensajería, esta solo proporcionarán asincronia y enrutado del mensaje al destino, actuando de forma "muda".

Se utilizará softwar como RabbitMQ o ZeroMQ

<strong>5. Gobierno descentralizado de los Microservicios</strong>

El uso de gobiernos centralizados es la tendencia a estandarizar en una única plataforma tecnológica

Los microservicios eligen su propia plataforma (tanto el negocio como los datos)

Los equipos de microservicios prefieren un acercamiento diferente al de los estándares. En vez de utilizar un conjunto de estándares bien definidos y todo cerrado, prefieren producirse herramientas útiles que otros desarrolladores pueden utilizar para resolver problemas similares.

Incluso llegando a utilzar modelos OpenSource internos.
<ul>
	<li>Esto lo hace mucho Netflix.</li>
</ul>
<strong>6. Gestión de datos descentralizada</strong>

La gestión de datos está descentralizada, se pueden utilizar diferentes sistemas de persistencia. "Persistencia Políglota".

Esta distribución de datos implica gestionar las actualizaciones en los múltiples sistemas de almacenamiento.

El escenario de enfoque suele ser el tener coordinaciones sin transaccionalidad entre los servicios y crear operaciones de compensación por si aparecen fallos en las actualizaciones.

Si bien hay que evaluar bien el escenario, ya que el coste de corregir errores puede llegar a ser menor que el de mantener la consistencia de los datos.

<strong>7. Automatización de la Infraestructura</strong>

Las técnicas de automatización de infraestructura han crecido mucho con el cloud y han reducido la complejidad operacional de los procesos de construcción, despliegue y operación de los microservicios.

Los equipos que desarrollan microservicios están muy acoplados con procesos de despliegue (o integración) continua.

Hay dos puntos muy importantes para los microservicios dentro del despliegue continuo que son los test automatizados y los despliegues automatizados.

<strong>8. Diseñados para fallar</strong>

La llamada a un servicio puede fallar por la indisponibilidad al llamarlo, esto implicará una gestión adicional. Esto es una desventaja en comparación con las aplicaciones monolíticas.

El invocante al servicio deberá de saber qué hacer si el servicio no responde.

<span style="text-decoration: underline;">Monitorización en tiempo real</span>

Las aplicaciones construidas mediante microservicios implican de un alto grado de monitorización en tiempo real. La monitorización será tanto técnica (peticiones por segundo, accesos a la bd,...) como de negocio (cuantos pagos se han ejecutado,...)

Las monitorizaciones semánticas suelen ser una alerta temprana de que algo en el sistema está yendo mal.

<strong>9. Diseño Evolutivo</strong>

La descomposición en servicios puede servir para que los diseños evolutivos la aplicación pueda controlar los cambios sin impactar los tiempos.

Hay que dividir los servicios pensando que haya que reescribir lo menos posible. Es por ello que dirigimos la modularidad atendiendo a un patrón de cambios.

La gestión de versiones en microservicios no debería de ser por nuevas versiones, el servicio debería de ser tolerante y no crear nueva versión, a no ser que no haya más recurso que hacerlo.

<span style="text-decoration: underline;">Los microservicios se utilizan para crear aplicaciones sobre aplicaciones monolíticas ampliando su funcionalidad.</span>
