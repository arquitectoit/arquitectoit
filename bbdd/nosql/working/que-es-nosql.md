Durante los últimos años estamos sufriendo un proceso de migración de las bases de datos Entidad-Relación (ER) a modelos NOSQL. Quizás la aparición de múltiples estructuras, no estables en el tiempo y con grandes volúmenes de información hayan hecho que los modelos NOSQL se hayan convertido en una solución arquitectural.

Pero vayamos paso a paso, ¿qué es NOSQL?

No se cumple el esquema entidad relación

No hay una estructura predefinida desde un principio. Ojo, esto no es bueno por no pensar, si no por la varianza de la información

&nbsp;

Tipos de Bases de datos NOSQL

<strong>Clave-Valor</strong>

Tienen una estructura con una clave y un valor que suele ser el contenido dinámico. Permiten hacer la distribución atendiendo a la clave. Permiten gran volúmen de lecturas e inserciones siempre atendiendo a la clave. ¿¿¿ Pueden atacar a la información contenida en el valor??

Almacenan el contenido en un BLOB

Ejemplos de bases de datos clave-valor: <em>BigTable</em> de Google, <em>SimpleDB</em> de Amazon, Cassandra, <em></em><em>Hadoop</em>, <em>Riak</em>, <em>Voldemort</em> y <em>MemcacheDB</em> entre otras.

<strong>Documentos</strong>

Almacenan la información variable en un documento ya sea JSON (BSON si es JSON binario) o XML ¿Son lo mismo las bases de datos XML que las bases de datos NOSQL?

Tienen lenguajes que permiten realizar accesos a los datos del contenido JSON.

Tenemos aquí a MongoDB, CouchDB

<strong>Grafos</strong>

Representan relaciones entre los nodos. Se basan principalmente en las relaciones que existen dentro de los nodos.

Las relaciones pueden tener atributos

Almacenar información de redes sociales (la básica), mapas???

Como bases de datos NOSQL encontramos a Neo4j

<strong>Columnares</strong>

Es un modelo ER girado. ¿Los beneficios son las consultas rápidas pero lentas insercciones?

Un ejemplo es Cassanda, ¿SAP Hana? ¿¿¿Qué más IBM BLU???

&nbsp;

<strong>Qué es la escalabilidad vertical versus la horizontal???</strong>
En las BD NOSQL se basan en el Horizontal? Sharding??

La idea es escalar horizontalmente con mucha información, paralelizando. ¿Pero porque son atómicos?

¿Problemas del ER al insertar? Por ejemplo en DB2 se tiene que buscar la página en la cual se inserta y esto es complejo?

Características de una base de datos NOSQL
<ul>
	<li>No garantiza ACID (Atomicity, Consistency, Isolation, Durability)  - No implementan mecanismos de consistencia (atómicas???). ¿¿¿Se conoce como??? <a title="BASE" href="http://en.wikipedia.org/wiki/Eventual_consistency" target="_blank">BASE</a> (Basically Available Soft-state Eventual Consistency, o coherencia eventual flexible básicamente disponible). http://en.wikipedia.org/wiki/Eventual_consistency</li>
	<li>Se distribuyen los datos en diferentes nodos (¿sharding?)</li>
	<li>Escalan horizontalmente, si se necesita más capacidad de procesamiento se añaden nodos de forma horizontal y ya está.</li>
	<li>Son tolerantes a fallos y tienen redundancia de datos.</li>
	<li>Manejan estructuras variables. Es la base del NOSQL</li>
	<li>No suelen necesitar de JOIN (por lo menos MongoDB) ya que contienen toda la información desnormalizada en el documento.</li>
	<li></li>
</ul>
&nbsp;

&nbsp;

Casos de uso??

Caso de las entidades básicas de una empresa
Los contenidos

<strong>¿Cuándo deberemos de utilizar NOSQL?</strong>

Apoyarnos en sistemas mixtos ER/NOSQL.

Cuando haya que distribuir información

Grandes volúmenes de información??

En algunos casos son utilizadas como sistemas de caché

&nbsp;

&nbsp;
<h3>Bibliografía de Apoyo</h3>
<ul>
	<li><a title="¿Qué es NOSQL?" href="http://codecriticon.com/que-es-nosql/">¿Qué es NOSQL?</a></li>
</ul>
<h3></h3>
Hay que sacar qué artículos se puedes escribir...

&nbsp;
