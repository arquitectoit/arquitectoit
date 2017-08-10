Si estás pensando en utilizar una base de datos NOSQL una de las cosas que debes de conocer es <strong>qué tipos de bases de datos NOSQL existen</strong>. Ya que dependiendo de tus necesidades encajarán mejor de un tipo o de otro.

Vamos a revisar una categorización de los tipos de bases de datos NOSQL. Entre las que encontramos.
<ul>
	<li>Clave/Valor</li>
	<li>Documento</li>
	<li>Columnares</li>
	<li>Grafos</li>
</ul>
<h3>Clave/Valor</h3>
Son bases de datos NOSQL perfectas para almacenar metamodelos de información. Su estructura es muy sencilla ya que lo que se almacena son tuplas de pares clave/valor.

La información de la clave suele contener el nombre de la información que guardamos y el valor el contenido de dicha información.

En las claves, a diferencia de un modelo ER se guardan valores que no tienen por qué tener una relación entre sí. Y que además pueden crecer de forma dinámica sin tener que acudir a modificar un esquema.

Los tipos de bases de datos clave/valor dejan una carga alta a la gestión del metamodelo por parte de la aplicación. Incluidos elementos como las validaciones, formatos,....

Clave - Valor
<h3>Documento</h3>
El contenido que almacenan las bases de datos NOSQL enfocadas en documentos (o documentales) es, como su nombre bien indica, documentos.

Los documentos que suelen almacenar las bases de datos NOSQL de tipo documento suelen ser JSON (o su formato binario BSON) o XML. Aunque, en algunos casos almacenan cualquier otro tipo de documentos.

Los casos de documentos  JSON y XML lo que hacen es definir su esquema mediante el propio documento. En el caso del XML con sus XML-Schema asociados y para el JSON en el contenido embebido.

Un ejemplo de documento JSON para un tipo de base de datos NOSQL orientada a documentos sería:
<pre>{ documento }</pre>
<h3>Grafos</h3>
Las relaciones entre los elementos que almacenamos en una base de datos no tienen por qué ser lineales y de 1 a 1, si no que hay relaciones más complejas que hacen evolucionar los sitemas ER a sistemas de grafos.

&nbsp;

-- Basadas en la teoría de grafos.

&nbsp;

Además en estos sistemas de grafos existe, adicional a la información de los nodos, información relativa a la relación entre dichos nodos. Es decir, cualifica cómo se relacionan los nodos.

Es en este punto dónde nacen las bases de datos NOSQL para grafos. Las bases de datos NOSQL de grafos almacenan los nodos de los grafos, así como las relaciones entre dichos nodos.

&nbsp;

&nbsp;

Algunos ejemplos de bases de datos NOSQL de tipo grafo son: Neo4j,

&nbsp;

&nbsp;
<h3>Columnares</h3>
Aunque se les cataloga como bases de datos NOSQL quizás sean las que están más lejos del NOSQL.

Las bases de datos ER tradicionales se basan en un sistema que almacena la información por filas. En el caso de las bases de datos columnares se da la vuelta y se almacena la información por columnas, en vez de por filas.

El almacenar la información por columnas permite varias cosas: agregar la información de una forma más sencilla (simplificando los informes sobre las tablas y reduciendo el tiempo de respuesta de las queries), comprimir más la información, ya que es más alta la propbabilidad de que se repita una información por columna a que se repita por fila, ....

&nbsp;

Ejemplos de bases de datos columnares son:

SAP Hana

<a title="HP Vertica" href="http://www.vertica.com/" target="_blank">HP Vertica</a>

&nbsp;

&nbsp;

&nbsp;
