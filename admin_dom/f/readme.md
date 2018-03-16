# F. Se han organizado los objetos del dominio para facilitar su administración.
Para organizar los objetos del dominio para facilitar su administración necesitaremos crear `Unidades Organizativas`, que esta vez vamos a crearlas tanto por la terminal de comandos como por interfaz gráfica .
Como definición de Unidad Organizativa tenemos:
> Las Unidades organizativas proporcionan autonomía administrativa y los medios para controlar la visibilidad de los objetos en el directorio. Las unidades organizativas proporcionan aislamiento desde otros administradores de datos, pero no proporcionan el aislamiento de los administradores de servicio. Aunque los propietarios de unidad organizativa tienen control sobre un subárbol de objetos, el propietario de bosque conserva el control total sobre todos los subárboles.

> Las Unidades organizativas de la cuenta contienen los objetos de grupo, usuario y del equipo.

Para crear una cuenta organizativa en la interfaz gráfica del Windows Server nos vamos a la columna de la izquierda donde se encuentran nuestros objetos del dominio en Usuarios y Equipos de Active Directory en el Panel de Administrador del servidor, ponemos el cursor sobre nuestro dominio, hacemos click derecho sobre él, seleccionamos `Nuevo` y elegimos `Unidad Organizativa` 

![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/f/0.jpg)
Le damos un nombre a nuestra nueva unidad organizativa y aceptamos
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/f/1.jpg)
Una vez creada, podemos hacer click derecho sobre ella y rellenar los campos que queramos en propiedades de la misma.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/f/2.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/f/3.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/f/4.jpg)
Por lo tanto, ya en nuestro dominio disponemos de dos unidades organizativas, `1CFGS` y `2CFGS`, las cuales podremos administrar creando en ellas más objetos como usuarios, equipos, grupos, ...
Nuestra unidad organizativa `1CFGS` queda distribuida de esta manera
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/f/5.jpg)
--> [Siguiente apartado, apartado G](https://github.com/roareva/ISO-Administracion_de_dominios/tree/master/admin_dom/g)
