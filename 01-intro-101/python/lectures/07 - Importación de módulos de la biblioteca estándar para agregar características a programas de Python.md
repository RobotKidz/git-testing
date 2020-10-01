# Importación de módulos de la biblioteca estándar para agregar características a programas de Python



Explore la biblioteca estándar de Python, obtenga procedimientos para agregar un módulo a su programa y a fin de descargar paquetes de terceros.

## Learning Objectives

En este módulo, aprenderá a hacer lo siguiente:

- Explorar la biblioteca estándar de Python.
- Agregar la instrucción `include` para indicar al compilador de Python qué módulos se van a usar en el código.
- Usar la utilidad PIP para descargar paquetes de código abierto de terceros.

# Introducción

- 1 minuto

El lenguaje de programación Python incluye una biblioteca de funciones que puede usar en sus propios programas. También contiene herramientas que le permiten instalar otros proyectos de código abierto de terceros que agilizarán y simplificarán considerablemente el desarrollo de Python.

Imagine que le han pedido que cree un programa que extraiga datos de Internet, procese la información, guarde los datos en un archivo y use el protocolo de Internet FTP para enviar ese archivo al servidor de un cliente. Si tuviera que programar usted mismo todos los detalles, tardaría muchísimo. Afortunadamente, puede usar la biblioteca estándar de Python a fin de aprovechar el trabajo de otras personas que ya han escrito código para hacer que este programa sea posible e, incluso, trivial.

En este módulo, se explorará la biblioteca estándar de Python. Obtendrá información sobre cómo usar miles de funciones precompiladas distribuidas en cientos de módulos y cómo ampliarlas para aprovechar el trabajo de la comunidad más amplia de desarrollo de software. Esta comunidad ha creado cientos de miles de paquetes de Python que pueden cubrir todas las necesidades imaginables. Obtendrá información sobre dónde puede ir para investigar los paquetes disponibles y cómo instalarlos localmente e incluirlos en el código.

Cuando finalice este módulo, será capaz de escribir programas que pueden aprovechar la potencia de la biblioteca estándar de Python y el trabajo de la comunidad de Python.

## Objetivos de aprendizaje

En este módulo, aprenderá a hacer lo siguiente:

- Explorar la biblioteca estándar de Python.
- Agregar la instrucción `include` para indicar al compilador de Python qué módulos se van a usar en el código.
- Usar la utilidad `pip` para descargar paquetes de código abierto de terceros.

## Requisitos previos

- Un entorno de desarrollo de Python totalmente configurado.
- Debe entender los tipos de datos básicos, como cadenas e `int`, y saber cómo crear, establecer y obtener valores de una variable.
- Debe tener experiencia con las llamadas a métodos mediante el operador de acceso a miembros `.` y saber cómo pasar argumentos a las funciones.

# Información general sobre la biblioteca estándar de Python

- 5 minutos

Antes de empezar a trabajar con la biblioteca estándar de Python, vamos a comprender exactamente qué es, cómo se relaciona con el lenguaje de programación de Python, cómo se divide en elementos administrables y cómo se puede aprovechar.

## ¿Qué es la biblioteca estándar de Python?

La biblioteca estándar de Python es una amplia colección de funciones, tipos y servicios que abordan diversas necesidades de programación. Aunque no forman parte del lenguaje Python, las funciones se distribuyen con el intérprete de Python y están disponibles para todos los programas de Python.

La biblioteca se divide en módulos. Algunos están *integrados*, de modo que puede empezar a usarlos sin notificárselo con antelación al compilador de Python. Otros módulos deben importarse primero.

Parte del código de esos módulos se escribe en el lenguaje de programación C, que puede abordar un conjunto de función de hardware y sistema operativo de nivel inferior que Python. Los desarrolladores de Python usan este acceso de bajo nivel a la memoria, el procesador, el sistema de archivos, el sistema operativo del equipo y demás para implementar características eficaces. C es un lenguaje de programación de nivel inferior, por lo que es eficaz, pero también más complicado que Python. A menudo, requiere una cantidad considerable de código para realizar tareas que son triviales en Python. Al empaquetar el código de C y ponerlo a disposición de Python, obtendrá lo mejor de ambos mundos.

## ¿Qué es un módulo?

Un *módulo* es simplemente un archivo de código. Más adelante, crearemos un módulo para que pueda experimentar cómo se trabaja con ellos. Los módulos que forman parte de la biblioteca estándar de Python son complejos y están enriquecidos con características, pero en el fondo, son simplemente archivos de código.

Cuando hablemos sobre un módulo, es posible que hagamos referencia al concepto de módulo (como archivo de código) o a la función que admite el archivo de código. Por ejemplo, cuando hacemos referencia al módulo `zipfile`, nos referimos a la colección de funciones que admiten la compresión y la descompresión de datos de archivo mediante el estándar de archivo ZIP.

## ¿Qué se puede hacer con la biblioteca estándar?

La biblioteca estándar abarca una amplia gama de funciones, entre las que se incluyen las siguientes:

- Módulos de fecha y hora
- Módulos numéricos y matemáticos
- Módulos del sistema de archivos
- Módulos del sistema operativo
- Módulos para leer y escribir formatos de datos específicos, como HTML, XML y JSON
- Módulos para trabajar con protocolos de Internet, como HTTP, SMTP, FTP, etc.
- Módulos para trabajar con datos multimedia, como sonido y vídeo
- Módulos para trabajar con información localizada, como presentar la moneda y las fechas
- Y mucho más

Para obtener una lista completa de los módulos de la biblioteca estándar de Python, vea [La biblioteca estándar de Python ](https://docs.python.org/3/library/).

### Funciones integradas frente a módulos de importación

Hay cierto debate sobre el significado exacto de una función integrada. Por lo general, se trata de una función que se ha integrado en el intérprete de Python. Suelen ser funciones que se usan tan a menudo que sería laborioso importarlas cada vez que se necesitan. Por ejemplo, dado que casi todos los programas de Python necesitan usar la instrucción `print()` en algún elemento, tiene sentido incluirlo como una función integrada.

Hay otras características y funciones útiles, pero solo se necesitan de vez en cuando. En estos casos, puede indicar al compilador de Python que espera usarlas en el programa. Para ello, usará la instrucción `import` en un ejercicio de este módulo.

En el caso de paquetes de terceros (por lo general, bibliotecas de código abierto de funciones que crean una comunidad de desarrolladores voluntarios), primero debe descargar e instalar las bibliotecas localmente y, después, usar una instrucción `import` para indicar al compilador de Python que tiene previsto usar sus funciones en el código. Use una utilidad de la línea de comandos de Python llamada `pip` para instalar un paquete localmente y usarlo en el programa. En un ejercicio de este módulo, instalaremos e importaremos las funciones y las llamaremos desde un paquete.

### ¿Cómo puedo encontrar lo que busco?

Con la gran cantidad de módulos que existen en la biblioteca estándar de Python, por no mencionar las bibliotecas de terceros disponibles, encontrar el módulo adecuado puede parecer una tarea abrumadora.

En primer lugar, no necesita aprender todo esto. Es imposible leer toda la documentación de la biblioteca estándar, y mucho menos la documentación de todas las bibliotecas de Python populares, por lo que ni siquiera debe intentar hacerlo. Con el tiempo, se familiarizará con un subconjunto de módulos y bibliotecas que afectan al trabajo que le ocupa.

En segundo lugar, debe empezar por buscar una solución para el problema específico que trata de resolver. Aunque es posible que todavía no conozca todos los detalles, debe ser capaz de formular un conjunto de palabras clave que describan el problema.

Una vez que pueda plantearlo con claridad, el siguiente paso consiste en convertirse en un detective. Deberá recurrir a motores de búsqueda para encontrar posibles soluciones. Es probable que exista una docena de maneras diferentes de resolver el problema. Tal vez tarde unos minutos, unas horas o incluso un día en revisar los diferentes enfoques para solucionarlo. También es probable que algunos de esos enfoques requieran módulos de la biblioteca estándar de Python, paquetes de terceros o ambos.

Si piensa que buscar la solución es *hacer trampa*, hágase la pregunta siguiente. ¿Deja de ser buen programador por no saberlo todo? En absoluto. Todo el mundo lo hace, sobre todo los desarrolladores profesionales experimentados. Existe una extensa comunidad y una tradición orgullosa de desarrolladores que se ayudan entre sí en línea. Nadie puede saber de todo.

Sin duda, debe comprender bien el lenguaje Python. Si copia código de blogs, artículos o vídeos, deberá dedicar un tiempo a comprender qué hace y decidir cómo incorporarlo en su trabajo, como si fuera suyo. Sin embargo, no debe sentirse mal por *robar* la solución de una persona para resolver un problema determinado. Precisamente para eso está publicada en Internet.

## Resumen

- Un módulo es un archivo que contiene funciones que implementan funcionalidad. La biblioteca estándar de Python se compone de más de 200 módulos que contienen miles de funciones.
- Las funciones importantes que se usan con más frecuencia están integradas directamente en el compilador y el intérprete de Python.
- Debe usar una instrucción `import` para indicar al compilador de Python qué módulos de la biblioteca estándar de Python contienen las funciones, los tipos, los servicios y los demás elementos que usará en el código.
- Mediante la búsqueda en línea, encontrará módulos y funciones de la biblioteca estándar de Python (y otros paquetes de terceros) que se pueden combinar para resolver el problema de programación al que se enfrenta.

# Ejercicio: Uso de una instrucción include para aprovechar un módulo de la biblioteca estándar

- 5 minutos

En este ejercicio, usará el módulo `random` para generar un valor aleatorio. Esto resulta útil cuando se compilan simulaciones o juegos para introducir aleatoriedad. Lo más importante que aprenderá es cómo usar las instrucciones `import` y `import ... as` en los programas.

### Paso 1: Crear una nueva carpeta de trabajo y un archivo de código de Python

Con las técnicas que ha aprendido en los módulos anteriores, cree una carpeta nueva para su trabajo en este módulo. Por ejemplo, puede crear una carpeta denominada `python-standard-library`.

Dentro de esa carpeta, cree un archivo para este ejercicio. Por ejemplo, puede crear un archivo denominado `exercise1.py`.

Cuando se le pida ejecutar el código, puede usar la integración de las Herramientas de Python para Visual Studio Code seleccionando la flecha verde. También puede usar un comando en el terminal integrado mediante las técnicas que se han aprendido en módulos anteriores.

### Paso 2: Importar el módulo `random` de la biblioteca estándar de Python

La sintaxis de la instrucción `import` es sencilla. Debe usar la instrucción `import` antes de intentar usar las funciones que contiene el módulo que va a importar. Además, por convención, debe agregar la instrucción `import` en la parte superior del archivo de código, antes que cualquier otro código.

Agregue la siguiente instrucción `import` a su archivo de código.

PythonCopiar

```python
import random
```

### Paso 3: Escribir la palabra `random` y el operador de acceso a miembros para ver IntelliSense

Incluso sin leer la documentación del módulo `random` de forma detallada, podrá explorar sus funciones, constantes y servicios mediante el uso de IntelliSense en Visual Studio Code. A medida que escriba en el editor de código, IntelliSense mostrará mensajes contextuales con las mejores opciones. Para navegar, escriba las primeras letras de la opción que quiere usar o desplácese con la flecha arriba y la flecha abajo. La opción resaltada mostrará la documentación en el lado derecho, en una ventana emergente independiente. Una vez que encuentre la opción que quiere usar, puede seleccionar las teclas Entrar o Tabulación para que se escriba automáticamente el resto de la palabra.

A fin de invocar IntelliSense para el módulo `random`, escriba la línea de código siguiente en la lista de códigos que aparece más abajo. Haga una pausa después de escribir el operador de acceso a miembros `.` después del identificador `random`.

PythonCopiar

```python
import random
roll = random.
```

Si ha parado de escribir en el signo `.`, debería ver que la ventana de IntelliSense muestra todas las funciones disponibles en el módulo `random`.

Puede aprender mucho sobre las funciones de un módulo si las examina detenidamente. Busque la función `randint` con las teclas flecha arriba y flecha abajo. Cuando la encuentre, lo que verá en la copia de Visual Studio Code debería coincidir con lo siguiente.

![Captura de pantalla de IntelliSense en Visual Studio Code que localiza la función randint del módulo random.](https://docs.microsoft.com/es-es/learn/language/python-standard-library/media/3-exercise-include-1.png)

Ahora, seleccione las teclas Entrar o Tabulación para que se escriba automáticamente el resto del nombre de la función `randint`.

Luego, escriba el símbolo de paréntesis de apertura `(` para que vuelva a aparecer IntelliSense. Esta vez, mostrará que la función `randint` toma dos argumentos de entrada que definen el rango, "incluidos ambos puntos de conexión".

![Captura de pantalla de IntelliSense en Visual Studio Code en la que se muestra la ayuda de los argumentos de entrada para la función randint.](https://docs.microsoft.com/es-es/learn/language/python-standard-library/media/3-exercise-include-2.png)

Al definir un rango de valores en programación, la palabra "inclusive" (inclusivo) suele indicar que el valor proporcionado se encuentra dentro de los límites, mientras que "exclusive" (exclusivo) significa que el valor está fuera de los límites. Por lo tanto, si queremos un valor aleatorio entre 1 y 10, la documentación de IntelliSense en formato breve indica que podemos definirlo si pasamos los valores `1` y `10` como argumentos.

Por lo tanto, la línea de código debería coincidir totalmente con la lista de códigos siguiente.

PythonCopiar

```python
roll = random.randint(1, 10)
```

### Paso 4: Agregar código para imprimir el valor generado por el módulo random

Para completar el ejemplo de código, agregue una instrucción `print()` que dé formato a la línea mediante una cadena f. Asegúrese de que el código coincide con la lista de código siguiente.

PythonCopiar

```python
import random
roll = random.randint(1, 10)
print(f'You rolled {roll}.')
```

Al ejecutar el código, debería ver el resultado siguiente (el número será aleatorio).

ResultadosCopiar

```output
You rolled 3.
```

El número probablemente cambiará cada vez que ejecute el programa.

### Paso 5: Modificar el código a fin de crear un alias para el nombre del módulo

Puede que no le guste usar el nombre del módulo `random` en el código. Es posible que no describa el rol que quiera que desempeñe el módulo en el programa, o bien que ya use el identificador `random` en el programa y que volver a usarlo provoque un conflicto. En estos casos, puede agregar la cláusula `as` a la instrucción `import` para crear un alias.

Modifique su código para que coincida con la lista de códigos siguiente.

PythonCopiar

```python
import random as alias
roll = alias.randint(1, 10)
print(f'You rolled {roll}')
```

En este ejemplo concreto, el nombre `random` es bastante descriptivo, pero tal vez prefiera asignar un alias al nombre para que resulte más ilustrativo. Ahora puede acceder a la función del módulo `random` mediante el identificador `alias`.

Al ejecutar el programa, verá que se imprime de nuevo el mismo valor aleatorio.

ResultadosCopiar

```output
You rolled 6.
```

Hemos elegido el identificador `alias` como ejemplo, pero puede usar cualquier identificador válido que siga las mismas reglas de nomenclatura que las variables de Python.

Vamos a cambiar el nombre del alias. Reemplace el identificador `alias` por el identificador `dice`.

PythonCopiar

```python
import random as dice
roll = dice.randint(1, 10)
print(f'You rolled {roll}')
```

Cuando ejecute el programa, debería seguir funcionando.

## Resumen

- Use la instrucción `import` para incluir en el programa un paquete de la biblioteca estándar de Python. Todas las funciones del módulo están disponibles mediante el uso del operador de acceso a miembros `.`.
- En Visual Studio Code, la característica IntelliSense mostrará los miembros (funciones, constantes y servicios) que están disponibles cuando escriba el operador de acceso a miembros.
- Use la instrucción `import ... as` a fin de crear un alias para el módulo, si esto le ayuda a describir el rol que desempeña en el sistema de software.
- El paquete `random` proporciona una manera de generar un valor aleatorio. Esto le resultará muy práctico a medida que creemos más ejemplos de código interesantes en los próximos módulos de Microsoft Learn.

# Ejercicio: Instalación de un paquete de terceros mediante PIP

- 5 minutos

Aunque la biblioteca estándar de Python tiene una gran compatibilidad con una amplia gama de características, no puede solucionar todos los posibles problemas. Afortunadamente, una comunidad de OSS ha creado miles de paquetes que compensan las carencias.

En este ejercicio, se usará `pip`, una utilidad que accede a Índice de paquetes de Python (PyPI), un popular índice de paquetes. Si combina ambos elementos, encontrará los paquetes que necesita para prácticamente cualquier propósito imaginable.

Supongamos que quiere mejorar la salida con emoticonos, como una cara sonriente o un símbolo de pulgares hacia arriba. La biblioteca estándar de Python no lo admite, pero puede encontrar paquetes candidatos disponibles en PyPI y usar `pip` para instalar un paquete localmente para el desarrollo.

### ¿Qué es un paquete de Python?

Un paquete de Python es un medio para organizar, recopilar y distribuir código de modo que puedan usarlo otros desarrolladores. Los paquetes proporcionan un sistema jerárquico de archivos y carpetas para organizar el código y permiten distribuir también las dependencias con el código.

La creación de paquetes está fuera del ámbito de este módulo, pero debe saber como mínimo en qué consiste y cómo `pip` instala tanto el paquete que necesita como las dependencias en las que se basa.

### ¿Qué es una dependencia?

Una dependencia es un paquete independiente que el código necesita para funcionar correctamente. Supongamos que quiere crear un paquete con algunas funciones que piensa que beneficiarían a otras personas. Uno de los pasos que debe llevar a cabo al empaquetar el código consiste en especificar el nombre y la versión de los paquetes de los que depende en un archivo de manifiesto denominado `setup.py`. Cuando otro desarrollador quiera usar el paquete, utilizará `pip`. La utilidad `pip` examinará el manifiesto y además instalará (o actualizará) todas las dependencias necesarias que haya especificado para que el paquete funcione correctamente en el equipo.

### Paso 1: Agregar un archivo de código al directorio de trabajo para este ejercicio

Suponiendo que continúa desde la unidad anterior, use las técnicas que ha aprendido en los módulos anteriores para agregar un archivo de código nuevo en la carpeta actual dedicada a este módulo. Por ejemplo, puede crear un archivo denominado `exercise2.py`.

### Paso 2: Navegar a través del explorador web hasta el Índice de paquetes de Python (PyPI)

En el explorador web, navegue hasta el [Índice de paquetes de Python (PyPI) ](https://pypi.org/).

PyPI dispone de más de 200 000 proyectos diferentes. Use la barra de búsqueda de la página principal para buscar el término "emoji". Obtendrá 16 páginas de resultados de búsqueda.

Está buscando el proyecto denominado "emoji", que debería ser uno de los primeros resultados. Encontrará el hipervínculo directo en la dirección URL siguiente:

[https://pypi.org/project/emoji/ ](https://pypi.org/project/emoji/)

Esta dirección URL muestra una descripción del proyecto, un ejemplo, las instrucciones de instalación, la licencia, los autores, etc.

Lo que nos interesa son las instrucciones de instalación y el código de ejemplo.

### Paso 3: Usar `pip` para instalar el paquete `emoji`

De nuevo en el terminal de Visual Studio Code, escriba el comando siguiente en Linux y macOS.

BashCopiar

```bash
pip install emoji
```

Si en Linux o macOS recibe un mensaje que indica que no tiene privilegios suficientes, deberá usar la cuenta de superusuario. Escriba el comando siguiente.

BashCopiar

```bash
sudo pip install emoji
```

Si está en Windows, puede que necesite emplear la utilidad `py` para ejecutar `pip`. Pruebe el comando siguiente en Windows.

cmdCopiar

```cmd
py -m pip install emoji
```

### Paso 4: Agregar código para importar y llamar a la función del nuevo paquete

En el código de ejemplo de la página de PyPI se muestra cómo usar la función `emojize` del paquete `emoji` para codificar una representación de cadena de un emoticono que se puede mostrar mediante la función `print()`.

Con una técnica similar a la que hemos aprendido en la unidad anterior, agregue el código siguiente para importar mediante `import` el paquete que ha instalado y llame a la función que codificará el emoticono.

PythonCopiar

```python
import emoji
message = emoji.emojize('Howdy :sun_with_face:')
print(message)
```

Al ejecutar el código, debería ver la salida siguiente.

![Captura de pantalla del terminal de Visual Studio Code en la que se muestra el resultado del código de ejemplo con un emoji de sol.](https://docs.microsoft.com/es-es/learn/language/python-standard-library/media/4-exercise-pip-1.png)

### Resumen

- Visite PyPI para buscar paquetes que puedan resolver su necesidad de programación, en lugar de intentar compilar por su cuenta la lógica del código. Use la información de la documentación de los paquetes de PyPI para instalar y usar la función del paquete en el programa.
- Use el comando `pip install ` para instalar un paquete localmente con todas sus dependencias.

## Comprobación de conocimientos

\1. 

¿Qué es un módulo?



Un paquete de archivos de código que se instala en el equipo local.



Una lista de las dependencias que usa el código.



Un archivo de código que solo puede crear el equipo de desarrollo de Python.



Un archivo de código con funciones a las que se puede hacer referencia y llamar desde su propio código.

Correcto.

\2. 

¿Qué hace la utilidad `pip`?



La utilidad `pip` instala paquetes de GitHub.



La utilidad `pip` instala los paquetes y las dependencias que se enumeran en el Índice de paquetes de Python (PyPI).

Correcto.



La utilidad `pip` ayuda a encontrar paquetes para solucionar problemas de programación.



La utilidad `pip` instala los paquetes de la biblioteca estándar de Python.



# Resumen

- 1 minuto

Nuestro objetivo consistía en explorar y usar la biblioteca estándar de Python en nuestros propios programas y obtener información sobre cómo encontrar soluciones a problemas comunes de desarrollo de software en la comunidad de Python.

Hemos importado el módulo `random` de la biblioteca estándar de Python para generar números aleatorios mediante una llamada a una función de ese módulo. Hemos explorado el módulo mediante IntelliSense en Visual Studio Code y comprobado que podemos obtener información sobre cada función del módulo si consultamos la documentación en formato breve en IntelliSense. Hemos buscado soluciones a nuestras necesidades mediante el índice de paquetes de Python (PyPI) y, después, hemos empleado la utilidad `pip` para instalar un paquete localmente y llamar a una función del paquete.

Si no pudiéramos aprovechar este completo ecosistema, tendríamos que compilarlo todo, lo que probablemente llevaría mucho tiempo y sería más propenso a errores. También se requieren amplios conocimientos de Python antes de que podamos ser productivos. Afortunadamente, esta extensa colección de funciones de los creadores de Python y de la comunidad permite compilar programas de forma más rápida y sencilla.



