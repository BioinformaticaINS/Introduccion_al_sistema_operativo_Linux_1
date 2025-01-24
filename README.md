# Introducción al sistema operativo Linux 1

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

Profundizar en nuestro entendimiento acerca de los organismos vivos y sus relaciones, partiendo desde el genoma que los codifica.

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

Muchos desarrolladores de programas en Bioinformática prefieren el uso del sistema operativo Linux. Aqui algunos ejemplos sobre estos programas: FASTQC, trimmomatic, kraken, bwa, bowtie, SPAdes, etc. Dichos programas requieren de un usuario con un buen nivel en el manejo de Linux; sin embargo, muchos investigadores que necesitan trabajar con Next Generation Sequecing (NGS) no se familiarizan aún con el sistema operativo Linux y requieren de una introducción en el tema. 

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

## Introducción a comandos básicos

### **1. Estructura típica de un proyecto NGS**
Explica brevemente que un proyecto NGS necesita una organización clara para almacenar los datos crudos, resultados intermedios y análisis finales. Una estructura sugerida puede ser:

```
Proyecto_NGS/
├── raw_data/
├── quality_control/
├── assembly/
├── annotation/
├── results/
└── scripts/
```

- **`raw_data/`**: Archivos FASTQ o BAM/CRAM originales.
- **`quality_control/`**: Archivos generados tras realizar el control de calidad (por ejemplo, con `fastqc` o `multiqc`).
- **`assembly/`**: Ensambles generados (fasta, índices, etc.).
- **`annotation/`**: Archivos relacionados con anotación funcional.
- **`results/`**: Resultados finales para el análisis.
- **`scripts/`**: Scripts utilizados en el proyecto.

---

### **2. Ejercicio práctico: Crear la estructura desde cero**
**Objetivo:** Enseñar comandos básicos como `mkdir`, `cd`, `ls`, `pwd`, `touch`, `cp`, y `mv`, mientras se crea y organiza la estructura de carpetas.

#### **Paso 1: Crear la carpeta del proyecto**
1. **Comando básico:** `mkdir`
   - Introduce `mkdir` para crear la carpeta principal del proyecto.
   - Ejemplo:  
     ```bash
     mkdir Proyecto_NGS
     ```

2. **Verificar la creación:** `ls`
   - Ejemplo:  
     ```bash
     ls
     ```

---

#### **Paso 2: Navegar dentro del proyecto**
1. **Comando básico:** `cd`
   - Muéstrales cómo entrar en la carpeta:
     ```bash
     cd Proyecto_NGS
     ```
2. **Verificar ubicación:** `pwd`
   - Ejemplo:
     ```bash
     pwd
     ```

---

#### **Paso 3: Crear subcarpetas**
1. Usar `mkdir` para crear las subcarpetas.
   - Ejemplo:
     ```bash
     mkdir raw_data quality_control assembly annotation results scripts
     ```
2. **Comando avanzado:** Crear varias carpetas al mismo tiempo.
   - Explica cómo separar nombres con espacios para crear múltiples carpetas.

---

#### **Paso 4: Verificar la estructura**
1. **Comando básico:** `ls -l`
   - Ejemplo:
     ```bash
     ls -l
     ```
2. **Comando avanzado:** `tree` (si está instalado).
   - Instalar y usar `tree` para mostrar la estructura jerárquica.

---

#### **Paso 5: Crear archivos vacíos**
1. Usar `touch` para simular archivos:
   - Ejemplo:
     ```bash
     touch raw_data/sample1.fastq raw_data/sample2.fastq
     ```
2. Mostrar cómo listar el contenido con `ls`.

---

#### **Paso 6: Mover y copiar archivos**
1. Crear una copia de los archivos FASTQ en la carpeta de control de calidad:
   ```bash
   cp raw_data/sample1.fastq quality_control/
   ```
2. Renombrar un archivo con `mv`:
   ```bash
   mv quality_control/sample1.fastq quality_control/sample1_qc.fastq
   ```

---

### **3. Integración de comandos adicionales**
A medida que los estudiantes se familiaricen con los comandos básicos, puedes introducir conceptos como:
- **Permisos:** `chmod`, `chown`.
- **Buscar archivos:** `find`, `grep`.
- **Compresión:** `gzip`, `tar`.
- **Monitorización:** `du`, `df`.

---

### **4. Tarea opcional**
Pídeles que creen un script en Bash para automatizar la creación de la estructura del proyecto y la generación de archivos vacíos. Ejemplo de script:

```bash
#!/bin/bash

mkdir -p Proyecto_NGS/{raw_data,quality_control,assembly,annotation,results,scripts}
touch Proyecto_NGS/raw_data/sample1.fastq Proyecto_NGS/raw_data/sample2.fastq
```
