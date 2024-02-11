# Hibernar - Descripción general
------------------------------------------
https://www.tutorialspoint.com/hibernate/hibernate_overview.htm

## Ventajas de Hibernate
------------------------
 - Hibernate se encarga de asignar clases Java a tablas de bases de datos utilizando archivos XML y sin escribir ninguna línea de código.

 - Proporciona API simples para almacenar y recuperar objetos Java directamente hacia y desde la base de datos.

 - Si hay cambios en la base de datos o en cualquier tabla, entonces sólo necesita cambiar las propiedades del archivo XML.

 - Abstrae los tipos de SQL desconocidos y proporciona una manera de trabajar con objetos Java familiares.

 - Hibernate no requiere un servidor de aplicaciones para funcionar.

 - Manipula asociaciones complejas de objetos de su base de datos.

 - Minimiza el acceso a la base de datos con estrategias de recuperación inteligentes.

 - Proporciona una consulta sencilla de datos.


## Conexión mediante JDBC, Hibernate a base de datos Oracle.
------------------------------------------------------------------------------
https://stackoverflow.com/questions/3807503/what-is-the-purpose-of-two-config-files-for-hibernate/3808406#3808406

Si está utilizando la API patentada de Hibernate, necesitará hibernate.cfg.xml. Si está utilizando JPA, es decir, Hibernate EntityManager, necesitará persistence.xml.

Por lo tanto, generalmente no necesita ambos, ya que utiliza la API patentada de Hibernate o JPA.

Sin embargo, si estaba utilizando la API patentada de Hibernate y ya tiene hibernate.cfg.xml (y archivos de mapeo XML hbm.xml) pero desea comenzar a usar JPA, puede reutilizar los archivos de configuración existentes haciendo referencia a hibernate.cfg.xml en el persistence.xml en la propiedad hibernate.ejb.cfgfile y, por lo tanto, tendrá ambos archivos. Reutilizar archivos hbm.xml existentes es, en mi opinión, un escenario realista que podría justificar conservar ambos (incluso si probablemente migraría a anotaciones JPA a largo plazo).

***
Nota: Si utiliza 'Hibernate.cfg.xml' la conexión es mediante 'SessionFactory' o 
      si utiliza 'persistence.xml' la conexion es mediante 'EntityManagerFactory'
***
