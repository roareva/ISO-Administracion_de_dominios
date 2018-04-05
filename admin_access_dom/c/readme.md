# C. Se ha administrado el acceso a recursos locales y recursos de red.
De primera mano, sabemos que Windows Server 2016 ha sido desarrollado para facilitar la administración centralizada de todos los elementos de la infraestructura organizacional y uno de estos pilares tiene que ver con el almacenamiento y la gestión de archivos.

Para esta parte vamos a implementar y configurar un servidor de archivos en Windows Server 2016, pero antes de nada: 

**¿Qué es un servidor de archivos en Windows Server 2016?**
Básicamente un servidor de archivos nos dará la posibilidad de tener una ubicación central en la red local donde los usuarios del dominio pueden agregar, compartir y editar archivos.
 
Esto es muy eficaz ya que se pueden crear estructuras teniendo en cuenta los roles de los usuarios y de este modo ellos podrán acceder a este servidor de archivos de una forma práctica sin necesidad de pasar un archivo usando otros medios como correo, memorias USB, discos externos, etc.

Un servidor de archivos entonces es un punto de encuentro en la red donde cada usuario puede alojar diversos archivos para que otras personas puedan acceder a ellos de forma sencilla y directa.

El primer paso importante para desarrollar este apartado, que además debemos tener en cuenta, es crear una carpeta compartida en Windows Server 2016 a la cual posteriormente le otorgaremos los permisos necesarios para su funcionamiento adecuado con el servidor de archivos. En este caso hemos creado una carpeta llamada Perfiles.


Una vez creada le damos click derecho sobre la carpeta y seleccionamos la opción Propiedades y allí nos dirigimos a la pestaña Compartir.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/0.jpg)
Allí pulsamos sobre la opción Uso compartido avanzado y en la ventana desplegada activamos la casilla Compartir esta carpeta, asignamos el nombre a la carpeta compartida.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/1.jpg)
Ahora vamos a la opción Permisos ubicada en la parte inferior y allí eliminamos la opción Todos pulsando el botón Quitar.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/2.jpg)
Ahora podemos agregar los usuarios que consideremos deben tener acceso a la carpeta, en este ejemplo ingresaremos el grupo Usuarios del dominio.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/3.jpg)
Antes de pulsar en el botón Aplicar debemos asignar los permisos respectivos, por defecto solo está activa la opción Leer pero si el usuario debe hacer cambios será necesario activar la casilla Cambiar, que en nuestro caso vamos a marcar todas las casillas para permitir.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/4.jpg)
Una vez listo, le damos a aplicar y a aceptar hasta salir de la configuración.

Para comprobar, vamos a un equipo cliente y en el sistema de archivos, como ruta ponemos `\\EVA-CORE\` y podemos ver que está la carpeta que hemos creado.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/5.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/6.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/7.jpg)
Tomando esto como base es necesario que en la ficha `Permisos` esté activa como mínimo la opción `Cambiar` para que los usuarios ejecuten cambios en la carpeta compartida. Esta es la opción básica para crear un servidor de archivos en Windows Server 2016:
- Crear la carpeta
- Compartirla
- Asignar los respectivos permisos

Ahora, desde el Administrador del servidor, vamos a añadir algunas características que serán de gran ayuda para la gestión y el tema del servidor de archivos. Para esto vamos al Administrador del servidor y allí seleccionamos la opción Servicios de archivos y de almacenamiento ubicada en el costado izquierdo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/8.jpg)
Al pulsar esta opción veremos la siguiente ventana donde debemos seleccionar la opción Recursos compartidos.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/9.jpg)
Allí podemos ver la carpeta que hemos compartido, Perfiles, a la cual daremos clic derecho y seleccionamos la opción Propiedades y allí vamos a la opción Configuración.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/10.jpg)
Aquí podemos ver las opciones que pueden ser asignadas a la carpeta compartida, las cuales son:
- Habilitar enumeración basada en el acceso
Esta opción permite que el usuario que accede al recurso compartido visualice únicamente las carpetas a las cuales tiene permiso de acceso, de lo contrario no podrá ver nada ya que Windows Server 2016 la ocultara.
- Permitir almacenamiento en cache del recurso compartido
Esta opción permite que los recursos compartidos sean almacenados en la caché del sistema permitiendo así su disponibilidad sin conexión.
- Cifrar acceso a datos
Esta opción nos permite incrementar los valores de seguridad de los recursos compartidos cifrando el acceso a los mismos.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/11.jpg)
Para este ejemplo vamos a activar la casilla `Habilitar enumeración basada en el acceso` y pulsamos Aplicar / Agregar para guardar los cambios. 
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/12.jpg)
Ahora vamos a ver cómo funciona esta característica, por lo que hemos creado las carpetas `Acceso` y `Acceso2` dentro de la carpeta compartida.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/13.jpg)
Hasta este punto el cliente podrá ve ambas carpetas al conectarse por red a la carpeta compartida
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/14.jpg)
pero si editamos los permisos, por ejemplo, a la carpeta `Acceso` para que dicho usuario no pueda acceder, el usuario ya no vera dicha carpeta al momento de conectarse. Como vemos, la carpeta `Acceso` ha sido ocultada por Windows Server 2016 gracias a la característica que hemos habilitado.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/c/15.jpg)

--> [Siguiente apartado, apartado D](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/d/readme.md)
