# A. Se han incorporado equipos al dominio.
En esta parte vamos a incorporar dos equipos distintos, ambos Windows 10, a nuestro dominio haciendo uso de máquinas virtuales.

Pero antes que nada, hacer un pequeño inciso sobre ¿por qué es importante agregar un equipo al dominio en una organización? Pues bien, las razones son las siguientes:
- Para que puedan gestionarlo de manera centralizada.
- Para poder compartir archivos o carpetas.
- Para que el equipo forme parte de la infraestructura e inventario de la organización.
- Y además, un equipo agregado al dominio goza de los beneficios que tengan  establecidos.

Después de este inciso, continuamos con nuestro desarrollo.

Para incorporar equipos al dominio en nuestra máquina virtual, en Virtual Box en este caso, lo primero será que en cada uno de nuestros sistemas (equipos) que vayamos a incorporar al dominio y el sistema que hace de servidor (Windows Server 2016) configuremos la pestaña de red (estando apagadas todas estas máquinas), en concreto el Adaptador de Red, donde cambiaremos donde dice "Conectado a:" a "Adaptador puente" y en "Nombre:" seleccionaremos la misma tarjeta de red para todas.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/red.jpg)
Luego necesitaremos (ya dentro de las máquinas) configurar las direcciones ip de cada uno de nuestros sistemas, añadiéndoles una dirección ip estática y que todas pertenezcan al mismo segmento de red, además de (lo más importante) añadir una dirección de servidor DNS, en Servidor DNS preferido, donde en la configuración de la misma, en el sistema servidor le pondremos la dirección ip loopback, que hace referencia al localhost, es decir, a sí mismo, mientras que en nuestras otras dos máquinas con los sistemas windows 10, le pondremos la dirección ip del sistema servidor. La tabla de direcciones de cada uno de los sistemas que estamos usando quedan recogidos en la siguiente tabla:

|     Sistemas     | Dirección ip | Máscara de subred | Puerta de enlace predeterminada | Servidor DNS preferido |
| ---------------- | ------------ | ----------------- | ------------------------------- | ---------------------- |
| Windows Server   | 192.168.1.1  | 255.255.255.0     |                                 |  127.0.0.1             |
| Windows 10       | 192.168.1.2  | 255.255.255.0     |     192.168.1.1                 |  192.168.1.1           |
| Windows 10(2)    | 192.168.1.3  | 255.255.255.0     |     192.168.1.1                 |  192.168.1.1           |

![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/server/1.jpg)
Si hemos configurado las ip correctamente, ahora las máquinas podrán hacerse ping entre ellas en la ventana de comandos y podremos pasar al siguiente paso, que consistirá en hacer coincidir el nombre de cada equipo cliente (cada sistema que vayamos a conectar al dominio) con las cuentas de equipo asociadas en el dominio, que en nuestro caso ya la tenemos configurada de anteriormente.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/5.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/server/2.jpg)
Y por último, procedemos a unir los equipos al dominio, en la ventana del Sistema, en la sección de `Configuración de nombre, dominio y grupo de trabajo del equipo`, clickeamos en la opción de `Cambiar configuración`, en la nueva ventana que nos aparece de `Propiedades del sistema`, seleccionamos el cuadro de `Cambiar` y nos saldrá otra nueva ventana, `Cambios en el dominio o el nombre del equipo`, donde en la sección de `Miembro del` marcaremos la opción `Dominio` y escribiremos el nombre de nuestro dominio, que en este caso es `roareva.local`, aceptamos, 
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/0.jpg)
nos pedirán credenciales de usuario, que las rellenaremos con las de la cuenta del `Administrador` con su respectiva contraseña, volvemos a aceptar 
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/1.jpg)
y nos saldrá un mensaje con la confirmación de que ya nos hemos unido al dominio, aceptamos
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/2.jpg)
y nos pedirá que reiniciemos el equipo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/3.jpg)
De forma predeterminada, el sistema nos ofrece iniciar sesión con el último usuario con el que hayamos trabajado. Sin embargo, en este caso se trata del usuario local, que sabemos que es una cuenta local porque, antes del nombre de usuario, aparece el nombre del dominio.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/6.jpg)
Una vez reiniciado, comprobaremos que efectivamente nuestro equipo Windows 10 está unido correctamente al dominio.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/a/4.jpg)
Realizamos exactamente los mismos pasos para nuestra otra máquina virtual con también Windows 10 como sistema operativo.
