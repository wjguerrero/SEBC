* What is ubertask optimization?
  Es una propiedad/parámetro de YARM, vinculada con la performance del servicio, que le indica la ejecución de procesos suficientemente pequeños (de acuerdo a la parametrización de mapreduce.job.ubertask.max*) en una sola JVM
* Where in CM is the Kerberos Security Realm value displayed?
  La cofiguración de REALM se encuentra en el menú Administratios, en CM, ingresando a la opción Setting, en la categoría Kerberos.
* Which CDH service(s) host a property for enabling Kerberos authentication?
  Todos los servicios tienen una propiedad donde se debe indicar el SPN de kerberos  
* How do you upgrade the CM agents?
  Los CM Agent se pueden/deben actualizar desde CM cuando estamos actualizando el CM Server, siguiendo los pasos de la actualización de éste. También pueden ser actualizados manualmentes desde la consola del SO, conectando con el repositorio adecuado a la versión requerida.
* Give the `tsquery` statement used to chart Hue's CPU utilization?
  SELECT cpu_system_rate + cpu_user_rate WHERE entityName = "hue-KT_RENEWER-fed7fa33e7e1d934998e53c26de5d786" AND category = ROLE
* Name all the roles that make up the Hive service
  Hive Metastore Server, 	HiveServer2 (WebHCat Server)
* What steps must be completed before integrating Cloudera Manager with Kerberos?
  Para habilitar la seguridad del Cluster con Kerberos, desde CM, hay que instalar y configurar Kerberos (editando los archivos de configuración del server y los client con los parámetros adecuados)
