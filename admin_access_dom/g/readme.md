# G. 	Se han documentado las tareas y las incidencias.
En esta sección 2 `Administración del acceso al dominio` hemos incorporado dos equipos virtuales (a través de dos Windows 10 en virtual box) a nuestro dominio roareva.local creado en la sección 1 `Administración de dominios`, uno cuenta equipo llamada `Eva-cliente` y otra llamada `Cliente-Eva`, ambas con sus respectivos cuentas de usuario, que todos estos a su vez pertenecen al dominio. Al principio dio lugar a fallos para poder vincular estos equipos al dominio, pero resultó ser problema del mal asignamiento de IP en el `DNS preferido`, fallo que se corrigió y tras ello, pudo funcionar correctamente.

Luego para prevenir bloqueos de accesos no autorizados al dominio y de ese modo dar seguridad al mismo, intentamos crear políticas asociadas a las contraseñas y bloqueo de cuentas en Windows Server 2016, pero no pudimos efectuar tales cambios, puesto que cada opción aparecía deshabilitada sin poder editarla para poder así habilitarla.

Para administrar el acceso a recursos locales y recursos de red hicimos uso de la carpeta compartida entre usuarios dentro del dominio `Perfiles` creada en la anterior sección `Administración de dominios`, de manera que configuramos dicha carpeta para ocultar las carpetas dentro de esta a usuarios que no tengan permisos de lectura (o similar) para la misma, de forma que se la oculta a dicho usuario.

Luego hemos asegurado el sistema teniendo en cuenta los requerimientos de seguridad tales como la actualización del sistema al último parche del que dispone Windows Server actualmente, como el generar una copia de seguridad del mismo dentro de la carpeta compartida en red local `Perfiles` de la que disponíamos de anteriormente.

Y por último, hemos creado y configurado directivas de grupo al dominio en general, que es muy funcional para controlar ciertas acciones que pueden ser aplicadas tanto a usuarios como equipos.

Las incidencias ocasionadas están comentadas a lo largo de este apartado con sus respectivos puntos a realizar en esta segunda sección, por lo que no hay nada más que objetar.

--> [Volver a la página principal](https://github.com/roareva/ISO-Administracion_de_dominios)
