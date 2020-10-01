# Iteración de bloques de código mediante la instrucción "while"

Use la instrucción `while` y construcciones de código de Python relacionadas para agregar lógica de bucle a sus programas.

## Learning Objectives

Objetivos de este módulo:

- Usar la instrucción `while` para recorrer en iteración un bloque de código.
- Usar las instrucciones `break`, `continue` y `else` para controlar mejor la iteración.
- Usar operadores de asignación alternativos para realizar operaciones matemáticas que también asignan valores.

## Requisitos previos

- Tener configurado un entorno de desarrollo de Python, saber crear una carpeta de trabajo y archivos de código, y saber cómo ejecutar el código en un archivo de código.
- Conocer tipos de datos como `str` y `int`, y saber cómo definir, establecer y obtener valores de una variable.
- Entender qué es un bloque de código y cómo definir uno.
- Saber cómo incluir un módulo desde la biblioteca estándar de Python.
- Experiencia en el uso de instrucciones "if" y del método auxiliar `isnumeric()` de cadena para evaluar los datos proporcionados por el usuario.

# Introducción

- 1 minuto

Además de ejecutar código ramificado, a menudo es necesario repetir la ejecución del código hasta que se cumpla una determinada condición. Este proceso se denomina iteración en la terminología de programación.

Supongamos que necesita solicitar una entrada a un usuario y le envía solicitudes hasta que escriba un valor que esté dentro de un intervalo aceptable. O supongamos que necesita leer todas las líneas de un archivo de datos hasta llegar al final de este. En estas situaciones, usará la instrucción `while`, que crea una estructura de bucle en el código. Con una instrucción `while`, se itera la ejecución del código hasta que se cumple una condición, momento en el que la ruta de ejecución continúa a través del resto del programa.

En este módulo, usará la instrucción `while` para recorrer en iteración un bloque de código. Agregará otras instrucciones como `break`, `continue` y `else` para controlar mejor el flujo de ejecución del código. Usará nuevos operadores de asignación para realizar operaciones matemáticas que también asignan el nuevo valor a la variable (un patrón frecuente en muchas instrucciones de bucle).

Al final de este módulo, podrá compilar programas que controlan el flujo de código con estructuras de bucle.

## Objetivos de aprendizaje

Objetivos de este módulo:

- Usar la instrucción `while` para recorrer en iteración un bloque de código.
- Usar las instrucciones `break`, `continue` y `else` para controlar mejor la iteración.
- Usar operadores de asignación alternativos para realizar operaciones matemáticas que también asignan valores.

## Requisitos previos

- Tener configurado un entorno de desarrollo de Python, saber crear una carpeta de trabajo y archivos de código, y saber cómo ejecutar el código en un archivo de código.
- Conocer tipos de datos como `str` y `int`, y saber cómo definir, establecer y obtener valores de una variable.
- Entender qué es un bloque de código y cómo definir uno.
- Saber cómo incluir un módulo desde la biblioteca estándar de Python.
- Tener experiencia en el uso de instrucciones "if" y del método auxiliar `isnumeric()` de la cadena para evaluar los datos proporcionados por el usuario.

# Ejercicio: La instrucción "while"

- 8 minutos

En este ejercicio, usaremos la instrucción `while` para compilar un juego sencillo que repetirá en bucle un bloque de código con la lógica de juego necesaria para generar y evaluar un valor aleatorio.

### Paso 1: Crear una carpeta de trabajo y un archivo de código de Python nuevos

Con las técnicas que ha aprendido en módulos anteriores, cree una carpeta nueva para su trabajo en este módulo. Por ejemplo, puede crear una carpeta denominada `python-while`.

Dentro de esa carpeta, cree un archivo para este ejercicio. Por ejemplo, puede crear un archivo denominado `exercise1.py`.

A la hora de ejecutar el código en los pasos de los ejercicios, puede seleccionar la flecha verde para usar la integración de Herramientas de Python para Visual Studio Code. También puede usar un comando en el terminal integrado mediante las técnicas que ha aprendido en módulos anteriores.

### Paso 2: Agregar código para recorrer en bucle un bloque de código mediante la instrucción "while"

Agregue la siguiente lista de código a su nuevo archivo:

PythonCopiar

```python
import random 

roll = 0
count = 0

while roll != 5:
  count = count + 1
  roll = random.randint(1, 5)
  print(roll)

print(f'It took {count} rolls to roll a 5!')
```

La instrucción `while` tiene tres partes:

- La palabra clave `while`.
- Una expresión booleana.
- Un símbolo de dos puntos `:` que indica el final de la instrucción.

También es importante el bloque de código que hay debajo de la instrucción `while`. Hemos explicado los bloques de código de otros módulos. Este bloque de código pertenece a la instrucción "while" y seguirá ejecutándose repetidamente hasta que la expresión booleana se evalúe como `False`.

En este caso, usamos la función `randint()` del módulo `random` para generar un número aleatorio entre 1 y 5. Usamos la variable `roll` para mantener el valor actual del número generado de forma aleatoria. Usamos la variable `count` para realizar un seguimiento del número de veces que se ha llamado a la función `randint()`.

Cada vez que se ejecuta el bloque de código, el valor de `roll` se establece en un nuevo número aleatorio comprendido entre 1 y 5. Una vez que se ejecuta la última línea del bloque de código, el intérprete de Python vuelve a comprobar la expresión booleana. Si el nuevo valor de `roll` aún no es `5`, el proceso se repite en bucle hasta que la expresión booleana se evalúa como `False`. En otras palabras, una vez que `roll` es igual a `5`, la expresión booleana se evalúa como `False`. La ruta de acceso de ejecución sale del bucle y continúa con el resto del programa.

Cada vez que se ejecuta el bloque de código, se incrementa el valor de `count` en `1`, por lo que sabemos cuántas veces se ha repetido en bucle nuestro código.

Al ejecutar el código, debería ver una salida similar a la siguiente:

ResultadosCopiar

```output
3
1
4
2
4
1
5
It took 8 rolls to roll a 5!
```

El uso de una instrucción `while` con el módulo `random` puede ser la base de muchos minijuegos. En el siguiente paso, vamos a compilar una versión ligeramente más interactiva.

### Paso 3: Usar las instrucciones opcionales "break" y "else"

En algunas situaciones, puede que quiera interrumpir la instrucción "while" prematuramente. Por ejemplo, quizás quiera solicitar información al usuario. Si este escribe un determinado carácter o término, es posible que usted quiera salir del bucle que evita el flujo normal.

Actualice el código del paso anterior para que coincida con la lista de códigos siguiente:

PythonCopiar

```python
import random 

roll = 0
count = 0

print('First person to roll a 5 wins!')
while roll != 5:
  
  name = input('Enter a name, or \'q\' to quit:  ' )
  if name == 'q':
    break
  
  count = count + 1
  roll = random.randint(1, 5)
  print(f'{name} rolled {roll}')
else:
    print(f'{name} Wins!!!')

print(f'You rolled the dice {count} times.')
```

En esta versión de nuestro minijuego, le pedimos al usuario que proporcione un nombre. Cada vez que se escribe un nuevo nombre, se genera un valor aleatorio, un "roll" (es decir, una tirada). La primera persona que obtenga un `5` gana.

Si el jugador sigue introduciendo nombres hasta que obtiene un `5`, la expresión booleana ya no se evalúa como `True`. Si pasa esto, la ruta de ejecución del código omite la instrucción `else` para imprimir el mensaje de que ha ganado.

Si ejecuta el código y escribe varios nombres, debería ver una salida similar a la siguiente:

ResultadosCopiar

```output
First person to roll a 5 wins!
Enter a name, or 'q' to quit:  Grant
Grant rolled 2
Enter a name, or 'q' to quit:  Charlee
Charlee rolled 5
Charlee Wins!!!
You rolled the dice 2 times.
```

Permitimos que el jugador salga del juego antes de tiempo si escribe la letra `q` en lugar de un nombre. Usamos una instrucción `if` para comprobar el valor que ha escrito el usuario. Si ha escrito `q`, se llama a la instrucción `break`.

La instrucción `break` indica al intérprete de Python que salga del bucle y continúe ejecutando el código que hay después del bloque de código de la instrucción `while`. En este caso, se omite la instrucción `else` y no hay ningún ganador.

Si ejecuta el código pero escribe la letra `q` en algún momento, verá una salida similar a la siguiente:

ResultadosCopiar

```output
First person to roll a 5 wins!
Enter a name, or 'q' to quit:  Bob
Bob rolled 4
Enter a name, or 'q' to quit:  Beth
Beth rolled 3
Enter a name, or 'q' to quit:  Conrad
Conrad rolled 1
Enter a name, or 'q' to quit:  q
You rolled the dice 3 times.
```

Tanto `break` como `else` son instrucciones opcionales en la estructura de bucle de la instrucción `while`.

### Paso 4: Actualizar el ejemplo de código para que incluya la instrucción "continue" y así controlar qué sucede cuando el usuario no introduce ningún valor

Vamos a ampliar el ejemplo anterior y a asegurarnos de que el jugador no pueda introducir una cadena vacía. En otras palabras, si el usuario selecciona Entrar sin pulsar ninguna otra tecla o simplemente selecciona la barra espaciadora, queremos omitir esa entrada y volver a pedirle al usuario que escriba un nombre.

PythonCopiar

```python
import random 

roll = 0
count = 0

print('First person to roll a 5 wins!')
while roll != 5:
  name = input('Enter a name, or \'q\' to quit:  ' )

  if name.strip() == '':
    continue

  if name.strip() == 'q':
      break
  
  count = count + 1
  roll = random.randint(1, 5)
  print(f'{name} rolled {roll}')
else:
    print(f'{name} Wins!!!')

print(f'You rolled the dice {count} times.')
```

En este caso, realizamos una comprobación controlada del valor que ha escrito el usuario. Después de quitar los espacios vacíos mediante el método auxiliar de cadena `strip()`, la variable `name` está vacía. A continuación, usamos la palabra clave `continue` para omitir el resto del bloque de código y volver a la parte superior, donde evaluaremos la expresión booleana y continuaremos recorriendo en bucle el bloque de código.

Mediante el uso de una comprobación controlada, podemos evitar la posibilidad de que nuestro programa cree tiradas cuando no haya ningún nombre.

Si ejecuta el código y selecciona la tecla Entrar varias veces sin escribir un nombre, debería ver una salida similar a la siguiente:

ResultadosCopiar

```output
First person to roll a 5 wins!
Enter a name, or 'q' to quit:  Adrian
Adrian rolled 2
Enter a name, or 'q' to quit:
Enter a name, or 'q' to quit:  
Enter a name, or 'q' to quit:  
Enter a name, or 'q' to quit:  Judy
Judy rolled 3
Enter a name, or 'q' to quit:  Ashley
Ashley rolled 5
Ashley Wins!!!
You rolled the dice 3 times.
```

## Resumen

- La instrucción `while` permite crear una estructura de bucle que recorre continuamente un bloque de código hasta que una expresión booleana se evalúa como `False`.
- Agregue la instrucción `break` para salir de un bloque de código prematuramente antes de que la expresión booleana se evalúe como `False`.
- Agregue la instrucción `else` para proporcionar un segundo bloque de código que se ejecutará después de que la expresión booleana de la instrucción `while` se evalúe como `False`.
- Agregue la instrucción `continue` para omitir el resto del bloque de código y volver a establecer la ruta de acceso de ejecución en la expresión booleana.

# Ejercicio: Operadores de asignación

- 4 minutos

Hemos usado el operador de asignación básico, un solo símbolo de signo igual `=`, a la hora de asignar un valor a nuestra primera variable. Hay otros operadores de asignación que también debe tener en cuenta.

Incrementar un valor en una estructura de bucle es una operación común. En este ejercicio, aprenderá a usar otros operadores de asignación que realizarán una operación matemática y asignarán un nuevo valor a una variable en un formato abreviado.

Más allá del incremento básico, hay varios operadores de asignación potencialmente útiles que puede usar en sus programas.

### Paso 1: Crear un nuevo archivo de código para este ejercicio

Suponiendo que continúa desde la unidad anterior, use las técnicas que ha aprendido en los módulos anteriores para agregar un nuevo archivo de código en la carpeta actual dedicada a este módulo. Por ejemplo, puede crear un archivo denominado `exercise2.py`.

### Paso 2: Agregar código para usar un operador de incremento y asignación

PythonCopiar

```python
count = 0
while count != 5:
    count += 1
    print(count)
```

Vamos a centrarnos en la primera línea de código del bloque: `count += 1`. El operador `+=` toma el valor actual de `count`, le suma `1` y, luego, asigna el nuevo valor a `count`. Es el equivalente de la siguiente línea de código:

PythonCopiar

```python
count = count + 1
```

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
1
2
3
4
5
```

### Paso 3: Marcar el código anterior como comentario y agregar código para incrementar el recuento en 3

Puede incrementar cualquier valor. Vamos a incrementar `count` en `3` hasta que `count` no sea `<= 20`.

Marque como comentario el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
count = 0
while count <= 20:
    count += 3
    print(count)
```

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
3
6
9
12
15
18
21
```

### Paso 4: Marcar el código anterior como comentario y agregar código para restar 3 al recuento

Puede usar el operador de asignación `-=` para restar un valor y, después, asignarlo a la variable. ¿Qué ocurre si queremos contar hacia atrás desde un número hasta llegar a `0`?

Marque como comentario el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
count = 20
while count >= 0:
    count -= 3
    print(count)
```

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
17
14
11
8
5
2
-1
```

### Otros operadores de asignación

Hay varios operadores de asignación adicionales, pero su funcionalidad podría resultar menos útil en programas reales. A continuación se muestra una tabla con algunos de los operadores de asignación adicionales que están disponibles en Python.

| Operador | Propósito                                        |
| :------- | :----------------------------------------------- |
| =        | Asignar                                          |
| +=       | Sumar y asignar                                  |
| -=       | Restar y asignar                                 |
| *=       | Multiplicar y asignar                            |
| /=       | Dividir y asignar                                |
| %=       | Obtener el módulo y asignar                      |
| **=      | Calcular la potencia y asignar                   |
| //=      | Dividir redondeando al entero inferior y asignar |

## Resumen

- Los nuevos operadores de asignación `+=` y `-=` pueden simplificar las operaciones de incremento y decremento.
- Hay muchos operadores de asignación adicionales en Python, pero puede que no sean tan útiles.

