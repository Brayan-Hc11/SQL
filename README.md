# Aprender SQL (lenguaje de consulta estándar) para bases de datos

SQL significa Structured Query Language (Lenguaje de consulta estructurado). SQL se utiliza para consultar y manipular las bases de datos relacionales subyacentes, como SQL Server, Oracle, MySQL, PostgreSQL, SQLite, etc.

SQL es un lenguaje estándar ANSI (American National Standards Institute) e ISO (International Organization for Standardization). Sin embargo, no todas las bases de datos admiten el mismo SQL, pero hay poca variación. Además, la mayoría de las bases de datos incluyen su propia adición a SQL.
***

<details>  
  <summary>  
    
  ## __¿Qué es SQL?__
   </summary>

SQL significa Structured Query Language (Lenguaje de consulta estructurado). SQL se utiliza para consultar y manipular las bases de datos relacionales subyacentes, como SQL Server, Oracle, MySQL, PostgreSQL, SQLite, etc.

SQL es un lenguaje estándar ANSI (American National Standards Institute) e ISO (International Organization for Standardization). Sin embargo, no todas las bases de datos admiten el mismo SQL, pero hay poca variación. Además, la mayoría de las bases de datos incluyen su propia adición a SQL.
***
## Sintaxis SQL
SQL incluye las siguientes partes:

 - __Palabras clave:__ Las palabras clave son palabras reservadas o no reservadas. Las palabras clave reservadas en SQL son SELECT, INTO, UPDATE, DELETE, DROP, ASC, DESC, etc.
   
 - __Identificadores:__ Los identificadores son los nombres de los objetos de la base de datos como el nombre de la tabla, el nombre del esquema, el nombre de la función, etc.
   
 - __Cláusulas:__ Las cláusulas forman los componentes de las instrucciones SQL y las consultas como WHERE, GROUP BY, HAVING, ORDER BY.
   
 - __Expresión:__ Las expresiones en SQL producen valores escalares o columnas y filas de datos.
   
 - __Condiciones booleanas:__ Las condiciones son las expresiones que dan como resultado el valor booleano TRUE o FALSE. Se utilizan para limitar el efecto de las declaraciones o consultas.
 - __Consultas:__ Las consultas son las instrucciones SQL que recuperan los datos en función de criterios específicos. Las instrucciones que comienzan con la cláusula SELECT se denominan consultas porque recuperan datos de la base de datos subyacente.
   
 - __Declaraciones:__ Las instrucciones SQL pueden tener un efecto persistente en el esquema y los datos, o pueden controlar las transacciones, el flujo del programa, las conexiones, las sesiones o los 
diagnósticos. Las instrucciones INSERT, UPDATE, DROP, DELETE se denominan instrucciones SQL porque modifican la estructura o los datos de la base de datos subyacente.
***

## Clasificación SQL
SQL se clasifica en las siguientes categorías. Tenga en cuenta que las instrucciones mencionadas en las tablas siguientes pueden variar en diferentes bases de datos.

|Comandos|Descripción|
|--------|-----------|
|DDL | Lenguaje de definición de datos|
|DML | Lenguaje de manipulación de datos|
|TCL | Lenguaje de control de transferencias|
|DCL | Lenguajde de control de datos|

### DDl/ Lenguaje de definición de datos
Las instrucciones del lenguaje de definción de datos (DDL) se utilizan para definir la estructura de los datos en la base de datos, como tablas, procedemientos, funciones,vistas, etc. En la tabla siguiente se enumeran las instrucciones DDL;

|Declaración|Descripción|
|-----------|-----------|
|Create| Crear un nuevo objeto (tabla, procedimiento, función, vista, etc.) en la base de datos|
|Alter | Modificar la estructura de la base de datos|
|Drop | Eliminar objetos de la bases de datos |
|Rename | Cambiar el nombre de los objetos de la base de datos (Tabla, vista, secuencia, sinónimo privado)|
|Trucate | Quitar todos los registros de una tabla|

### DML/ Lenguaje de manipulación de datos 
Las instrucciones de lentguaje de manipulación de datos (DML) se utilizan para administrar datos dentro de un objeto de bases de datos. Permiite manipular y consultar lo exitente objetos de esquemas de bases de datos. En la siguiente tabla enumeran las instrucciones de DML 

|Declaración|Descripción|
|----|----|
|Select| Recuperar filas/columnas de una tabla |
|Insert| Insertar nuevos datos en una tabla|
|Update| Actualizar los registros existentes de una tabla |
|Delete| Eliminar los registros exitentes de una tabla |
|Merge | Inserte nuevas filas o actualice las fillas exitentes en un tabla en función de las condiciones especificas|
|Lock Table| Bloquee una o más tablas en un modo especificado. Basado en el bloqueo aplicado acceso a la tabla denegado o solo acceso real otorgado a otros usuarios|

### TLC/ Lenguaje de control de datos
Las instrucciones del lenguaje de control de transferencias (TLC) se utilizan para finalizar los cambios en los datos realizados mediante la ejecución de las intrucciones DML.

|Declaración|Descripción|
|-----------|-----------|
|Commit| Guarde permanentemente los cambios de transacción en la base de datos.|
|Rollback| Restaurar la base de datos a su estado original desde la última confirmación.|
|Savepoint | Crear un SAVEPOINT para que el comando Rollback lo ulitilice más tarde para deshacer los cambios realizados hasta ese momento.|
|Set Transaction| Establezca las propiedades de la transacción, como READ,WRITE o READ ONLY access.|

### DCL/ Lenguaje de control de datos
Las instrucciones de lenguaje de control de datos(DCL) se utiliza para aplicar la base de datos seguridad al otorgar privilegios a diferentes usuarios para acceder a la base de datos.

|Declaración|Descripción|
|-----------|-----------|
|Grant| Otorga privilegios al usuario para acceder a los datos.|
|Revoke | Recuperar los privilegios otorgados por el usuario.|
|Comment | Especifique los comentarios en las tablas y columnas de la base de datos.|
|Analyze| Recopilar estadisticas de la tabla, indice, partición, clúster,etc.|
|Audit | Realizar un seguimiento de la aparición de instrucciones u operadores SQL especificas o todas en algún objeto Schema especifico.|

### SCL/ Lenguaje de control de sesión
Las instrucciones de lenguaje de control de seción(SCL) se utilizan para administrar las cambios hecho a la base de datos mediante la ejecución de instrucciones DML. Los comandos SCL varían en una función
de la base de datos mediante ejecución de instrucciones DML. Los comandos SCL varían en función de la base de datos. En la siguiente tabla se enumeran los comandos SCL para la base de datos de Oracle.

|Declaración|Descripción|
|-----------|-----------|
|Alter session| Modificar los parametros  de la base de datos para la sesión actual.|
|Set role | Para habilitar o deshabilitar roles para la sesión actual. |
</details>

***

<details>
  <summary>
    
  ## __SQL crear tabla en la base de datos__
  </summary>
  
Las sentencias __CREATE__ se utilizan para crear las estructuras de la base de datos como la tabla, vista, secuencia, función, procedimiento, paquete, disparador, etc. Iremos y exploraremos todas estas de bases de datos en la última parte de los tutoriales. 

La instrucción __CREATE TABLE__ Se utiliza para crear una nueva tabla en la base de datos. A continuación se muestra la sintaxis para crear una nueva tabla en la base de datos.

~~~
CREATE TABLE table_name(
    column_name1 data_type [NULL|NOT NULL],
    column_name2 data_type [NULL|NOT NULL],
);
~~~
</details>




