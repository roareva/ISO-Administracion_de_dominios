# F. Se han asignado directivas de grupo.
Para asignar directivas de grupo editaremos nuestra GPO creada con anterioridad (en el anterior apartado) de manera que le definiremos los parámetros requeridos que deben ser aplicados ya sea a los usuarios o equipos del dominio o OU indicada.

Para añadir una tarea debemos editar la GPO, y para ello daremos clic derecho sobre nuestra GPO y seleccionamos la opción `Editar`
Imagen 0
Seremos redireccionados a otra ventana en la que nos encontramos dos secciones principales, que son:
- Configuración del equipo: donde encontramos configuraciones que se aplican exclusivamente a los equipos, independientemente de qué usuarios inicien sesión en ellos. Estas suelen ser configuraciones de sistema y seguridad que configuran y controlan el equipo.
- Configuración de usuario: donde encontramos configuraciones que se aplican a los usuarios, independientemente del equipo que sea usado. Estas configuraciones tienen que ver con la experiencia del usuario.
Imagen 1
También dentro de las mismas encontramos dos elementos en cada una de ellas, que son:
- Directivas: que hace referencia a las políticas definidas que han de ser impuestas por el grupo.
- Preferencias: que incluye configuraciones de preferencias que podemos implementar para cambiar elementos como configuración de registro, archivo, carpeta u otro elemento. Al usar la configuración de preferencias, será posible configurar aplicaciones y funciones de Windows que no sean compatibles con la directiva de grupo.
Desplegamos las diversas opciones
Imagen 2
Vemos que aquí tenemos una serie de categorías disponibles para editar la acción que la GPO usará en el objeto seleccionado; para visualizar las diversas políticas, basta con pulsar sobre alguna de las opciones
Imagen 3
Tenemos a disposición cientos de acciones a configurar y esto está basado por los requerimientos de la organización.
En nuestro caso, usaremos la política llamada “Ocultar la pestaña Hardware”, es decir, cuando accedemos al panel de control vemos allí la opción Hardware
Imagen 4
Ahora damos doble clic sobre la política anteriormente mencionada
Imagen 5
Aquí nos encontramos con las siguientes opciones:
- No configurada: que deja la configuración de la política indefinida de modo que la Política de grupo no escribe la configuración de la política en el registro, por lo que no tendrá ninguna acción en los objetos del dominio.
- Habilitada: que escribe la configuración de la política en el registro con un valor que lo habilita.
- Deshabilitada: que escribe la configuración de la política en el registro con un valor que lo deshabilita.
En nuestro caso marcaremos la casilla `Habilitada` y pulsamos en Aplicar y Aceptar para guardar los cambios. Podremos ver que la política ha cambiado su estado a Habilitada.
Imagen 6
Imagen 7
De esta manera, si accedemos de nuevo al panel de control ya no está la opción `Hardware` disponible.
