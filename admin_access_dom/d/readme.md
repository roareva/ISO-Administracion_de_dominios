# D. Se han tenido en cuenta los requerimientos de seguridad.
Para este apartado vamos a tener en cuenta tanto las copias de seguridad en el sistema Windows Server 2016 como instalar actualizaciones en el mismo.

Indudablemente uno de los aspectos que debemos tener en cuenta es velar por mantener al día nuestros sistemas, y sobre todo, tener fundamentalmente respaldo de nuestros servidores en todo sentido ya que en caso de alguna falla podemos estar en serios problemas que pueden implicar tiempo, dinero y, en algunas situaciones, el puesto.

Por esto nos preguntaremos, **¿por qué crear un respaldo de nuestro servidor?**

Muchas personas creen que su equipo nunca va a presentar fallas, pero tener una copia de respaldo debe ser una buena costumbre que debemos implementar ya que puede suceder que hayan cortes abruptos de luz que afectan el servidor, daños en hardware del equipo (discos, memoria, unidades, fuentes,etc), mal manejo de la configuración del sistema, virus o malware, personal mal intencionado, etc.

Existen diversas razones por las cuales debemos tener un respaldo de nuestro controlador de dominio, de los roles, de los usuarios, equipos, grupos, etc, así aque en esta sección analizaremos cómo podemos crear respaldo de nuestro servidor, es decir, realizar copias de seguridad de nuestro sistema.

Para comenzar el proceso de respaldo vamos a ir a la opción Agregar roles y características desde el Administrador del servidor.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/0.jpg)
Una vez abierto, pasamos la primera ventana informativa (le damos a siguiente)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/1.jpg)
y en la siguiente marcamos la opción `Instalación basada en características o en roles`.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/2.jpg)
Pulsamos siguiente y seleccionamos el servidor donde hemos de instalar la herramienta de respaldo
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/3.jpg)
nuevamente pulsamos Siguiente y en la ventana de roles no vamos a agregar ninguno ya que vamos a adicionar una característica y no un rol.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/4.jpg)
Pulsamos Siguiente. Llegamos a la ventana de características y ya aquí marcamos la opción `Copias de seguridad de Windows Server` y le damos a Siguiente
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/5.jpg)
(con esta herramienta vamos a poder crear copias de seguridad y restauración de múltiples parámetros en nuestro equipo Windows Server 2016). Continuamos con la instalación de la característica dandole a Instalar.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/6.jpg)
Una vez finalizada la instalación podremos encontrarnos la herramienta desde el menú Herramientas en el Administrador del servidor.
Ahora vamos a proceder a abrir `Copias de seguridad de Windows Server` desde la opción Herramientas en el Administrador del servidor.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/7.jpg)
Para iniciar el respaldo de nuestro Windows Server 2016 vamos a dar clic en la opción Copia de seguridad local
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/8.jpg)
Aquí es donde podremos ver la información acerca de los últimas copias de seguridad, de cuando será la siguiente, etc y en la columna derecha podremos elegir diferentes opciones para iniciar el respaldo o la restauración del sistema.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/9.jpg)
Las distintas opciones de las que dispone son:
- Programar copia de seguridad, que nos permite programar la copia de seguridad usando días y horas determinadas.
- Hacer copia de seguridad de una vez, que nos permite ejecutar un respaldo único.
- Recuperar, que nos permite realizar unan recuperación tomando como base un respaldo ya realizado anteriormente.
- Configurar opciones de rendimiento, que nos permite establecer los parámetros de la herramienta.

En nuestro caso vamos a seleccionar la opción `Hacer copia de seguridad de una vez` y se abre una ventana para la misma
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/10.jpg)
Dejamos marcada la opción que viene marcada de manera predeterminada y le damos a Siguiente.
En la siguiente ventana de configuración podemos elegir el tipo de respaldo a realizar, podemos seleccionar `Servidor completo` para respaldar todo el sistema, que viene marcada de manera predeterminada o podemos elegir `Personalizada` para configurar según nuestro decisión lo que deseemos respaldar. En nuestro caso dejamos marcado `Servidor completo` y pulsamos Siguiente.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/11.jpg)
Ahora definimos donde se va a almacenar la copia, localmente o remotamente, que viene marcada la opción que viene por predeterminada, `Unidades locales`, pero nosotros vamos a seleccionar la opción de `Carpeta compartida remota` y le damos a Siguiente
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/12.jpg)
Especificamos la ubicación de nuestra carpeta compartida, que en nuestro caso es `\\EVA-CORE\Perfiles` y donde "Control de acceso" dejamos marcada la opción que está por predeterminada, la opción `Heredar`, que con esta opción la copia de seguridad será accesible a todos aquellos usuarios que tengan acceso a dicha carpeta compartida.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/13.jpg)
Le damos a Siguiente y nos encontramos en la confirmación del respaldo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/14.jpg)
Aquí podemos ver los elementos que van a ser respaldados. Para iniciar ya nuestra copia de seguridad pulsamos el botón `Copia de seguridad` y comenzará el respaldo de nuestro equipo Windows Server 2016.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/15.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/16.jpg)
Esperamos a que se termine la copia de seguridad hasta que el estado de la misma esté en `Completado`, de modo que la copia de seguridad ha sido satisfactoria.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/17.jpg)
Cerramos la ventana para salir del asistente y ya en la ventana principal de `Copias de seguridad de Windwos Server` nos encontramos que está la copia que acabamos de realizar.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/18.jpg)
Por lo tanto, ya tenemos creado el respaldo de nuestro sistema Windows Server.

Ahora procedemos a instalar actualizaciones en nuestro sistema Windows Server 2016. Una de las primeras tareas que se debe realizar al administradar una red, es asegurarse de que los sistemas operativos que intervienen en la instalación se actualizan como es debido, ya que es particularmente importante la actualización del servidor (o los servidores) que estemos utilizando.
Para ello, en el panel del `Adminstrador del servidor` hacemos clic sobre Servidor local, en el panel izquierdo de la ventana.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/19.jpg)
Podemos comprobar que en el apartado `Windows Update`, el estado actual es `Sólo descargar actualizaciones mediante Windows Update`, que significa que las actualizaciones se descargarán automáticamente, pero no se instalarán sin la intervención del administrador.
Para acceder a las actualizaciones tenemos que hacer clic sobre el enlace `Sólo descargar actualizaciones mediante Windows Update` nombrado anteriormente y se nos abrirá la ventana de `Configuración` en la sección de `Windows Update`.
En nuestro caso, en el panel derecho aparece un mensaje indicando que hay actualizaciones disponibles y podemos hacer clic en `Instalar ahora` para proceder a instalar las actualizaciones pendientes en el sistema y así tenerlo actualizado hasta la fecha actual.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/20.jpg)
Esperamos a que termine el proceso de instalación de las actualizaciones.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/d/21.jpg)
Tras la instalación es necesario reiniciar el sistema para terminar de instalar algunas actualizaciones y ya por último sólo nos quedaría esperar hasta que se complete el reinicio del equipo para que nuestro sistema esté totalmente actualizado.

--> [Siguiente apartado, apartado E](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/e/readme.md)
