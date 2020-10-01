Aprenda a usar listas para administrar una colección de datos. Use las funciones auxiliares para manipular la lista. Use la instrucción for para recorrer en iteración la lista.

## Learning Objectives

En este módulo, aprenderá a:

- Crear listas de datos relacionados.
- Obtener un elemento o un subconjunto de elementos de una lista mediante índices y segmentos.
- Agregar y eliminar elementos de una lista.
- Usar las funciones auxiliares para otras acciones relacionadas con las listas.
- Recorrer en iteración una lista mediante la instrucción de iteración `for`.

## Requisitos previos

- Una configuración de desarrollo de Python local en la que pueda crear una carpeta de trabajo para el código, agregar archivos de código y ejecutarlos desde la línea de comandos o desde el editor de código.
- Experiencia con el trabajo con variables, tipos de datos como `str` y `int`, etc.
- Conocimiento de la importación del módulo de `random` y de la llamada a funciones como `randint()` desde el módulo.

# Introducción

- 1 minuto

A menudo, al compilar programas en Python, debe trabajar con un conjunto completo de datos, no solo un elemento. En Python, puede trabajar con una colección de datos de varias maneras. Una de las formas más sencillas y versátiles es una lista. Cuando la colección de datos se encuentra en una lista, puede acceder a un elemento individual o a un subconjunto de elementos, ordenar la lista e invertir su orden, recorrer en iteración los elementos, etc.

Supongamos que necesita llevar un seguimiento de los mensajes y de la salida numérica que genera otro sistema de software. Le interesa examinar cada uno de los valores, filtrar algunos de ellos, guardar otros, etc. En este caso, puede administrar todos los datos en una estructura de lista.

En este módulo, creará e inicializará los valores de una lista. Accederá a los elementos individuales y a subconjuntos completos de valores de la lista. Llamará a funciones auxiliares para realizar operaciones como agregar, quitar u ordenar elementos. Por último, usará la instrucción `for` para recorrer en iteración la lista y operar en cada elemento de ella.

Al final de este módulo, podrá controlar los datos que almacene en una lista.

## Objetivos de aprendizaje

En este módulo, aprenderá a:

- Crear listas que contengan datos relacionados.
- Usar índices y segmentos para obtener un elemento o un subconjunto de elementos de la lista.
- Usar funciones auxiliares para agregar y quitar elementos de la lista y realizar otras acciones relacionadas con la lista.
- Recorrer en iteración la lista con la instrucción `for`.

## Requisitos previos

- Una configuración de desarrollo de Python local en la que pueda crear una carpeta de trabajo para el código, agregar archivos de código y ejecutarlos desde la línea de comandos o desde el editor de código.
- Experiencia con tipos de datos como `str` y `int`, variables, etc.
- Conocimiento de la importación del módulo de `random` y de la llamada a funciones del módulo, como `randint()`.

# Ejercicio: trabajo con listas de datos

- 10 minutos

Las listas permiten recopilar datos en una única estructura. Los elementos de la lista pueden ser de cualquier tipo de datos. Mediante el uso de una lista, puede hacer lo siguiente:

- Agregar y quitar elementos de varias maneras.
- Hacer referencia a elementos individuales o a segmentos de elementos (sublistas).
- Recorrer en bucle cada elemento de una lista, como verá en la unidad siguiente.

Las listas son una manera popular de administrar datos relacionados en las aplicaciones.

En este ejercicio, trabajará con listas de datos. En otros módulos, exploraremos estructuras de datos similares, como el conjunto, el diccionario, la tupla y el intervalo.

## Paso 1: creación de una carpeta de trabajo y un archivo de código de Python

Con las técnicas que aprendió en los módulos anteriores, cree una carpeta para su trabajo en este módulo. Por ejemplo, puede crear una carpeta denominada *python-lists*.

Dentro de esa carpeta, cree un archivo para este ejercicio. Por ejemplo, puede crear un archivo denominado *exercise1.py*.

Para ejecutar el código de los ejercicios, puede usar las herramientas de Python para la integración con Visual Studio Code si selecciona la flecha verde. También puede usar un comando en el terminal integrado mediante las técnicas que ha aprendido en módulos anteriores.

## Paso 2: creación de una lista de valores

Escriba código para crear una lista de colores. Después, imprima la lista y su tipo en la consola. Agregue el código de la lista siguiente al nuevo archivo del ejercicio:

PythonCopiar

```python
colors = ['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown']

print(colors)
print(type(colors))
```

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown']
<class 'list'>
```

Para definir una lista, se usa un conjunto de corchetes (`[]`). Dentro de los corchetes, se agregan valores separados con comas.

La referencia a todos los elementos de la lista es un identificador único. En este caso, el identificador es la variable `colors`. Más adelante en este ejercicio descubrirá la manera de recuperar, agregar y quitar elementos.

Es importante entender que puede agregar valores de cualquier tipo de datos a una lista. En la lista de código siguiente, se agrega un valor de tipo cadena, float, entero y booleano en una única lista.

PythonCopiar

```python
sundry = ['John', 3.14, 7, False]
print(sundry)
print(type(sundry))
```

Si ejecuta el código, la salida será la esperada: los valores de la lista no cambiarán y el tipo de datos seguirá siendo `list`. Esta es la salida:

ResultadosCopiar

```output
['John', 3.14, 7, False]
<class 'list'>
```

Es posible agregar muchos tipos de datos a una lista, pero normalmente no es preferible ni práctico. Cuando compile programas reales, por lo general le interesará que los elementos de la lista compartan un propósito o un uso. Por esta razón, usará la lista `colors` para este ejercicio.

Puede crear una lista vacía como la siguiente:

PythonCopiar

```python
my_list = []
```

Es útil crear una lista vacía cuando no se puede inicializar la lista con valores. Para agregar elementos, debe usar la lógica del programa. Verá cómo usar este método más adelante en este ejercicio.

## Paso 3: uso de un índice para acceder a elementos individuales

En primer lugar, comente las dos últimas líneas de código que imprimen el contenido de la lista `colors`. Comente también la línea de código que imprime el elemento `type()` de la lista `colors`.

Después, agregue tres líneas de código que usen un conjunto de corchetes para acceder a los elementos individuales de la lista `colors`. Actualice el código para que coincida con esta lista de código:

PythonCopiar

```python
colors = ['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown']

# print(colors)
# print(type(colors))

print(f'0-based indexing into the list ... second item: {colors[1]}')

print(f'Last item of the list: {colors[-1]}')

print(f'Next to last item in the list: {colors[-2]}')
```

En este contexto, los corchetes nos permiten usar un valor numérico basado en cero para acceder a un elemento de la lista. Por lo tanto, cuando usemos el índice `[0]`, accederemos al primer elemento; cuando usemos el índice `[1]`, accederemos al segundo, y así sucesivamente.

También podemos usar números negativos como índices para contar hacia atrás desde el final de la lista. Así pues, cuando usemos el índice `[-1]`, accederemos al último elemento; cuando usemos el índice `[-2]`, accederemos al penúltimo elemento, y así sucesivamente.

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
0-based indexing into the list ... second item: green
Last item of the list: brown
Next to last item in the list: purple
```

Este es un intento de acceder a un elemento mediante el uso de un índice que no existe en la lista:

PythonCopiar

```python
colors = ['red', 'green', 'blue']
print(colors[3])
```

Este intento produce un error:

ResultadosCopiar

```output
IndexError: list index out of range
```

## Paso 4: creación de un segmento

Un *segmento* define un intervalo de elementos mediante una sintaxis especial. A primera vista, es similar a la sintaxis que usa un índice para acceder a un único elemento de la lista. La diferencia es que la sintaxis del segmento usa un signo de dos puntos (`:`), que separa el principio del segmento, a la izquierda, y el final del segmento, a la derecha.

Comente el código que agregó en el paso anterior y, después, agregue código nuevo que imprima varios segmentos de ejemplo.

PythonCopiar

```python
colors = ['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown']

# print(f'0-based indexing into the list ... second item: {colors[1]}')

# print(f'Last item of the list: {colors[-1]}')

# print(f'Next to last item in the list: {colors[-2]}')

print('\nPrint a SLICE, starting at index 2 and excluding index 5:')
print(colors[2:5])
print(type(colors[2:5]))

print('\nPrint a slice, starting at index 0 to index 3:')
print(colors[:3])

print('\nPrint a slice, starting a index 4 to the end of the list:')
print(colors[4:])

print('\nPrint a slice, from the 4th from the end up until the last item:')
print(colors[-4:-1])
```

Como hemos visto en la primera instrucción `print()`, el valor a la izquierda de los dos puntos es *inclusivo*. Por lo tanto, el segmento incluye el elemento en el índice. El valor a la derecha de los dos puntos es *exclusivo*. Por lo tanto, el segmento no incluye el elemento en el índice.

Si no define un índice a la izquierda del signo de dos puntos, el segmento comenzará al principio de la lista. Si no define un índice a la derecha del signo de dos puntos, el segmento continuará hasta el final de la lista.

Como puede ver en el último ejemplo, puede usar valores negativos. Los valores negativos permiten trabajar desde el final de la lista. El uso de este método puede ser un poco abrumador al principio, pero tenga en cuenta que se aplican las reglas que ya ha aprendido. Si define el segmento como `[-4:-1]`, contendrá los últimos cuatro elementos de la lista.

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
Print a SLICE, starting at index 2 and excluding index 5:
['blue', 'yellow', 'orange']
<class 'list'>

Print a slice, starting at index 0 to index 3:
['red', 'green', 'blue']

Print a slice, starting a index 4 to the end of the list:
['orange', 'purple', 'brown']

Print a slice, from the 4th from the end up until the last item:
['yellow', 'orange', 'purple']
```

## Paso 5: inversión y ordenación de la lista

Al igual que otros tipos de datos con los que hemos trabajado en módulos anteriores, las listas tienen varias funciones auxiliares. Dichas funciones le ayudarán a realizar ciertas operaciones en la lista.

Comente el código que agregó en la sección anterior. Después, agregue el código siguiente para invertir el orden de la lista y ordenarla alfabéticamente.

PythonCopiar

```python
colors.reverse()
print(colors)

colors.sort()
print(colors)
```

La llamada a estas funciones cambia de forma permanente el orden en el que los elementos de la lista se almacenan en la memoria.

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
['brown', 'purple', 'orange', 'yellow', 'blue', 'green', 'red']
['blue', 'brown', 'green', 'orange', 'purple', 'red', 'yellow']
```

## Paso 6: tratamiento de la lista como una cola

Una *cola* es un término especial en programación que hace referencia a una lista que almacena los elementos en el orden en el que se han agregado. Las colas son útiles cuando es necesario realizar lógica de cálculo en muchos elementos en un orden específico. Después de agregar elementos a la lista, quítelos para procesarlos uno a uno.

Una operación *pop* quita un elemento de la cola para su procesamiento. Puede quitar un elemento del principio de la lista ("primero en entrar, primero en salir", o FIFO). También puede quitar un elemento del final de la lista ("último en entrar, primero en salir", o LIFO).

La función auxiliar `pop()` permite seleccionar un elemento de la lista mediante su índice. El primer elemento es `0` y el último elemento, `-1`.

Comente el código que agregó en la sección anterior. Después, agregue el siguiente código:

PythonCopiar

```python
print(colors)

color = colors.pop(0)
print('popped', color)

print(colors)
```

La función auxiliar `pop()` toma el elemento del índice que se pasa como argumento. Lo quita de la lista y lo asigna a una variable para su procesamiento. En este caso, no haremos ningún procesamiento real en el elemento, sino que simplemente lo imprimiremos. La tercera línea de código imprime el nuevo contenido de la lista. Puede ver que el primer elemento ya no está presente.

ResultadosCopiar

```output
['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown']
popped red
['green', 'blue', 'yellow', 'orange', 'purple', 'brown']
```

## Paso 6: adición y eliminación de elementos de una lista

Si solo necesita administrar los elementos de la lista, puede usar las funciones auxiliares `append()` y `remove()`.

Comente el código que agregó en la sección anterior. Después, agregue el siguiente código:

PythonCopiar

```python
print(colors)

colors.append('black')
colors.append('white')

colors.remove('yellow')
colors.remove('orange')

print(colors)
```

La función auxiliar `append()` agrega un elemento a la lista. La función auxiliar `remove()` quita un elemento de la lista.

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown']
['red', 'green', 'blue', 'purple', 'brown', 'black', 'white']
```

Aquí intentaremos quitar un elemento que no existe en la lista:

PythonCopiar

```python
colors.remove('whatever')
```

Este código produce el error siguiente:

ResultadosCopiar

```output
ValueError: list.remove(x): x not in list
```

## Paso 7: combinación de una lista nueva con una existente

Para combinar una lista con la lista inicial, puede usar la función auxiliar `extend()`.

Comente el código que agregó en la sección anterior. Después, agregue el siguiente código:

PythonCopiar

```python
new_colors = ['lime', 'gray']
colors.extend(new_colors)
print(colors)
```

La función auxiliar `extend()` agrega elementos de una lista que se pasa como argumento.

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown']
['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown', 'lime', 'gray']
```

## Paso 8: borrado de todos los elementos de una lista

Para quitar todos los elementos de una lista, llame a la función `clear()`.

Comente el código que agregó en la sección anterior. Después, agregue el siguiente código:

PythonCopiar

```python
colors.clear()
print(colors)
```

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
['red', 'green', 'blue', 'yellow', 'orange', 'purple', 'brown']
[]
```

## Resumen

- Las listas son estructuras de datos diseñadas para recopilar datos relacionados en los programas. Aunque los datos pueden ser de cualquier tipo, los elementos suelen tener el mismo tipo de datos, ya que sirven para un propósito similar en los programas.
- Cree una lista mediante el uso de corchetes. Use una coma para separar cada elemento.
- Acceda a los elementos individuales de la lista mediante el uso de corchetes y de un índice basado en cero. Acceda al primer elemento de la lista mediante el índice `0`. Acceda al último elemento de la lista mediante el índice `-1`. Acceda a los elementos respecto al final de la lista mediante el uso de otros números negativos como índices.
- Cree segmentos mediante el uso de corchetes y dos puntos. El signo de dos puntos separa el principio del segmento, a la izquierda, y el final del segmento, a la derecha.
- Use funciones auxiliares como `pop()`, `append()`, `remove()`, `extend()` y `clear()` para cambiar los elementos de una lista.

# Ejercicio: recorrer listas en iteración mediante la instrucción for

- 6 minutos

La mayoría de las colecciones son *iterables*. Cuentan con una implementación interna que permite recorrer en iteración todos los elementos de la colección de uno en uno mediante una instrucción `for`. En este módulo, recorreremos en iteración una lista de Python.

## Paso 1: adición de un archivo para este ejercicio

Use las técnicas que ha aprendido en módulos anteriores para agregar un nuevo archivo de código en la carpeta del módulo. Por ejemplo, puede crear un archivo denominado *exercise2.py*.

## Paso 2: comprobar la inclusión de un valor en una lista

La palabra clave `in` permite recorrer en iteración todos los elementos de una lista, pero también se puede usar como operador independiente para comprobar si un elemento pertenece a una lista.

¿Qué ocurre si queremos saber si un número determinado forma parte de una lista de números? Podemos recorrer en iteración cada número y usar una instrucción `if` para ver si encontramos el valor, pero es más recomendable usar los operadores `in` o `not in` para comprobar si elemento está incluido.

Agregue el código siguiente al archivo de código nuevo:

PythonCopiar

```python
numbers = [1, 3, 5]

print(5 in numbers)
print(8 in numbers)

print(5 not in numbers)
print(8 not in numbers)
```

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
True
False
False
True
```

## Paso 3: recorrido en bucle por una lista

La instrucción `for` permite recorrer en iteración todos los elementos de una lista. La instrucción `for` incluye lo siguiente:

- La palabra clave `for`.
- El nombre de la variable que contendrá el siguiente elemento de la lista. Esta variable está disponible en el bloque de código que aparece a continuación.
- La palabra clave `in`.
- El nombre de la variable de la lista.
- El signo de dos puntos (`:`), que finaliza la instrucción.

La parte que aparece después de la instrucción `for` es igual de importante. Allí definirá un bloque de código que se ejecutará para cada elemento de la lista. El valor del elemento actual se establece en una variable en la instrucción `for`. Está disponible en el cuerpo del bloque de código.

Comente el código de la sección anterior. Después, agregue la siguiente lista de código:

PythonCopiar

```python
cities = ["Chicago", "London", "Tokyo"]

for city in cities:
  print(city)
```

En este ejemplo, simplemente imprimiremos los elementos de la lista, uno por línea. Aun así, puede ver la estructura básica del bucle `for` y cómo funcionan todas las partes.

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
Chicago
London
Tokyo
```

## Paso 4: interrupción de un bucle `for`

La instrucción `for` tiene características similares a la instrucción `while`, que exploramos en otro módulo.

La instrucción `break` permite interrumpir la iteración `for`. En este ejemplo, interrumpiremos el bucle después de encontrar un valor que supere un umbral específico. Una vez que se produzca la interrupción, podremos filtrar la lista original.

Comente el código de la sección anterior. Después, agregue la siguiente lista de código:

PythonCopiar

```python
numbers = [42, 77, 16, 101, 23, 8, 4, 15, 55]
numbers.sort()

for number in numbers:
  if number > 42:
    break
  print(number)
```

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
4
8
15
16
23
42
```

## Paso 5: uso de una instrucción `else`

Si no ha interrumpido el bucle y quiere ejecutar código solo después de que se haya procesado cada elemento de la lista, puede usar la instrucción `else`. En el ejemplo siguiente, imprimiremos la frase `No numbers greater than 90` solo si cada número de la lista aleatoria de cinco números es inferior al valor `90`.

Comente el código de la sección anterior. Después, agregue la siguiente lista de código:

PythonCopiar

```python
import random
numbers = []

while len(numbers) < 5:
  numbers.append(random.randint(1, 100))

for number in numbers:
  print(number)
  if number >= 90:
    print('Found at least one number greater than 90')
    break
else:
  print('No numbers greater than 90')

print('Complete')
```

Al ejecutar el código, podría ver algo parecido a la salida siguiente. La salida será diferente, ya que los números generados son aleatorios.

ResultadosCopiar

```output
82
60
84
29
49
No numbers greater than 90
```

Si uno de los números aleatorios es 90 o superior, verá algo parecido a la salida siguiente. También en esta ocasión la salida será diferente, ya que los números generados son aleatorios.

ResultadosCopiar

```output
37
70
2
69
95
Found at least one number greater than 90
Complete
```

## Paso 6: uso de una instrucción `continue`

Use la instrucción `continue` en un bloque de código para omitir la lógica restante y pasar al siguiente elemento de una lista en una instrucción `for`.

En esta sección, compilaremos un breve programa para filtrar una lista. La lista contiene valores `int` y `string`. Queremos crear una lista que contenga solo los valores `str`. Usaremos la instrucción `continue` para movernos al siguiente elemento de la lista, en lugar de agregar el elemento actual a la lista filtrada.

Comente el código de la sección anterior. Después, agregue la siguiente lista de código:

PythonCopiar

```python
values = ["laptop", 7, "phone", 3, "dslr", 5]
equipment = []

for value in values:
  if isinstance(value, str) == False:
    continue
  equipment.append(value)

print(equipment)
```

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
laptop
phone
dslr
```

## Paso 7: creación de bucles `for` anidados

La anidación de un bucle `for` en otro bucle `for` es una forma habitual de generar una combinación de valores.

Supongamos que estamos compilando un programa para jugar a las cartas. Queremos crear una carta para cada combinación de palo y número. Podríamos codificar de forma rígida los 52 valores en una baraja de cartas. También podríamos generar una baraja de cartas si creamos primero una lista de palos y una lista de números y, después, usamos un bucle `for` anidado.

Comente el código de la sección anterior. Después, agregue la siguiente lista de código:

PythonCopiar

```python
suits = ["Hearts", "Spades", "Clubs", "Diamonds"]
ranks = ["2", "3", "4", "5", "6", "7", "8", "9", "10", "Jack", "Queen", "King", "Ace"]

for  suit in suits:
  for rank in ranks:
    print(f'{rank} of {suit}') 
```

Al ejecutar el código, debería ver la salida siguiente:

ResultadosCopiar

```output
2 of Hearts
3 of Hearts
4 of Hearts
5 of Hearts
6 of Hearts
7 of Hearts
8 of Hearts
9 of Hearts
10 of Hearts
Jack of Hearts
Queen of Hearts
King of Hearts
Ace of Hearts
2 of Spades
3 of Spades
4 of Spades
5 of Spades
6 of Spades
7 of Spades
8 of Spades
9 of Spades
10 of Spades
Jack of Spades
Queen of Spades
King of Spades
Ace of Spades
2 of Clubs
3 of Clubs
4 of Clubs
5 of Clubs
6 of Clubs
7 of Clubs
8 of Clubs
9 of Clubs
10 of Clubs
Jack of Clubs
Queen of Clubs
King of Clubs
Ace of Clubs
2 of Diamonds
3 of Diamonds
4 of Diamonds
5 of Diamonds
6 of Diamonds
7 of Diamonds
8 of Diamonds
9 of Diamonds
10 of Diamonds
Jack of Diamonds
Queen of Diamonds
King of Diamonds
Ace of Diamonds
```

Esta técnica resultará útil cuando trabajemos en el desafío que se plantea más adelante en el módulo.

## Paso 8: selección aleatoria de una lista

Supongamos que quiere recuperar un muestreo de todos los valores de una lista. Mediante el módulo `random`, puede llamar a la función `choice()` para seleccionar de manera aleatoria un elemento de una lista. También puede llamar a la función `choices()` para seleccionar aleatoriamente un número de elementos de una lista.

Comente el código de la sección anterior. Después, agregue la siguiente lista de código:

PythonCopiar

```python
import random

numbers = [42, 77, 16, 101, 23, 8, 4, 15, 55]
selected_number = random.choice(numbers)
print(selected_number)

selected_numbers = random.choices(numbers, k=3)
print(selected_numbers)
```

Al ejecutar el código, debería ver algo parecido a la salida siguiente. La salida será diferente, ya que los elementos seleccionados son aleatorios.

ResultadosCopiar

```output
101
[77, 4, 8]
```

Esta técnica también resultará útil cuando trabajemos en el desafío que se plantea más adelante en el módulo.

### Resumen

- Use las palabras clave `in` y `not in` como parte de una expresión booleana para comprobar si un valor forma parte de una lista.
- Use la instrucción `for` para recorrer en iteración todos los elementos de una lista. Úsela también para ejecutar un bloque de código que coloque el elemento actual en el ámbito para inspeccionarlo en la lógica del bloque de código.
- Use la instrucción `continue` para omitir la lógica del bloque de código restante y continuar con el siguiente elemento de la lista asignado por la instrucción `for`.
- Use la instrucción `break` para interrumpir antes de tiempo la instrucción `for`.
- Use la instrucción `else` para crear un bloque de código que se ejecute después de usar la instrucción `for` para recorrer en iteración todos los elementos de la lista.
- Anide instrucciones `for` para crear una lista de cada combinación de dos listas.
- Use las funciones `choice()` y `choices()` del módulo `random` para seleccionar uno o varios elementos de la lista, respectivamente.

