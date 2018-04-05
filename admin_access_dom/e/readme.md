# E. Se han implementado y verificado directivas de grupo.
En este apartado vamos a implementar directivas de grupo denominadas comúnmente como `directivas de políticas de grupo o GPO (Group Policy Object)`, que es una utilidad integrada al sistema que será muy funcional para controlar ciertas acciones que pueden ser aplicadas tanto a usuarios como equipos.

**¿Qué es una GPO?** *Una GPO es básicamente una política que podremos crear y editar, también remover en cualquier momento, mediante la cual se permite establecer la configuración en los diversos objetos a administrar como usuarios y equipos.*

 Una de las ventajas de las GPO es que pueden ser implementadas en cualquier tipo de escenario y podremos usarlas para todo el dominio en general o únicamente para una unidad organizativa (OU), en especial.

 La implementación de una GPO ha sido diseñada para que sea implementada en redes basadas en los Servicios de dominio de Active Directory (AD DS) de Windows Server.
 
Existen una serie de requisitos básicos y simples para usar e implementar de forma correcta las políticas de grupo en Windows Server 2016, que son los siguientes:
- La red local debe estar basada en AD DS, con esto indicamos que por lo menos un servidor debe tener instalada la función de AD DS.
- Los equipos que vamos a administrar deben estar unidos al dominio y los usuarios que gestionemos deben usar las credenciales de dominio para iniciar sesión en sus equipos directamente al dominio.
- Será necesario contar con permisos para editar la Política de grupo en el dominio, es decir, pertenecer al grupo de Administradores o de Administradores de Política de grupo.
 
Existen dos tipos de GPO, de dominio y locales, que implica que la política de grupo basada en el dominio nos da la posibilidad de centralizar la administración de modo que una sola política creada puede afectar a todos los equipos del dominio a la vez, mientras que la política de grupo local requiere que cada máquina a configurar se haga directamente en ella, lo cual implica más trabajo administrativo.

Vamos a proceder a crear una GPO en Windows Server 2016, para ello vamos a usar la combinación de teclas Windows+R y ejecutaremos el comando `gpmc.msc` y pulsamos Enter.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/e/0.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/e/1.jpg)
Hacer especial inciso en que por defecto, las políticas de grupo en Windows Server 2016 viene con dos políticas por defecto:
- Default Domain Controllers Policy: Cuando instalamos el rol del servidor de AD DS se crea esta política de forma predeterminada, dentro de ella encontramos configuraciones de políticas que se aplican específicamente a los controladores de dominio creados.
- Default Domain Policy: Igual que la anterior, cuando se instala el rol de servidor de AD DS se crea esta política por defecto y dentro de ella encontramos configuraciones de políticas que se aplican a todas los equipos y usuarios en el dominio.
En el nivel superior del AD DS (Active Directory Domain Server) encontramos sitios y dominios. Cuando se crea un dominio simple, estas tendrán un único sitio y un solo dominio. Y dentro de un dominio será posible crear unidades organizativas (OU).
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/e/2.jpg)
Sigamos; en la ventana desplegada daremos clic derecho sobre nuestro dominio y seleccionamos la opción `Crear un GPO en este dominio y vincularlo aquí`
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/e/3.jpg)
Se desplega una ventana donde asignaremos un nombre a dicha GPO y aceptamos
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/e/4.jpg)
Vemos que se ha creado la GPO según nuestro criterio. De esta forma tan simple hemos creado una política de grupo o GPO en Windows Server 2016.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/e/5.jpg)

--> [Siguiente apartado, apartado F](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/f/readme.md)
