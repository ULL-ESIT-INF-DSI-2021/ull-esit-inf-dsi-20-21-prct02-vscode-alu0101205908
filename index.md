# PRÁCTICA 2: Instalación y configuración de Visual Studio Code

En esta segunda práctica hemos configurado en nuestro entorno de trabajo el que va a ser nuestro **[IDE](https://es.wikipedia.org/wiki/Entorno_de_desarrollo_integrado)** para la asignatura de Desarrollo de Sistemas Informáticos. Se trata de **[Visual Studio Code](https://code.visualstudio.com/)** (VS), un editor de código fuente desarrollado por Microsoft para Windows, Linux y macOS. Incluye soporte para la depuración, control integrado de Git, resaltado de sintaxis, finalización inteligente de código, fragmentos y refactorización de código. Lo que vamos a realizar es mediante el protocolo SSH, vamos a utilizar de manera remota el VS que tendremos en nuestra  máquina local (ML) en nuestra máquina virtual (MV) del IaaS.

Para acceder a la GitHub page: **[AQUÍ](https://ull-esit-inf-dsi-2021.github.io/ull-esit-inf-dsi-20-21-prct02-vscode-alu0101205908/)** 


## Tareas iniciales:

* Para empezar, debemos instalar el  VS en nuestra ML, para ello hacemos:

  * borja@ubuntu:~$ sudo apt install code

* En mi caso, ya lo tengo instalado, dado que me parece el mejor editor y entorno para programar cualquier lenguaje.


## Configuración de Visual Studio Code para conectarse a una máquina remota por SSH:

* Una vez tenemos el VS instalado en nuestra ML, tendremos que activar la VPN de la ULL, porque vamos a empezar a trabajar con la MV. Para realizar la configuración, debemos:

   * Abrir el VS y pulsar la combinación **Ctrl * Shift * P**.
   * Tecleamos **ssh** y hacemos clic en **Connect to Host**.

* Se nos iniciará una nueva ventana de VS, gracias a la conexión vía SSH que hemos realizado. A continuación, abrimos una nueva terminal en el VS, y comprobamos el nombre del host:

![Hostname][Hostname]


[Hostname]: images/hostname.JPG "Hostname"
