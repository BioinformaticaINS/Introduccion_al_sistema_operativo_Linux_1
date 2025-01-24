# Introduccion al sistema operativo Linux 1

Familiarizarse con los comandos básicos del sistema operativo Linux para el manejo de data relacionada con Next Generation Sequencing (NGS), en este caso trabajaremos con datos de la tecnología de Illumina.

Si quieres saber más sobre NGS te invitamos a que revises el tutorial de NGS: https://github.com/bioinfoperu/Introduccion_Next_Genetarion_Sequencing

## Instructor 👨‍🏫  
Manuel Alain Ramírez Sáenz --> Llámame `MARS`


## Bioinformática 🚀


"La bioinformática comprende los métodos matemáticos, estadísticos y computacionales que pretenden solucionar  problemas biológicos usando secuencias de ADN y aminoácidos e información relacionada" `Fredj Tekaia - Instituto Pasteur`

## Requerimientos

**Necesario:**
* Conocimiento y entendimiento del Dogma Central de la Biología Molecular.
* Conocimiento en Biología Molecular (Bioquímica, Biología Molecular, Biofísica Molecular).

**Muy necesario:**
* Conocimiento en el manejo de sistemas de cómputo.

**Recomendado:**
* **_Manejo básico de linea de comandos en ambientes UNIX (GNU/Linux)._**

**Muy deseable:**
* Experiencia con algún lenguaje de programación (Python, Perl o R).

## Objetivo de la Bioinformática

"Profundizar en nuestro entendimiento acerca de los organismos vivos y sus relaciones, partiendo desde el genoma que los codifica"

## Campos de trabajo

* Genómica comparativa
* Análisis de DNA (ORFs, contenidos GC, etc.)
* Recuperación de secuencias.
* Ensamblajes de secuencias.
* Predicción de estructuras de proteínas.
* Visualización de estructuras de proteínas.
* Microarreglos.
* PCR.
* Filogenia.
* Educación.

La Bioinformática provee de algoritmos, bases de datos, interfaces y herramientas estadísticas para resolver nuestras preguntas biológicas.

## Sistema operativo Linux

Muchos desarrolladores de programas en Bioinformática prefieren el uso del sistema operativo Linux. Aqui algunos ejemplos sobre estos programas: FASTQC, trimmomatic, kraken, bwa, bowtie, SPAdes, etc. Dichos programas requieren de un usuario con un buen nivel en el manejo de Linux; sin embargo, muchos investigadores que necesitan trabajar con Next Generation Sequecing (NGS) no son familiares con el sistema operativo Linux y requieren de una introducción en el tema. Ahora, el usuario se preocupará entre conocer las características de Linux y los programas mientras aprende sobre las herramientas para NGS.

## Objetivo

El objetivo de este módulo es **introducir a los participantes en el sistema oprativo Linux** y cubrir con algunas cosas básicas que les permitirán correr algunos de los programas en sus computadoras o laptops. 

## ¿Qué es LINUX?

LINUX es un sistema operativo que fue desarrollado por primera vez en la década de los 90’s por Linus Torvalds, y ha estado en constante desarrollo desde entonces. Por sistema operativo, nos referimos al conjunto de programas que hacen que la computadora trabaje. Además Linux es:

* Es un sistema multi-usuario estable. 
* Multi-tarea para servidores, equipos de escritorio y portátiles.

El sistemas Linux disponen de una interfaz gráfica de usuario (GUI), similar a Microsoft Windows, que proporciona un entorno fácil de usar; sin embargo, se requieren conocimientos de Linux para las operaciones que no estén cubiertos por un programa gráfico, o cuando no hay una interfaz de ventanas disponibles, por ejemplo, cuando se trabaja en un servidor local o en una nube, ya que ellos tienen una sesion de telnet. Hay muchas versiones diferentes de Linux, aunque comparten similitudes comunes. Las variedades más populares de LINUX son los sistemas Sun Solaris, GNU/Linux y MacOS X.

## Sistema operativo Linux

El sistema operativo LINUX se compone de tres partes: **el núcleo (Kernel), el shell y los programas.**

![image](https://github.com/bioinfoperu/Introduccion_a_Linux_para_bioinformatica/blob/main/img/OS_Linux.PNG)

_Introduction to Linux and Command Line Tools for Bioinformatics_ (Figure 1.1)

## Interfaz Gráfica de Usuario (GUI) vs. Interfaz de Línea de Comandos (CLI)

|  Característica  |              GUI             |                CLI                |
|:----------------:|:----------------------------:|:---------------------------------:|
| Interacción      | Iconos y elementos visuales  | Comandos de texto                 |
| Facilidad de uso | Más fácil para principiantes | Requiere conocimiento de comandos |
| Eficiencia       | Puede ser más lento          | Generalmente más rápido           |
| Flexibilidad     | Menos flexible               | Más flexible                      |
| Precisión        | Menor                        | Mayor                             |
| Apariencia       | Personalizable               | No personalizable                 |
| Recursos         | Requiere más memoria         | Requiere menos memoria            |

## El nucleo (kernel)

El kernel de Linux es el centro del sistema operativo: asigna el tiempo y la memoria a los programas, maneja el almacenamiento de archivos y la comunicación en respuesta a las llamadas del sistema operativo.

Como ejemplo, la forma en que el **shell** y el **kernel** trabajan juntos, supongamos que un usuario escribe **rm myfile** (que tiene el efecto de eliminar el file myfile). El **shell** busca en el almacén de archivos, el archivo que contiene el programa rm, y luego pide al **kernel**, a través de las llamadas del sistema, ejecuta el programa **rm** en **myfile**. Cuando el proceso **rm myfile** ha terminado de ejecutarse, el shell devuelve el indicador de LINUX para el usuario, lo que indica que se está a la espera de nuevas órdenes.

## El shell
  
El **shell** actúa como una interfaz entre el **usuario** y el **kernel**. Cuando un usuario inicia una sesión, el programa de inicio de sesión comprueba el nombre de usuario y contraseña, y luego se inicia otro programa llamado el shell. El shell es un **intérprete de línea de comandos** (ILC). Interpreta los comandos que el usuario escribe para que puedan ser llevadas a cabo. Los comandos son los mismos programas, cuando se terminan, el shell retorna al al usuario para los siguientes pasos a desarrollar (**$** en nuestros sistemas).

El usuario experto puede personalizar su propia shell, y los usuarios pueden utilizar diferentes shells en la misma máquina. Para el tema de hoy, el profesor y los alumnos la **bash** shell de forma predeterminada.

El bash shell tiene ciertas características que ayudan al usuario introducir comandos.

**Finalización del nombre** - Al escribir parte del nombre de un comando, nombre de archivo o directorio y pulsando el **Tab** (una vez), el bash shell completará el resto del nombre de forma automática. Si en el directorio se encuentra más de un nombre que empiece con esas letras que ha escrito, se emitirá un resultado, mostrará una cantidad de palabras o las palabras encontradas que empiezan con esas letras.

**Historial** - El shell mantiene una lista de comandos que ha escrito. Si usted tiene que repetir un comando, utilice las teclas de cursor para desplazarse hacia arriba y abajo en la lista de comandos anteriores o puede escribir el comando **history** para poder observar una lista de los comandos que estuvo trabajando. 

`~$ history`

## Archivos y Procesos

**Todo en LINUX es un archivo.**

Un proceso es un programa en ejecución identificado por un PID único (identificador de proceso).

Un archivo es una colección de datos. Son creados por los usuarios que utilizan los editores de texto, compiladores en procesos, etc.

Ejemplos de archivos:

* Un documento (informe, ensayo, etc.)

* El texto de un programa escrito en un lenguaje de programación de alto nivel (Python, R, Perl, etc).

* Instrucciones comprensibles directamente a la máquina e incomprensible para un usuario ocasional, por ejemplo, una  colección de dígitos binarios (un archivo ejecutable o binaria);

* Un directorio, que contiene información acerca de su contenido, que puede ser una mezcla de otros directorios (subdirectorios) y archivos ordinarios.

## La estructura de los directorios

Todos los archivos se agrupan en la estructura de directorios. El sistema de archivos se organiza en una estructura jerárquica, como un **árbol invertido**. La parte superior de la jerarquía se denomina tradicionalmente **root** (escrita como una barra /)

![image](https://github.com/bioinfoperu/Introduccion_a_Linux_para_bioinformatica/blob/main/img/Estructure_Directories.PNG)

_En clase mencionaremos que contiene cada diretorio_
