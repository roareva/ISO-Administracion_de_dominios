# C. Se ha centralizado la información personal de los usuarios del dominio mediante el uso de perfiles móviles y carpetas personales.
De primera mano, ¿para qué sirven los perfiles móviles? Los perfiles de usuario móviles permiten que la información sobre el perfil de la cuenta de un usuario se almacene en el servidor.

Usándolos, el usuario dispondrá de su perfil (documentos, favoritos de Internet, fondo de escritorio, etc.) con independencia del equipo cliente que esté utilizando en cada momento.

Además, el administrador puede centralizar la copia de seguridad de los datos de todos los usuarios y puede sustituir los equipos clientes sin preocuparse de que se pierdan datos.

Así pues, teniendo claro los conceptos, ahora procedemos a crearlos en el Windows Server por interfaz gráfica, que para ello, necesitaremos crear una carpeta en el servidor que actúe como contenedora de los perfiles, cambiar los permisos para que todos los usuarios del servidor puedan tener todo el control sobre esta carpeta creada y modificar la configuración del usuario para que guarde su perfil en la carpeta. 

Para crear una carpeta en el servidor que actué como contenedora de los perfiles, nos vamos al explorador de archivos y nos desplazamos a la carpeta donde queramos crearla, que en nuestro caso la hemos creado en el disco local C:\ y la hemos denominado "Perfiles"; una vez creada, hacemos sobre ella click derecho con el ratón y nos vamos "Propiedades", en la solapa de "Compartir".
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/c/0.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/c/1.jpg)
Ahora hacemos click en la opción "Uso compartido avanzado" y dejamos marcada la opción "Compartir esta carpeta"
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/c/2.jpg)
nos vamos a la pestaña de "Permisos", le damos a la pestaña de "Agregar" y en la parte donde dice "Escriba los nombres de objeto que desea seleccionar" escribimos a quiénes queremos darle los permisos, que en nuestro caso ponemos "Todos" para que esté disponible para todos los usuarios del servidor, le damos a "Comprobar nombre" y aceptamos.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/c/3.jpg)
Al aceptar, en la ventana de Permisos de Perfiles nos aparecerá este "Todos" y le asignaremos en las opciones de abajo de "Permisos" todos los permisos, seleccionando para cada uno de ellos la casilla de Permitir y aceptamos.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/c/4.jpg)
Aceptamos en la ventana de "Uso compartido avanzado"
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/c/5.jpg)
Y de esta manera ya tenemos activa una carpeta compartida en red para todos los usuarios del servidor.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/c/6.jpg)
Una vez activa esta carpeta compartida en red, podemos proceder a crear un perfil móvil. Nos vamos a la consola Usuarios y equipos de Active Directory y localizamos la cuenta a la que queremos asignar el perfil móvil, que en nuestro caso, vamos a tomar la cuenta de usuario "UsuarioEva", hacemos click derecho con el ratón sobre ella y nos vamos a "Propiedades"; en esta ventana nos vamos a la pestaña "Perfil", donde tenemos que poner la ruta de la carpeta llamada Perfiles que hemos creado anteriormente y será ahí donde se guarde el perfil de dichos usuarios, así aunque se cambie de equipo, siempre va a tenerlo porque lo cargará desde el servidor. La sintaxis de la ruta será "\\nombre_servidor\carpeta_perfiles\nombre_usuario", que en nombre_usuario hemos usado la variable de sistema %username% para que de esta manera coja automáticamente el nombre del usuario, que será muy útil cuando cambiemos el perfil de varios usuarios al mismo tiempo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/c/7.jpg)
De este modo habremos creado un perfil móvil y ahora al iniciar sesión con el usuario, en la carpeta Perfiles se ha creado la carpeta con el perfil de cada usuario.
--> [Siguiente apartado, apartado D](https://github.com/roareva/ISO-Administracion_de_dominios/tree/master/admin_dom/d)
