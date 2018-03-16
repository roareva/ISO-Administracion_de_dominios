# A. Se han implementado dominios.
Para implementar dominios en Windows Server Core usaremos la terminal de comandos, en la cuál ejecutaremos powershell.exe para ello, pero primero le daremos un nombre a la computadora con el comando *Rename-computer -newname* **nombre**.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/0.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/1.jpg)
Y reiniciamos el sistema para hacer efectivo el cambio con el comando *Restart-Computer*.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/2.jpg)
Comprobamos que efectivamente se ha cambiado el nombre del equipo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/3.jpg)
Para proceder a implementar un dominio tenemos que instalar primero el rol de Servicios de dominio de Active Directory, que para ello, emplearemos el comando *Install-WindowsFeature*, que en este caso, la característica que vamos a instalar se llama AD-Domain-Services. Además, de paso, aprovecharemos para instalar todas las herramientas de gestión que puedan aplicarse a esta característica, lo que conseguimos con el argumento -IncludeManagementTools. Por lo tanto, la sintaxis del comando sería *Install-WindowsFeature -Name AD-Domain-Services -IncludeManagementTools*.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/4.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/5.jpg)
Una vez instalado, debemos importar los contenidos en el módulo ADDSDeployment a la sesión de trabajo actual, que es donde se encuentran los cmdlets que se utilizan en la implementación de servicios de dominio de Active Directory, que lo importamos con el comando 
*Import-Module ADDSDeployment*
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/6.jpg)
Y ahora para instalar un dominio, en vez de usar para ello el comando *Install-ADDSDomain*, vamos a usar el comando *Install-ADDSForest* ya que en nuestro caso estamos comenzando desde cero y no tenemos creada ninguna parte de la infraestructura (ni dominio ni controlador de dominio ni bosque), por lo que, si comenzamos creando el bosque, se creará automáticamente el resto de la estructura.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/7.jpg)
Como no añadimos todos los argumentos necesarios, el comando asignará valores predeterminados y nos pedirá lo imprescindible, como es el nombre del dominio y la contraseña de administración para el modo seguro (la contraseña deberá seguir los parámetros de seguridad exigidos por Windows Server, que debe contener mayúsculas, minúsculas y números).
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/8.jpg) 
Al hacerlo, nos aparece un aviso que nos informa de que nuestro servidor se convertirá en un controlador de dominio tras esta operación y que, al terminar, se producirá un reinicio de forma automática, que debemos escribir la letra S y después pulsar Intro para que se haga efectivo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/9.jpg)
Esperamos a la instalación del nuevo bosque.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/10.jpg)
Cuando se termine la instalación, procederá a reiniciarse el equipo.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/11.jpg)
Una vez reiniciado, ya al iniciarse el equipo, podremos autenticarnos como administradores del dominio.
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/12.jpg)
Para comprobar que se ha hecho efectivo el nuevo dominio, usamos de nuevo el sconfig.cmd y comprobamos que efectivamente es así, por lo tanto, ya hemos implementado un dominio en nuestro servidor. 
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/13.jpg)
--> [Siguiente apartado, apartado B](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/admin_dom/b/readme.md)
