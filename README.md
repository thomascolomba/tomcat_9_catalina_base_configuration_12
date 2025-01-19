# tomcat_9_catalina_base_configuration_12

Ejemplo de emisión de notificación con MBean por JMX.

el archivo jmx_examples.zip ha sido descargado desde : https://docs.oracle.com/javase/6/docs/technotes/guides/jmx/examples.html (ejemplos de SUN)

1) En jmx_examples\Essential\, abro un terminal ejecuto "javac com/example/mbeans/*.java", y "java com.example.mbeans.Main". Eso me enseña el mensaje "Waiting forever...".
2) En el Administrador de tareas (Ctrl+Alt+Supr), buscar el proceso de java que ejecuta el mando "java com.example.mbeans.Main" que hemos lanzado, se llama java.exe, copiar su número de proceso (columna PID), en mi caso es : 10496
3) Abro otro terminal, ejecuto "jconsole 10496", se me abre la jconsole en una interfaz, abro la pestaña "Mbeans", en el menú de la izquierda abro "com.example.mbeans", y abro "Hello".
4) En esa interfaz, clico en "Notifications", y clico en el botón [Subscribe]
5) En la interfaz, en "Attributes", clico "CacheSize", y modifico el valor de CacheSize por 120.
6) En el terminal que enseña "Waiting forever...", ahora se ve el mensaje "Cache size now 120". Y en la interfaz, en "Notifications", se ve una nueva línea con el tiemstamp, el número de secuencia, elmensaje de la notificación, y el MBean que lo emitió.




doc JMX : https://docs.oracle.com/javase/6/docs/technotes/guides/jmx/index.html
