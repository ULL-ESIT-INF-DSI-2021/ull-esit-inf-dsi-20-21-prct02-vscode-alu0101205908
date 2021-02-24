# PRÁCTICA 2: Instalación y configuración de Visual Studio Code

En esta segunda práctica, hemos configurado en nuestro entorno de trabajo el que va a ser nuestro **[IDE](https://es.wikipedia.org/wiki/Entorno_de_desarrollo_integrado)** para la asignatura de Desarrollo de Sistemas Informáticos. Se trata de **[Visual Studio Code](https://code.visualstudio.com/)** (VS), un editor de código desarrollado por Microsoft para distintos sistemas operativos. Lo que vamos a realizar es, mediante el protocolo SSH vamos a utilizar de manera remota el VS que tendremos instalado en nuestra  máquina local (ML) en nuestra máquina virtual (MV) del IaaS.

Para acceder a la GitHub page: **[AQUÍ](https://ull-esit-inf-dsi-2021.github.io/ull-esit-inf-dsi-20-21-prct02-vscode-alu0101205908/)** 


## Tareas iniciales:

* Para empezar, debemos instalar el  VS en nuestra ML, para ello hacemos:

  * borja@ubuntu:~$ sudo apt install code

* En mi caso, ya lo tengo instalado, dado que me parece el mejor editor y entorno para programar cualquier lenguaje.


## Configuración de Visual Studio Code para conectarse a una máquina remota por SSH:

* Una vez tenemos el VS instalado en nuestra ML, tendremos que activar la VPN de la ULL, porque vamos a empezar a trabajar con la MV. Para realizar la configuración, debemos:

   * Abrir el VS y pulsar la combinación **Ctrl + Shift + P**.
   * Tecleamos **ssh** y hacemos clic en **Connect to Host**.

   **NOTA:** Cabe destacar, que para que funcione debemos de haber realizado correctamente la configuración de los ficheros pertinentes tanto en la ML como en la MV que se vió en la **[práctica 1](https://ull-esit-inf-dsi-2021.github.io/ull-esit-inf-dsi-20-21-prct01-iaas-alu0101205908/)** 

* Se nos iniciará una nueva ventana de VS (gracias a la conexión vía SSH que hemos realizado). A continuación, abrimos una nueva terminal en el VS, y comprobamos que el nombre del host se corresponde con el nombre de nuestra máquina (***iaas-dsi16***):

![Hostname][Hostname]


## Primer proyecto en TypeScript: “Hola Mundo”:

* A continuación, vamos a realizar nuestro primer mini proyecto en TypeScript. En primer lugar vamos a instalar la extensión ***ESLint*** en el VS. Asimismo, instalaremos el compilador de TypeScript desde la terminal de VS en la MV, para ello ejecutaremos:

    * npm install --global typescript
    * **Y para comprobar la versión:** tsc --version

![npm][npm]

* Por otra parte, para empezar con nuestro primer proyecto, crearemos un nuevo directorio (*hello-world*), y dentro de él, ejecutamos el siguiente comando:

   * **Para crear el fichero package.json (establecer dependencias de desarrollo y ejecución):** npm init --yes

![npm init][npmInit]

* Una vez realizado lo anterior, vamos a abrir nuestra carpeta (directorio *hello-world*) en el VS, haciendo clic en **File** --> **Open Folder** --> **hello-world**. Además, vamos a añadir el directorio a un espacio de trabajo, haciendo clic en **File** --> **Add Folder to Workspace** --> **hello-world** y para guardarlo, hacemos clic en **File** --> **Save Workspace As** y el nombre que le queramos poner al espacio de trabajo.

* A continuación, desde la terminal de VS y en el directorio *hello-world*, crearemos el fichero **tsconfig.json**, donde se especificaran las opciones de nuestro compilador de TypeScript. En dicho fichero, añadimos las siguientes líneas.

![Configuración compilador TS][tsconfig]

[Hostname]: images/hostname.JPG "Hostname"
[npm]: images/npm.JPG "npm"
[npmInit]: images/npmInit.JPG "npm init"
[tsconfig]: images/tsconfig.JPG "Configuración compilador TS"
