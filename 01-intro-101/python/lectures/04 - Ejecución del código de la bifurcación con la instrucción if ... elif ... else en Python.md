# Ejecución del código de la bifurcación con la instrucción if ... elif ... else en Python

Use las expresiones booleanas de la instrucción If con operadores de comparación y lógica para expresar la lógica de decisión.

## Learning Objectives

Objetivos de este módulo:

- Utilizar las instrucciones `if ... elif ... else` para agregar la lógica de decisión al código Python.
- Comprender el tipo de datos booleano y lo que representa en Python.
- Crear expresiones booleanas mediante un amplio conjunto de operadores de comparación y lógica.



## Requisitos previos

- Debería tener el entorno de desarrollo de Python ya configurado y saber cómo crear, editar y ejecutar el código de Python almacenado en un archivo `.py`.
- Debería tener nociones del uso de funciones de entrada y salida, como `print()` e `input()`.
- Debería saber cómo crear y asignar valores a variables.

# Introducción

- 1 minuto

En el módulo anterior, aprendió que el intérprete de Python ejecuta secuencialmente cada línea de código en el archivo de código. Una vez que se ejecuta correctamente la última línea de código, el programa finaliza.

Una de las características más eficaces de cualquier lenguaje de programación es la posibilidad de crear una bifurcación de la ruta de acceso de la ejecución del código del programa en función de alguna decisión. El término *bifurcación* hace referencia a dos o más rutas de acceso independientes que el programa puede tomar. En lugar de una ruta de acceso secuencial, se crean rutas de acceso independientes que se ejecutan o se omiten en función de alguna condición que se cree. Por ejemplo, puede que quiera ejecutar cierto código que realiza una tarea importante si el usuario escribe el valor `y` o `yes` cuando se le solicite. En caso contrario, quiere que el intérprete de Python ignore ese código y, posiblemente, ejecute un código diferente.

En este módulo, aprenderá a usar la instrucción `if` y también las instrucciones `elif` y `else` para bifurcar la ruta de acceso de la ejecución del código de Python. Usará expresiones booleanas para crear condiciones que permitan al código evaluar los valores de las variables para ver si coinciden. Usará distintos operadores de comparación para aumentar la utilidad de las expresiones booleanas.

Al final de este módulo, podrá agregar lógica de decisión a su código de Python para que pueda crear aplicaciones más interesantes y complejas.

## Objetivos de aprendizaje

En este módulo, conseguirá lo siguiente:

- Utilizar las instrucciones `if ... elif ... else` para agregar la lógica de decisión al código Python.
- Comprender el tipo de datos booleano y lo que representa en Python.
- Crear expresiones booleanas mediante un amplio conjunto de operadores de comparación y lógica.

## Requisitos previos

- Debería tener el entorno de desarrollo de Python ya configurado y saber cómo crear, editar y ejecutar el código de Python almacenado en un archivo `.py`.
- Debería tener nociones del uso de funciones de entrada y salida, como `print()` e `input()`.
- Debería saber cómo crear y asignar valores a variables.

Si necesita revisar o aprender algunos de estos conceptos, visite los módulos anteriores de esta ruta de aprendizaje.



# Ejercicio: bifurcar código con la instrucción If

- 8 minutos

El uso de la instrucción `if ... elif ... else` es una parte fundamental de la compilación de prácticamente cualquier programa válido. Puede utilizarlo para automatizar la lógica de decisiones complicada, de modo que se pueda aplicar de forma repetida y coherente a los datos o la entrada del usuario.

Cuando se usa el término *lógica del código* o *lógica de decisión*, se hace referencia a la capacidad de conferir al programa la posibilidad de tomar una decisión basada en las entradas. En función de la decisión, se puede indicar al intérprete de Python que ejecute un código y omita otro.

En este ejercicio, se usará la instrucción `if`, junto con las instrucciones opcionales `elif` y `else`, para bifurcar la ejecución del código en función de una expresión booleana.

Una *expresión booleana* es cualquier código que devuelve un *valor booleano*. Un valor booleano puede ser `True` o `False` y es su propio tipo de datos en Python, al igual que `str` y `int`.

En este ejercicio, se utilizará una expresión booleana para evaluar si dos valores son iguales. En la unidad siguiente, ser verá cómo crear expresiones booleanas más expresivas y trabajar con funciones que devuelven un valor booleano.

Se comenzará con un ejemplo sencillo de una instrucción `if`.

### Paso 1: Crear una carpeta de trabajo y un archivo de código de Python nuevos

Con las técnicas que aprendió en los módulos anteriores, cree una nueva carpeta para su trabajo en este módulo. Por ejemplo, puede crear una carpeta denominada `python-if`.

Dentro de esa carpeta, cree un archivo para este ejercicio. Por ejemplo, puede crear un archivo denominado `exercise1.py`.

A la hora de ejecutar el código, puede usar las herramientas de Python para la integración con Visual Studio Code seleccionando la flecha verde. También puede usar un comando en el terminal integrado mediante las técnicas que ha aprendido en módulos anteriores.

### Paso 2: Agregar una instrucción `if` al nuevo archivo de código

Agregue el siguiente código a la función:

PythonCopiar

```python
value = '7'

if value == '7':
    print('The value is 7')

print('Finished!')
```

Una instrucción `if` se compone de tres partes:

- La palabra clave `if`.
- La expresión booleana `value == '7'`.
- El carácter de dos puntos `:` requerido.

Lo que viene a continuación es igual de importante. La línea siguiente debe contener un bloque de código que se ejecuta si la expresión booleana se evalúa como `True`. En Python, un bloque de código se define mediante el uso de la sangría. En este caso, usamos la tecla Pestaña para insertar cuatro espacios individuales. Esta sangría indica al intérprete de Python que este código *pertenece a* la instrucción `if` y debe ejecutarse cuando la expresión booleana se evalúa como `True`.



Si la expresión booleana se evalúa como `False`, el intérprete de Python debe omitir todo el código con sangría.

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
The value is 7
Finished!
```

Para ver cómo funciona este código cuando la expresión booleana se evalúa como `False`, modifique el valor de la primera línea de código `value` a la cadena `'6'`.

PythonCopiar

```python
value = '6'
```

Cuando ejecute el código, verá la salida siguiente:

ResultadosCopiar

```output
Finished!
```

La línea de código que se encuentra debajo de la instrucción `if` se omite porque la expresión booleana se evalúa como `False`. La última línea de código que imprime el término `Finished` se ejecuta porque no tiene una sangría debajo de la instrucción `if`.

### Paso 3: Agregar un carácter de tabulación a la última línea de código para comprender la importancia de la sangría

Ahora verá lo que sucede cuando se agrega sangría a la última línea de código.

Modifique la última línea de código agregando una tabulación delante de la línea. El código debería coincidir con la salida siguiente:

PythonCopiar

```python
value = '6'

if value == '7':
    print('The value is 7')

    print('Finished!')
```

Al ejecutar el código esta vez, no hay ninguna salida. Esto se debe a que la última línea de código ahora forma parte del mismo bloque de código que pertenece a la instrucción `if`.

La sangría define un bloque de código en Python. Un bloque de código consta de una o varias líneas de código que se tratan como una unidad de trabajo. El bloque de código solo se ejecuta en función de la instrucción anterior, que, en este caso, es la instrucción `if`. Con frecuencia se tratarán los bloques de código en Python, a medida que vaya aprendiendo sobre nuevas construcciones, como bucles, funciones, clases, etc.

Python es exigente cuando se trata de las sangrías. Se debe aplicar sangría a todas las líneas en el mismo nivel. Si no es así, Python mostrará una excepción al ejecutar el código. Si quita un solo carácter de espacio vacío antes de la última línea de código:

PythonCopiar

```python
value = '6'

if value == '7':
    print('The value is 7')

   print('Finished!')
```

Y luego intenta volver a ejecutar el código; verá el siguiente error:

ResultadosCopiar

```output
  File "exercise1.py", line 6
    print('Finished!')
                     ^
IndentationError: unindent does not match any outer indentation level
```

### Paso 4: Actualizar el ejemplo de código para incluir una instrucción `else`

La instrucción `else` es una parte opcional de una instrucción `if` que puede controlar el caso contrario. En otras palabras, cuando la expresión booleana de la instrucción `if` se evalúa como `False`, ejecute en su lugar el bloque de código que pertenece a la instrucción `else`.

Modifique su código para que coincida con el fragmento de código siguiente: Además de agregar la instrucción `else`, observe que se ha quitado la pestaña de la última línea de código.

PythonCopiar

```python
value = '6'

if value == '7':
    print('The value is 7')
else:
    print('The value is not 7') 

print('Finished!')
```

Si ejecuta el código, verá la salida siguiente:

ResultadosCopiar

```output
The value is not 7
Finished!
```

Una instrucción `else` se compone de dos partes:

- La palabra clave `else`.
- El símbolo de teclado de dos puntos `:`.

Al igual que antes, el bloque de código que sigue a la instrucción `else` tiene la misma importancia. Todas las líneas de código con sangría debajo de la instrucción `else` pasan a formar parte de su bloque de código y se ejecutan con la expresión booleana si la instrucción `if` se evalúa como `False`.

### Paso 5: Actualizar el ejemplo de código para incluir una instrucción `elif`

La instrucción `elif`, o en su lugar, *else if* es otra instrucción opcional que se puede agregar bajo una instrucción `if`. Use la instrucción `elif` para probar otra expresión booleana relacionada. Si la expresión booleana se evalúa como `True`, se ejecuta el código con sangría que se encuentra debajo. Se omiten todos los bloques de código que pertenecen a otras instrucciones `if`, `elif` y `else`.

Modifique el ejemplo de código para que coincida con la lista de código siguiente:

PythonCopiar

```python
value = '8'

if value == '7':
    print('The value is 7')
elif value == '8':
    print('The value is 8')
else:
    print('The value is not one we''re looking for')

print('Finished!')
```

Al igual que la instrucción `if`, una instrucción `elif` se compone de tres partes:

- Debe comenzar con la palabra clave `elif`.
- Debe incluir una expresión booleana.
- Debe finalizar con un símbolo del teclado de dos puntos `:`.

Y, al igual que antes, todo el código con sangría debajo de la instrucción `elif` forma parte del bloque de código que se ejecuta si la expresión booleana se evalúa como `True`.

Cuando ejecute el código, verá la salida siguiente:

ResultadosCopiar

```output
The value is 8
```

Puede usar tantas instrucciones `elif` como necesite. Si utiliza una instrucción `else`, debe aparecer después de todas las instrucciones `elif`.

Modifique el código para que incluya una instrucción `elif` adicional antes de la instrucción `else`.

PythonCopiar

```python
value = '8'

if value == '7':
    print('The value is 7')
elif value == '8':
    print('The value is 8')
elif value == '9':
    print('The value is 9')
else:
    print('The value is not one we''re looking for')
```

Después de que cualquier expresión booleana `if` o `elif` se evalúe como `True`, el intérprete de Python no seguirá evaluando expresiones booleanas adicionales. Sale de la estructura `if ... elif ... else` completa y continúa procesando la siguiente línea de código que no tiene sangría.

### Tenga en cuenta las expresiones booleanas superpuestas.

Tenga en cuenta el código siguiente:

PythonCopiar

```python
value = '6'

if value < '8':
    print('The value is less than 8')
elif value < '7':
    print('The value is less than 7')
else:
    print('The value is greater than 8')
```

En primer lugar, se ha introducido un nuevo operador, del que se obtendrá más información en la siguiente unidad. El operador menor que `<` compara dos valores numéricos. Si el valor de la izquierda es menor que el de la derecha, la expresión se evalúa como `True`. En caso contrario, se evalúa como `False`.

¿Puede identificar el problema con las instrucciones `if` y `elif`? Fíjese bien y piense cómo funcionará este código.

El problema es que la instrucción `elif` no se llegará a ejecutar porque cualquier `value` que sea `True` para la instrucción `if` también será `True` para la instrucción `elif`. Como resultado, la ruta de acceso de ejecución nunca llegará a la instrucción `elif`.

Probablemente, este escenario nunca se manifestará como error en tiempo de ejecución. Si se esperase administrarlas de forma diferente, se habría introducido un error de lógica sutil en la aplicación. Es necesario intercambiar las expresiones booleanas entre `if` y `elif` para corregir el problema. Siempre resulta útil probar la aplicación con varias entradas para asegurarse de que obtiene el resultado previsto.

### Bloques de código `if` anidados

Tenga en cuenta el siguiente código de ejemplo:

PythonCopiar

```python
first_value = True
second_value = '6'

if first_value:
    if second_value == '6':
        print('Got here!')
```

Aquí se evalúan dos valores de datos independientes. En primer lugar, se prueba el valor de `first_value`. Dado que una expresión booleana es cualquier código que es `True` y `first_value` es igual a `True`, no es necesario escribir toda la expresión booleana como tal:

PythonCopiar

```Python
if first_value == True:
```

En segundo lugar, y más pertinente para este ejemplo de código, es el anidamiento de la segunda instrucción `if` dentro del bloque de código de la primera instrucción `if`. Como resultado, la segunda instrucción `if` solo se evalúa cuando la primera instrucción `if` se evalúa como `True`.

Esta estructura de anidamiento es habitual cuando se necesitan robar varios valores de datos relacionados (pero distintos) antes de realizar una operación.

Si quita la sangría adecuada:

PythonCopiar

```python
first_value = True
second_value = '6'

if first_value:
if second_value == '6':
    print('Got here!')
```

... es probable que vea el siguiente mensaje de error:

ResultadosCopiar

```output
  File "c:/python/numeric-operations-decisions/exercise2.py", line 65
    if second_value == '6':
    ^
IndentationError: expected an indented block
```

## Resumen

En esta unidad se han visto algunas ideas fundamentales:

- Use la instrucción `if` para evaluar una expresión booleana. Si la expresión se evalúa como `True`, el bloque de código debajo de la instrucción `if` lo ejecuta el intérprete de Python. De lo contrario, se omite.
- Un bloque de código es una o varias líneas de código con sangría. El bloque de código *pertenece a* la instrucción `if` y se ejecuta o se omite en función de la evaluación de la expresión booleana. Si, por accidente, se aplica (o se deja de aplicar) sangría a líneas de código, afectará sin duda a cómo funciona el mismo y podrían incluso producirse errores. Todas las sangrías deben usar el mismo número de caracteres de espacio o el intérprete de Python producirá un error.
- Agregue una instrucción `else` opcional si quiere ejecutar código que solo es relevante si la expresión booleana se evalúa como `False`. De lo contrario, se omite.
- Agregue una instrucción `elif` opcional después de la instrucción `if` (pero antes de la instrucción `else`, si existe) para evaluar una segunda expresión booleana posterior. Al igual que la instrucción `if`, el bloque de código con sangría de debajo se ejecuta si la expresión booleana se evalúa como `True`. De lo contrario, se omite.
- Cuando se usa la instrucción `if` junto con una o varias instrucciones `elif` y la instrucción `else`, una vez que se cumple una expresión booleana, ya no se evalúan más instrucciones. Como resultado, el orden en que se realizan las evaluaciones puede ser importante.
- Puede anidar instrucciones `if` si necesita comprobar las condiciones relacionadas (pero distintas) antes de realizar alguna operación.

# Ejercicio: expresiones booleanas

- 7 minutos

Como se ha visto en la unidad anterior, un valor booleano solo puede ser uno de dos valores, ya sea `True` o `False`. El tipo de datos booleano es la base de las expresiones booleanas. A su vez, las expresiones booleanas son la base de gran parte del código que escribirá en Python para comparar, evaluar y agregar lógica de bifurcación y de bucle a sus aplicaciones.

Una expresión booleana es cualquier código que devuelve un valor booleano.

En este ejercicio, trabajará con valores booleanos y expresiones booleanas. Proporcionan un lenguaje más completo para expresar la lógica.

### Paso 1: Crear un nuevo archivo de código de Python

Cree un nuevo archivo de código para este ejercicio. Por ejemplo, puede crear un archivo denominado `exercise2.py`.

### Paso 2: Agregar código para mostrar los tipos de datos de un valor de cadena, entero y booleano

Python tiene muchos tipos de datos diferentes. En el módulo anterior, trabajó con un tipo de datos de cadena y un tipo de datos numéricos denominado *entero*. Puede usar una función integrada llamada `type()` para mostrar el tipo de datos de cualquier valor. Esta función puede ayudarle a entender el tipo de datos con los que está trabajando y lo que puede hacer con ellos.

Para comprender mejor la naturaleza de los valores booleanos, agregue las siguientes líneas de código al nuevo archivo de código.

PythonCopiar

```python
print(type('Hello world'))
print(type(7))

print(type(True))
print(type(False))

print(type('True'))
print(type('False'))
```

Las dos primeras líneas de código muestran lo que se espera de una cadena y un entero, respectivamente. El método `type()` indica que estos valores son instancias de una clase denominada `str` e `int`. Más adelante hablaremos sobre las clases y las instancias. Por ahora, puede considerar estos valores como clasificaciones de datos. En función de la clasificación, puede realizar distintas tareas, ya sean concatenaciones de cadenas o aritméticas.

Las dos líneas de código siguientes muestran el tipo de datos booleano `bool`. Observe que los valores `True` y `False` deben escribirse en mayúsculas y no son valores de cadena.

Las dos líneas finales de código muestran que hay una diferencia entre los valores booleanos `True` y `False`, y los valores de cadena `'True'` y `'False'`.

Ejecute el archivo de código. Debería ver la siguiente salida:

ResultadosCopiar

```output
<class 'str'>
<class 'int'>
<class 'bool'>
<class 'bool'>
<class 'str'>
<class 'str'>
```

### Paso 3: Comentar el código del paso anterior y, después, agregar el código que usa la función integrada `bool()` para convertir varios valores de cadena en valores booleanos

La función `bool()` funciona de forma similar a las funciones `str()` y `int()` que ha visto en el módulo anterior. La función acepta cualquier valor e intenta convertirlo en un valor booleano.

A veces, el resultado es predecible. Otras veces podría no resultar evidente lo que está ocurriendo.

Comente todo el código anterior del archivo de código. Después, agregue el código siguiente que imprime el resultado de usar la función `bool()` para convertir valores diferentes en un valor booleano.

PythonCopiar

```python
print(bool('True'))
print(bool('False'))
print(bool(''))
print(bool(' '))
print(bool('Hello world!'))
```

Si ejecuta el código, verá la salida siguiente:

ResultadosCopiar

```output
True
True
False
True
True
```

La función `bool()` convirtió las cadenas `'True'` y `'False'` a los valores booleanos `True` y `False`. Cuando se proporciona la función con una cadena vacía, devuelve `False`, mientras que cualquier otra cadena que no esté vacía devuelve `True`.

### Paso 4: Comentar el código del paso anterior y, después, agregar el código que usa la función integrada `bool()` para convertir varios valores de enteros en valores booleanos

Comente todo el código anterior del archivo de código. Después, agregue el código siguiente que imprime el resultado de usar la función `bool()` para convertir valores diferentes en un valor booleano.

PythonCopiar

```python
print(bool(7))
print(bool(1))
print(bool(0))
print(bool(-1))
```

Si ejecuta el código, verá la salida siguiente:

ResultadosCopiar

```output
True
True
False
True
```

La función `bool()` convierte cualquier valor distinto de cero en `True`, pero convierte el valor `0` en `False`.

## ¿Qué es una expresión booleana?

A medida que se agregue lógica a las aplicaciones, se evaluarán las expresiones booleanas. Un ejemplo sencillo ilustra la idea principal.

```
1 + 1 = 3
```

Se trata de una instrucción `False`. Pero:

```
1 + 1 = 2
```

... es una instrucción `True`. En estos dos ejemplos sencillos, se está evaluando la expresión completa para ver si es true o false.

En Python, una expresión booleana hace lo mismo. Una expresión booleana amplía esta idea a cualquier llamada de función que, en última instancia, devuelve `True` o `False`.

En Python, se usa el *operador de igualdad* `==` para crear una expresión booleana que evalúe dos valores para determinar si son iguales. El operador de igualdad utiliza dos símbolos de signo igual.

### Paso 5: Comentar el código del paso anterior y, después, agregar código para imprimir el resultado de las expresiones booleanas

Comente todo el código anterior del archivo de código. Después, agregue el código siguiente que imprime el resultado de dos expresiones booleanas.

PythonCopiar

```Python
print(1 + 1 == 3)
print(1 + 1 == 2)
```

Si agrega este código al archivo de código y lo ejecuta, verá el siguiente resultado:

OutputCopiar

```Output
False
True
```

Si Python es el primer lenguaje de programación que usa, es probable que se olvide de usar dos símbolos de signo igual cuando quiere comprobar la igualdad. El *operador de asignación* es un único signo igual. Se usa para asignar un valor a una variable. Si olvida e intenta usar un único signo igual en un contexto que no es el adecuado, Python genera un error y una sugerencia útil.

PythonCopiar

```python
print(1 + 1 = 3)
print(1 + 1 = 2)
```

Si agrega este código al archivo de código y lo ejecuta, verá el siguiente resultado:

ResultadosCopiar

```output
SyntaxError: expression cannot contain assignment, perhaps you meant "=="?
```

### ¿Qué es un operador?

Un operador es como una minifunción. Los operadores realizan una operación en operandos, que podrían ser valores literales, valores de variables o cualquier identificador como un método o una clase. Hay docenas de operadores en Python. Se pueden dividir en una de estas categorías:

- Operadores aritméticos
- Operadores de asignación
- Operadores bit a bit
- Operadores de comparación
- Operadores de identidad
- Operadores lógicos
- Operadores de pertenencia

En esta unidad se verán los operadores de comparación y lógicos. Probablemente se irán tratando la mayoría de los operadores a medida que continúe con esta ruta de aprendizaje.

Algunos operadores constan de un solo símbolo, como muchos de los operadores que se usarán en esta unidad. Operan sobre los valores a su izquierda y a su derecha. Otros operadores constan de un par de símbolos. Operan sobre los valores entre su símbolo de apertura y su símbolo de cierre.

## Operadores de comparación

El operador de igualdad `==` es una de las familias de operadores que puede usar para comparar dos valores. En la tabla siguiente no se muestran todos los operadores posibles. Estos son los operadores de comparación que probablemente usará con más frecuencia.

| Operador | Descripción                |
| :------- | :------------------------- |
| `==`     | Operador de igualdad       |
| `!=`     | Operador de desigualdad    |
| `>`      | Operador mayor que         |
| `<`      | Operador menor que         |
| `>=`     | Operador mayor o igual que |
| `<=`     | Operador menor o igual que |

El operador de desigualdad `!=` se evalúa como `True` cuando los operandos de sus lados no son los mismos. Este concepto puede ser un poco confuso, pero a veces quiere asegurarse de que dos valores no son iguales.

### Paso 6: Comentar el código del paso anterior y, después, agregar código para imprimir el resultado de las expresiones booleanas

Para ejercitar estos operadores de comparación, comente el código del archivo de código y agregue el código siguiente:

PythonCopiar

```python
print(3 == 4)
print(3 != 4)

print(3 > 4)
print(3 < 4)
print(3 >= 4)
print(3 <= 4)
```

La ejecución de este código proporciona la salida siguiente:

ResultadosCopiar

```output
False
True
False
True
False
True
```

## Operadores lógicos

A veces, querrá evaluar más de una expresión booleana. En este caso, puede usar los operadores lógicos `and`, `or` y `not`. Estos operadores permiten emparejar dos expresiones booleanas juntas para generar un valor booleano final.

Utilice el operador `and` para asegurarse de que ambas expresiones booleanas se evalúen como `True`. Utilice el operador `or` para asegurarse de que al menos una de las expresiones booleanas se evalúa como `True`.

El operador `not` devuelve el valor booleano opuesto. Se puede utilizar para asegurarse de que una o varias expresiones booleanas se evalúan como `False`.

### Paso 7: Comentar el código del paso anterior y, después, agregar código para imprimir el resultado de las expresiones booleanas

Para ejercitar estos operadores lógicos, comente el código del archivo de código y agregue el código siguiente:

PythonCopiar

```python
first_number = 5
second_number = 0
true_value = True
false_value = False

if first_number > 1 and first_number < 10:
    print('The value is between 1 and 10.')

if first_number > 1 or second_number < 1:
    print('At least one value is greater than 1')

print(not true_value)
print(not false_value)

if not first_number > 1 and second_number < 10:
    print('Both values pass the test')
else:
    print('Both values do NOT pass the test')
```

La ejecución de este código proporciona la salida siguiente:

ResultadosCopiar

```output
The value is between 1 and 10.
At least one value is greater than 1
False
True
Both values do NOT pass the test
```

## Resumen

- Utilice la función `bool()` para convertir cadenas y enteros en valores booleanos. Las cadenas no vacías se convierten en `True` y los números distintos de cero se convierten en `True`. El valor de cadena `'False'` y las cadenas vacías se convierten en `False`. El valor `0` se convierte en `False`.
- Python proporciona varios operadores de comparación para comprobar la igualdad, la desigualdad y mayor o menor que.
- Python también proporciona varios operadores lógicos para asegurarse de que una o ambas expresiones booleanas son `True`. También proporciona el operador `not` para asegurarse de que las expresiones booleanas se evalúan como `False`.
