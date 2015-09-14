#Título: Gestor de versiones subversion.
##Tarea: Número 1 en equipo.
##Nombre: Edilzar Cisneros Ancheyta
**Introducción**.
<p style="text-align: justify;">
En este documento se tomara a fondo el tema de gestión de versiones tratado previemente en el curso, con una investigación especifica del gestor de versiones Subversion. Tomando en cuenta los puntos vistos en clase podremos hablar del funcionamiento de la herramienta, como son sus comandos y la forma en la que se utiliza además de tratar un poco de su historia y las caracteristicas principales que pueden o no distinguir de otros gestores de versiones.
</p>

**Historia**.
<p style="text-align: justify;">
A principios del 2000, CollabNet, Inc. comenzó a buscar desarrolladores para escribir un sustituto para CVS. CollabNet ofrece un conjunto de herramientas de software colaborativo llamado SourceCast, del cual un componente es el control de versiones. Aunque SourceCast usaba CVS como su sistema de control de versiones inicial, las limitaciones de CVS se hicieron evidentes desde el principio, y CollabNet sabía que tendría que encontrar algo mejor. Desafortunadamente, CVS se había convertido en el estándar de facto en el mundo del código abierto porque no había nada mejor, al menos no bajo una licencia libre. Así CollabNet decidió escribir un nuevo sistema de control de versiones desde cero, manteniendo las ideas básicas de CVS, pero sin sus fallos y defectos.
En febrero del 2000, contactaron con Karl Fogel, autor de Open Source Development with CVS, y le preguntaron si le gustaría trabajar en este nuevo proyecto. Casualmente, por aquel entonces Karl ya se encontraba discutiendo sobre el diseño de un nuevo sistema de control de versiones con su amigo Jim Blandy. En 1995, los dos habían fundado Cyclic Software, compañía que hacía contratos de soporte de CVS, y aunque después vendieron el negocio, seguían usando CVS todos los días en sus trabajos. La frustración de ambos con CVS había conducido a Jim a pensar cuidadosamente acerca de mejores vías para administrar datos versionados , y no sólo tenía ya el nombre de “Subversion”, sino también el diseño básico del repositorio de Subversion. Cuando CollabNet llamó, Karl aceptó inmediatamente trabajar en el proyecto, y Jim consiguió que su empresa, RedHat Software, básicamente lo donara al proyecto por un período de tiempo indefinido
</p>
<p style="text-align: justify;">
Después de catorce meses de codificación, Subversion pasó a ser “auto-hospedado” el 31 de agosto de 2001. Es decir, los desarrolladores de Subversion dejaron de usar CVS para la administración del propio código fuente de Subversion, y en su lugar empezaron a usar Subversion.
Si bien fue CollabNet quien inició el proyecto, y todavía financia una gran parte del trabajo, Subversion funciona como la mayoría de proyectos de código abierto, dirigido por un conjunto informal de reglas transparentes que fomentan el mérito. La licencia copyright de CollabNet es completamente compatible con las Directrices de Software Libre de Debian.
</p>
- - -

* * *

**Características**.
<p style="text-align: justify;">
A continuación se alistaran las características que Subversion brinda, tratando de mejorar por lo que fue creado es decir los pequeños o grandes fallos que CVS contenía.
</p>
* **Versionado de directorios.** Es un sistema de ficheres versionados que sigue los cambios sobre arboles de directorios completos a través del tiempo.
* Verdadero historial de versiones: se puede añadir, copiar, borrar  y renombrar ficheros y directorios.
* **Envíos atómicos.** Una colección cualquiera de modificaciones o bien entra por completo al repositorio o no entra en absoluto.
* **Versionado de metadatos.** Se puede crear y almacenar cualquier par arbitrario de clave o valor que se desee agregar.
* **Elección de capas de red.** Aquí se puede elegir la conexión a el servidor HTTP.
* **Manipulación consistente de los datos.** Subversion utiliza un algoritmo de diferenciación binario que funciona para los ficheros de texto y binarios.
* **Ramificación y etiquetado eficientes.** Es la creación de ramas y etiquetas simplemente copiando el proyecto.
* **Hackability.** Puede ser usado fácilmente por otras aplicaciones y lenguajes.

**Comandos y su descripción.**

A continución alistaremos los comandos básicos para el uso de Subversion, así como su descripción y su sintaxis.

1. **Ayuda.**
Este comando nos sirve para ver la ayuda necesaria para el uso de un comando y su sintaxis es la siguiente:
$ svn help subcomando

	Donde Subcomando es el comando para el cual requerimos ayuda.

2. **Subir los cambios**
El siguiente comando es CI el cual utilizaremos para compartir los cambios con los demás desarrolladores, su sintaxis es:
$ svn ci

3. **Agregar un archivo.**
Para agregar un archivo o una carpeta y todo su contenido al control de versiones se usa el subcomando add, su sintaxis es la siguiente:
$ svn add archivo.src carpeta/

4. **Borrar un archivo.**
De la misma manera en que se agrega un archivo para borrar es algo similar, su sintaxis es la siguiente:
$ svn delete archivo.src carpeta/

5. **El comando update.**
Nos sirve para asegurar que despues de dejar de trabajar con un repositorio y retomarlo tiempo despues, sea la ultima copia del repositorio, su sintaxis es
$ svn update

- - -

* * *

6. **Cambios.**
Para observar el historial de cambios y saber que usuario modificó el archivo podemos utilizar el siguiente comando:
$ svn log

7. **Diferencias entre versiones.**
Si queremos encontrar los cambios que se han realizado en un archivo en particular entre la versión actual y la anterior podemos usar el comando diff, su sintaxis es la siguiente:
$svn diff nombre_archivo

8. **Exportar.**
Si se desea trabajar con unn archivo fuera del ambiente subversion, se pueden exportar con el siguiente comando:
$ svn export carpeta_origen carpeta_destino

9. **Etiquetar versión.**
Si se desea hacer el etiquetado de una nueva versión y estabilizar los cambios de la rama trunk podemos utilizar el siguiente comando:
$ svn copy nombre del repo/trunk -r #revisión nombre del repo/tags/nombre de la etiqueta -m "comentario".

10. **Excluir archivos.**
Si se desea excluir archivos generados manualmente y no se quieren subir al repositorio podemos agregarlos a la lista de exclusión con el siguiente comando:
$ svn propedit svn:ignore

**Referencias**

>Ben Collins-Sussman, Brian W. Fitzpatrick, C. Michael Pilato. (2004). Control de versiones con Subversion. Stanford, California 94305, USA.: Creative Commons Attribution License.
