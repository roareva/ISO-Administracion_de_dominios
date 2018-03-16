# G. Se han utilizado máquinas virtuales para administrar dominios y verificar su funcionamiento.
Para la elaboración de este documento que consistía en la administración de dominios en Windows Server 2016 hemos hecho uso de máquinas virtuales, en concreto de Virtual Box. 

Descargamos la ISO del sistema correspondiente y la instalamos en nuestra máquina virtual, de manera que usando este proceso podemos virtualizar este poderoso sistema operativo de Microsoft y aprovechar al máximo sus grandes capacidades y beneficios para la gestión de usuarios, equipos y demás elementos de la infraestructura organizacional.

Para concluir esta parte, dejamos las ventajas de la virtualización de un sistema:
1. Sacar más partido de los recursos existentes, permitiendo el uso compartido de los mismos. Antes de virtualizar, es frecuente que el índice de uso de los recursos no supere el 50%, de hecho, es muy común que no supere el 15%.
2. Reducir los costes de los centros de datos reduciendo su infraestructura física. Esto deriva en una necesidad menor de espacio y una reducción en el consumo de energía y en las necesidades de refrigeración, lo que, además de suponer un ahorro, contribuye a la mejora del medio ambiente en consonancia con las nuevas tendencias en Green Computing (conocido también como Green-IT) que podríamos traducir al español Tecnologías Verdes.
3. Reducir el tiempo dedicado a la administración, ya que se dispone de herramientas más avanzadas. Además, podemos tener agrupada toda la capacidad de proceso en varios servidores físicos, entre los que se produce un balanceo dinámico de las máquinas virtuales, administrando de forma centralizada toda la capacidad de cálculo, memoria, almacenamiento, red, etc., y garantizando que cada máquina virtual se ejecuta sobre el host más adecuado en cada momento.
4. Otra forma de reducir el tiempo de administración es fragmentar los servicios porque, en lugar de tener un gran servidor que centralice todos los servicios de la empresa, podemos definir pequeños servidores virtuales, especializados cada uno de ellos en un servicio concreto (un servidor web, un servidor de impresión, un servidor de centralita telefónica, etc.). De este modo, se simplifica la administración de cada uno de ellos y se evitan las posibles interrelaciones no deseadas.
5. Relacionado con lo anterior, podemos mencionar el aislamiento entre las diferentes máquinas virtuales, que repercutirá en que un fallo en una de ellas no afecte al resto.
6. Aumentar la disponibilidad, ya que se puede disponer de mecanismos de copia de seguridad y clonación de máquinas virtuales completas para migrarlas a un hardware diferente, eliminando tiempos de inactividad y recuperándose de forma inmediata de cualquier problema. En ocasiones, la migración de un sistema a otro puede hacerse incluso en caliente (sin parar el host y sin dejar de ofrecer servicio).
7. Aumentar la flexibilidad de la implantación, para responder de una forma más rápida a los posibles cambios que deban realizarse. Por ejemplo, podemos añadir recursos a los servidores virtualizados de una forma rápida y sencilla.
8. Disponer de un método para crear entornos de prueba que nos permitan analizar nuevas soluciones antes de que puedan afectar al resto de la infraestructura.
9. Administrar y gestionar sistemas de escritorio seguros que estén accesibles a los usuarios de forma local o remota desde casi cualquier ordenador del lado cliente.

Nuestra máquina virtual con el Windows Server con la versión GUI es la siguiente:
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/g/w.jpg)
Mientras que versión Core:

![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/g/0.jpg)
![img](https://github.com/roareva/ISO-Administracion_de_dominios/blob/master/img/g/1.jpg)
