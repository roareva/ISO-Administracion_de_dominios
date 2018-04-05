# F. Se han asignado directivas de grupo.
Para asignar directivas de grupo editaremos nuestra GPO creada con anterioridad (en el anterior apartado) de manera que le definiremos los parámetros requeridos que deben ser aplicados ya sea a los usuarios o equipos del dominio o OU indicada.

Para añadir una tarea debemos editar la GPO, y para ello daremos clic derecho sobre nuestra GPO y seleccionamos la opción `Editar`
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/f/0.jpg)
Seremos redireccionados a otra ventana en la que nos encontramos dos secciones principales, que son:
- Configuración del equipo: donde encontramos configuraciones que se aplican exclusivamente a los equipos, independientemente de qué usuarios inicien sesión en ellos. Estas suelen ser configuraciones de sistema y seguridad que configuran y controlan el equipo.
- Configuración de usuario: donde encontramos configuraciones que se aplican a los usuarios, independientemente del equipo que sea usado. Estas configuraciones tienen que ver con la experiencia del usuario.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/f/1.jpg)
También dentro de las mismas encontramos dos elementos en cada una de ellas, que son:
- Directivas: que hace referencia a las políticas definidas que han de ser impuestas por el grupo.
- Preferencias: que incluye configuraciones de preferencias que podemos implementar para cambiar elementos como configuración de registro, archivo, carpeta u otro elemento. Al usar la configuración de preferencias, será posible configurar aplicaciones y funciones de Windows que no sean compatibles con la directiva de grupo.
Desplegamos las diversas opciones
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/f/2.jpg)
Vemos que aquí tenemos una serie de categorías disponibles para editar la acción que la GPO usará en el objeto seleccionado; para visualizar las diversas políticas, basta con pulsar sobre alguna de las opciones
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/f/3.jpg)
Tenemos a disposición cientos de acciones a configurar y esto está basado por los requerimientos de la organización.
En nuestro caso, usaremos la política llamada “Ocultar la pestaña Hardware”, es decir, cuando accedemos al panel de control vemos allí la opción Hardware
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/f/4.jpg)
Ahora damos doble clic sobre la política anteriormente mencionada
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/f/5.jpg)
Aquí nos encontramos con las siguientes opciones:
- No configurada: que deja la configuración de la política indefinida de modo que la Política de grupo no escribe la configuración de la política en el registro, por lo que no tendrá ninguna acción en los objetos del dominio.
- Habilitada: que escribe la configuración de la política en el registro con un valor que lo habilita.
- Deshabilitada: que escribe la configuración de la política en el registro con un valor que lo deshabilita.

En nuestro caso marcaremos la casilla `Habilitada` y pulsamos en Aplicar y Aceptar para guardar los cambios. Podremos ver que la política ha cambiado su estado a Habilitada.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/f/6.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/f/7.jpg)
De esta manera, si accedemos de nuevo al panel de control ya no está la opción `Hardware` disponible.

--> [Siguiente apartado, apartado G](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/g/readme.md)
