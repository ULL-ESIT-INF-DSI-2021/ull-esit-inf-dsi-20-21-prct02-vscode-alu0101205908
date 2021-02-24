# PRÁCTICA 2: Instalación y configuración de Visual Studio Code

En esta segunda práctica, hemos configurado en nuestro entorno de trabajo el que va a ser nuestro **[IDE](https://es.wikipedia.org/wiki/Entorno_de_desarrollo_integrado)** para la asignatura de Desarrollo de Sistemas Informáticos. Se trata de **[Visual Studio Code](https://code.visualstudio.com/)** (VSC), un editor de código desarrollado por Microsoft para distintos sistemas operativos. Lo que vamos a realizar es, mediante el protocolo SSH vamos a utilizar de manera remota el VSC que tendremos instalado en nuestra máquina local (ML), en nuestra máquina virtual (MV) del IaaS.

Para acceder a la GitHub page: **[AQUÍ](https://ull-esit-inf-dsi-2021.github.io/ull-esit-inf-dsi-20-21-prct02-VScode-alu0101205908/)** 


## Tareas iniciales:

* Para empezar, debemos instalar el  VSC en nuestra ML, para ello hacemos:

  * borja@ubuntu:~$ sudo apt install code

* En mi caso, ya lo tengo instalado, dado que me parece un editor y entorno para programar muy bueno.


## Configuración de Visual Studio Code para conectarse a una máquina remota por SSH:

* Una vez tenemos el VSC instalado en nuestra ML, tendremos que activar la VPN de la ULL, porque vamos a empezar a trabajar con la MV. Para realizar la configuración, debemos:

   * Abrir el VSC y pulsar la combinación **Ctrl + Shift + P**.
   * Tecleamos **ssh** y hacemos clic en **Connect to Host**.

   **NOTA:** Cabe destacar, que para que funcione debemos de haber realizado correctamente la configuración de los ficheros pertinentes tanto en la ML como en la MV que se vió en la **[práctica 1](https://ull-esit-inf-dsi-2021.github.io/ull-esit-inf-dsi-20-21-prct01-iaas-alu0101205908/)** 

* Se nos iniciará una nueva ventana de VSC (gracias a la conexión vía SSH que hemos realizado). A continuación, abrimos una nueva terminal en el VSC, y comprobamos que el nombre del host se corresponde con el nombre de nuestra máquina (***iaas-dsi16***):

![Hostname][Hostname]


## Primer proyecto en TypeScript: “Hola Mundo”:

* A continuación, vamos a realizar nuestro primer mini proyecto en TypeScript. En primer lugar vamos a instalar la extensión ***ESLint*** en el VSC. Asimismo, instalaremos el compilador de TypeScript desde la terminal de VSC en la MV, para ello ejecutaremos:

    * npm install --global typescript
    * **Y para comprobar la versión:** tsc --version

![npm][npm]

* Por otra parte, para empezar con nuestro primer proyecto, crearemos un nuevo directorio (*hello-world*), y dentro de él, ejecutamos el siguiente comando:

   * **Para crear el fichero package.json (establecer dependencias de desarrollo y ejecución):** npm init --yes

![npm init][npmInit]

* Una vez realizado lo anterior, vamos a abrir nuestra carpeta (directorio *hello-world*) en el VSC, haciendo clic en **File** --> **Open Folder** --> **hello-world**. Además, vamos a añadir el directorio a un espacio de trabajo, haciendo clic en **File** --> **Add Folder to Workspace** --> **hello-world** y para guardarlo, hacemos clic en **File** --> **Save Workspace As** y el nombre que le queramos poner al espacio de trabajo.

* A continuación, desde la terminal de VSC y en el directorio *hello-world*, crearemos el fichero **tsconfig.json**, donde se especificarán las opciones de nuestro compilador de TypeScript. En dicho fichero, añadimos las siguientes líneas.

![Configuración compilador TS][tsconfig]

* Ahora, crearemos en nuestro directorio *hello-world*, un subdirectorio *src* que va a ser donde tendremos el código fuente de TypeScript. Además crearemos el fichero index.ts y agregaremos las siguientes líneas:

let myString: string = "Hola Mundo";

console.log(myString);

* Compilamos el código TS desde la terminal de VSC (fuera de /src):

   * tsc

* Esto nos creará un nuevo directorio, *dist*, y dentro de este directorio el fichero index.js, que contendrá el  mismo código que el fichero index.ts pero en JavaScript. 

* Como podemos observar, la diferencia entre ambos ficheros es que la variable myString del fichero en TS está tipada (:string). Por último, ejecutamos el código JS generado en el directorio /dist:

   * node dist/index.js

![Diferencia TS y JS][diferencia]


## Opcional:

* He completado el siguiente curso: **[Curso GitHub Pages](https://lab.github.com/githubtraining/github-pages)**

  * El repositorio de muestra está en: **[Mi cuenta de GitHub](https://github.com/borjaguanchesicilia/github-pages-with-jekyll)**

* He completado el siguiente curso: **[Curso TypeScript Udemy](https://www.udemy.com/course/typescript-2020/)**


## Conclusión:

* En esta práctica, hemos configurado el Visual Studio Code de nuestra máquina local para utilizarlo en nuestra máquina virtual. Es bastante curioso como podemos utilizar el protocolo SSH no solo en nuestra terminal de la máquina local (para acceder a nuestra máquina virtual), sino que poder simular que tenemos el VSC en nuestra máquina virtual. Respecto a conceptos nuevos aprendidos están: la creación del espacio de trabajo, dado que yo ya era usuario de VSC, pero no me había percatado de que existía esta funcionalidad, asimismo, he aprendido a implementar un pequeño proyecto en VSC, en este caso utilizando TypeScript. Además, de manera opcional y por aprender a utilizar las herramientas que vamos a utilizar en la asignatura, he completado el curso de GitHub Pages y un curso de TypeScript en Udemy que recomendó un compañero de clase, dado que era gratuito.

[Hostname]: images/hostname.JPG "Hostname"
[npm]: images/npm.JPG "npm"
[npmInit]: images/npmInit.JPG "npm init"
[tsconfig]: images/tsconfig&WS.JPG "Configuración compilador TS"
[diferencia]: images/diferencia.JPG "Diferencia TS y JS"
