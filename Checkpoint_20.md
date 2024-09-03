# CHECKPOINT 20

# 1. What is Redux?

Redux es una biblioteca de Javascript y que resulta particularmente útil cuando se trabaja con aplicaciones que requieren el manejo de estados, como REACT. Lo que permite es gestionar el estado de nuestra aplicación de manera global. Es ideal para aplicaciones con un gran número de componentes, cuando los estados de los diferentes componentes se actualizan de manera frecuente, cuando actualizar los estados requiere de una lógica compleja o cuando el código de la aplicación es manejado por varias personas.

## Ventajas de usar Redux:

Redux almacena todos los estados de los diferentes componentes de la aplicación en un objeto llamado store. Esto hace que sea mucho más sencillo acceder y gestionar el estado de los diversos componentes de nuestra aplicación. 

Al poder gestionar los estados de manera centralizada, es ideal para trabajar con aplicaciones grandes con múltiples componentes.

Redux posee además herramientas de desarrollo que permiten ver y entender cómo se actualizan los estados de los diversos componentes de nuestra aplicación.

Sería de utilidad por ejemplo, en una aplicación de eCommerce en la que varios componentes están en funcionamiento de manera simultanea. Por ejemplo, existe la lista de los productos, la lista filtrada en función del criterio de búsqueda, y el carrito en el que se han almacenado algunos productos que ha seleccionado el cliente.

En lugar de actualizar el estado en cada componente, Redux permite que el estado se actualice en la store directamente. Cuando el usuario realiza una búsqueda, se despacha (envía) una acción. 

Una **acción** es un objeto que indica el tipo de cambio a realizar (mediante el campo **type**) y, opcionalmente, los datos relevantes necesarios para esa acción (mediante el campo **payload**). El payload es opcional porque algunas modificaciones de estado no requieren datos adicionales, como resetear un estado, mientras que otras acciones como agregar o eliminar un elemento del carrito, sí requieren información específica para saber de qué elemento se trata.

Luego, el **reducer**, que es una función, se encarga de actualizar el estado en el store. Como resultado, el estado de cualquier componente que dependa de este se actualiza automáticamente. Esto elimina la necesidad de pasar datos entre componentes manualmente, haciendo la gestión del estado más sincronizada y sncilla.

# 2. What is a SQL database?

Las bases de dato SQL son bases de datos relaciones que utilizan un lenguajes de consulta estructurado. Esto significa que se deben seguir ciertas normas o procedimientos preestablecidos a la hora de ingresar datos a la base de datos. Tienen como ventaja que los esquemas que creamos en ellas siguen un orden bien definifo y , gracias eso, mantienen una estructura coherente que permite establecer relaciones entre los diferentes conjuntos de datos. Por ejemplo, entre la tabla de usuarios y los cursos en lso que estos están inscritos.

Las bases SQL tiene múltiples ventajas:

- Permiten relacionar los datos almacenados en sus diferentes tablas.
- Dada la forma como se almacenan los datos, se asegura la integridad de los mismos.
- Permite realizar consultas complejas y generar resúmenes o informes.
- Los datos se almacenan en tablas que si bien están relacionadas, son independientes.

Un ejemplo claro en el que sería ideal utilizar una base de datos SQL sería una plataforma de eCommerce en la cual se necesita vincualar al cliente a los productos que ha seleccionado, así como a sus datos como dirección, id. Y por otro lado vincular el producto con su precio, talla, disponiblilidad, etc. No se puede realizar una acción sin acceder y verificar el resto de datos.

Por otro lado, las bases de datos NoSQL o no relacionales permiten trabajar con datos no estructurados(que son en realidad semi-estructurados). Esto es ideal para datos que se modifican frecuentemente. Un ejemplo claro sería del uso de bases de datos NoSQL sería para almacenar datos en el caché, que no son datos de almacenamiento permanente sino que pueden ser modificados con frecuencia.

Tienen la ventaja de que son más flexibles que la bases de dato SQL a la hora de ingresar datos, sin embargo, dado que si no existe una estructura preestablecida, es el desarrollador quien debe decidir como estructurar esos datos para poder luego realizar las consultas pertinentes (que son más complejas que en bases de datos SQL) y poder acceder a ellos cuando sea necesario. Es decir, es le propio desarrollador el que debe asegurarse de mantener la consistencia en el nombre de los diferentes campos y el tipo de dato a ingresar para cada uno, ya que la base de datos admitirá para el campo "edad" por ejemplo, tanto un string como un entero, o decimal. 

Algunos ejemplos de bases de datos NoSQL son MongoDB, Cassandra, CouchDB, Redis y Neo4j.

# 3. Why do we use MySQL Workbench?

MySQL Workbench es una interfaz gráfica de usuario (GUI) que se utiliza para diseñar y administrar bases de datos MySQL. Las bases de datos pueden trabajarse utilizando la línea de comandos, sin embargo, esta interfaz lo que hace es facilitar el proceso y hacerlo más visual.

## DBeaver

Esta interfaz tiene la ventaja de que es una herramienta universal para el trabajo con bases de datos. La lista de bases de datos que soporta es sumamente extensa e inclute MySQL, SQLite, MariaDB, Microsoft SQL Server, Oracle y muchas más (más de 80, tanto SQL como NoSQL).

Es posible utilizarla desde Mac OS, Windows y sería ideal en el caso de usar Linux.

## phpMyAdmin

Está basada en PHP (lenguaje de programación destinado a desarrollar aplicaciones para la web y crear páginas web). Tanto phpMyAdmin como MySQL Workbench utilizan el mismo motor de base de datos MySQL, por lo que las consultas SQL y comandos que se ejecutan son los mismos. La diferencia radica en la interfaz de usuario y las herramientas adicionales que cada uno ofrece para facilitar la gestión de bases de datos.

PhpMyAdmin se accede a través de un navegador web, lo cual la hace ideal para administración remota y en entornos con acceso limitado a herramientas de escritorio, además permite la adición de algunos plugins y personalizaciones a través de la configuración de PHP, por ejemplo.

## HeidiSQL

Es una interfaz para utilizar con windows, es ligero y más sencillo de usar que MySQL Workbench. Además de Mysql permite trabajar con otros sistemas de gestión de bases de datos como PostgreSQL o SQL Server (de Microsoft). Tiene como desventaja que sólo está disponible para Windows.

## Sequel Pro

Es una interfaz gráfica de usuario para Mac OS. Es simple y fácil de usar. Tiene como desventaja que solo soporta MySQL y nop puede usarse en otros sistemas operativos.

## MyDB Studio

Es menos popular que las mencionadas anteriormente. Admite varios sistemas de bases de datos SQL, incluidos MySQL, PostgreSQL, SQL Server y Oracle. Es fácil de usar.

## SQLyogMySQL GUI

AL igual que MyDB Studio es menos conocida que las mencionadas anteriormente.  Proporciona un editor SQL con autocompletado y resaltado de sintaxis. Permite la sincronización de esquemas y datos entre diferentes servidores MySQL. La interfaz es fácil de usar.

Existen además más alternativas como DataGrip y Navicat for MySQL, siendo estas de pago.

# 4. What are some SQL Data Types?

Los tipos de datos pueden variar en función de la base de datos con la que se esté trabajando. En el caso de MySQL los principales tipos de datos incluyen:

## TIPOS DE DATOS NUMÉRICOS

## Enteros (INTEGER, full integer, INT )

Se refiere a datos numéricos, concretamente a números enteros dentro de un rango que va desde con un rango de -2,147,483,648 a 2,147,483,647. Si hay decimales estos se truncarán.  

Existen variantes de los integers como **TINYINT, SMALLINT, MEDIUMINT, BIGINT** para diferentes rangos de valores. La elección de uno u otro dependerá de las necesidades de nuestra base de datos. Por ejemplo, un tinyint será suficiente para la edad de una persona, pero podría no ser suficiente para representar valores más grandes, como el saldo de una cuenta bancaria, el sueldo de una persona o sus gastos mensuales. 

La elección del tipo de entero adecuado depende del contexto y de los límites máximos y mínimos que se esperan para los datos almacenados.

---------------------------------------------------------------------------------------------------------------
| **Tipo de datos** | **Intervalo**                                                                           |
|-------------------|-----------------------------------------------------------------------------------------|
| `BIGINT`          | De -9,223,372,036,854,775,808 a 9,223,372,036,854,775,807                               |
| `MEDIUMINT`       | De -8,388,608 a 8,388,607                                                               |
| `INT`             | De -2,147,483,648 a 2,147,483,647                                                       |
| `SMALLINT`        | De -32,768 a 32,767                                                                     |
| `TINYINT`         | De 0 a 255 (unsigned) o de -128 a 127 (signed --cuando se almacenan valores negativos)  |
---------------------------------------------------------------------------------------------------------------

Si bien algunos tipos de datos engloban a otros, por ejemplo, BIGINT tiene en su rango incluidos a todos los demás, la elección del tipo de dato se realiza en función del rango de valores con el que vayamos a trabajar y la eficiencia del uso de recursos (memoria y almacenamiento) a fin de no afectar el rendimiento, especialmente en sistemas con grandes cantidades de datos. Independientemente del tipo de entero que se use, si hay decimales estos se truncarán.

## Decimals:

Es un tipo de dato numérico que permite almacenar números exactos con una precisión definida(número de dígitos almacenados en la columna) y una escala fija, esto significa que se almacena el mismo número de decimales después de la coma para todos los datos almacenados en la BD. El máximo de dígitos para un tipo de dato DECIMAL es de 65, dentro de ellos hasta 30 pueden ser decimales (ubicados después del punto).

Ejemplo:

```sql
DECIMAL(6,2) -- Almacena valores como 1234.56, donde hay un total de 6 dígitos, de los cuales 2 están después del punto decimal.
DECIMAL(10,4) -- Almacena valores como 12345.6789, donde hay un total de 10 dígitos, de los cuales 4 están después del punto decimal. Se usa el punto (.) y no la coma como el separador decimal en los números.
```
Este tipo de datos es ideal para trabajar con números en las que los errores de redondeo pueden tener consecuencias importantes, como por ejemplo entidades financieras, cálculos o mediciones relativas al ámbito científico, cálculos relativos los costos de producción de una empresa, etc.


## Floats:

Los Floats son útiles almacenar números sumamente grandes con una precisión aproximada. Son indicados para cálculos que no requieren precisión exacta y donde los errores de redondeo no tienen una relevancia significativa. 

## TIPOS DE DATO STRING (Cadena de texto o de caracteres)

## Caracteres (Characters, Chars):

Chars son cadenas de longitud fija. Esto significa que el número que designemos para esa columna será el espacio que se reservará en la memoria. Si bien no hace falta usar todos esos caracteres, son buenas prácticas. 

Son ideales para valores que tienen una longitud determinada como un número telefónico, DNI, o similar, mientras que no es recomendado para nombres, correos, direcciones y otros tipos de datos de longitud variable. Aceptan de 1 a 255 chars.

## Varchars ( Caracteres variables):

Estos también se usan para trabajar con cadenas pero estas son de longitud variable. Es decir para los ejemplos que mencionamos anteriormente en los que no sabemos la cantidad de caracteres que va a necesitar cada dato, ya que pueden variar ( nombres, correos, direcciones).

A diferencia de los Chars, los Varchars no tienen un espacio reservado en memoria de antemano y se ajustan a los datos que ingresemos, y si bien esto los hace más flexibles en cuanto a los datos que podemos ingresar, esto también los hace más lentos ya que la memoria se asigna de manera dinámica. 

Los Varchars admiten además muchos más caracteres que los Chars, hasta 65,535.

## TEXT 

Es un tipo de dato en MySQL para almacenar diferentes cantidades de texto. Existen cuatro tipos de TEXT:

-----------------------------------------------------------------------------
| **Tipo de Dato**  | **Tamaño Máximo**                                     |
|-------------------|-------------------------------------------------------|
| **TINYTEXT**      | Hasta 255 caracteres (longitud variable)              |
| **TEXT**          | Hasta 65,535 caracteres (más lentos que los varchar)  |
| **MEDIUMTEXT**    | Hasta 16,777,215 caracteres                           |
| **LONGTEXT**      | Hasta 4,294,967,295 caracteres                        |
-----------------------------------------------------------------------------

## CLOB (Character Large Object):

También se utiliza en bases de datos para almacenar grandes cantidades de texto como artículos o documentos. Sin embargo, no es típico de Mysql sino de otras bases de datos como Oracle, en el que puede almacenar hasta 4GB, mientras que si no se especifica nada, almacena hasta 2GB por defecto.

## Booleans (booleanos):

MySQL permite utilizar valores booleanos (TRUE y FALSE) en las consultas, los cuales son interpretados como código binario, siendo el 1 true y el 0 false. 

```sql
INSERT INTO usuarios (nombre, email, verificado) VALUES 
('Ana', 'ana@example.com', TRUE),  -- Correo verificado
```

La única sintaxis admitida es TRUE o FALSE. Sin embargo, también se utilizan estos valores binarios a la hora de activar o desactivar el modo seguro de manera controlada en lugar de desactivarlo permanentemente (controla la seguridad de las operaciones de actualización y eliminación).

```sql
SET SQL_SAFE_UPDATES = 0; -- desactiva el modo safe updates
SET SQL_SAFE_UPDATES = 1; -- activa el modo safe updates
```

## BLOB (Binary Large Object)

Se utiliza para  para almacenar grandes cantidades de datos binarios. Se utilizan para almacenar aquellos datos que no tienen un formato de texto legibles como podrían ser imágenes, o archivos multimedia.

-------------------------------------------------------------------------------------------------------------------------------------------------------
| **Tipo de BLOB**  | **Tamaño Máximo**                 | **Uso Típico**                                                                              |
|-------------------|-----------------------------------|---------------------------------------------------------------------------------------------|
| **TINYBLOB**      | Hasta 255 bytes                   | Ideal para datos binarios muy pequeños, como una pequeña imagen o un archivo comprimido.    |
| **BLOB**          | Hasta 64 KB                       | Para almacenar, por ejemplo, imágenes de tamaño pequeño a mediano.                          |
| **MEDIUMBLOB**    | Hasta 16 MB                       | Archivos de datos binarios más grandes, como videos cortos.                                 |
| **LONGBLOB**      | Hasta 4 GB                        | Para datos binarios muy grandes, como archivos de video de alta resolución.                 |
-------------------------------------------------------------------------------------------------------------------------------------------------------


### TIPOS DE DATOS DATE AND TIME (fecha y hora):

Estos tipos de datos se utilizan para representar fecha, hora, año. Puede representarse tanto uno de esos valores como una combinación de ellos. 

---------------------------------------------------------------------------------------------------------------------------------------
| **Tipo de Dato** | **Uso**                                                                               | **Formato**              |
|------------------|---------------------------------------------------------------------------------------|--------------------------|
| **DATE**         | Para representar fechas.                                                              | `'YYYY-MM-DD'`           |
| **TIME**         | Para representar horarios.                                                            | `'HH:MM:SS'`             |
| **DATETIME**     | Para representar combinaciones de fecha y hora.                                       | `'YYYY-MM-DD HH:MM:SS'`  |
| **TIMESTAMP**    | Puede ser configurado para que se establezca en la fecha y hora actual por defecto .  | `'YYYY-MM-DD HH:MM:SS'`  |
| **YEAR**         | Para representar años.                                                                | `'YYYY'`                 |
---------------------------------------------------------------------------------------------------------------------------------------







Fuentes consultadas:

https://redux.js.org/tutorials/essentials/part-1-overview-concepts
https://dev.mysql.com/doc/refman/8.0/en/data-types.html
https://learn.microsoft.com/es-es/sql/t-sql/data-types
https://www.w3schools.com/sql/sql_datatypes.asp
https://docs.oracle.com/javadb/10.10.1.2/ref/rrefclob.html
https://azure.microsoft.com/es-es/resources/cloud-computing-dictionary/what-is-a-relational-database
https://azure.microsoft.com/es-es/resources/cloud-computing-dictionary/what-is-nosql-database
https://www.dydserveis.com/repasamos-las-mejores-interfaces-graficas-mysql/
https://www.arsys.es/blog/interfaces-graficas-mysql
https://dbeaver.io/about/
Guías https://basque.devcamp.com/
