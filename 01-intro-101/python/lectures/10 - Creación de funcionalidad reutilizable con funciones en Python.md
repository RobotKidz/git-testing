# Creación de funcionalidad reutilizable con funciones en Python



Defina funciones para crear código modular encapsulado que acepte la entrada y devuelva resultados.

## Learning Objectives

Objetivos de este módulo:

- Definir funciones que encapsulen la funcionalidad.
- Agregar parámetros de entrada a las funciones para que se puedan llamar mediante argumentos de entrada.
- Devolver valores a partir de funciones.
- Crear módulos para hospedar funciones que se puedan importar en otros archivos de código.

[Inicio](https://docs.microsoft.com/es-es/learn/modules/python-functions/1-introduction/)MarcadorAgregar a la colección



## Requisitos previos

- Un entorno de desarrollo de Python local configurado para ejecutar Python 3 con un editor de código como Visual Studio Code.
- Conocimientos sobre cómo ejecutar un script de código mediante una línea de comandos o el entorno de desarrollo local de Python.
- Conocimientos básicos de Python, que incluye una descripción de los tipos, variables, asignación de valores, llamadas a funciones, paso de argumentos e importación de módulos.

# Introducción

- 1 minuto

Los programas de gran tamaño pueden requerir cientos, miles o incluso millones de líneas de código.

Una vez que el programa crezca hasta contar con aproximadamente 50 líneas de código, necesitará una manera mejor de organizarlo.

Suponga que escribe o pega el mismo código en varios lugares en todo el programa. ¿Qué ocurre si es necesario cambiar ese código repetido debido a una lógica defectuosa o a un cambio en los requisitos? Se debería buscar en todo el programa y realizar cambios en varios lugares.

Las funciones pueden reducir las molestias. Representan uno de los primeros bloques de compilación que se aprenderán para ayudar a compilar y mantener programas de mayor tamaño.

En este módulo, compilará funciones que aceptan argumentos de entrada y valores devueltos. Obtendrá información sobre técnicas avanzadas para compilar funciones que puedan aceptar muchos tipos de entrada distintos. Y, por último, compilará módulos que hospeden funciones que se puedan importar en los programas.

Al final de este módulo, podrá crear funciones y módulos para ayudar a administrar el código a medida que se compilan programas de mayor tamaño.

## Objetivos de aprendizaje

Objetivos de este módulo:

- Definir funciones que encapsulen la funcionalidad.
- Agregar parámetros de entrada a las funciones para que se puedan llamar mediante argumentos de entrada.
- Devolver valores a partir de funciones.
- Crear módulos para hospedar funciones que se puedan importar en otros archivos de código.

## Requisitos previos

- Un entorno de desarrollo de Python local configurado para ejecutar Python 3 con un editor de código como Visual Studio Code.
- Conocimientos sobre cómo ejecutar un script de código mediante una línea de comandos o el entorno de desarrollo local de Python.
- Conocimientos básicos de Python, que incluye una descripción de los tipos, variables, asignación de valores, llamadas a funciones, paso de argumentos e importación de módulos.

# Ejercicio: Definición de una función

- 8 minutos

Una función es un bloque de código con un nombre. Dado que tiene un nombre, el programa puede llamarlo desde otra ubicación del código. La ruta de acceso de ejecución fluye en ese bloque de código. Una vez completada la ejecución de la función, la ruta de acceso de ejecución vuelve a la línea de código que ha llamado a la función y continúa.

Las funciones proporcionan un bloque de compilación básico para crear código modular. Este código se reutiliza de forma más sencilla en todo el programa. Tal como se describirá más adelante, se pueden separar las funciones en módulos para obtener una mayor portabilidad y usarlos en otros programas.

## ¿Cuándo se debe usar una función?

Cuando acabe de iniciar un nuevo programa, es probable que escriba todo el código en un único archivo de script. Todo el mundo ha escrito código de esta manera. Pero después de que el código crezca hasta 50 líneas o más, resulta difícil comprender y cambiar.

Las funciones de Python ayudan a reducir algunos de estos desafíos.

En primer lugar, use funciones para que el programa siga siendo comprensible. Cada función debe contener una única tarea o responsabilidad en el programa. Idealmente, cada función es breve. Algunos desarrolladores sugieren que una función debe tener aproximadamente seis líneas de código. Si el número de líneas aumenta de tamaño, quizás la función está tomando demasiada responsabilidad. Mantener las funciones cortas y centradas ayuda a que uno mismo y los demás comprendan el código más rápidamente.

En segundo lugar, use funciones para que el programa siga siendo administrable. Si necesita actualizar alguna funcionalidad del programa, busque las funciones que implementan esa funcionalidad y actualícelas. El uso de un buen nombre para cada función ayuda a encontrar rápidamente la funcionalidad que necesita entre miles de líneas de código.

En tercer lugar, use funciones para que el programa se siga escribiendo con más facilidad. Para crear una aplicación completa, se deben tener las funciones de llamada a la aplicación según sea necesario a partir de una función principal en la lógica de la aplicación. (Una función principal se denomina a veces controlador o administrador). Este diseño ayuda a comprender el flujo de la ruta de acceso de ejecución de la aplicación y a actualizar el programa o a agregar funcionalidades nuevas.

En cuarto lugar, use funciones para mantener reutilizables partes del programa.

- Si se va a volver a escribir un fragmento de código varias veces en un programa, es posible que se quiera extraer ese código en una función. Después, el programa llamará a la función desde cualquier lugar que se necesite.
- Si el código tiene un problema o necesita algún otro cambio, se puede actualizar en un lugar en lugar de buscarlo en todas partes.
- Si está copiando y pegando código, es posible que valore que tiene una oportunidad para crear una función.

Entonces, ¿cuándo se deben usar funciones? Siempre que empiece a compilar un programa no trivial. Las funciones ayudan a encapsular la funcionalidad en un solo lugar, crear el programa, actualizar el código y agregar características nuevas.

## Qué se va a compilar en este ejercicio

En este ejercicio, se obtendrá información sobre cómo crear y llamar a funciones, devolver valores a partir de funciones y proporcionar argumentos como parámetros de entrada a las funciones.

### Paso 1: Crear una carpeta de trabajo y un archivo de código de Python nuevos

Con las técnicas que se han aprendido en los módulos anteriores, cree una carpeta nueva denominada python-functions para su trabajo en este módulo. Dentro de esa carpeta, cree un archivo nuevo denominado exercise1.py para este ejercicio.

Cuando esté a punto para ejecutar el código, se pueden usar las herramientas de Python integradas para Visual Studio Code seleccionando la flecha verde. También se puede usar un comando en el terminal integrado con las técnicas que ha aprendido en módulos anteriores.

### Paso 2: Agregar código al archivo de código para crear una función pequeña y llamarla

Agregue el código siguiente al archivo de código nuevo. El código define la función simple `say_hello()` y luego llama a la función.

PythonCopiar

```python
def say_hello():
  print('Hello World!')

say_hello()
```

Aquí ha creado su primera función. La función tiene cinco partes:

- La palabra clave `def`.
- Un nombre de función. Debe seguir las mismas reglas de nomenclatura que se usan para las variables.
- Un par de símbolos de paréntesis (`()`). Los parámetros de entrada se definen dentro de estos paréntesis.
- Un símbolo de dos puntos (`:`) para terminar la signatura de la función.
- Un bloque de código debajo de la signatura. Este bloque es el cuerpo de la función. Se ejecuta cuando se llama a la función.

Debajo del bloque de código de la función se llama a la función mediante su nombre `say_hello` y el operador de invocación del método (`()`).

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
Hello World!
```

La otra parte crítica de la definición y la llamada a funciones es la ubicación de la definición de función y la llamada de función. La definición debe aparecer antes de la llamada. El código siguiente es problemático porque intenta llamar a la función antes de definirla:

PythonCopiar

```python
say_hello()

def say_hello():
  print('Hello World!')
```

Si se ha ejecutado el código, se verá el error siguiente:

ResultadosCopiar

```output
NameError: name 'say_hello' is not defined
```

### Paso 3: Actualizar el código del paso anterior y agregar código para aceptar un parámetro de entrada

Después, cree una versión nueva de la función que sea un poco más útil. Cambie el código del paso anterior para que coincida con la siguiente lista de códigos:

PythonCopiar

```python
def say_hello(name):
  print(f'Hello {name}!')

say_hello('Bob')
```

Esta versión de la función es más útil porque permite que el autor de la llamada especifique a quién debe decir "Hola". Para especificar un nombre, el autor de la llamada lo pasa como argumento a la función `say_hello()`.

Defina la función `say_hello()`, tal como se ha hecho anteriormente. Pero, entre paréntesis (`()`), especifique el parámetro de entrada `name`. Este parámetro permite al autor de la llamada pasar un argumento a la función. Después, la función utiliza ese valor en su cuerpo a través de la variable `name`.

Cuando se llama a la función, esta recibe el elemento `'Bob'` de cadena que se ha pasado como argumento a la función `say_hello()`.

Al ejecutar el código, debería ver la siguiente salida:

Copiar

```
Hello Bob!
```

### Paso 4: Modificar la llamada de función para omitir el argumento

A causa de cómo se ha definido la función, se requiere un argumento.

Actualice el código quitando la cadena que se ha pasado como argumento. Ahora, la llamada debería coincidir con la siguiente lista de códigos:

PythonCopiar

```python
say_hello()
```

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
TypeError: say_hello() missing 1 required positional argument: 'name'
```

Al definir un parámetro de entrada como parte de la función, se requiere un argumento. Si se quiere que el argumento sea opcional, se puede proporcionar un valor predeterminado que se usa si el autor de la llamada no pasa un argumento.

Vuelva a actualizar el ejemplo de código. Esta vez, cambie la definición del parámetro de entrada para establecer un valor predeterminado y, después, agregue una llamada a `say_hello()`. El código llama a la función con un parámetro de entrada y sin este parámetro. El código debería coincidir con la lista siguiente:

PythonCopiar

```python
def say_hello(name='World'):
  print(f'Hello {name}!')

say_hello()
say_hello('Bob')
```

La primera llamada a `say_hello()` utiliza el valor predeterminado del parámetro de entrada, mientras que la segunda proporciona su propio valor.

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
Hello World!
Hello Bob!
```

### Paso 5: Actualizar el ejemplo de código para incluir un segundo parámetro opcional de entrada

Las definiciones de funciones pueden tener varios parámetros de entrada. Para definirlos, separe cada par de parámetros con un símbolo de coma (`,`).

También puede usar el valor **None** cuando se defina el valor predeterminado de un parámetro de entrada. Este uso permite que una función busque el valor **None** en el cuerpo e imprima un mensaje adecuado.

Actualice el código del ejercicio para que coincida con la lista de códigos siguiente:

PythonCopiar

```python
def say_hello(name='World', greeting=None):
  if greeting == None:
    print(f'Hello {name}!')
  else:
    print(f'{greeting} {name}!')

say_hello()
say_hello('Bob')
say_hello(greeting='Howdy')
say_hello('Bob', 'Howdy')
```

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
Hello World!
Hello Bob!
Howdy World!
Howdy Bob!
```

Aquí se ha agregado el parámetro de entrada `greeting` y se ha establecido su valor predeterminado en `None`. Este valor es una palabra clave especial que representa el objeto **NoneType**.

Ejecute esta línea de código:

PythonCopiar

```python
print(type(None))
```

Debería ver la siguiente salida:

ResultadosCopiar

```output
<class 'NoneType'>
```

**None** representa un valor desconocido o indeterminado. No es lo mismo que una cadena vacía, el valor booleano **False**, el número cero o cualquier otro valor. El valor simplemente no está ahí. En este caso, **None** es la manera perfecta de representar un valor que no existe, para que la función pueda probarlo.

En este paso, se han agregado dos llamadas nuevas a `say_hello`:

PythonCopiar

```python
say_hello(greeting='Howdy')
say_hello('Bob', 'Howdy')
```

La primera llamada nueva omite `name` y se basa en su valor predeterminado. La llamada también especifica el nombre del parámetro `greeting` y establece su valor con el operador de asignación (`=`).

La segunda llamada nueva pasa ambos argumentos a la función.

Como se puede ver, hay muchas variaciones disponibles para crear y usar parámetros de entrada en las funciones.

### Paso 6: Comentar el código de los pasos anteriores y agregar una función nueva que devuelve un valor

Ahora que ha obtenido información sobre cómo definir parámetros de entrada, cree una función que devuelva un único valor mediante la palabra clave **return**.

Comente el código de los pasos anteriores y agregue el código siguiente:

PythonCopiar

```python
def add_two_numbers(x, y):
    return x + y

add_two_numbers(4, 6)
result = add_two_numbers(5, 7)
print(result)
```

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
12
```

Aquí se ha creado la nueva función `add_two_numbers()` que acepta dos parámetros de entrada. Después, realiza una operación de suma en esos parámetros en el cuerpo de la función y devuelve la suma.

Al escribir una llamada de función, puede omitir el valor devuelto. (Aunque, en este caso, eso no parece útil). También puede asignarlo a una variable que se usaría igual que cualquier otra variable del programa.

### Paso 7: Comentar el código de los pasos anteriores y agregar una función nueva que devuelve una lista

Aunque solo se puede devolver un valor desde una función, ese valor puede ser una lista que contenga muchos otros valores.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
def create_deck():
  suits = ["Hearts", "Spades", "Clubs", "Diamonds"]
  ranks = ["2", "3", "4", "5", "6", "7", "8", "9", "10", "Jack", "Queen", "King", "Ace"]
  deck = []

  for  suit in suits:
    for rank in ranks:
      deck.append(f'{rank} of {suit}')

  return deck

my_deck = create_deck()
print(len(my_deck))
```

Puede que reconozca este código de un módulo anterior. Este código genera 52 cartas combinando cada palo y valor de una baraja de cartas habitual. A medida que la función genera cada combinación, anexa la cadena a una lista vacía denominada `deck`. La función devuelve esa lista.

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
52
```

### Paso 8: Comentar el código de los pasos anteriores y agregar una función nueva que muestra un ámbito variable en una función

El ámbito es la accesibilidad de un valor dentro y fuera de una estructura de código, como el bloque de código de una función. Este paso del ejercicio ayudará a comprender el ámbito de las variables declaradas dentro y fuera de una función.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
def some_function():
    value = 10

print(value)
```

Esta primera versión del código define una variable denominada `value`, pero no devuelve `value`. En su lugar, solo se quiere ver si el código puede acceder a `value` fuera del bloque de código de la función.

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
NameError: name 'value' is not defined
```

El código no puede acceder a `value` fuera del bloque de código en el que se ha declarado e inicializado. La variable está oculta y no está disponible fuera del bloque de código.

¿Qué ocurre si el código define una variable del mismo nombre fuera del bloque de código de la función y, después, intenta utilizarla o devolverla desde dentro del bloque de código?

Actualice el código del ejercicio para que coincida con la lista de códigos siguiente:

PythonCopiar

```python
value = 1

def some_function():
    value = 10
    return value

print(value)
```

Aquí el código establece `value` en `1`. Dentro de `some_function()`, el código utiliza el mismo nombre de variable y establece el valor en `10`. Incluso se puede intentar que la función devuelva la nueva variable `value`. Pero ¿qué ocurre cuando el código imprime `value`?

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
1
```

Se podría pensar que esta salida tiene sentido. Dado que el código nunca ha ejecutado `some_function()`, el cuerpo de la función nunca ha tenido la oportunidad de ejecutarse.

Continúe con el experimento. Haga que el código llame realmente a `some_function()` y vea si eso cambia `value`. Actualice el código del ejercicio para que coincida con la lista de códigos siguiente:

PythonCopiar

```python
value = 1

def some_function():
    value = 10
    return value

print(value)
some_function()
print(value)
```

Ahora el código imprime `value` antes y después de llamar a `some_function()`.

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
1
1
```

La moraleja de la historia es que las variables definidas fuera de una función no afectan a las variables definidas dentro de una función, a menos que el código devuelva el valor de dentro y luego lo use. El ámbito de las variables de una función está sellado y oculto del código que hay fuera de la función, y viceversa.

## Resumen

En este ejercicio se ha obtenido información acerca de las funciones.

- Una función es un bloque de código con un nombre. Puede definir sus propias funciones y usarlas como unidades de modularidad y reutilización. Piense en una función como si tuviera una única responsabilidad. Si una función comienza a realizar más de un trabajo, quizás esta se deba dividir.
- La palabra clave **def** define una función. Cree un nombre para la función con las mismas reglas de nomenclatura que ha aprendido para las variables. Use paréntesis para definir parámetros de entrada.
- Una función tiene cero o más parámetros de entrada. Separe los parámetros de entrada con comas. Se necesita un parámetro a menos que proporcione un valor predeterminado opcional.
- La palabra clave **None** indica que una variable tiene un valor indeterminado o incognoscible.
- El ámbito es la visibilidad de un valor dentro y fuera del bloque de código de una función. Las funciones tienen su propio ámbito, privado y oculto del código que hay fuera de esas funciones.

# Ejercicio: Incorporación de listas arbitrarias de argumentos y argumentos de palabra clave a las funciones

- 6 minutos

En la unidad anterior, ha tenido la primera oportunidad para crear sus propias funciones. Se crearon funciones con varios parámetros de entrada y parámetros de entrada con valores predeterminados.

Cuenta con opciones adicionales para los parámetros de entrada. Estas opciones incluyen listas arbitrarias de argumentos y argumentos de palabra clave (o con nombre).

### Paso 1: Agregar un archivo nuevo para este ejercicio al directorio de trabajo

En esta unidad se asume que se va a continuar desde la unidad anterior. Use las técnicas que se han aprendido en los módulos anteriores para agregar un nuevo archivo de código en la carpeta dedicada a este módulo. Asigne al archivo nuevo el nombre exercise2.py.

### Paso 2: Agregar código que cree una función que acepte una lista arbitraria de argumentos

Agregue el código siguiente al archivo de código nuevo:

PythonCopiar

```python
def print_args(*args):
  for arg in args:
    print(f'arg = {arg}')

print_args('a')
print_args('a', 'b')
print_args('a', 'b', 'c')
```

Aquí se crea la función `print_args()`, que acepta una lista arbitraria de argumentos, tal y como se define en el parámetro de entrada `*args`. Un autor de llamada de esta función puede pasar cualquier número de argumentos a la función. Luego la función usa la variable `args` para acceder a todos los argumentos. Esa variable almacena una colección de los argumentos en los que la función puede iterar.

Después de la definición de función, el código llama a `print_args()` tres veces, pasando un valor diferente cada vez.

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
arg = a
arg = a
arg = b
arg = a
arg = b
arg = c
```

Use listas arbitrarias de argumentos en las funciones cuando no sepa cuántos argumentos pasan los autores de llamadas pero quiera que las funciones controlen todo lo que se pasa. Probablemente, el código necesitará iterar en cada elemento de `args` y sumar, concatenar o realizar alguna otra operación de agregado en esos elementos.

Pero, ¿cuál es el tipo de datos de `args`? Comente la instrucción de iteración y agregue instrucciones `print` que muestren el contenido y el tipo de datos de `args`.

PythonCopiar

```python
def print_args(*args):
  #for arg in args:
  #  print(f'arg = {arg}')
  print(args)
  print(type(args))

print_args('a')
print_args('a', 'b')
print_args('a', 'b', 'c')
```

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
('a',)
<class 'tuple'>
('a', 'b')
<class 'tuple'>
('a', 'b', 'c')
<class 'tuple'>
```

Una lista arbitraria de argumentos no es de tipo **lista**, sino de tipo **tupla**.

¿Qué es una tupla? En resumen, es lo mismo que una lista pero con algunas diferencias. La diferencia más destacada es que no se puede modificar el contenido de una tupla. En el ejemplo de código actual, la función no puede llamar a **append()** o **remove()**, llamar a **sort()** o **reverse()** o asignar un valor nuevo a un elemento.

Por ejemplo, el código no puede realizar esta asignación:

PythonCopiar

```python
args[0] = 'z'
```

Dicho código genera este error:

ResultadosCopiar

```output
TypeError: 'tuple' object does not support item assignment
```

### Paso 3: Comentar el código del paso anterior y agregar código que acepte argumentos de palabra clave

Los argumentos de palabra clave, que también se denominan argumentos con nombre, son similares a las listas arbitrarias de argumentos. Los autores de las llamadas pueden pasar cualquier número de argumentos de palabra clave. Cada argumento debe especificar su nombre junto con su valor.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
def print_keyword_args(**kwargs):

  third = kwargs.get('third', None)
  if third != None:
    print('third arg =', third)


print_keyword_args(first='a')
print_keyword_args(first='b', second='c')
print_keyword_args(first='d', second='e', third='f')
```

En este caso, el código llama a la función `print_keyword_args()` tres veces. Con cada llamada pasa uno o más argumentos de palabra clave, como `first='a'`. El cuerpo de la función puede acceder a un argumento existente específico mediante el método `kwargs.get()`.

Cada llamada a `kwargs.get()` pasa un nombre y un valor predeterminado. En el ejemplo actual, la función busca una palabra clave denominada `'third'`. Si `'third'` no existe en `kwargs`, la variable `third` se establece en el valor predeterminado `None`.

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
third arg = f
```

Este enfoque proporciona una manera flexible para que un autor de llamada pase argumentos. El inconveniente es que debe basarse en la documentación o el código fuente de una función para comprender lo que espera la función. Si aún no sabe que podría (o debería) pasar un argumento llamado `third`, es posible que nunca entienda cómo usar la función correctamente.

### Paso 4: Actualizar el ejemplo de código para iterar en cada palabra clave y valor

Después, obtendrá información sobre cómo iterar en cada palabra clave y valor en `kwargs`.

Actualice el código del ejercicio para que coincida con la lista de códigos siguiente:

PythonCopiar

```python
def print_keyword_args(**kwargs):

  print('\n')

  for key, value in kwargs.items():
    print(f'{key} = {value}')

  third = kwargs.get('third', None)
  if third != None:
    print('third arg =', third)


print_keyword_args(first='a')
print_keyword_args(first='b', second='c')
print_keyword_args(first='d', second='e', third='f')
```

Se ha agregado una instrucción `for` para iterar en la colección. Si está familiarizado con el uso de una instrucción `for` para iterar en un objeto **list** objeto, puede que se pregunte cómo funciona este código:

PythonCopiar

```python
for key, value in kwargs.items():
```

En este caso no está trabajando con un objeto **list**, sino con un objeto o diccionario **dict**. Un diccionario es como una lista, salvo que cada elemento tiene dos partes: un nombre (o clave) y un valor. Obtendrá más información sobre los diccionarios en otro módulo. En el ejemplo de código, `key` se establece en la palabra clave de un argumento y `value` se establece en el valor de ese argumento.

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
first = a 


first = b 
second = c


first = d
second = e
third = f
third arg = f
```

### Paso 5: Actualizar el ejemplo de código para imprimir el valor de kwargs y su tipo de datos

Para ver el tipo de datos de `kwargs`, actualice el código del ejercicio para que coincida con la lista de códigos siguiente:

PythonCopiar

```python
def print_keyword_args(**kwargs):

  print('\n')
  print(kwargs)
  print(type(kwargs))

  for key, value in kwargs.items():
    print(f'{key} = {value}')

  third = kwargs.get('third', None)
  if third != None:
    print('third arg =', third)


print_keyword_args(first='a')
print_keyword_args(first='b', second='c')
print_keyword_args(first='d', second='e', third='f')
```

Al ejecutar el código, debería ver la siguiente salida:

ResultadosCopiar

```output
{'first': 'a'}
<class 'dict'>
first = a


{'first': 'b', 'second': 'c'}
<class 'dict'>
first = b
second = c


{'first': 'd', 'second': 'e', 'third': 'f'}
<class 'dict'>
first = d
second = e
third = f
third arg = f
```

El diccionario se define mediante símbolos de llaves (`{}`). Cada elemento del diccionario sigue el formato `'': ''`. También verá que el tipo de datos de `kwargs` es `dict`.

## Resumen

En este ejercicio, se ha obtenido información sobre algunas maneras de hacer que las funciones sean más flexibles.

- Se pueden definir funciones que utilicen listas arbitrarias de argumentos. Una lista permite que un autor de llamada pase cualquier número de argumentos. En los ejemplos anteriores, el parámetro de entrada `args` administra las entradas como valores **tuple**.
- Se pueden definir funciones que utilicen palabras clave o argumentos con nombre. Un autor de llamada puede pasar cualquier número de argumentos con nombre. En los ejemplos anteriores, el parámetro de entrada `kwargs` administra las entradas como valores **dict**.

# Ejercicio: Definición de un módulo

- 4 minutos

Ahora que ya sabe cómo crear funciones, cree su propio módulo para que contenga una o varias funciones.

Ha obtenido información sobre los módulos de Python en un módulo anterior de Microsoft Learn. Un módulo de Python es simplemente un archivo de código que contiene archivos, constantes o servicios. Se puede dividir un programa en varios archivos de código para aumentar la modularidad del código y reutilizarlo en todo el programa. Los módulos incluso permiten que varios programas compartan el mismo código.

En este ejercicio se usa un módulo para separar el código que podría usarse en varias aplicaciones. El módulo separa el código que implementa la baraja del código que la usa.

### Paso 1: Crear un archivo nuevo en la carpeta de trabajo para este ejercicio

En esta unidad se asume que se va a continuar desde la unidad anterior. Use las técnicas que se han aprendido en los módulos anteriores para agregar un nuevo archivo de código en la carpeta dedicada a este módulo. Asigne al archivo nuevo el nombre exercise3.py.

### Paso 2: Crear otro archivo nuevo en la carpeta de trabajo para un nuevo módulo denominado `deck`

En la misma carpeta de trabajo donde se encuentra el archivo exercise3.py, cree otro archivo denominado deck.py.

### Paso 3: Agregar código para crear una baraja en el nuevo módulo de baraja

Agregue el código siguiente al archivo deck.py. Este código es similar a lo que se ha creado en el módulo en el que se ha obtenido información acerca de las listas. La función `create_deck()` devuelve una lista llamada `deck`. La lista contiene 52 cadenas que representan cada combinación de palo y valor de una baraja estándar.

PythonCopiar

```python
def create_deck():
  suits = ["Hearts", "Spades", "Clubs", "Diamonds"]
  ranks = ["2", "3", "4", "5", "6", "7", "8", "9", "10", "Jack", "Queen", "King", "Ace"]
  deck = []

  for  suit in suits:
    for rank in ranks:
      deck.append(f'{rank} of {suit}')

  return deck
```

### Paso 4: Agregar código al archivo de código exercise3 que llama al método `create_deck()` del módulo `deck`

En el archivo exercise3.py, agregue el código siguiente.

PythonCopiar

```python
import deck

cards = deck.create_deck()

for card in cards:
  print(card)
```

Este código consume el módulo de baraja y su funcionalidad.

La primera línea de código importa el módulo `deck`. La segunda línea de código llama a la función `create_deck()` del módulo `deck`.

Al ejecutar el código, debe imprimir la lista de cartas.

## Resumen

En este ejercicio, ha obtenido información sobre cómo crear sus propios módulos.

- Cree un módulo para separar el código reutilizable de manera modular. Un módulo de Python es un archivo de código. Al colocar funciones en un módulo, se hace que ese código se pueda usar desde otros archivos de código dentro y fuera de los programas.
- Use la instrucción **import** para acceder a las funciones de un módulo.

