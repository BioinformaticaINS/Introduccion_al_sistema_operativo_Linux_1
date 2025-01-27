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

3. **Obtención y ensamblaje de lecturas:**  
   - Obtención de lecturas de datos genómicas.  
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

Un sistema operativo está organizado en varias capas o componentes que trabajan juntos para gestionar los recursos de la computadora y permitir la ejecución de programas. Estas son las partes principales:

1. **Núcleo (Kernel):**  
   - Es el **corazón del sistema operativo**.  
   - Gestiona los recursos del hardware, como la memoria, el procesador (CPU) y los dispositivos de entrada/salida (teclado, mouse, discos duros, etc.).  
   - Se encarga de tareas críticas, como la asignación de memoria para programas y la gestión de procesos.  

2. **Interfaz de usuario:**  
   - Es la parte con la que los usuarios interactúan directamente.  
   - Puede ser una **interfaz gráfica (GUI)**, como ventanas e íconos, o una **interfaz de línea de comandos (CLI)**, donde se escriben comandos de texto.  
   - En bioinformática, muchas herramientas se usan desde la línea de comandos (CLI), especialmente en sistemas Linux.

3. **Sistema de archivos:**  
   - Organiza y gestiona cómo se almacenan y acceden los datos en el disco duro.  
   - En bioinformática, es crucial para manejar grandes volúmenes de datos, como secuencias de DNA, archivos FASTQ, BAM, etc.  

4. **Gestión de procesos:**  
   - Controla la ejecución de programas (procesos) en la computadora.  
   - Asigna tiempo de CPU a cada proceso y gestiona la ejecución de múltiples tareas al mismo tiempo (multitarea).  

5. **Gestión de memoria:**  
   - Administra el uso de la memoria RAM para que los programas puedan ejecutarse de manera eficiente.  
   - En bioinformática, esto es importante porque herramientas como alineadores de secuencias o ensambladores de genomas requieren mucha memoria.  

6. **Controladores de dispositivos (Drivers):**  
   - Son programas que permiten al sistema operativo comunicarse con el hardware (impresoras, tarjetas gráficas, discos duros, etc.).  
   - Por ejemplo, permiten que una computadora lea datos de un secuenciador de DNA.  

7. **Servicios del sistema:**  
   - Son programas que brindan funcionalidades adicionales, como la conexión a redes, la gestión de usuarios y permisos, o la instalación de software.  
   - En bioinformática, estos servicios son esenciales para acceder a bases de datos en línea o usar herramientas en la nube.  

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

![image](https://github.com/bioinfoperu/Introduccion_a_Linux_para_bioinformatica/blob/main/img/OS_Linux.PNG)

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

### **1. Comandos básicos para crear y navegar directorios**

1. **`mkdir`**: Crear directorios (carpetas).  
   - Ejemplo: Crear la carpeta principal del proyecto.  
     ```bash
     mkdir Proyecto_NGS
     ```
   - Crear múltiples subcarpetas al mismo tiempo:  
     ```bash
     mkdir raw_data quality_control assembly annotation results scripts
     ```

2. **`cd`**: Cambiar de directorio (navegar entre carpetas).  
   - Ejemplo: Entrar a la carpeta del proyecto.  
     ```bash
     cd Proyecto_NGS
     ```
   - Volver al directorio anterior:  
     ```bash
     cd ..
     ```
   - Ir al directorio personal (home):  
     ```bash
     cd ~
     ```

3. **`pwd`**: Mostrar la ruta completa del directorio actual.  
   - Ejemplo: Verificar en qué carpeta estás trabajando.  
     ```bash
     pwd
     ```

4. **`ls`**: Listar el contenido de un directorio.  
   - Ejemplo: Ver las carpetas y archivos dentro de `Proyecto_NGS`.  
     ```bash
     ls
     ```
   - Listar con detalles (permisos, tamaño, etc.):  
     ```bash
     ls -l
     ```
   - Listar todos los archivos, incluidos los ocultos:  
     ```bash
     ls -a
     ```

---

### **2. Comandos para crear y gestionar archivos**

1. **`touch`**: Crear archivos vacíos.  
   - Ejemplo: Crear archivos FASTQ simulados.  
     ```bash
     touch raw_data/sample1.fastq raw_data/sample2.fastq
     ```

2. **`cp`**: Copiar archivos o directorios.  
   - Ejemplo: Copiar un archivo FASTQ a la carpeta de control de calidad.  
     ```bash
     cp raw_data/sample1.fastq quality_control/
     ```
   - Copiar un directorio completo (usar `-r` para recursivo):  
     ```bash
     cp -r raw_data/ backup_raw_data/
     ```

3. **`mv`**: Mover o renombrar archivos o directorios.  
   - Ejemplo: Mover un archivo a otra carpeta.  
     ```bash
     mv raw_data/sample1.fastq quality_control/
     ```
   - Renombrar un archivo:  
     ```bash
     mv quality_control/sample1.fastq quality_control/sample1_qc.fastq
     ```

4. **`rm`**: Eliminar archivos o directorios.  
   - Ejemplo: Eliminar un archivo.  
     ```bash
     rm raw_data/sample1.fastq
     ```
   - Eliminar un directorio y su contenido (usar `-r` para recursivo):  
     ```bash
     rm -r backup_raw_data/
     ```

---

### **3. Comandos para verificar y explorar la estructura**

1. **`tree`**: Mostrar la estructura de directorios en forma de árbol.  
   - Ejemplo: Ver la estructura completa del proyecto.  
     ```bash
     tree Proyecto_NGS
     ```
   - Si no tienes `tree` instalado, puedes instalarlo con:  
     ```bash
     sudo apt install tree  # En distribuciones basadas en Debian/Ubuntu
     ```

2. **`find`**: Buscar archivos o directorios.  
   - Ejemplo: Buscar todos los archivos FASTQ en el proyecto.  
     ```bash
     find Proyecto_NGS -name "*.fastq"
     ```

3. **`du`**: Verificar el tamaño de archivos y directorios.  
   - Ejemplo: Ver el tamaño de la carpeta `raw_data`.  
     ```bash
     du -sh raw_data/
     ```

---

### **4. Comandos para comprimir y descomprimir archivos**

1. **`gzip`**: Comprimir archivos.  
   - Ejemplo: Comprimir un archivo FASTQ.  
     ```bash
     gzip raw_data/sample1.fastq
     ```

2. **`gunzip`**: Descomprimir archivos comprimidos con `gzip`.  
   - Ejemplo: Descomprimir un archivo FASTQ.  
     ```bash
     gunzip raw_data/sample1.fastq.gz
     ```

3. **`tar`**: Crear o extraer archivos comprimidos en formato `.tar.gz`.  
   - Ejemplo: Comprimir la carpeta `raw_data`.  
     ```bash
     tar -czvf raw_data.tar.gz raw_data/
     ```
   - Extraer un archivo `.tar.gz`:  
     ```bash
     tar -xzvf raw_data.tar.gz
     ```

---

### **5. Comandos para permisos y propiedad**

1. **`chmod`**: Cambiar permisos de archivos o directorios.  
   - Ejemplo: Dar permisos de ejecución a un script.  
     ```bash
     chmod +x scripts/mi_script.sh
     ```

2. **`chown`**: Cambiar el propietario de un archivo o directorio.  
   - Ejemplo: Cambiar el propietario de la carpeta `raw_data`.  
     ```bash
     sudo chown usuario:grupo raw_data/
     ```

---

### **6. Comandos para visualizar y editar archivos**

1. **`cat`**: Mostrar el contenido de un archivo.  
   - Ejemplo: Ver el contenido de un archivo FASTQ.  
     ```bash
     cat raw_data/sample1.fastq
     ```

2. **`less`**: Visualizar archivos largos página por página.  
   - Ejemplo: Navegar por un archivo FASTQ.  
     ```bash
     less raw_data/sample1.fastq
     ```

3. **`nano`**: Editor de texto en terminal.  
   - Ejemplo: Editar un script en Bash.  
     ```bash
     nano scripts/mi_script.sh
     ```

---

### **7. Comandos para redirección y tuberías (pipes)**

1. **`>`**: Redirigir la salida de un comando a un archivo.  
   - Ejemplo: Guardar la lista de archivos en un archivo de texto.  
     ```bash
     ls raw_data/ > lista_archivos.txt
     ```

2. **`|`**: Pasar la salida de un comando como entrada a otro.  
   - Ejemplo: Contar el número de archivos FASTQ.  
     ```bash
     ls raw_data/ | grep ".fastq" | wc -l
     ```

---

### **Resumen de comandos esenciales**

| Comando | Descripción |
|---------|-------------|
| `mkdir` | Crear directorios. |
| `cd`    | Cambiar de directorio. |
| `pwd`   | Mostrar la ruta actual. |
| `ls`    | Listar archivos y directorios. |
| `touch` | Crear archivos vacíos. |
| `cp`    | Copiar archivos o directorios. |
| `mv`    | Mover o renombrar archivos o directorios. |
| `rm`    | Eliminar archivos o directorios. |
| `tree`  | Mostrar la estructura de directorios. |
| `find`  | Buscar archivos o directorios. |
| `gzip`  | Comprimir archivos. |
| `tar`   | Crear o extraer archivos comprimidos. |
| `chmod` | Cambiar permisos. |
| `cat`   | Mostrar el contenido de un archivo. |
| `less`  | Visualizar archivos largos. |
| `nano`  | Editar archivos de texto. |

## **Introducción a comandos básicos para proyectos NGS**

Ahora utilizaremos comandos básicos de Linux para organizar y gestionar la estructura de un proyecto de **Next-Generation Sequencing (NGS)**. Estos comandos son esenciales para trabajar en bioinformática, ya que te permiten crear directorios, moverte entre carpetas, manipular archivos y automatizar tareas.

### **1. Estructura típica de un proyecto NGS**

Un proyecto de NGS requiere una organización clara para almacenar los datos crudos, resultados intermedios y análisis finales. A continuación, se propone una estructura de carpetas sugerida:

```
Proyecto_NGS/
├── raw_data/          # Datos crudos (FASTQ, BAM/CRAM)
├── quality_control/   # Resultados de control de calidad
├── assembly/          # Ensambles generados (FASTA, índices)
├── annotation/        # Anotaciones funcionales
├── results/           # Resultados finales del análisis
└── scripts/           # Scripts utilizados en el proyecto
```

#### **Descripción de las carpetas:**
- **`raw_data/`**: Contiene los archivos FASTQ o BAM/CRAM originales generados por el secuenciador.
- **`quality_control/`**: Aloja los resultados del control de calidad (por ejemplo, informes de `fastqc` o `multiqc`).
- **`assembly/`**: Guarda los ensambles genómicos o transcriptómicos en formato FASTA, así como índices asociados.
- **`annotation/`**: Archivos relacionados con la anotación funcional de genes o proteínas.
- **`results/`**: Resultados finales del análisis, como tablas de expresión génica o variantes identificadas.
- **`scripts/`**: Scripts en Bash, Python u otros lenguajes utilizados para automatizar tareas.

---

### **2. Comandos básicos para crear y organizar la estructura**

A continuación, se presentan los comandos esenciales para crear y gestionar la estructura de un proyecto NGS.

---

#### **Paso 1: Crear la carpeta del proyecto**

1. **`mkdir`**: Crear directorios.  
   - Crea la carpeta principal del proyecto:  
     ```bash
     mkdir Proyecto_NGS
     ```

2. **`ls`**: Listar el contenido de un directorio.  
   - Verifica que la carpeta se creó correctamente:  
     ```bash
     ls
     ```

---

#### **Paso 2: Navegar dentro del proyecto**

1. **`cd`**: Cambiar de directorio.  
   - Entra a la carpeta del proyecto:  
     ```bash
     cd Proyecto_NGS
     ```

2. **`pwd`**: Mostrar la ruta actual.  
   - Confirma que estás dentro de `Proyecto_NGS`:  
     ```bash
     pwd
     ```

---

#### **Paso 3: Crear subcarpetas**

1. **`mkdir`**: Crear múltiples subcarpetas.  
   - Crea las subcarpetas necesarias:  
     ```bash
     mkdir raw_data quality_control assembly annotation results scripts
     ```

2. **`ls -l`**: Listar con detalles.  
   - Verifica la creación de las subcarpetas:  
     ```bash
     ls -l
     ```

---

#### **Paso 4: Crear archivos vacíos**

1. **`touch`**: Crear archivos vacíos.  
   - Simula archivos FASTQ en la carpeta `raw_data`:  
     ```bash
     touch raw_data/sample1.fastq raw_data/sample2.fastq
     ```

2. **`ls`**: Listar archivos.  
   - Verifica que los archivos se crearon:  
     ```bash
     ls raw_data
     ```

---

#### **Paso 5: Mover y copiar archivos**

1. **`cp`**: Copiar archivos.  
   - Copia un archivo FASTQ a la carpeta de control de calidad:  
     ```bash
     cp raw_data/sample1.fastq quality_control/
     ```

2. **`mv`**: Mover o renombrar archivos.  
   - Renombra el archivo en la carpeta de control de calidad:  
     ```bash
     mv quality_control/sample1.fastq quality_control/sample1_qc.fastq
     ```

---

#### **Paso 6: Verificar la estructura**

1. **`tree`**: Mostrar la estructura de directorios.  
   - Si tienes `tree` instalado, visualiza la estructura del proyecto:  
     ```bash
     tree Proyecto_NGS
     ```
   - Si no lo tienes, instálalo con:  
     ```bash
     sudo apt install tree  # En distribuciones basadas en Debian/Ubuntu
     ```

2. **`find`**: Buscar archivos.  
   - Busca todos los archivos FASTQ en el proyecto:  
     ```bash
     find Proyecto_NGS -name "*.fastq"
     ```

---

### **3. Comandos adicionales útiles**

A medida que te familiarices con los comandos básicos, puedes explorar herramientas más avanzadas:

1. **`gzip`**: Comprimir archivos.  
   - Comprime un archivo FASTQ:  
     ```bash
     gzip raw_data/sample1.fastq
     ```

2. **`chmod`**: Cambiar permisos.  
   - Da permisos de ejecución a un script:  
     ```bash
     chmod +x scripts/mi_script.sh
     ```

3. **`cat`**: Mostrar el contenido de un archivo.  
   - Visualiza un archivo FASTQ:  
     ```bash
     cat raw_data/sample1.fastq
     ```

4. **`less`**: Visualizar archivos largos.  
   - Navega por un archivo FASTQ:  
     ```bash
     less raw_data/sample1.fastq
     ```

---

### **4. Automatización con un script en Bash**

Para ahorrar tiempo, puedes crear un script en Bash que automatice la creación de la estructura del proyecto y la generación de archivos vacíos. Ejemplo de script:

```bash
#!/bin/bash

# Crear la estructura de carpetas
mkdir -p Proyecto_NGS/{raw_data,quality_control,assembly,annotation,results,scripts}

# Crear archivos FASTQ vacíos
touch Proyecto_NGS/raw_data/sample1.fastq Proyecto_NGS/raw_data/sample2.fastq

# Mensaje de confirmación
echo "Estructura del proyecto NGS creada con éxito."
```

**Instrucciones para ejecutar el script:**
1. Guarda el código en un archivo, por ejemplo, `crear_proyecto.sh`.
2. Dale permisos de ejecución:  
   ```bash
   chmod +x crear_proyecto.sh
   ```
3. Ejecuta el script:  
   ```bash
   ./crear_proyecto.sh
   ```

---

### **Conclusión**

Con estos comandos básicos, podrás organizar y gestionar eficientemente un proyecto de NGS. La práctica constante te ayudará a dominar estas herramientas y a prepararte para tareas más avanzadas en bioinformática. ¡Manos a la obra! 😊

---

Esta versión mejora la claridad, añade ejemplos prácticos y proporciona una estructura más amigable para los estudiantes. ¡Espero que sea útil! 🚀

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

![enviroment](https://cdn.prod.website-files.com/660c0df1e3166c3704dd67fc/6628cc978a3b3baaaad5ff6d_image-3.png)

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

---

## **Ejercicio práctico: Creación y gestión de entornos con CONDA**

### **Objetivo:**
Aprender a crear, activar y gestionar entornos virtuales con CONDA, así como instalar paquetes específicos para proyectos de bioinformática.

---

### **1. Instalación de Miniconda (si no está instalado)**

Si no tienes Miniconda instalado, sigue estos pasos:

```bash
# Crear carpeta para Miniconda
mkdir -p ~/miniconda3

# Descargar el instalador
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh

# Ejecutar el instalador
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3

# Eliminar el instalador
rm -rf ~/miniconda3/miniconda.sh

# Inicializar Conda en el terminal
~/miniconda3/bin/conda init bash

# Cerrar y abrir un nuevo terminal para aplicar los cambios
```

---

### **2. Configuración de canales**

Antes de crear entornos, configura los canales de CONDA para acceder a paquetes de bioinformática:

```bash
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
```

Verifica que los canales estén correctamente configurados:

```bash
conda config --get channels
```

---

### **3. Creación de un entorno**

1. **Crear un entorno llamado `bioinfo_env` con Python 3.9:**
   ```bash
   conda create -n bioinfo_env python=3.9
   ```

2. **Activar el entorno:**
   ```bash
   conda activate bioinfo_env
   ```

3. **Verificar que el entorno está activo:**
   - El nombre del entorno (`bioinfo_env`) debería aparecer al principio del prompt en tu terminal.

---

### **4. Instalación de paquetes**

1. **Instalar herramientas de bioinformática:**
   - Instala `fastqc` para control de calidad y `multiqc` para resumir resultados:
     ```bash
     conda install -c bioconda fastqc multiqc
     ```

   - Instala `bwa` para alineamiento de secuencias:
     ```bash
     conda install -c bioconda bwa
     ```

2. **Verificar la instalación:**
   - Lista los paquetes instalados en el entorno:
     ```bash
     conda list
     ```

---

### **5. Desactivar y reactivar el entorno**

1. **Desactivar el entorno:**
   ```bash
   conda deactivate
   ```

2. **Reactivar el entorno:**
   ```bash
   conda activate bioinfo_env
   ```

---

### **6. Eliminar un entorno**

Si ya no necesitas el entorno, puedes eliminarlo:

1. **Desactivar el entorno (si está activo):**
   ```bash
   conda deactivate
   ```

2. **Eliminar el entorno `bioinfo_env`:**
   ```bash
   conda env remove -n bioinfo_env
   ```

3. **Verificar que el entorno ha sido eliminado:**
   ```bash
   conda env list
   ```

---

### **7. Crear un entorno desde un archivo YAML**

1. **Crear un archivo YAML (`environment.yml`) con la siguiente configuración:**
   ```yaml
   name: ngs_env
   channels:
     - defaults
     - bioconda
     - conda-forge
   dependencies:
     - python=3.8
     - fastqc
     - multiqc
     - bwa
     - samtools
   ```

2. **Crear el entorno a partir del archivo YAML:**
   ```bash
   conda env create -f environment.yml
   ```

3. **Activar el entorno:**
   ```bash
   conda activate ngs_env
   ```

4. **Verificar los paquetes instalados:**
   ```bash
   conda list
   ```

---

### **8. Exportar un entorno a un archivo YAML**

Si deseas compartir o replicar un entorno, puedes exportarlo a un archivo YAML:

1. **Activar el entorno que deseas exportar:**
   ```bash
   conda activate ngs_env
   ```

2. **Exportar el entorno a un archivo YAML:**
   ```bash
   conda env export > ngs_env.yml
   ```

3. **Compartir el archivo YAML con otros usuarios para que puedan recrear el entorno:**
   ```bash
   conda env create -f ngs_env.yml
   ```

---

### **9. Tarea opcional: Automatización con un script**

Crea un script en Bash para automatizar la creación de un entorno y la instalación de paquetes. Ejemplo de script (`crear_entorno.sh`):

```bash
#!/bin/bash

# Crear el entorno
conda create -n bioinfo_env python=3.9 -y

# Activar el entorno
conda activate bioinfo_env

# Instalar paquetes
conda install -c bioconda fastqc multiqc bwa samtools -y

# Mensaje de confirmación
echo "Entorno 'bioinfo_env' creado y paquetes instalados con éxito."
```

**Instrucciones para ejecutar el script:**
1. Guarda el código en un archivo, por ejemplo, `crear_entorno.sh`.
2. Dale permisos de ejecución:  
   ```bash
   chmod +x crear_entorno.sh
   ```
3. Ejecuta el script:  
   ```bash
   ./crear_entorno.sh
   ```
