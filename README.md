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

1. **Genómica comparativa:**  
   - Estudio de las similitudes y diferencias entre genomas de diferentes organismos.

2. **Análisis de DNA:**  
   - Identificación de ORFs (Marcos Abiertos de Lectura).  
   - Análisis de contenido GC (proporción de bases Guanina y Citosina).  
   - Anotación de secuencias genómicas.

3. **Recuperación y ensamblaje de secuencias:**  
   - Recuperación de secuencias de bases de datos genómicas.  
   - Ensamblaje de secuencias a partir de datos de secuenciación (por ejemplo, lecturas cortas de NGS).

4. **Predicción y visualización de estructuras de proteínas:**  
   - Modelado de estructuras proteicas a partir de secuencias de aminoácidos.  
   - Visualización de estructuras 3D de proteínas utilizando herramientas computacionales.

5. **Microarreglos:**  
   - Análisis de datos de expresión génica mediante microarreglos de DNA.

6. **PCR (Reacción en Cadena de la Polimerasa):**  
   - Diseño de cebadores y análisis de resultados de PCR.

7. **Filogenia:**  
   - Reconstrucción de árboles filogenéticos para estudiar relaciones evolutivas entre especies.

8. **Metagenómica:**  
   - Análisis de comunidades microbianas a partir de muestras ambientales.  
   - Identificación y caracterización de genomas de microorganismos no cultivables.

9. **Transcriptómica:**  
   - Estudio de la expresión génica mediante el análisis de RNA.  
   - Análisis de datos de RNA-seq para identificar genes activos y sus niveles de expresión.

10. **Educación:**  
    - Desarrollo de herramientas y recursos educativos para la enseñanza de la bioinformática.

La Bioinformática provee de algoritmos, bases de datos, interfaces y herramientas estadísticas para resolver nuestras preguntas biológicas.

## Definición y funciones básicas de un sistema operativo

**Definición:**  
Un **sistema operativo (SO)** es el software principal que gestiona los recursos de hardware y software de una computadora, actuando como intermediario entre el usuario, las aplicaciones (como herramientas de bioinformática) y el hardware.

**Funciones básicas en bioinformática:**  
1. **Gestión de recursos:**  
   - Asigna memoria, procesamiento y almacenamiento para ejecutar programas de análisis de datos biológicos (por ejemplo, alineación de secuencias o ensamblaje de genomas).  

2. **Ejecución de herramientas bioinformáticas:**  
   - Permite correr software especializado (como BLAST, GROMACS o herramientas de RNA-seq) de manera eficiente.  

3. **Manejo de archivos y datos:**  
   - Organiza y gestiona grandes volúmenes de datos genómicos, proteómicos o de secuenciación.  

4. **Interfaz de usuario:**  
   - Proporciona entornos gráficos (GUI) o de línea de comandos (CLI) para interactuar con programas y scripts.  

5. **Conectividad y redes:**  
   - Facilita el acceso a bases de datos remotas (como NCBI o UniProt) y el uso de recursos en la nube.  

6. **Seguridad y permisos:**  
   - Protege datos sensibles (por ejemplo, genomas personales) y controla el acceso a recursos compartidos en servidores.  

## Estructura básica de un sistema operativo

![image](https://github.com/bioinfoperu/Introduccion_a_Linux_para_bioinformatica/blob/main/img/OS_Linux.PNG)
*Un sistema operativo está organizado en varias capas o componentes que trabajan juntos para gestionar los recursos de la computadora y permitir la ejecución de programas. Estas son las partes principales*

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

## Sistemas operativos en Bioinformática

## Linux

### ¿Qué es LINUX?

LINUX es un sistema operativo que fue desarrollado por primera vez en la década de los 90’s por Linus Torvalds, y ha estado en constante desarrollo desde entonces. Por sistema operativo, nos referimos al conjunto de programas que hacen que la computadora trabaje. Además Linux es:

* Es un sistema multi-usuario estable. 
* Multi-tarea para servidores, equipos de escritorio y portátiles.

El sistemas Linux disponen de una interfaz gráfica de usuario (GUI), similar a Microsoft Windows, que proporciona un entorno fácil de usar; sin embargo, se requieren conocimientos de Linux para las operaciones que no estén cubiertos por un programa gráfico, o cuando no hay una interfaz de ventanas disponibles, por ejemplo, cuando se trabaja en un servidor local o en una nube, ya que ellos tienen una sesion de telnet. Hay muchas versiones diferentes de Linux, aunque comparten similitudes comunes. Las variedades más populares de LINUX son los sistemas Sun Solaris, GNU/Linux y MacOS X.

### Sistema operativo Linux

El sistema operativo LINUX se compone de tres partes: **el núcleo (Kernel), el shell y los programas.**



_Introduction to Linux and Command Line Tools for Bioinformatics_ (Figure 1.1)

### El nucleo (kernel)

El kernel de Linux es el centro del sistema operativo: asigna el tiempo y la memoria a los programas, maneja el almacenamiento de archivos y la comunicación en respuesta a las llamadas del sistema operativo.

Como ejemplo, la forma en que el **shell** y el **kernel** trabajan juntos, supongamos que un usuario escribe **rm myfile** (que tiene el efecto de eliminar el file myfile). El **shell** busca en el almacén de archivos, el archivo que contiene el programa rm, y luego pide al **kernel**, a través de las llamadas del sistema, ejecuta el programa **rm** en **myfile**. Cuando el proceso **rm myfile** ha terminado de ejecutarse, el shell devuelve el indicador de LINUX para el usuario, lo que indica que se está a la espera de nuevas órdenes.

### El shell
  
El **shell** actúa como una interfaz entre el **usuario** y el **kernel**. Cuando un usuario inicia una sesión, el programa de inicio de sesión comprueba el nombre de usuario y contraseña, y luego se inicia otro programa llamado el shell. El shell es un **intérprete de línea de comandos** (ILC). Interpreta los comandos que el usuario escribe para que puedan ser llevadas a cabo. Los comandos son los mismos programas, cuando se terminan, el shell retorna al al usuario para los siguientes pasos a desarrollar (**$** en nuestros sistemas).

El usuario experto puede personalizar su propia shell, y los usuarios pueden utilizar diferentes shells en la misma máquina. Para el tema de hoy, el profesor y los alumnos la **bash** shell de forma predeterminada.

El bash shell tiene ciertas características que ayudan al usuario introducir comandos.

**Finalización del nombre** - Al escribir parte del nombre de un comando, nombre de archivo o directorio y pulsando el **Tab** (una vez), el bash shell completará el resto del nombre de forma automática. Si en el directorio se encuentra más de un nombre que empiece con esas letras que ha escrito, se emitirá un resultado, mostrará una cantidad de palabras o las palabras encontradas que empiezan con esas letras.

**Historial** - El shell mantiene una lista de comandos que ha escrito. Si usted tiene que repetir un comando, utilice las teclas de cursor para desplazarse hacia arriba y abajo en la lista de comandos anteriores o puede escribir el comando **history** para poder observar una lista de los comandos que estuvo trabajando. 

`~$ history`

### Archivos y Procesos

**Todo en LINUX es un archivo.**

Un proceso es un programa en ejecución identificado por un PID único (identificador de proceso).

Un archivo es una colección de datos. Son creados por los usuarios que utilizan los editores de texto, compiladores en procesos, etc.

Ejemplos de archivos:

* Un documento (informe, ensayo, etc.)

* El texto de un programa escrito en un lenguaje de programación de alto nivel (Python, R, Perl, etc).

* Instrucciones comprensibles directamente a la máquina e incomprensible para un usuario ocasional, por ejemplo, una  colección de dígitos binarios (un archivo ejecutable o binaria);

* Un directorio, que contiene información acerca de su contenido, que puede ser una mezcla de otros directorios (subdirectorios) y archivos ordinarios.

### La estructura de los directorios

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

## Instalación de entornos en CONDA

### ¿Qué es un entorno?

Un entorno es un directorio que contiene una colección específica de paquetes o herramientas que ha instalado. Por ejemplo, puede tener un entorno con Python 2.7 y sus dependencias, y otro entorno con Python 3.4 para realizar pruebas heredadas. Si cambia un entorno, los demás no se verán afectados. Puede activar o desactivar entornos fácilmente, que es la forma de cambiar entre ellos.

![entornos](https://angus.readthedocs.io/en/2019/_static/envs.png)

### CONDA

CONDA como gestor de paquetes te ayuda a encontrar e instalar paquetes. Si necesitas un paquete que requiere una versión diferente de Python, no necesitas cambiar a un gestor de entorno diferente, porque CONDA también es un gestor de entorno.

Con sólo unos pocos comandos, puedes configurar un entorno totalmente separado para ejecutar esa versión diferente de Python, mientras sigues ejecutando tu versión habitual de Python en tu entorno normal.

![conda](https://miro.medium.com/v2/resize:fit:720/format:webp/0*hNmbKX5rGY19csb0.png)

### Miniconda

CONDA proporciona paquetes o binarios pre-compilados (lo que generalmente evita la necesidad de tener que compilar paquetes desde el código fuente).

CONDA es multiplataforma, con soporte para Windows, MacOS, GNU/Linux, y soporte para múltiples plataformas de hardware, como x86 y Power 8 y 9.

CONDA está pensado para proyectos en ciencia de datos (data scientists), con los que compartimos diseño y ejecución de proyectos (workflows).

### Instalación de Miniconda

```bash
# creación de carpeta, preferiblemente en /home/USUARIO/
mkdir -p ~/miniconda3
#descargar el instalador
wget repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
#correr el instalador
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
# eliminar el instalador
rm -rf ~/miniconda3/miniconda.sh
# ejecutar conda por defecto en el terminal
~/miniconda3/bin/conda init bash
# abrir un nuevo terminal y deberías encontrarte en:
```

### ¿Cómo trabaja CONDA?

![work](https://angus.readthedocs.io/en/2019/_static/conda2.png)

### Entornos de CONDA

### Canales de CONDA

![channels](https://angus.readthedocs.io/en/2019/_static/conda4.png)

![channels](https://angus.readthedocs.io/en/2019/_static/conda5.png)


```
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
```

### Comandos de CONDA

|                 Comando de Conda                |                                                Acción                                                |
|:-----------------------------------------------:|:----------------------------------------------------------------------------------------------------:|
| `conda install`                                  | Instalar un paquete.                                                                                 |
| `conda list`                                      | Listar los paquetes instalados en el entorno actualmente activo.                                     |
| `conda search`                                    | Buscar un paquete en los canales configurados.                                                       |
| `conda info`                                      | Mostrar información sobre el entorno actual.                                                         |
| `conda remove`                                    | Eliminar un paquete de Conda.                                                                        |
| `conda config --get channels`                     | Listar los canales activos y sus prioridades.                                                        |
| `conda update`                                    | Actualizar todos los paquetes instalados.                                                            |
| `conda config --remove channels unwanted_channel` | Eliminar un canal de Conda específico.                                                               |
| `conda env list`                                  | Listar los diferentes entornos creados con Conda.                                                    |
| `conda activate myNewEnvironment`                 | Activar el entorno de Conda llamado myNewEnvironment. También funciona para activar el entorno base. |
| `conda info --envs`                               | Mostrar la ubicación de los directorios de Conda y los entornos disponibles.                         |
