# D. Se han creado y administrado grupos de seguridad.
Para crear y administrar grupos de seguridad necesitaremos primero crear una cuenta de grupo y darle la propiedad de tipo "Seguridad".
Así pues, para crear una cuenta de grupo de seguridad nos iremos a la herramienta Usuarios y equipos de Active Directory, allí buscaremos en el panel de la izquierda el contenedor en el que queremos guardar el nuevo grupo, que en nuestro caso, vamos a hacerlo en la carpeta "1CFGS", que es una unidad organizativa que hemos creado, donde tenemos añadido tanto el usuario "UsuarioEva" como el de "Administrador" (en uno de los siguientes apartados tendremos que explicar cómo crear unidades organizativas, y después haremos click con el botón derecho del ratón sobre esta unindad organizativa, eligiendo en el menú de contexto que aparece Nuevo > Grupo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/0.jpg)
En la nueva ventana que aparece, Nuevo objeto: Grupo, rellenamos únicamente el campo de Nombre del Grupo, el primero que aparece, ya que el siguiente se rellena automáticamente al rellenar éste y dejamos marcadas las opciones que nos vienen marcadas por defecto, que son en Ámbito de grupo la opción "Global" y en Tipo de Grupo la opción "Seguridad", puesto que son las que nos interesan en este caso; tras ello, aceptamos.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/1.jpg)
Ya tendremos en nuestra unidad organizativa esta cuenta de grupo de seguridad.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/2.jpg)
Ya una vez teniendo esto, para administrarlo contamos con que podemos modificarlo, añadirle miembros, eliminarle miembros, convertir a un grupo en miembro de otro grupo, conseguir que un grupo deje de ser miembro de otro, eliminarlo, ...
Vamos a proceder a explicar cada una de ellas.
Para modificar los valores de un grupo nos vamos al grupo que queremos modificar y hacemos click derecho sobre él, seleccionando la opción Propiedades, y ya ahí podemos modificarlo en sus diferentes pestañas que son la pestaña "General", "Miembros", "Miembro de" y "Administrado por", en las cuáles podremos cambiar el Nombre de grupo, la Descripción y el Correo electrónico donde se recibirán incidencias relacionadas con el grupo, y además modificar el Ámbito del grupo y el Tipo de grupo; elegir los usuarios, equipos o grupos que son miembros del grupo que estamos modificando; hacer que este grupo sea, a su vez, miembro de un grupo distinto; y permitir delegar la administración de este grupo en otro usuario diferente; respectivamente.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/3.jpg)
Para añadir miembros al grupo podemos hacerlo desde sus propiedades, en la pestaña "Miembros", le damos a Agregar, y en esa ventana que nos aparece, la de Seleccione Usuarios, Contactos, Equipos, Cuentas de servicio o Grupos, sólo tendremos que escribir los nombres de las cuentas de usuario en el cuadro titulado Escriba los nombres de objeto que desea seleccionar y darle a "Comprobar nombres"
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/4.jpg)
Aceptamos
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/5.jpg)
Y podemos comprobar que se han añadido los usuarios al grupo, y aceptamos de nuevo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/6.jpg)
Para eliminar miembros del grupo es el mismo proceso para añadirlos, pero en lugar de "Agregar", elegiremos la opción "Quitar" cuando seleccionemos al usuario que queremos quitar del grupo, nos saldrá un mensaje de confirmación y aceptamos.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/7.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/8.jpg)
Para eliminar un grupo simplemente hacemos click derecho sobre el grupo que queremos eliminar y seleccionamos la opción "Eliminar" del menú de contexto que nos aparece, nos pedirá confirmación y aceptamos.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/9.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/d/10.jpg)
--> [Siguiente apartado, apartado E](https://github.com/roareva/ISO-Administracion_de_dominios/tree/master/admin_dom/e)
