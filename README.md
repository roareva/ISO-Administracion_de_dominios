# ISO-Administracion_de_dominios

### Realizado por Eva Rodríguez Araujo 

*Creación de documento sobre cómo administrar dominios y los accesos al dominio en Windows Server 2016.*

En este documento vamos a desarrollar dos secciones, una primera parte de cómo administrar dominios y, una segunda, manejar los accesos al dominio en Windows Server 2016.

Para ello y para poder así también verificar su funcionamiento, utilizaremos máquinas virtuales, que en este caso, vamos a usar la última versión de Oracle VM VirtualBox.

En primer lugar, tendríamos que descargarnos la respectiva ISO en la página oficial de Microsoft, que nos ofrece una versión de evaluación de dicho sistema por 180 días, y tras disponer finalmente de él, lo instalamos en nuestra máquina virtual ya sea con o sin interfaz gráfica, que en nuestro caso, hemos instalado tanto la versión Standard sin interfaz gráfica, denominada como "Windows Server Core" como la versión GUI (interfaz gráfica).

Una vez instalada la versión Core dispondremos únicamente del cmd en la ventana del sistema, en el cuál podremos ejecutar tanto powershell como la herramienta de configuración de servidores Sconfig.cmd.

Para el desarrollo de este documento vamos a dividirlo en las dos secciones comentadas anteriormente con sus respectivos apartados:

**Sección 1:**
>**1. Administración de dominios:**
>----------------------------------
>- [A - Se han implementado dominios.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/a/readme.md)
>
>- [B - Se han administrado cuentas de usuario y cuentas de equipo.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/b/readme.md)
>
>- [C - Se ha centralizado la información personal de los usuarios del dominio mediante el uso de perfiles móviles y carpetas personales.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/c/readme.md)
>
>- [D - Se han creado y administrado grupos de seguridad.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/d/readme.md)
>
>- [E - Se han creado plantillas que faciliten la administración de usuarios con características similares.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/e/readme.md)
>
>- [F - Se han organizado los objetos del dominio para facilitar su administración.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/f/readme.md)
>
>- [G - Se han utilizado máquinas virtuales para administrar dominios y verificar su funcionamiento.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/g/readme.md)
>
>- [H - Se ha documentado la estructura del dominio y las tareas realizadas.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/h/readme.md)

**Sección 2:**
>**2. Administración del acceso al dominio:**
>--------------------------------------------
>- [A - Se han incorporado equipos al dominio.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/a/readme.md)
>
>- [B- Se han previsto bloqueos de accesos no autorizados al dominio.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/b/readme.md)
>
>- [C - Se ha administrado el acceso a recursos locales y recursos de red.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/c/readme.md)
>
>- [D - 	Se han tenido en cuenta los requerimientos de seguridad.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/d/readme.md)
>
>- [E - Se han implementado y verificado directivas de grupo.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/e/readme.md)
>
>- [F - Se han asignado directivas de grupo.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/f/readme.md)
>
>- [G - Se han documentado las tareas y las incidencias.](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/g/readme.md)
