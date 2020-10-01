# Creación de su primer programa de Python

Comience a usar Python y escriba código para interactuar con los usuarios finales.

## Learning Objectives

Objetivos de este módulo:

- Crear archivos de código de Python y ejecutar el código dentro de Visual Studio Code.
- Escribir código para enviar un mensaje de texto a la línea de comandos.
- Escribir código para aceptar la entrada del usuario desde la línea de comandos.
- Comprender por qué se producen errores de compilación y en tiempo de ejecución, y qué hacer a continuación.
- Concatenar texto codificado de forma rígida con datos proporcionados por el usuario para mostrar mensajes con formato personalizado al usuario.
- Realizar sumas matemáticas en datos numéricos.
- Convertir datos alfanuméricos en datos numéricos y viceversa (y saber por qué necesita hacerlo).

## Requisitos previos

- Python 3.x instalado
- Visual Studio Code instalado
- Herramientas de Python para Visual Studio Code instaladas, así como todas las herramientas recomendadas, como Pylint

# Introducción

- 1 minuto

Un objetivo común de muchos programas es tomar una entrada, procesarla, darle formato y, después, enviarla de alguna manera. En este módulo escribirá código de Python para realizar cada una de estas tareas. A lo largo del proceso, aprenderá muchas ideas fundamentales, como trabajar con datos, realizar operaciones en los datos, recuperar entradas, generar resultados y mucho más.

Al final de este módulo, podrá compilar aplicaciones sencillas que puedan aceptar entrada del usuario, combinar esa entrada con texto literal y mostrar el resultado al usuario. Lo que es más importante, habrá dado los primeros pasos imprescindibles para aprender Python.

## Objetivos de aprendizaje

Objetivos de este módulo:

- Crear archivos de código de Python y ejecutar el código en Visual Studio Code.
- Escribir código para enviar un mensaje de texto a la línea de comandos.
- Escribir código para aceptar la entrada del usuario desde la línea de comandos.
- Comprender por qué se producen errores de compilación y en tiempo de ejecución, y qué hacer a continuación.
- Concatenar texto codificado de forma rígida con datos proporcionados por el usuario para mostrar mensajes con formato personalizado al usuario.
- Realizar sumas matemáticas en datos numéricos.
- Convertir datos alfanuméricos en datos numéricos y viceversa.

## Requisitos previos

- Python 3.x instalado
- Visual Studio Code instalado
- Herramientas de Python para Visual Studio Code instaladas, incluidas todas las herramientas recomendadas, como Pylint.

Si necesita ayuda con la instalación de estos requisitos previos, siga las instrucciones del módulo "Configuración del entorno de desarrollo para principiantes de Python con Visual Studio Code".



# Ejercicio: Hello world!

- 5 minutos

La forma más fácil de aprender a programar es escribir docenas (si no centenas) de programas pequeños que le ayudarán a comprender las ideas fundamentales y a practicar las principales técnicas.

## Qué va a crear

En esta unidad, comenzará por compilar un programa que imprime un mensaje en la pantalla mediante una sola línea de código. Esta actividad requiere que navegue por Visual Studio Code y trabaje en el editor de código.

### Paso 1: Crear una carpeta para el primer proyecto de Python

En primer lugar, en el equipo, cree una estructura de carpetas donde almacenará el trabajo.

Se recomienda crear una sola carpeta para que contenga todos los ejercicios de cada módulo. Puede asignar el nombre que quiera a esta nueva carpeta principal, como *Python* o *Learn*. Use las herramientas y técnicas con las que esté familiarizado y cree la carpeta en un lugar del disco duro que sea fácil de encontrar.

En segundo lugar, en esta carpeta de nivel superior, cree una subcarpeta para los archivos de ejercicios con los que trabajará en este módulo. Puede asignar el nombre que quiera a la nueva carpeta secundaria, como *Hello*.

En los próximos módulos de Python, cuando se le pida que cree una nueva carpeta, asegúrese de crear subcarpetas como elementos secundarios en la carpeta primaria de este paso.

### Paso 2: Abrir Visual Studio Code

Use la técnica con la que esté familiarizado para abrir Visual Studio Code desde su sistema operativo.

### Paso 3: Abrir la carpeta recién creada

En Visual Studio Code, seleccione **Archivo** > **Abrir carpeta**.

En la ventana **Abrir carpeta**, busque y seleccione la carpeta que creó en el paso 1.

El nombre de la carpeta se muestra en el panel izquierdo de la vista del explorador.

### Paso 4: Crear y guardar un archivo

Seleccione **Archivo** > **Nuevo archivo**. Esto agrega una nueva pestaña titulada "Sin título-1" en el panel del editor.

Seleccione **Archivo** > **Guardar como** y, después, asigne al archivo el nombre *hello.py*.

### Paso 5: Agregar código al archivo

El nuevo archivo *hello.py* está vacío. En el panel del editor, escriba el código siguiente:

PythonCopiar

```python
print("Hello World!")
```

 Importante

Escriba el código exactamente como lo ve aquí, escribiendo los paréntesis y comillas en el orden correcto y usando letras minúsculas para la palabra *print*. Basta un solo carácter incorrecto para provocar que el programa produzca un error y no funcione.

### Paso 6: Guardar el archivo y ejecutar el programa

Después de escribir el código, seleccione **Archivo** > **Guardar**.

 Nota

Puede ver que el archivo debe guardarse si hay un punto en blanco a la derecha del nombre de archivo en la pestaña.

Para ejecutar el programa, seleccione la flecha verde situada a la derecha de las pestañas. Si mantiene el mouse sobre la flecha, verá la información sobre herramientas "Ejecutar el archivo de Python en el terminal". Esto le permite saber que está en el lugar correcto.

![Captura de pantalla de Visual Studio Code con una llamada alrededor del botón de flecha verde "Reproducir" que selecciona para ejecutar el código de Python.](https://docs.microsoft.com/es-es/learn/language/python-create-first/media/2-exercise-hello-world-03.png)

Cuando se ejecuta el código, aparecen dos líneas en la ventana **Terminal**:

- La primera línea es el comando para compilar y ejecutar el archivo de código.

  ResultadosCopiar

  ```output
  C:\python\hello>C:/Users/<user>/AppData/Local/Programs/Python/Python38-32/python.exe c:/python/hello/hello.py
  ```

   Nota

  La salida varía según el sistema operativo. Además, desde Windows, la ruta de acceso será diferente. Para **, sustituya su nombre de usuario.

- La otra línea impresa en la ventana de terminal aparece debajo de la ventana de código:

  ResultadosCopiar

  ```output
  Hello World!
  ```

Terminado.

### Se ha producido un error

Es posible que se produzca un error al intentar ejecutar el código. Esto puede ocurrir por diversos motivos.

Por ejemplo, podría haber usado una *P* mayúscula en lugar de una *p* minúscula en *print*, como se muestra a continuación:

PythonCopiar

```python
Print("Hello World!")
```

Una *P* mayúscula produce el siguiente mensaje de error en la salida:

ResultadosCopiar

```output
Traceback (most recent call last):
  File "c:/python/hello/hello.py", line 1, in <module>
    Print("Hello World!")
NameError: name 'Print' is not defined
```

Como se explicó anteriormente, la precisión es fundamental cuando se escribe código. Python distingue entre mayúsculas y minúsculas, lo que significa que *print* y *Print* son dos cosas diferentes. No hay ninguna función llamada `Print` con una *P* mayúscula.

Afortunadamente, Visual Studio Code puede ayudarle a detectar errores como esto antes de ejecutar el código. Debería ver una línea ondulada roja en *Print*. Si mantiene el mouse sobre la palabra, una información sobre herramientas muestra la frase "Variable no definida 'Print'". El mensaje específico requiere más explicación, pero, por ahora, al menos puede detectar posibles problemas en el código.

![Captura de pantalla de Visual Studio Code con una línea ondulada de color rojo debajo de la palabra "Print" con una P mayúscula incorrecta.](https://docs.microsoft.com/es-es/learn/language/python-create-first/media/2-exercise-hello-world-01.png)

 Importante

Debe guardar los cambios en el archivo para mostrar la línea ondulada de color rojo.

Puede usar esta misma técnica para buscar otros tipos de problemas en el código. Por ejemplo, supongamos que ha transpuesto el orden de ciertos caracteres, como el paréntesis de cierre y la comilla de cierre, como se muestra aquí:

PythonCopiar

```python
print("Hello World!)"
```

Si ejecutase el código, vería el siguiente mensaje de error:

ResultadosCopiar

```output
  File "c:/python/hello/hello.py", line 2

                         ^
SyntaxError: unexpected EOF while parsing
```

En este caso, es posible que el mensaje de error todavía no sea significativo. Después de guardar el archivo, Visual Studio Code agrega una línea ondulada de color rojo debajo de la comilla de cierre, que por lo menos le debería proporcionar una pista útil para diagnosticar automáticamente el error.

Esto no funciona porque no sigue las reglas de sintaxis de Python. La sintaxis en el código es similar a la gramática en lenguaje humano. En breve se explicará por qué esto infringe las reglas de sintaxis de Python.

Algunos errores son fáciles de identificar y de corregir. Otros requieren un poco más de esfuerzo. Supongamos que ha usado corchetes en lugar de paréntesis, como se muestra aquí:

PythonCopiar

```python
print["Hello World!"]
```

Después de guardar el archivo, aparece una línea ondulada de color rojo debajo de *print*. Esta vez, cuando mantenga el mouse sobre la línea ondulada roja, verá un párrafo con información adicional.

![Captura de pantalla de Visual Studio Code con un cuadro de mensaje que muestra información de referencia sobre el comando print y un mensaje de error.](https://docs.microsoft.com/es-es/learn/language/python-create-first/media/2-exercise-hello-world-02.png)

En otro módulo se explicará qué significa esta información, pero por el momento se omitirá, puesto que todavía es un poco avanzado para el momento en que nos encontramos. La clave principal es que hay un problema con el código.

Al ejecutar el programa, aparece el siguiente mensaje de error en la salida:

ResultadosCopiar

```output
Traceback (most recent call last):
  File "c:/python/hello/hello.py", line 1, in <module>
    print["Hello World!"]
TypeError: 'builtin_function_or_function' object is not subscriptable
```

Desafortunadamente, este mensaje de error no es útil porque no describe el problema: para invocar una función, debe reemplazar los corchetes por paréntesis.

En futuras situaciones como esta, apóyese en sus conocimientos de Python y su buen ojo para detectar el problema.

Obtendrá tanto los conocimientos como su buen ojo a base de experiencia. Puede parecer desalentador al principio, pero, con la práctica, dominará esta información y mucho más.

## ¿Cómo ha funcionado el programa?

Invocó una *función* denominada `print`. Una función contiene código que funciona conjuntamente para completar una sola tarea en un sistema de software. A la función se le asigna un nombre para que pueda llamarla con ese nombre e invocar su funcionalidad. El único trabajo de la función `print` es enviar información a la salida, y esa salida se puede mostrar a través de una línea de comandos o una ventana de terminal.

Para invocar una función, se usa un conjunto de paréntesis denominados operadores de invocación de funciones. El conjunto de paréntesis es la instrucción para el intérprete de Python que quiere que ejecute esa función.

Más adelante, aprenderá a crear sus propias funciones. Al principio usará funciones que los creadores de Python han desarrollado para ayudarle a escribir aplicaciones con más rapidez. Además, aprenderá a usar bibliotecas de terceros que amplían drásticamente la funcionalidad disponible de los programas de Python para realizar una amplia variedad de tareas.

Algunas funciones permiten pasar un argumento, que la función puede usar para completar su tarea. En este caso, envió a la función `print` una *cadena literal* que contiene el mensaje `Hello World!`. Los argumentos se pasan dentro de los operadores de invocación de funciones.

Una cadena literal es un valor codificado de forma rígida que contiene caracteres alfanuméricos. En otras palabras, quiere imprimir en la salida exactamente esta cadena de caracteres: `H`, `e`, `l`, `l`, `o`, un espacio vacío, `W`, etc. Una cadena literal se define mediante un par de comillas o un par de comillas simples.

Cuando el compilador de Python evalúa el código, comprueba si hay errores de sintaxis y, después, convierte el código en una sintaxis compacta llamada *código de bytes* que solo consta de ceros y unos. El intérprete de Python sabe cómo leer esta sintaxis y procesa cada una de las instrucciones que contiene, línea a línea.

En este escenario, solo hay una línea de código. Si hubiera más, funcionaría desde arriba a abajo. Después, cuando se haya ejecutado la última línea, el programa se cerrará y se devolverá el control al sistema operativo.

## Resumen

Dedique un momento a recapitular las lecciones más importantes de esta primera unidad:

- El proceso de escribir código de Python es un ejercicio de precisión. Use la ortografía, las mayúsculas, las minúsculas y los símbolos correctos al escribir código.
- Utilice la función `print` para mostrar información de texto en la salida a través de una línea de comandos o una interfaz de terminal.
- Una cadena literal es una cadena de caracteres individuales que quiere utilizar exactamente como se escribe en el programa. Una cadena literal se define mediante un par de comillas o de comillas simples.
- Visual Studio Code permite crear fácilmente un archivo de código, guardar el trabajo y, después, ejecutar el código seleccionando el icono de flecha verde.
- Si el código incluye una sintaxis no válida, el compilador de Python detiene la ejecución y muestra un error. Con las pistas proporcionadas por el compilador, puede corregir el error y volver a intentarlo.
- Al guardar el archivo de código, Visual Studio Code analiza el código y agrega una pista visual que le ayuda a detectar posibles errores antes de intentar ejecutar el programa.

# Ejercicio: HELLO name

- 5 minutos

Los programas son más interesantes cuando puede solicitar información al usuario y usar esa entrada en los programas.

## Qué va a crear

Se basará en el ejercicio anterior para solicitar a los usuarios su nombre para enviar un mensaje personalizado.

### Paso 1: Comentar el código del ejercicio anterior

Al comentar una línea de código, le interesa mantener el código en el archivo de código, pero le indica al compilador que omita esta instrucción. Es posible que quiera agregar un comentario de línea si no está seguro de si quiere eliminar permanentemente la línea de código y prefiere aplazar esa decisión.

También puede usar los comentarios de código para agregar notas breves para usted mismo u otros desarrolladores de software que puedan ver el código, explicando algo sobre el código que no sería obvio simplemente al leerlo.

Para comentar el código, coloque un signo de número único (**#**) al principio de la línea, seguido de un espacio vacío. Ahora, su código debería coincidir con el siguiente ejemplo:

PythonCopiar

```python
# print("Hello World!")
```

Si guarda y ejecuta el programa ahora, no sucederá nada porque ha indicado al compilador de Python que omita esta línea de código.

### Paso 2: Agregar código debajo del código comentado

Después, agregue una línea vacía y tres líneas nuevas de código. Asegúrese de que el código coincide con el siguiente ejemplo de código:

PythonCopiar

```python
# print("Hello World!")

print("What is your name?")
name = input()
print("Hello, " + name)
```

Este ejemplo de código presenta tres ideas nuevas:

- La primera línea es similar a la del ejercicio anterior. Simplemente está imprimiendo una nueva cadena literal en la salida.
- La segunda línea realiza tres operaciones distintas. Para empezar, está invocando la función `input()`, que recupera la entrada de teclado de un usuario final. Cuando el usuario escribe información y selecciona ENTRAR, la información se devuelve desde la función `input()`.
- Algunas funciones, como la función `print()`, pueden finalizar su trabajo de forma silenciosa. La función envía texto alfanumérico a la salida y sale sin devolver ningún valor. Otras funciones pueden devolver un valor al salir. En este caso, la función `input()` devuelve todos los caracteres alfanuméricos especificados por el usuario.

¿Qué debe hacer con el valor devuelto de la función `input()`? Debe almacenarlo temporalmente para su uso en las siguientes líneas de código. Para ello, crea una variable.

### Crear una variable

En Python, puede crear una variable con solo elegir un nombre de variable que no esté en uso y no sea una de las palabras clave especiales de Python. En este caso, crea una variable denominada `name` que almacenará los caracteres alfanuméricos que se devuelven de la función `input()`.

Ahora que ha definido una variable, debe asignarle un valor. El símbolo del signo igual (**=**) es el operador de asignación. Va a asignar el valor recuperado de la función `input()` a la nueva variable `name`.

Como resumen de la línea 2, ha realizado tres operaciones:

- Ha llamado a la función `input()` para recuperar los datos proporcionados por el usuario.
- Ha creado una nueva variable denominada `name`.
- Ha realizado una asignación, estableciendo `name` en el valor devuelto de `input()`.

Después de ejecutar esta línea de código, la variable `name` contiene el valor que especificó el usuario.

En la tercera línea, quiere imprimir un mensaje que combine una cadena literal y la variable de la línea 2. Una vez más, llama a la función `print` y pasa una cadena literal `"Hello, "`, pero también se usa el símbolo más (**+**) y el nombre de la variable. La combinación de dos o más cadenas se denomina *concatenación de cadenas*. Quiere anexar la cadena literal a la variable. Cuando se usa el símbolo de signo más (**+**) en este contexto, el compilador de Python sabe que quiere combinar estos dos valores en un nuevo valor.

Una vez creado el nuevo valor de cadena, se pasa a la función `print`.

### Paso 3: Guardar y ejecutar el programa mediante la utilidad py

Para ver el programa en acción, puede usar el icono de flecha verde en Visual Studio Code, como hizo en el ejercicio anterior. Pero esta vez, para demostrar que hay muchas maneras diferentes de ejecutar el código, se usará el terminal de Visual Studio Code.

En la ventana de terminal debajo del editor de código, coloque el cursor del mouse en el símbolo del sistema, escriba el siguiente comando y, después, seleccione ENTRAR:

dosCopiar

```dos
py hello.py
```

Si lo escribió correctamente, debería ver el siguiente resultado (en el símbolo del sistema, use su propio nombre):

ResultadosCopiar

```output
What is your name?
Bob
Hello, Bob
```

El comando `py` inicia el compilador de Python. Proporcione el nombre de archivo del código fuente como argumento. Si instaló Python correctamente y el símbolo del sistema funciona en el mismo directorio que los archivos de código, debería funcionar. De lo contrario, deberá usar la ruta de acceso completa y el nombre de archivo del archivo de código.

### ¿Qué son las palabras clave?

Las palabras clave son comandos integrados en el lenguaje de programación que tienen un significado especial en Python. Aprenderá muchas de estas palabras clave en los próximos módulos. Para obtener una lista de palabras clave que no se pueden usar como nombres de variable, consulte esta [documentación de Python ](https://docs.python.org/3/reference/lexical_analysis.html#keywords?azure-portal=true).

### ¿Qué son los operadores?

Un operador es un carácter que indica al compilador de Python que realice alguna operación especial. Ya ha visto varios operadores:

- Los paréntesis de apertura y cierre `()` son operadores de invocación de funciones (cuando se colocan a la derecha de un nombre de función).
- El signo igual `=` es el operador de asignación que se usa para asignar un valor a una variable.
- El signo más (`+`) es el operador de concatenación de cadenas. Como verá en la siguiente unidad, también es el operador de suma cuando está trabajando con números.
- El signo de número `#` es el operador de comentario, que indica al compilador que omita todo el código o el texto que aparece después de él en una línea de un archivo de código.

Python tiene docenas de operadores que realizan operaciones matemáticas, lógicas y relacionales en el código.

### ¿De dónde proceden las funciones?

Como se mencionó anteriormente, los desarrolladores de Python crearon funciones como `print()` e `input()`. Las funciones forman parte de la biblioteca estándar de Python, un amplio conjunto de funcionalidades que está disponible de forma automática o que se puede retrasar y agregar fácilmente según sea necesario. La biblioteca se divide en módulos. Cada módulo contiene funciones relacionadas. Aprenderá más sobre el acceso a todas las funcionalidades en los próximos módulos.

Cuando dice que quiere "aprender a usar Python", realmente está diciendo que quiere:

- Aprender muchas o todo lo que hacen las palabras clave y los operadores.
- Aprender a escribir código que use las palabras clave y los operadores correctamente (es decir, la sintaxis).
- Familiarizarse con algunas de las funciones y los módulos más importantes de la biblioteca estándar de Python y aprender a usar las funciones y los módulos de las bibliotecas de terceros.
- Aprender a estructurar el código para crear programas cada vez más interesantes y complejos.

A lo largo de estos módulos y rutas de aprendizaje, aprenderá todas estas cosas.

## Resumen

Este es un resumen breve de los aspectos más importantes que debe recordar de esta unidad:

- Use el símbolo de signo de número (**#**) para comentar una línea de código o agregar una nota corta. El compilador omite todo lo que se encuentra después del símbolo de signo de número (**#**) en una línea determinada y no se ejecuta.
- Utilice la función `input` para recuperar la entrada del teclado de un usuario final.
- Una variable es un puntero descriptivo a un valor que se almacena en la memoria del equipo.
- Cree una nueva variable eligiendo un nombre que no se haya usado en el programa y que no sea una de las palabras clave reservadas de Python.
- Use el símbolo de signo más (**+**) para concatenar dos cadenas con el fin de crear un nuevo valor de cadena.
- Una palabra clave es un comando que forma parte de un lenguaje de programación que realiza alguna función especial.
- Un operador es un símbolo que forma parte de un lenguaje de programación que realiza alguna operación especial.
- Las funciones son colecciones de código que realizan una sola tarea en un sistema de software.
- La biblioteca estándar de Python contiene cientos de funciones que se reparten entre docenas de módulos y que proporcionan una funcionalidad común para todos los desarrolladores. Otras bibliotecas de terceros contienen funcionalidades adicionales para ampliar las capacidades del lenguaje de programación

# Ejercicio: Suma de números

- 5 minutos

En este ejercicio, obtendrá información sobre los valores del programa, los tipos de datos y cómo convertir un valor de un tipo de datos en otro.

## Compilación de un programa que realiza sumas

Mediante el uso de técnicas como las que se presentan en los ejercicios anteriores, creará un programa que solicita al usuario final dos valores, los suma y muestra los resultados. A lo largo del proceso, encontrará problemas y soluciones nuevos que le proporcionarán información más detallada sobre cómo funciona Python.

### Paso 1: Crear un nuevo archivo de código .py

Se creará un archivo para el siguiente ejercicio. Mediante el uso de la técnica que acaba de aprender, cree un archivo y asígnele el nombre *numbers.py*.

 Nota

Recuerde que, en Visual Studio Code, puede seleccionar **Archivo** > **Nuevo archivo** para crear el archivo y, después, seleccionar **Archivo** > **Guardar como** para asignarle un nombre.

### Paso 2: Agregar código al nuevo archivo

En el nuevo archivo *numbers.py*, escriba el código siguiente:

PythonCopiar

```python
print("First Number:")
first_number = input()
print("Second Number:")
second_number = input()
sum = first_number + second_number
print(sum)
```

En su mayor parte, este ejemplo de código es casi idéntico a lo que creó en ejercicios anteriores. Pero ha hecho algo ligeramente diferente en esta línea de código:

PythonCopiar

```python
sum = first_number + second_number
```

Aquí introduce una *variable temporal* para contener un valor calculado que se usará más adelante en el programa. En otras palabras, podría haber escrito la última línea de código de esta otra manera:

PythonCopiar

```python
print(first_number + second_number)
```

Si decide hacerlo, no necesitará introducir la variable `sum`. Por lo tanto, ¿por qué ha creado la variable `sum`? A veces, una variable temporal puede hacer que el código sea más legible. En este caso, sabe que la última línea de código se hará más complicada más adelante en este ejercicio, y podría hacer que esa línea sea más corta y más fácil de administrar para eliminar la suma, la concatenación e imprimir todo en una sola línea de código. Esto es solo cuestión de opinión y, como desarrollador, a medida que vaya escribiendo código creará su propio estilo y preferencias personales sobre lo que le parece legible.

La comunidad de Python simplemente recomienda que se asegure de que el código sea legible para su propio uso futuro o por el bien de otros usuarios que leerán el código en el futuro. Una frase que se oye a menudo en la comunidad de desarrolladores de Python es que "escribirá el código una vez, pero lo leerá muchas veces, por lo que debe optimizarlo para la lectura".

### Asignación de nombres a variables

Puede asignar a las variables el nombre que prefiera, pero es recomendable elegir un nombre que describa los datos a los que apunta la variable. A veces es difícil elegir el nombre correcto, pero es una tarea que merece la pena. Idealmente, el nombre sería lo más corto y descriptivo posible. En general, debería poder hacerlo en una o dos palabras.

Un procedimiento recomendado de Python es usar solo letras minúsculas para los nombres de variable. Si necesita más de una palabra para describir adecuadamente el propósito de la variable, sepárelas con un carácter de subrayado (**_**).

### Paso 3: Guardar y ejecutar el código

Guarde y ejecute el programa mediante una de las técnicas que aprendió anteriormente. Debería ver la siguiente salida:

ResultadosCopiar

```output
First Number:
5
Second Number:
4
54
```

Este no es el resultado deseado. Quiere que el programa agregue dos números para crear una suma, pero parece que, en su lugar, el programa ha concatenado dos cadenas. El problema es que la función `input()` devuelve datos representados como cadenas, no números.

En Python, cada valor de los programas tiene un tipo de datos asociado que describe el tipo de datos que es y lo que se puede hacer con él. En otras palabras, dado que los dos valores son cadenas, solo se pueden concatenar. Si quiere realizar operaciones matemáticas con dos valores, ambos deben ser tipos de datos numéricos.

¿Cómo se puede convertir un valor de cadena en un valor entero y por qué es necesario?

### ¿Qué es un tipo de datos?

Los tipos de datos existen en todos los lenguajes de programación. La mayoría de los lenguajes de programación tienen diversos tipos de datos, que representan diferentes tipos de datos y los tipos de operaciones que quiere realizar en los propios datos. Python tiene tipos de datos simples, como string, integer y float (que pueden representar datos numéricos que contienen fracciones), y tipos de datos complejos que representan colecciones de valores y mucho más.

Cada tipo de datos existe para satisfacer una necesidad que los programadores puedan tener en algún momento durante su carrera. Algunos tipos de datos los usará con frecuencia, y otros con poca, si es que llega a usarlos.

Si los valores con los que está trabajando en el programa no son del tipo de datos correcto, puede convertirlos al tipo de datos deseado mediante funciones integradas. En este escenario, usará la función `int()` para convertir una cadena en un número entero (entero). Cuando el valor es del tipo de datos correcto, puede usarlo como prefiera. Por ejemplo, después de convertir los datos de cadena en datos enteros, puede realizar la operación de suma de los datos.

### Paso 4: Revisar el código para convertir la entrada en enteros

Modifique su código para que coincida con el ejemplo siguiente:

PythonCopiar

```python
print("First Number:")
first_number = int(input())
print("Second Number:")
second_number = int(input())
sum = first_number + second_number
print(sum)
```

Tenga en cuenta la diferencia clave en este ejemplo de código. Aquí, está ajustando la llamada a la función `input()` con una llamada a la función `int()`. En otras palabras, el intérprete de Python ejecuta primero la función `input()` y, después de que se devuelva un valor de la función `input()` que contiene los datos proporcionados por el usuario, se pasa como parámetro de entrada a la función `int()`, que convierte el valor de una cadena a un entero.

### Paso 5: Guardar y ejecutar el código

Guarde y ejecute el programa mediante una de las técnicas que aprendió anteriormente. Debería ver la siguiente salida:

ResultadosCopiar

```output
First Number:
5
Second Number:
4
9
```

Terminado.

Pero, ¿qué ocurre si vuelve a ejecutar el programa y proporciona valores no numéricos? En otras palabras, ¿qué ocurre si escribe su nombre y apellido en lugar de dos números cuando se le solicita?

ResultadosCopiar

```output
First Number:
bob
Traceback (most recent call last):
  File "c:/python/hello/stuff.py", line 8, in <module>
    first_number = int(input())
ValueError: invalid literal for int() with base 10: 'bob'
```

Aquí, cuando volvió a ejecutar el programa, escribió un nombre, *Bob*, en lugar de un número. Al seleccionar ENTRAR, el programa encuentra un error en tiempo de ejecución y se cierra. A diferencia de un error en tiempo de compilación que el compilador de Python puede detectar al intentar ejecutar el programa y corregirlo antes de distribuir el programa a los usuarios finales, el error de tiempo de ejecución se produce cuando los usuarios, sin ningún error por su parte, experimentan un error al utilizar el programa.

Idealmente, primero debe realizar una comprobación para asegurarse de que el valor que escriben los usuarios se puede convertir en un número antes de realizar realmente la conversión de datos. Si los usuarios no especificaron un número, podría omitir la entrada y pedirles que escriban un número. Por ahora, confirme que se trata de un posible problema con el programa. Puede solucionarlo después de obtener más información sobre Python.

### Paso 6: Revisar el código para mostrar una etiqueta delante del valor de suma

La siguiente tarea consiste en dar formato a la última línea de contenido para que indique claramente lo que representa el número `9`. Idealmente, ese número debería ir precedido por una etiqueta, como *Sum:*.

Actualice la última línea de código para que coincida con el siguiente ejemplo:

PythonCopiar

```python
print("Sum: " + sum)
```

¿Cree que funcionará? ¿Por qué o por qué no?

### Paso 7: Guardar y ejecutar el código

Guarde y ejecute el programa mediante una de las técnicas que aprendió anteriormente. Debería ver la siguiente salida:

ResultadosCopiar

```output
First Number:
5
Second Number:
4
Traceback (most recent call last):
  File "c:/python/hello/numbers.py", line 11, in <module>
    print("Sum: " + first_number + second_number)
TypeError: can only concatenate str (not "int") to str
```

Parece que el problema está relacionado con la concatenación de una *cadena* con un *int*.

El motivo por el que este código no funcionará es porque Python no convertirá implícitamente el primer_número en una cadena. Examina la cadena literal y, después, ve un `+`, por lo que espera otro valor de tipo cadena para poder realizar una concatenación. Cuando encuentra un entero, se interrumpe e informa de un error.

Para solucionar este error, primero debe realizar la operación de suma, convertir la suma de un entero a una cadena y, después, realizar la concatenación.

### Paso 8: Revisar el código para convertir el entero en cadena para la concatenación

Para corregir este problema, modifique la última línea de código para que coincida con el siguiente ejemplo:

PythonCopiar

```python
print("Sum: " + str(sum))
```

Aquí utiliza la función `str()` para convertir el valor de la variable de suma en una cadena. Después, puede realizar la concatenación de cadenas para que la suma tenga el formato correcto.

### Paso 9: Guardar y ejecutar el código

Guarde y ejecute el programa mediante una de las técnicas que aprendió anteriormente. Debería ver la siguiente salida:

ResultadosCopiar

```output
First Number:
5
Second Number:
4
Sum: 9
```

Terminado.

## Resumen

- Elija buenos nombres de variable que ayuden a la legibilidad del código.
- Opte por introducir variables temporales si ayudan a aumentar la legibilidad del código. Use la mejor resolución y optimice la legibilidad.
- Para realizar operaciones matemáticas en los datos, primero se deben convertir a un tipo de datos numérico. Si tiene un valor de cadena que representa un número entero y quiere realizar cálculos matemáticos, puede utilizar la función `int()` para convertir el valor en un entero.
- Si intenta utilizar `int()` para convertir una cadena en un entero, pero la cadena no es un valor que se pueda convertir, como un nombre, el usuario final experimentará un error en tiempo de ejecución. Los errores en tiempo de ejecución se producen cuando el programador no prevé problemas con los datos u otros posibles problemas de lógica de antemano.
- Cuando se usa con un tipo de datos numérico, el símbolo de signo más (**+**) realiza la suma.
- Puede llamar a una función y pasar su valor devuelto a otra función.
- Utilice la función `str()` para convertir un valor numérico en una cadena.

