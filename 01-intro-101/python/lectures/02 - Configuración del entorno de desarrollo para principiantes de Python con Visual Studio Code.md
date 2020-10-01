# Configuración del entorno de desarrollo para principiantes de Python con Visual Studio Code



Como introducción a Python, instale y configure las herramientas que necesitará para compilar aplicaciones reales.

## Learning Objectives

Objetivos de este móduloa:

- Determinar qué versión de Python tiene instalada en el equipo (si tiene alguna).
- Instalar Python 3.
- Iniciar el modo interactivo de Python para ejecutar código de Python línea a línea.
- Instalar Visual Studio Code, Python y la extensión de Python para Visual Studio Code en el equipo.
- Crear un archivo de script de Python y escribir código de Python en Visual Studio Code.
- Ejecutar el código de su archivo de script de Python con las herramientas de línea de comandos de Python.

# Introducción

- 1 minuto

En este módulo, creará un entorno de desarrollo de Python que le permitirá obtener información sobre Python y compilar muchos tipos de aplicaciones. Aprenderá a ejecutar código de Python en el modo interactivo. También aprenderá a usar Visual Studio Code para crear un archivo de código de Python, a escribir código Python en ese archivo y, a continuación, a ejecutar ese archivo.

Al final de este módulo, tendrá instaladas en su equipo las herramientas necesarias para avanzar en su objetivo de compilar aplicaciones reales con Python.

## Objetivos de aprendizaje

En este módulo, aprenderá a:

- Determinar qué versión de Python tiene instalada en el equipo (si tiene alguna).
- Instalar Python 3.
- Iniciar el modo interactivo de Python para ejecutar código de Python línea a línea.
- Instalar Visual Studio Code, Python y la extensión de Python para Visual Studio Code en el equipo.
- Crear un archivo de script de Python y escribir código de Python en Visual Studio Code.
- Ejecutar el código de su archivo de script de Python con las herramientas de línea de comandos de Python.

# Introducción a Python

- 5 minutos

Elija su sistema operativo

**Windows**

Tal como ha aprendido en el módulo anterior, antes de empezar a escribir código de Python, deberá instalar algunas herramientas en su equipo local. Necesitará lo siguiente:

- El instalador de Python, que contiene el intérprete que compila y ejecuta el código, bibliotecas de código adicionales y otras herramientas útiles para los desarrolladores de Python. Es posible que ya lo tenga instalado. En unos momentos comprobaremos si es así.
- Un editor de código, idealmente, uno que tenga características que puedan ayudarle a escribir código de Python. En este módulo, le guiaremos a través de la instalación de Visual Studio Code, uno de los editores de código gratuitos más populares. También instalaremos la extensión de Python para Visual Studio Code para agregar una funcionalidad mejorada.

### Python 2 frente a Python 3

En este módulo, nos hemos esforzado por distinguir entre la versión 2 y la versión 3 de Python. Hemos hecho esta distinción porque los creadores de Python desaconsejan a los desarrolladores usar Python 2. Se han realizado mejoras significativas en Python 3 y algunas de ellas afectan al código escrito anteriormente en Python 2.

La idea clave es que, a partir de ahora, deberá usar Python 3.

 Nota

¿Por qué es importante resaltar la necesidad de usar Python 3? Los equipos que ejecutan macOS y algunas distribuciones de Linux tienen instalado Python 2, por lo que deberá realizar pasos adicionales para instalar Python 3.

### ¿Cómo puedo saber si ya tengo instalado Python 3 en mi equipo?

Es posible que ya tenga Python 3 instalado en su equipo. A veces, hay aplicaciones que instalan Python 3 sin que lo sepa.

En la parte superior de esta página, seleccione la pestaña que corresponda a su sistema operativo.

### Windows

Para determinar si su equipo Windows ya tiene instalado Python 3:

1. Abra un símbolo del sistema; para ello, escriba **símbolo del sistema** en el cuadro de búsqueda de Windows 10 y seleccione la aplicación **Símbolo del sistema** en la sección **Mejor coincidencia** de los resultados.
2. Escriba el siguiente comando y, a continuación, presione la tecla Entrar:

ConsolaCopiar

```console
py --version
```

Es probable que no obtenga ninguna salida después de ejecutar `py --version`. En este caso, no tiene ninguna versión de Python en el equipo. Le guiaremos a través de la instalación de Python 3 en Windows en la siguiente unidad.

Sin embargo, si se muestra la palabra `Python` seguida de un conjunto de números separados por puntos (`.`), significa que tiene instalada una versión de Python. Este es un ejemplo de la salida que podría obtener:

ResultadosCopiar

```output
Python 3.8.0
```

Si el primer número es `3`, todo listo. No tiene que hacer nada más. Puede omitir la siguiente unidad, en la que se explica cómo instalar Python en Windows.

Si el primer número es `2`, deberá instalar Python 3. Le guiaremos a través de la instalación de Python 3 en la siguiente unidad.

## Resumen

La conclusión principal de esta unidad es que ya no se debe usar la versión 2 de Python. A partir de ahora, deberá escribir código nuevo mediante la versión 3 de Python. Use la marca `--version` de Python para asegurarse de que sabe con qué versión está trabajando.



### ¿Cómo puedo saber si ya tengo instalado Python 3 en mi equipo?

Es posible que ya tenga Python 3 instalado en su equipo. A veces, hay aplicaciones que instalan Python 3 sin que lo sepa.

En la parte superior de esta página, seleccione la pestaña que corresponda a su sistema operativo.

### macOS

Para determinar si su equipo macOS ya tiene instalado Python 3:

1. Abra la aplicación Terminal. Para buscar e iniciar Python 3, puede usar la combinación de teclas Comando + Barra espaciadora para buscar con Spotlight. En el cuadro de búsqueda, escriba **Terminal**. Debería ver la aplicación Terminal en los resultados. Presione la tecla Entrar para iniciar la aplicación.
2. En el símbolo del sistema, escriba el siguiente comando:

BashCopiar

```bash
python3 --version
```

Es posible que vea la palabra `Python` seguida de un conjunto de números separados por puntos (`.`). Este es un ejemplo de la salida que podría obtener:

ResultadosCopiar

```output
Python 3.6.7
```

Si el primer número es `3`, todo listo. No tiene que hacer nada más.

Python 3 no viene preinstalado en macOS, pero es posible que lo haya instalado usted o un programa que use. Aunque no disponga de la versión más actualizada, podrá seguir los módulos de Python para principiantes en Microsoft Learn.

Es probable que vea esta salida:

ResultadosCopiar

```output
command not found
```

Le guiaremos a través de la instalación de Python 3 en macOS en la siguiente unidad.

## Resumen

La conclusión principal de esta unidad es que ya no se debe usar la versión 2 de Python. A partir de ahora, deberá escribir código nuevo mediante la versión 3 de Python. Use la marca `--version` de Python para asegurarse de que sabe con qué versión está trabajando.



### ¿Cómo puedo saber si ya tengo instalado Python 3 en mi equipo?

Es posible que ya tenga Python 3 instalado en su equipo. A veces, hay aplicaciones que instalan Python 3 sin que lo sepa.

En la parte superior de esta página, seleccione la pestaña que corresponda a su sistema operativo.

### Linux

Para determinar si su equipo Linux ya tiene instalado Python 3:

1. Abra una sesión de terminal de Linux. Las instrucciones para abrir esta sesión dependen de su distribución y de la versión de Linux. Consulte la documentación en línea de su distribución de Linux para obtener instrucciones sobre cómo abrir un terminal.
2. Escriba el siguiente comando y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
python3 --version
```

Es posible que vea la palabra `Python` seguida de un conjunto de números separados por puntos (`.`). Este es un ejemplo de la salida que podría obtener:

ResultadosCopiar

```output
Python 3.6.7
```

Si el primer número es `3`, todo listo. No tiene que hacer nada más.

Python viene preinstalado en algunas distribuciones de Linux (como Ubuntu). Aunque no disponga de la versión más actualizada, podrá seguir todos los módulos de Python para principiantes en Microsoft Learn.

En otras distribuciones de Linux, Python 3 no viene instalado de forma predeterminada, por lo que es posible que vea otro mensaje. Esta es la salida que verá en la versión 10 de Debian:

ResultadosCopiar

```output
-bash: python3: command not found
```

En este caso, deberá instalar Python 3. Le guiaremos a través de la instalación de Python 3 en Linux en la siguiente unidad.

## Resumen

La conclusión principal de esta unidad es que ya no se debe usar la versión 2 de Python. A partir de ahora, deberá escribir código nuevo mediante la versión 3 de Python. Use la marca `--version` de Python para asegurarse de que sabe con qué versión está trabajando.



# Instalación de Python 3

- 5 minutos

Elija su sistema operativo

LinuxMacWindows

En la unidad anterior, ha ejecutado un comando para determinar si tiene Python 3 instalado. Si necesita instalar Python 3, elija su sistema operativo en la parte superior de esta página y, a continuación, siga las instrucciones.

Si ha determinado que ya tiene instalado Python 3, desplácese hasta la parte inferior de esta página y seleccione **Continuar**.

## Instalación de Python en Linux

Cuando se escribió este módulo, Python 3.8 era la versión más reciente disponible de Python, por lo que haremos referencia a esa versión en las siguientes instrucciones.

Como sabrá probablemente, las distintas distribuciones de Linux usan diferentes administradores de paquetes. Entre las distribuciones de Linux más populares se incluyen APT (acrónimo de "Advanced Packaging Tool") o YUM (acrónimo de "Yellowdog Updater, Modified").

En esta unidad se proporcionan instrucciones para APT y YUM. Si su distribución de Linux usa un administrador de paquetes diferente, es posible que tenga que buscar las instrucciones para instalar Python 3 en ****.

### Instalación con APT

#### Paso 1: Abrir una ventana de terminal

Suponiendo que está ejecutando un entorno de escritorio de la interfaz gráfica de usuario de Linux, busque y abra una ventana de terminal mediante el icono Terminal.

#### Paso 2: Actualizar los índices de los paquetes de APT

Ejecute este comando:

BashCopiar

```bash
sudo apt-get update
```

El comando `apt-get update` actualiza la lista de paquetes (los índices de paquetes) de los repositorios y los archivos de paquetes personales (PPA) de los que es consciente. Esta actualización permite que `apt-get` encuentre las versiones más recientes de los paquetes que quiere instalar y sus dependencias.

El comando `sudo` eleva temporalmente los permisos a la raíz, el nivel más eficaz del sistema. A la hora de usar `sudo`, normalmente se le pedirá la contraseña de su cuenta de usuario.

`apt-get update` mostrará todos los elementos que se actualizarán. Es posible que se le pida que escriba `y` o `yes` y que presione la tecla Entrar para aprobar la acción.

#### Paso 3: Instalar Python 3

Escriba el siguiente comando en un símbolo del sistema de Bash y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
sudo apt-get install python3
```

`apt-get install` buscará los paquetes correspondientes del índice de paquetes, descargará los archivos necesarios y los instalará en las carpetas adecuadas.

#### Paso 4: Comprobar la instalación

Para confirmar que ha instalado correctamente Python 3, escriba el siguiente comando en un símbolo del sistema de Bash y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
python3 --version
```

Debería ver la palabra `Python` seguida de un conjunto de números separados por puntos (`.`). Este es un ejemplo de la salida que podría obtener:

ResultadosCopiar

```output
Python 3.6.7
```

Si el primer número es `3`, Python 3 se ha instalado correctamente.

Si no se ha podido realizar la instalación, es posible que vea un mensaje de error. Escriba el mensaje de error exacto en el cuadro de búsqueda de un motor de búsqueda para encontrar posibles causas y soluciones.

### Instalación con YUM

El administrador de paquetes de YUM se usa principalmente en los sistemas de Red Hat, como Red Hat Enterprise Linux y Fedora, y en CentOS. Si el administrador APT no está instalado en el sistema, puede usar YUM en su lugar.

#### Paso 1: Abrir una ventana de terminal

Suponiendo que está ejecutando un entorno de escritorio de la interfaz gráfica de usuario de Linux, busque y abra una ventana de terminal mediante el icono Terminal.

#### Paso 2: Actualizar los índices de los paquetes de YUM

Escriba el siguiente comando en un símbolo del sistema de Bash y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
sudo yum update
```

`yum update` se asegurará de que todos los paquetes y sus dependencias estén actualizados. Es conveniente actualizar la lista de paquetes antes de instalar software nuevo.

#### Paso 3: Instalar Python 3

Escriba el siguiente comando en un símbolo del sistema de Bash y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
yum install rh-python36
```

#### Paso 4: Comprobar la instalación

Para confirmar que ha instalado correctamente Python 3, escriba el siguiente comando en un símbolo del sistema de Bash y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
python3 --version
```

Debería ver la palabra `Python` seguida de un conjunto de números separados por puntos (`.`). Este es un ejemplo de la salida que podría obtener:

ResultadosCopiar

```output
Python 3.6.7
```

Si el primer número es `3`, Python 3 se ha instalado correctamente.

Si no se ha podido realizar la instalación, es posible que vea un mensaje de error. De lo contrario, continúe con el paso 5.

#### Paso 5: (Opcional) Habilitar la característica Software Collections en Bash

Software Collections le permite instalar varias versiones de los mismos componentes de software en el sistema. Por lo tanto, debe especificar qué versión de Python quiere ejecutar en el shell. Escriba el siguiente comando en un símbolo del sistema de Bash y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
scl enable rh-python36 bash
```

Ahora vuelva a intentar el paso 4. Debería obtener una salida similar a la siguiente:

ResultadosCopiar

```output
Python 3.6.7
```

Si el primer número es `3`, Python 3 se ha instalado correctamente, en el contexto de una colección de software.

`scl enable` inicia una nueva sesión de Bash y establece Python 3.6 como la versión predeterminada de Python. Sin embargo, Python 3.6 solo es la versión predeterminada para la sesión del shell actual. Si sale de la sesión o abre una nueva desde otro terminal, Bash volverá a establecer Python 2.7 como la versión predeterminada de Python.

Para obtener más información, consulte [Red Hat Software Collections 2.4 ](https://access.redhat.com/documentation/en-us/red_hat_software_collections/2/html/2.4_release_notes/chap-rhscl).

 Importante

Si necesita usar `scl enable` para ejecutar `python3 --version`, es posible que tenga que escribir ese comando cada vez que quiera trabajar en Python. Hay soluciones alternativas, pero esta es la funcionalidad prevista de Software Collections. Consulte [cómo conservar una colección de Red Hat Software Collections ](https://access.redhat.com/solutions/527703) para encontrar una posible solución alternativa.



## Instalación de Python en macOS

Siga estos pasos para descargar el instalador de Python desde el sitio web de Python.

 Nota

En el momento de redactar este documento, Python 3.8.0 era la versión más reciente, por lo que hacemos referencia a esa versión en estas instrucciones. Usted debe instalar la versión más reciente disponible. Si instala una versión diferente, el texto de los botones y los nombres de archivo que vea podrían ser ligeramente diferentes a los que aparecen en estas instrucciones.

 Nota

Como alternativa, puede usar Homebrew para instalar Python y Visual Studio Code. Para obtener instrucciones, consulte la [documentación de Homebrew ](https://docs.brew.sh/Homebrew-and-Python).

### Paso 1: Acceder al sitio web de descarga de Python y descargar el instalador

Vaya a la [página de descarga de Python ](https://www.python.org/downloads/).

El sitio web debería dirigirle automáticamente a una página específica para Mac OS X. Seleccione el botón **Download Python 3.8.0** (Descargar Python 3.8.0).

Es posible que aparezca una ventana en la que se le pida que permita las descargas desde python.org. Seleccione **Permitir**.

Después de unos instantes, debería descargarse un archivo denominado Python-3.8.0-mascosx10.9.pkg en la pila de descargas del Dock.

### Paso 2: Iniciar el instalador de Python y aceptar las opciones para una instalación estándar

Haga doble clic en el archivo .pkg que ha descargado para iniciar el instalador. El instalador de Python le pedirá que instale, compruebe y acepte diversas opciones y contratos de licencia. Dedique un tiempo a leer estos mensajes para comprender lo que hará el instalador en el equipo.

Cuando finalice el proceso de instalación, aparecerá una ventana de Finder que mostrará el contenido de la carpeta Python. También debería ver una pantalla de felicitación cuando finalice la instalación. En ese momento, puede seleccionar **Close** (Cerrar).

Si se le pide que mueva el instalador de Python a la papelera, puede hacerlo.

### Paso 3: Asegurarse de que Python 3 se ha instalado correctamente

En Spotlight (Comando + Barra espaciadora), escriba **terminal** y, a continuación, presione la tecla Entrar para iniciar Terminal.

En el símbolo del sistema de Terminal, escriba el siguiente comando y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
python3 --version
```

Debería ver la palabra `Python` seguida de un conjunto de números separados por puntos (`.`). Este es un ejemplo de la salida que podría obtener:

ResultadosCopiar

```output
Python 3.8.0
```

Si el primer número es `3`, Python 3 se ha instalado correctamente.



## Instalación de Python en Windows

Cuando se escribió este módulo, Python 3.8 era la versión más reciente disponible de Python, por lo que haremos referencia a esa versión en las siguientes instrucciones.

Además, estas instrucciones son específicas para Windows 10. Si tiene una versión anterior de Windows, las instrucciones básicas son las mismas, aunque es posible que el proceso en algunos pasos sea ligeramente diferente.

 Nota

En el momento de redactar este documento, Python 3.8.0 era la versión más reciente de Python, por lo que hacemos referencia a esa versión en estas instrucciones. Usted debe instalar la versión más reciente disponible. Si instala una versión diferente, el texto de los botones y los nombres de archivo que vea podrían ser ligeramente diferentes a los que aparecen en estas instrucciones.

### Paso 1: Descargar el instalador de Python 3.8 para Windows

Vaya a la [página de descarga de Python ](https://www.python.org/downloads/).

Seleccione el botón **Download Python 3.\*x\*** (Descargar Python 3.x). Cuando el explorador le pida que guarde el archivo, anote la ruta de descarga y, a continuación, guarde el archivo en su disco duro local. La mayoría de los exploradores web guardan los archivos descargados en la carpeta de descargas.

### Paso 2: Buscar y ejecutar la aplicación del instalador

En función del explorador web que use, es posible que tenga la opción de ejecutar el archivo inmediatamente después de descargarlo.

Si no es así, puede abrir el Explorador de archivos, ir a la ruta de descarga que anotó en el paso anterior y, después, hacer doble clic en el archivo. El nombre del archivo debería ser **Python-3.8.0.exe**.

### Paso 3: Elegir las opciones e iniciar el proceso de instalación

Cuando aparezca el cuadro de diálogo del instalador, seleccione **Add Python 3.8 to PATH** (Agregar Python 3.8 a PATH).

A continuación, tome nota de la ruta de instalación que aparece debajo de **Install Now** (Instalar ahora).

Si está satisfecho con la ruta de instalación, seleccione **Install Now** (Instalar ahora).

Si quiere cambiar la ruta de instalación, seleccione **Customize installation** (Personalizar instalación).

La primera página de opciones se llama **Optional Features** (Características opcionales). No es necesario que cambie las selecciones predeterminadas. Seleccione **Next** (Siguiente).

La segunda página de opciones se denomina **Advanced Options** (Opciones avanzadas). Cerca de la parte inferior de la página, puede cambiar la ruta de instalación en **Customize install location** (Personalizar la ruta de instalación).

Cuando esté satisfecho con la ruta, seleccione **Install** (Instalar).

### Paso 4: Aceptar la instalación

A continuación, verá el cuadro de diálogo Control de cuentas de usuario de Windows, que le pedirá que permita que la aplicación realice cambios en el dispositivo.

Seleccione **Sí** para continuar.

### Paso 5: Cerrar el instalador

Seleccione **Close** (Cerrar).

### Paso 6: Comprobar la instalación

Para confirmar que ha instalado correctamente Python 3, escriba el siguiente comando en un símbolo del sistema de Bash y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
py --version
```

Debería ver la palabra `Python` seguida de un conjunto de números separados por puntos (`.`). Este es un ejemplo de la salida que podría obtener:

ResultadosCopiar

```output
Python 3.8.0
```

Si el primero de los tres números es `3`, ya tiene todo listo. Ha instalado Python 3 correctamente en su equipo Windows.

# Uso del modo interactivo de Python para escribir y ejecutar código

- 5 minutos

Elija su sistema operativo

LinuxMacWindows

Ahora que ha instalado Python 3, vamos a escribir una línea de código de Python para verlo en funcionamiento. Esta pequeña línea de código no le ayudará a ganar ningún premio de diseño de software, pero es el primer paso que dan todos los desarrolladores de software cuando comienzan su proceso de aprendizaje.

## Uso del modo interactivo del intérprete de Python

En este módulo, aprenderá que hay dos flujos de trabajo para escribir y ejecutar código de Python:

- Use el modo interactivo del intérprete de Python para escribir y ejecutar las líneas de código de Python de una en una.
- Escriba código de Python en un archivo de script y, a continuación, use las herramientas de línea de comandos para ejecutar el contenido del archivo de script.

El modo interactivo le permite experimentar con Python sin tener que realizar ninguna configuración adicional, por lo que es ideal para aprender. Sin embargo, tiene limitaciones: al salir del modo interactivo, el código se elimina permanentemente.

 Nota

El modo interactivo a veces se conoce como "REPL", acrónimo de "read–eval–print loop". Muchos lenguajes de programación tienen un REPL que se puede usar para este mismo propósito.

 Importante

El modo interactivo del intérprete de Python es diferente de la ventana interactiva de Python en Visual Studio Code, de la que obtendrá información en otro módulo.

### Paso 1: Iniciar el modo interactivo de Python

#### Inicio del modo interactivo de Python en Linux

En el símbolo del sistema de Bash, escriba la siguiente línea de código y, a continuación, presione la tecla Entrar:

BashCopiar

```bash
python3
```

De esta manera, la utilidad `python3` iniciará Python en modo interactivo.

A continuación, debería ver este mensaje:

ResultadosCopiar

```output
>>>
```

Las tres flechas (`>>>`) se denominan * símbolo del sistema principal*. Hablaremos del *símbolo del sistema secundario* más adelante.

En el símbolo del sistema principal, puede escribir y ejecutar una línea de Python cada vez. Probémoslo.

### Paso 2: Escribir las primeras líneas de código de Python

Después del símbolo del sistema principal (`>>>`), escriba el siguiente código de Python y, a continuación, presione la tecla Entrar:

PythonCopiar

```python
print('Hello World!')
```

Debería ver esta salida en la línea siguiente:

ResultadosCopiar

```output
Hello World!
```

Si ve un mensaje de error en lugar de la salida, vuelva a escribir el código. Preste mucha atención a cada carácter y asegúrese de que su código es exactamente igual al código anterior. Incluso un pequeño error de puntuación puede producir problemas importantes al escribir código.

En el siguiente módulo, examinaremos esta línea de código para ayudarle a conocer la sintaxis de Python. Aprenderá qué hace cada palabra y cada signo de puntuación en el código.

### Paso 3: Cerrar el modo interactivo

Ya hemos terminado de trabajar en el modo interactivo, pero lo usaremos de nuevo en esta serie de módulos. Por ahora, puede cerrar el modo interactivo; para ello, escriba el siguiente comando después del símbolo del sistema principal (`>>>`) y, a continuación, presione la tecla Entrar:

PythonCopiar

```python
exit()
```

Regresará al comando o al símbolo del sistema de Bash.

## Resumen

Conclusiones importantes de esta unidad:

- La escritura de código requiere precisión. Hasta el más mínimo fallo puede producir un error.
- Puede usar el modo interactivo para escribir código de Python rápidamente. Cada línea se interpretará y se ejecutará de forma inmediata.
- Para cerrar el modo interactivo, use el comando `exit()`.

### Paso 1: Iniciar el modo interactivo de Python

#### Inicio del modo interactivo de Python en Windows

En el símbolo del sistema, escriba la siguiente línea de código y, a continuación, presione la tecla Entrar:

ConsolaCopiar

```console
py -3
```

De esta manera, la utilidad del iniciador `py` iniciará Python en modo interactivo. La marca opcional `-3` garantiza que trabajará con la versión 3 de Python.

A continuación, debería ver este mensaje:

ResultadosCopiar

```output
>>>
```

Las tres flechas (`>>>`) se denominan * símbolo del sistema principal*. Hablaremos del *símbolo del sistema secundario* más adelante.

En el símbolo del sistema principal, puede escribir y ejecutar una línea de Python cada vez. Probémoslo.

### Paso 2: Escribir las primeras líneas de código de Python

Después del símbolo del sistema principal (`>>>`), escriba el siguiente código de Python y, a continuación, presione la tecla Entrar:

PythonCopiar

```python
print('Hello World!')
```

Debería ver esta salida en la línea siguiente:

ResultadosCopiar

```output
Hello World!
```

Si ve un mensaje de error en lugar de la salida, vuelva a escribir el código. Preste mucha atención a cada carácter y asegúrese de que su código es exactamente igual al código anterior. Incluso un pequeño error de puntuación puede producir problemas importantes al escribir código.

En el siguiente módulo, examinaremos esta línea de código para ayudarle a conocer la sintaxis de Python. Aprenderá qué hace cada palabra y cada signo de puntuación en el código.

### Paso 3: Cerrar el modo interactivo

Ya hemos terminado de trabajar en el modo interactivo, pero lo usaremos de nuevo en esta serie de módulos. Por ahora, puede cerrar el modo interactivo; para ello, escriba el siguiente comando después del símbolo del sistema principal (`>>>`) y, a continuación, presione la tecla Entrar:

PythonCopiar

```python
exit()
```

Regresará al comando o al símbolo del sistema de Bash.

## Resumen

Conclusiones importantes de esta unidad:

- La escritura de código requiere precisión. Hasta el más mínimo fallo puede producir un error.
- Puede usar el modo interactivo para escribir código de Python rápidamente. Cada línea se interpretará y se ejecutará de forma inmediata.
- Para cerrar el modo interactivo, use el comando `exit()`.

# Instalación de Visual Studio Code

- 5 minutos

Elija su sistema operativo

LinuxMacWindows

Ya ha visto cómo puede ejecutar código de Python línea a línea mediante el modo interactivo de Python. El modo interactivo resulta útil cuando quiere experimentar con unas pocas líneas de código. El inconveniente es que, cuando sale del modo interactivo, el código que ha escrito se elimina permanentemente.

Como desarrollador principiante de Python, es probable que prefiera escribir un *script de Python*. Un script es un archivo de texto con una extensión .py en el que se escribe todo el código de Python. Después de guardar el código en el archivo de script, use el intérprete de Python para abrir, compilar, interpretar y ejecutar el código de ese archivo.

## Herramientas para escribir código de Python

Normalmente se escribe la sintaxis de Python en un archivo de texto y se guarda en el disco duro local. Se puede escribir código mediante un editor de archivos de texto simple, como el Bloc de notas de Windows. El Bloc de notas edita texto ASCII, un formato de archivo de texto estándar simple.

Se recomienda evitar el uso de editores de texto que incluyan opciones de formato, como negrita, subrayado o cursiva, o de cualquier otro programa que tenga características de procesamiento de texto. Por lo tanto, no se debe escribir código en Microsoft Word ni en TextEdit en macOS. Estos programas incluirán instrucciones de formato adicionales que el compilador de Python no entenderá.

Aunque se puede usar un editor de texto, normalmente se suele usar una herramienta que se adapte mejor a los desafíos únicos de la escritura de código. Hay gran cantidad de opciones, pero muchos desarrolladores confían en Visual Studio Code para este propósito. Es gratis y está disponible en Windows, macOS y Linux. Tiene muchas características que permiten navegar fácilmente por el código, independientemente del lenguaje de programación con el que quiera trabajar.

Microsoft también proporciona la extensión de Python para Visual Studio Code. Esta extensión ofrece características como el resaltado de sintaxis, la navegación por el código, la compatibilidad de formato del código, etc. Hay una característica en concreto, llamada IntelliSense, que es muy útil al principio. Proporciona ayuda contextual a medida que escribe. La instalará en la siguiente unidad.

## Instalación de Visual Studio Code en Windows

Esta sección le guiará a través de la descarga del instalador desde el sitio web de Visual Studio Code.

### Paso 1: Descargar el programa de instalación

Vaya a la [página de descarga de Visual Studio Code ](https://code.visualstudio.com/Download).

La página web muestra los logotipos de Windows, Linux y Mac.

Descargue el instalador para Windows. La mayoría de los exploradores ofrecen la opción de guardar el archivo en el equipo local (normalmente en la carpeta de descargas) o de ejecutar inmediatamente el archivo del instalador.

### Paso 2: Iniciar el instalador

Si ha descargado el instalador, es posible que necesite abrir el Explorador de archivos y navegar a la carpeta de descargas, o a donde su explorador web haya guardado el archivo del instalador.

Haga doble clic en el archivo del instalador para iniciar el proceso de instalación.

### Paso 3: Iniciar Visual Studio Code

Una vez finalizada la instalación, puede iniciar inmediatamente Visual Studio Code.



# Instalación de la extensión de Python y ejecución del primer script de Python

- 5 minutos

Elija su sistema operativo

LinuxMacWindows

Ahora que ha instalado Visual Studio Code, instalará la extensión de Python para Visual Studio Code y, opcionalmente, configurará otras herramientas y opciones de configuración.

## Instalación de la extensión de Python para Visual Studio Code

Visual Studio Code es un excelente editor de código de uso general y sencillo. Las extensiones proporcionan funcionalidad adicional solo para los lenguajes de programación o las características que quiera habilitar. La extensión de Python para Visual Studio Code proporciona indicaciones visuales y herramientas que le ayudarán a escribir código de Python mejor y con mayor rapidez.

### Paso 1: Abrir la vista de extensiones

Puede examinar las extensiones e instalarlas desde Visual Studio Code.

Abra la vista de extensiones. Vaya a **Ver** y seleccione **Extensiones**, o bien seleccione el icono **Extensiones** en la barra de actividades en el lado izquierdo de Visual Studio Code.

La vista de extensiones mostrará una lista de las extensiones de Visual Studio Code más populares en Visual Studio Code Marketplace.

### Paso 2: Buscar la extensión de Python

Para filtrar la lista de extensiones, escriba **python** en el cuadro de búsqueda situado en la parte superior de la vista de extensiones.

Seleccione la extensión publicada por Microsoft (normalmente es la primera de la lista). Los detalles sobre esa extensión aparecerán en una pestaña en el área principal a la derecha.

### Paso 3: Instalar la extensión de Python

En el área principal, donde verá los detalles sobre la extensión de Python, seleccione **Instalar**.

Una vez completada la instalación, el texto del botón cambiará a **Desinstalar**. Esto le permite saber que ha instalado correctamente la extensión de Python.

## Instalación de Pylint

Pylint es uno de los linter de Python más populares. Un *linter* es una herramienta útil que puede analizar el código en busca de posibles errores y problemas del estilo de codificación. Si instala un linter, Visual Studio Code analizará su código cada vez que guarde el archivo de código. Hay varias herramientas de linter disponibles para Python.

La extensión de Python para Visual Studio Code le recomendará que instale Pylint y controlará la mayoría de los detalles de la instalación.

Para iniciar la instalación, creará un archivo con la extensión .py, el cual desencadenará una ventana emergente con el botón Instalar. Comenzaremos el proceso en el paso siguiente.

 Nota

En este módulo, solo crearemos un archivo como una forma de desencadenar la extensión de Python para que Visual Studio Code muestre una ventana emergente para iniciar la instalación de Pylint. No usaremos el archivo en este módulo, pero aprenderá a escribir y ejecutar un archivo de código en el siguiente módulo, titulado "Creación de su primer programa de Python".

### Paso 1: Abrir la vista del explorador en Visual Studio Code

Abra la vista del explorador. Vaya a **Ver** y seleccione **Explorador**, o bien seleccione el icono **Explorador** en la barra de actividades en el lado izquierdo de Visual Studio Code.

Hay dos secciones en el explorador:

- **Editores abiertos**, que muestra todas las pestañas visibles en el área principal.
- El nombre de la carpeta de trabajo actual.

No obstante, como esta es la primera vez que abre Visual Studio Code, verá una sección titulada **No hay ninguna carpeta abierta** en su lugar. Debajo de este encabezado, verá el mensaje "Todavía no ha abierto ninguna carpeta" y el botón **Abrir carpeta**.

### Paso 2: Crear una carpeta de trabajo

Seleccione **Abrir carpeta** para abrir el cuadro de diálogo "Abrir" de su sistema operativo.

Cree una carpeta llamada **hola** dentro de la carpeta Documentos de su sistema. Selecciónela.

Después de seleccionar la nueva carpeta **hola**, vuelva a la vista del explorador y verá que el título de la sección cambia a **hola**.

### Paso 3: Crear un archivo

Para crear un archivo de script en la carpeta **hola**, vaya a **Archivo** y seleccione **Nuevo archivo**.

En el área principal, se mostrará el nuevo archivo.

Probablemente verá que aparecen uno o más mensajes emergentes en la esquina inferior derecha de Visual Studio Code.

### Paso 4: Iniciar la instalación de Pylint desde la ventana emergente

En este paso, nos centraremos en la ventana emergente con el mensaje "Linter pylint is not installed" (El linter Pylint no está instalado).

 Nota

La instalación de Pylint es opcional. Si por alguna razón no quiere instalarlo, seleccione la **x** para cerrar el mensaje emergente.

Para instalar Pylint, seleccione **Instalar**. La ventana del terminal de Visual Studio Code se abrirá debajo de su archivo de código. Puede usar una herramienta de línea de comandos denominada "pip" para instalar Pylint.

### Paso 5: Abordar otros mensajes emergentes

Es posible que vea otros mensajes emergentes.

El más importante es el siguiente:

"No Python interpreter is selected. You need to select a Python interpreter to enable features such as IntelliSense, linting, and debugging" (No se ha seleccionado ningún intérprete de Python. Debe seleccionar un intérprete de Python para habilitar características como IntelliSense, linting y la depuración).

Si hace clic en **Select Python Interpreter** (Seleccionar intérprete de Python), verá una lista de los intérpretes de Python cerca de la parte superior de Visual Studio Code, en la barra de comandos. Seleccione la versión más reciente que ha instalado y asegúrese de que es la versión 3 o una posterior.

La selección se mostrará en la barra de estado de Visual Studio Code, cerca de la esquina inferior izquierda.

De forma alternativa, podría ver este mensaje:

"Tip: you can change the Python interpreter used by the Python extension by clicking on the Python version in the status bar" (Sugerencia: Puede cambiar el intérprete que usa la extensión de Python; para ello, haga clic en la versión de Python en la barra de estado).

Este mensaje solamente le informa de que tiene un intérprete seleccionado, pero puede cambiarlo si quiere. Para cambiarlo, haga clic en el intérprete seleccionado actualmente cerca de la esquina inferior izquierda y, a continuación, elija otro en la lista de intérpretes de Python que se muestra cerca de la parte superior de Visual Studio Code en la barra de comandos.

Seleccione **Got it!** (Entendido) para descartar la sugerencia, o bien seleccione **Do not show again** (No volver a mostrar) para deshabilitarla de forma permanente.

Después de abordar todos los mensajes emergentes, ha configurado correctamente la extensión de Python para Visual Studio Code y tiene todo listo para empezar a escribir código de Python.





