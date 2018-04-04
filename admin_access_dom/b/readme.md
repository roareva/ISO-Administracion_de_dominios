## B. Se han previsto bloqueos de accesos no autorizados al dominio. ##
Al administrar servidores en Windows Server debemos velar constantemente para que todos los niveles de seguridad y privacidad estén funcionando correctamente, por ello es importante prevenir bloqueos de accesos no autorizados al dominio.

En Windows Server encontramos cientos de utilidades y roles y características que harán simplificarnos muchas acciones y permitiéndonos  tener un control directo y preciso sobre muchos objetos que están inmersos en la organización tales como usuarios, equipos y otros.

Como administradores que tienen acceso al sistema, en Windows Server podremos tener un control preciso y en tiempo real sobre cada acción que ejecutan los usuarios y mediante la cual podremos definir las políticas o requisitos que deben ser cumplicdos por los usuarios en la organización.

Como parte de documentación en este apartado, vamos a ver cómo podemos crear políticas asociadas a la contraseña y bloqueo de cuentas en Windows Server 2016.

En Windows Server se implementaron políticas de contraseñas estrictas con el fin de optimizar y mejorar los niveles de seguridad en la organización. Estas políticas serán aplicadas a los objetos Usuarios o a las Organizaciones, según se decida.

Al implementar una política de contraseñas en la organización podemos asegurarnos de que que mejorará de forma notable la seguridad y acceso a los equipos cliente al forzar el ingreso de determinados parámetros de contraseñas. Las recomendaciones para establecer una correcta política de contraseñas son:

- Establecer "Exigir historial de contraseñas a 24" ya que esto nos ayudará a prevenir múltiples vulnerabilidades provocados por la reutilización de contraseñas.
- Establecer "Vigencia máxima de la contraseña 60 días" al forzar la caducidad de las contraseñas entre los ciclos de negocios principales para evitar la pérdida de trabajo.
- Configurar "Vigencia mínima de contraseña" para que no se permitan cambios inmediatos de contraseñas.

Es vital configurar de forma adecuada nuestras políticas para evitar ataques y fallos de seguridad en el acceso de los usuarios.
 
Para poder configurar las políticas de contraseñas en Windows Server 2016 debemos irnos al editor de políticas de grupo usando la combinación de teclas Windows+R y en la ventana desplegada ingresar el comando gpedit.msc, pulsamos Enter o Aceptar. 
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/0.jpg)
Debemos ir a la siguiente ruta ->`Configuración del equipo`-> `Configuración de Windows` -> `Configuración de seguridad`->`Directivas de cuenta`-> `Directiva de contraseñas`.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/1.jpg)
Podemos ver que dicha política está compuesta de múltiples elementos como son:
 
- Almacenar contraseñas con cifrado reversible
Esta política habilita la compatibilidad de protocolos que requieren la contraseña del usuario para el inicio de sesión. Con esta política se pueden descifrar contraseñas que han sido previamente cifradas, por lo cual no es recomendable su habilitación ya que algún atacante puede aprovechar su vulnerabilidad para descifrar la contraseña y acceder al equipo, y con ello, a los recursos compartidos. Para realizar cualquier cambio sobre dicha política daremos doble clic sobre ella y podremos habilitarla o deshabilitarla según sea la necesidad.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/2.jpg)
- Exigir historial de contraseñas
Con esta política determinamos la cantidad de nuevas contraseñas deben estar asociadas a la cuenta antes de poder usar de nuevo la contraseña antigua. El usar la misma contraseña de forma seguida puede resultar en una fallo de seguridad dentro de nuestra gestión ya que esta será más vulnerable a un ataque de fuerza bruta. El valor por defecto es 10 lo cual indica que hasta dentro de 10 cambios de contraseñas nuevas podremos usar la contraseña actual. Podemos configurar el rango de veces entre 0 y 24 pero el objetivo, a nivel de seguridad, es establecer la mayor cantidad de veces posibles. Para su edición daremos doble clic sobre la política y editaremos los valores según sean necesarios.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/3.jpg)
- La contraseña debe cumplir los requisitos de complejidad
Esta es una de las políticas más vitales para llevar a cabo una excelente configuración de políticas de contraseñas ya que acá definiremos los niveles de complejidad que deben ser obligatorios aplicar a la contraseña asignada por el usuario. Con esta política indicamos la serie de requisitos a ser aplicados durante la creación de la contraseña como:
  - La contraseña no debe contener el samAccountName (Nombre de cuenta del usuario) o el DisplayName
  - (Nombre desplegado) sin importar si son mayúsculas o minúsculas.
  - Recomendable que posea los siguientes atributos:
  - Longitud mínima de 8 caracteres.
  - Contener caracteres especiales como ,!, $, #, %.
  - Incluir números.
  - Incluir letras mayúsculas y minúsculas.
 
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/4.jpg)
 
- Longitud mínima de la contraseña
Con esta política indicamos la cantidad mínima de caracteres que debe contener la contraseña para que sea aceptada por el sistema. Aquí podremos establecer valores entre 1 y 14, pero si dejamos el valor en 0, significa que el usuario ingresara sin contraseña. El valor por defecto en Windows Server 2016 es de 7 caracteres.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/5.jpg)
- Vigencia máxima de la contraseña
Esta política nos permite definir la cantidad de tiempo, en días, en las cuales la contraseña caducará y será necesario forzar al usuario a cambiarla por una nueva siguiendo las políticas configuradas. El valor por defecto es 42 días.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/6.jpg)
- Vigencia mínima de la contraseña
Indica el tiempo en el cual una contraseña puede ser usada antes de que el usuario decida modificarla. Allí podremos establecer tiempos entre 0 y 998 días.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/7.jpg)
 
 Ahora pasaremos a la configuración de políticas de bloqueo de cuentas, que es otra de las políticas a nivel de seguridad primordiales en Windows Server 2016, ya que a través de ella podremos definir si un usuario no autorizado está intentando acceder al sistema. Esto lo podemos lograr configurando dicha política para que después de tres intentos fallidos la cuenta sea bloqueada, por lo cual, deben recurrir al administrador para su desbloqueo.
 
Para llegar a esta política vamos de nuevo al editor de políticas de grupo como hemos hecho anteriormente e iremos a la siguiente ruta->
`Configuración del equipo`-> `Configuración de Windows`-> `Configuración de seguridad`-> `Directivas de cuenta`->`Directiva de bloqueo de cuenta`.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_access_dom/img/b/8.jpg)
Aquí podemos configurar los siguientes parámetros:
- Duración del bloqueo de cuenta
Esta política nos permite definir la cantidad de tiempo en la cual la cuenta involucrada permanecerá bloqueada y este tiempo se expresa en minutos en un rango entre 1 y 99.999 minutos; Si establecemos el valor 0 solo un administrador podrá desbloquear dicha cuenta.
- Duración del bloqueo de cuenta
Esta política nos permite definir la cantidad de tiempo en la cual la cuenta involucrada permanecerá bloqueada y este tiempo se expresa en minutos en un rango entre 1 y 99.999 minutos; Si establecemos el valor 0 solo un administrador podrá desbloquear dicha cuenta.
- Umbral de bloqueo de cuenta
Esta es la política que nos permite llevar un control especial en términos de seguridad ya que allí definiremos la cantidad de intentos de inicio de sesión fallidos antes de que la cuenta sea bloqueada. Si el valor está en cero la cuenta no será bloqueada, por lo que esa opción no es recomendable. Aquí podremos definir un valor entre 0 y 999. Esta política es la principal para los bloqueos de accesos, ya que una vez bloqueada por intentos de sesión fallidos, sólo un administrador tendrá el derecho para deshabilitarla.
