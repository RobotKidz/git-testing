Convierta la entrada de usuario en valores numéricos y use operadores matemáticos para realizar cálculos.

## Learning Objectives

En este módulo, usará:

- Los métodos `type()`, `isinstance()` e `isnumeric()` para inspeccionar el tipo de datos de un valor y su idoneidad para su uso o conversión a un tipo de datos numérico.
- Operadores matemáticos para realizar operaciones matemáticas básicas con datos numéricos.
- El tipo de datos `float` para representar valores que incluyan valores fraccionarios, representados por números después del separador decimal.

## Requisitos previos

- Un entorno de desarrollo de Python ya configurado.
- Conocimientos sobre cómo crear, editar y ejecutar código de Python almacenado en un archivo *.py*.
- Nociones sobre el uso de funciones de entrada y salida, como `print()` e `input()`.
- Conocimientos sobre cómo crear y usar variables, y cómo realizar operaciones básicas con cadenas, como la concatenación.
- Nociones sobre las funciones de conversión de tipos de datos, como `int()` y `str()`.

# Introducción

- 2 minutos

En casi todas las aplicaciones que se compilan, es necesario controlar los datos, tanto si se trata de datos que el usuario ha introducido mediante el teclado como de archivos que contienen datos que hay que procesar o transformar.

Ya ha visto que es posible que haga falta convertir los datos de una cadena en un número entero para realizar cálculos matemáticos. Es una tarea habitual.

Supongamos que está escribiendo un programa que realiza cálculos con datos numéricos. ¿Qué ocurre si pide al usuario que proporcione un dato numérico pero este escribe un valor no numérico? Si no tiene en cuenta esta posibilidad, la aplicación dará error, el programa se cerrará repentinamente y el usuario no comprenderá qué ha ocurrido.

Para evitar esta situación, el programa debe ser capaz de comprobar si el valor especificado se puede convertir en un número antes de que el programa intente convertir el tipo de datos. Si no se puede convertir el valor, el programa pedirá al usuario que intente escribir de nuevo el valor.

Así que, ¿cómo se hace una comprobación de conversión de tipo de datos mediante Python?

En este módulo, inspeccionará mediante programación un valor para conocer el tipo de datos actual y determinará si se puede convertir en un tipo de datos diferente, como un entero. Usará la instrucción de decisión `if` que aprendió en el módulo anterior para bifurcar la ejecución del código: para que realice la conversión de datos o para que muestre un mensaje a aquellos usuarios que escriban un valor diferente. Usará operadores matemáticos integrados para que el programa realice operaciones de suma, resta, división, multiplicación y otras operaciones.

Al terminar el módulo, podrá compilar un programa que pueda aceptar los datos proporcionados por el usuario, evaluar qué tipo de datos es, agregar lógica que decida cómo bifurcar la ejecución del código para controlar diversas situaciones y realizar una variedad de operaciones matemáticas con los datos numéricos.

## Objetivos de aprendizaje

En este módulo, usará:

- Los métodos `type()`, `isinstance()` y `isnumeric()` para inspeccionar el tipo de datos de un valor y su idoneidad para su uso o conversión a un tipo de datos numérico.
- Operadores matemáticos para realizar operaciones matemáticas básicas con datos numéricos.
- El tipo de datos `float` para representar valores que incluyan valores fraccionarios, representados por números después del separador decimal.

## Requisitos previos

Antes de empezar este módulo, debe:

- Tener configurado el entorno de desarrollo de Python.
- Saber cómo crear, editar y ejecutar código de Python que está almacenado en un archivo *.py*.
- Tener nociones del uso de funciones de entrada y salida, como `print()` y `input()`.
- Saber cómo crear y usar variables, y cómo realizar operaciones básicas con cadenas, como la concatenación.
- Tener nociones de las funciones de conversión de tipos de datos, como `int()` y `str()`.

Si necesita revisar o aprender algunos de estos conceptos, visite los módulos anteriores de esta ruta de aprendizaje.



# Ejercicio: Determinar los tipos de datos de los valores

- 6 minutos

Con Python es muy fácil trabajar con datos. Cada valor de datos tiene un tipo de datos subyacente y ese tipo de datos determina lo que se puede hacer con el valor. Por ejemplo, los valores numéricos se pueden usar para operaciones matemáticas. Los valores de cadena se pueden imprimir, concatenar, dividir, etc.

Python proporciona varias maneras de evaluar un valor para ver, evaluar y convertir su tipo de datos. Hay varias funciones integradas que se pueden usar. En este ejercicio, aprenderá sobre todas estas funciones y técnicas.

## La función `type()`

En el módulo anterior, ha aprendido sobre la función `type()`, que solo muestra el tipo de datos de un valor especificado.

### Paso 1: Crear una nueva carpeta de trabajo y un archivo de código de Python

Emplee las técnicas que ha aprendido en módulos anteriores para crear una carpeta nueva para el trabajo de este módulo. Por ejemplo, puede crear una carpeta llamada *python-numeric-operations*.

En esa carpeta, cree un archivo para este ejercicio. Por ejemplo, puede crear un archivo denominado *exercise1.py*.

Cuando llegue el momento de ejecutar el código, puede usar la integración de Herramientas de Python para Visual Studio Code. Para ello, seleccione la flecha verde o use un comando en el terminal integrado mediante las técnicas que aprendió en los módulos anteriores.

### Paso 2: Escribir un código que use la función `type()` en el archivo de código

Agregue estas líneas de código para imprimir el tipo de datos de varios valores. Cuando haya terminado, el código debe coincidir con este ejemplo:

PythonCopiar

```python
print(type('7'))
print(type(7))
print(type(7.1))
```

Con las técnicas que ha aprendido en módulos anteriores, ejecute el archivo de código al que ha agregado este código. Debería mostrarse este resultado:

ResultadosCopiar

```output
<class 'str'>
<class 'int'>  
<class 'float'>
```

Por ahora, puede considerar el término *clase* como una simple *clasificación*. Muy pronto aprenderá más sobre las clases y los objetos de Python, y comprenderá las ramificaciones del término *clase* en Python.

Volviendo a este ejercicio, hay tres tipos de datos:

- **str**: tipo de datos para cadenas. Las cadenas pueden contener todos los caracteres alfanuméricos, y pueden ser cortas (unos pocos caracteres) o muy largas (un párrafo completo de datos de texto).
- **int**: tipo de datos para valores enteros, que puede ser cualquier número no fraccionario, positivo o negativo.
- **float**: tipo de datos para los valores Float, que puede incluir valores fraccionarios representados como números con un separador decimal y números después del decimal.

La función `type()` simplemente examina el valor que se pasa como parámetro de entrada (la palabra entre paréntesis) y devuelve el tipo de datos. Es una buena herramienta que puede usar mientras aprende Python y descubre cómo funciona todo su engranaje con los valores. Pero para aplicaciones reales, hay formas más útiles de obtener esta información.

## La función `isinstance()`

La siguiente técnica usa la función `isinstance()`, que permite afirmar que espera que un valor sea de un tipo de datos determinado. La función `isinstance()` indica si el valor es el esperado. Devuelve el valor `True` si se cumple lo que esperaba y `False` si no se cumple.

### Paso 3: Comentar el código anterior y agregar código que emplea la función `isinstance()` al archivo de código

En el archivo de código, comente todo el código que escribió anteriormente agregando un signo de número (**#**), seguido de un espacio, al principio de cada línea.

Después, agregue el código que usa `isinstance()` para comprobar el tipo de datos de los distintos valores. Cuando termine, el archivo de código debería tener este aspecto:

PythonCopiar

```python
# print(type('7'))
# print(type(7))
# print(type(7.1))

print(isinstance('7', str))
print(isinstance(7, int))
print(isinstance(7.1, float))

print(isinstance(7, str))
print(isinstance('7', int))
print(isinstance('7.1', float))
```

Al ejecutar el código, debe mostrarse este resultado:

ResultadosCopiar

```output
True
True 
True 
False
False
False
```

La función `isinstance()` devuelve un valor booleano. A diferencia de la técnica anterior que usó al comprobar un valor mediante la función `type()` y usó el operador de igualdad, `isinstance()` consigue el mismo resultado de una forma más concisa.

Explorará el término *es una instancia de* en un próximo módulo que explora clases y objetos. Pero por ahora, puede considerarlo una manera fácil de comparar un valor y el tipo de datos que espera que sea.

### ¿Se puede crear una expresión booleana mediante la función `type()`?

Puede que se esté preguntando si es lo mismo usar la función `isinstance()` que usar este código:

PythonCopiar

```python
print(type('7') == str)
print(type(7) == int)
print(type(7.1) == float)

print(type(7) == str)
print(type('7') == int)
print(type('7.1') == float)
```

La respuesta es sí. En estos casos sencillos, son más o menos equivalentes. Conforme vaya aprendiendo más sobre clases y objetos, verá que es posible que este código no ofrezca los resultados esperados en escenarios más complejos. Se recomienda no usar la función `type()` con la intención de comprobar la igualdad.

Aunque las funciones `type()` y `isinstance()` permiten evaluar el tipo de datos actual, debe usar una técnica diferente para ayudarle a entender si un valor especificado *se puede convertir* en un tipo diferente. En la unidad siguiente, aprenderá una tercera técnica que le permite hacerlo.

### ¿Cuál es la relación entre los tipos de datos y las variables?

Es importante comprender que el tipo de datos forma parte del *valor*. El tipo de datos *no* forma parte de la variable que podría usar para acceder al valor. Una variable puede apuntar a cualquier valor, independientemente del tipo de datos del valor.

PythonCopiar

```python
x = 'a string'
print(type(x))
x = 7
print(type(x))
x = False 
print(type(x))
```

Al ejecutar el código, debe mostrarse este resultado:

ResultadosCopiar

```output
<class 'str'>
<class 'int'>
<class 'bool'>
```

En este ejemplo de código, lo único que cambió fue el valor literal al que apuntaba la variable `x`. No fue necesario convertir los datos para que `x` apuntara a una cadena en la primera línea de código y luego a un valor entero o booleano en las siguientes líneas de código.

Se trata de una distinción importante en Python y una diferencia importante con respecto a otros lenguajes de programación.

### Resumen

Ha aprendido algunas ideas importantes en esta unidad:

- La función `type()` devuelve el tipo de datos de un valor especificado.
- La función `instanceof()` permite comprobar si un valor es una instancia de un tipo de datos especificado.
- El tipo de datos `float` es para los valores numéricos que contienen valores fraccionarios y que se representan como números después del separador decimal.
- Los valores tienen tipos de datos y las variables no. Una variable simplemente apunta a un valor y puede apuntar a cualquier valor de cualquier tipo de datos.

# Ejercicio: Determinar si una cadena se puede convertir en un número

- 6 minutos

En el módulo anterior, creó un ejemplo que permitía a los usuarios escribir dos valores. El programa agregaría los valores juntos después de convertirlos mediante la función `int()`.

PythonCopiar

```python
first_value = int(input('First Number: '))
second_value = int(input('Second number: '))
sum = first_value + second_value
print("Sum: " + str(sum))
```

Como comentamos en la introducción de este módulo, es posible que los usuarios escriban un valor que no se pueda convertir en un tipo de datos numérico. Piense en qué sucede si alguien escribe *Bob* en lugar de un valor numérico.

ResultadosCopiar

```output
First Number: 6
Second Number: Bob
Traceback (most recent call last):
  File "c:/python/numeric-operations-datatypes/exercise1.py", line 2, in <module>
    second_number = int(input())
ValueError: invalid literal for int() with base 10: 'Bob'
```

### ¿Qué ha fallado?

Este código solo tiene en cuenta el mejor escenario: que los usuarios escriben un valor de entre un intervalo de valores determinado, es decir, un valor numérico. Los desarrolladores aprenden a prever que los valores introducidos por los usuarios u otros sistemas (incluidos los archivos generados por otros programas) podrían no estar dentro del intervalo de valores aceptable. A veces llamamos a este enfoque "considerar que los datos de entrada están mal", que es el equivalente de programación de "conducción preventiva".

Con un sano escepticismo, deberá realizar comprobaciones de tipo de datos y de valor en los datos antes de realizar operaciones reales con ellos.

### ¿Y después qué?

En este ejercicio, escribirá el código que da el primer paso para determinar qué acción es la más adecuada. Si el valor no se puede convertir en un número, debe detener el programa, indicar al usuario que el valor especificado no es válido y pedirle que vuelva a intentarlo.

Para poder hacerlo, debe conocer mejor los tipos de datos, que son funciones integradas que permiten determinar el tipo de datos de un valor. Debe saber cómo trabajar con expresiones booleanas como paso previo a probar los valores. Y debe aprender a bifurcar el código para controlar escenarios en los que los datos no se pueden usar tal cual.

### ¿Cómo se soluciona el problema?

Al principio de esta unidad, hemos descrito el problema fundamental como un tema de confianza. Confía en que los usuarios especificarán un valor que podría usarse como un número.

Para solucionarlo, debe realizar algunos pasos más. Primero, compruebe los datos proporcionados por el usuario para ver si se pueden convertir en `int`. Si se pueden convertir, conviértalos. Pero si no se pueden convertir, debe explicar el problema.

¿Cómo puede determinar si la entrada del usuario es numérica, aunque la función `input()` siempre devuelva un valor de cadena? ¿Y cómo puede determinar el tipo de datos de un valor?

## Usar la función `isnumeric()`

En un principio, le interesa encontrar la manera de determinar si el valor especificado se puede convertir en un valor numérico para poder realizar operaciones matemáticas con él. La función `isnumeric()` devuelve un valor booleano si el valor de cadena se puede convertir en un valor numérico.

### Paso 1: Crear un nuevo archivo de código de Python

Use las técnicas que ha aprendido en los módulos anteriores para agregar un nuevo archivo de código en la carpeta actual que está dedicada a este módulo. Por ejemplo, puede crear un archivo denominado *exercise2.py*.

### Paso 2: Agregar código que use la función `isnumeric()` para determinar si una cadena se puede convertir en un número

En el nuevo archivo de código, agregue este código:

PythonCopiar

```python
numeric_value = '7'
print(numeric_value.isnumeric())

string_value = 'Bob'
print(string_value.isnumeric())
```

Tenga en cuenta que la función `isnumeric()` es diferente de las otras funciones que ha usado hasta ahora. Para acceder a la función, use el carácter de punto (**.**) del *operador de descriptor de acceso de miembro*. Esto solo significa que la función no es de uso general y solo se puede usar en un tipo de datos de cadena. En realidad es algo más complicado, pero aprenderá más sobre los miembros de clase en un próximo módulo.

Las funciones que ofrecen características adicionales y que son accesibles para cualquier valor de un tipo de datos especificado se denominan *funciones auxiliares*, porque son aplicaciones auxiliares integradas con las que es más fácil usar o comprender el contenido del propio valor de la cadena.

Si ejecuta este código, verá este resultado:

ResultadosCopiar

```output
True
False
```

Tanto `numeric_value` como `string_value` apuntan a valores de cadena, pero la función `isnumeric()` indica que uno de ellos, `numeric_value`, podría convertirse y usarse como un tipo de datos `int` o `float`. Usará `numeric_value` dentro de un rato para crear un programa más sólido que acepte datos proporcionados por el usuario para el procesamiento matemático.

### Otras funciones is__ ()

El tipo de datos `str` de Python admite muchas funciones auxiliares similares. Como está empezando, estas son algunas de las más útiles:

| Función       | Finalidad                                                    |
| :------------ | :----------------------------------------------------------- |
| `isalnum()`   | Garantiza que la cadena no tiene caracteres especiales, como %, $, #, @ o !. |
| `isalpha()`   | Garantiza que la cadena contiene solo letras del alfabeto.   |
| `isdecimal()` | Garantiza que la cadena contiene solo valores decimales (números). |
| `istitle()`   | Garantiza que la cadena sigue las reglas de mayúsculas (como en una oración). |
| `isupper()`   | Garantiza que la cadena contiene solo letras en mayúscula.   |
| `islower()`   | Garantiza que la cadena contiene solo letras en minúscula.   |

Trabajará con algunas de estas funciones en otro módulo dedicado a trabajar con cadenas.

## Combinar `isnumeric()` con una instrucción `if`

En el módulo anterior, ha usado la instrucción `if ... elif ... else` para bifurcar la ejecución del código. Ahora aplicará lo que ha aprendido sobre la entrada de usuario, los tipos de datos y la función auxiliar `isnumeric()` para comprobar si se puede convertir la entrada antes de que el programa intente realizar la conversión.

La instrucción `if` permite realizar una *validación* de los datos de entrada. Validación es un término de programación que hace referencia a una comprobación de los datos para asegurarse de que tienen el formato adecuado antes de que el programa continúe.

### Paso 3: Comentar el código de los pasos anteriores y luego volver a escribirlo para validar los datos de entrada del teclado mediante una instrucción `if` y la función `isnumeric()`

Actualice el código para que coincida con esta lista de código:

PythonCopiar

```python
first_value = input('First Number: ')

if first_value.isnumeric() == False:
    print('Value is not a number.')
    exit()

second_value = input('Second Number: ')

if second_value.isnumeric() == False:
    print('Value is not a number.')
    exit()

first_value = int(first_value)
second_value = int(second_value)

sum = first_value + second_value
print('Sum: ' + str(sum))
```

Aquí se usa `isnumeric()`, esperando que la expresión booleana devuelva *False*. Si devuelve *True* (es decir, si `isnumeric()` es *False*), se muestra un mensaje y se ejecuta `exit()`. En caso contrario, continúe con el programa.

El método `exit()` finaliza el programa inmediatamente. Este método es útil cuando quiere finalizar el programa sin procesar líneas de código adicionales. En este caso, quiere finalizar el programa cuando sepa que la conversión de la entrada del usuario a `int` no se realizará correctamente. Cuando aprenda sobre las estructuras de bucle en Python, podrá pedir repetidamente a los usuarios un valor diferente hasta que escriban un valor numérico.

Si ejecuta el código y los usuarios proporcionan una respuesta numérica a `input()`, debe devolver una suma válida de los números.

ResultadosCopiar

```output
First Number: 4
Second Number: 5
Sum: 9
```

Si ejecuta el código y los usuarios proporcionan una respuesta no numérica a los mensajes, obtendrá una respuesta predecible cuando finalice el programa.

ResultadosCopiar

```output
First Number: 5
Second Number: bob
Value is not a number.
```

Sin duda, para el enfoque de *puerta* hay que escribir más líneas de código. Pero hace que el programa sea más resistente y menos propenso a generar un error con un uso real. Puede reducir ligeramente las líneas de código si combina las dos llamadas a `isnumeric()` en la misma línea de código mediante el operador `or`.

### Paso 4: Actualizar el ejemplo de código para usar el operador lógico `or`

Actualice el ejemplo de código para usar el operador lógico `or`. Asegúrese de que el código coincide con esta lista de código:

PythonCopiar

```python
first_value = input('First Number: ')
second_value = input('Second Number: ')

if first_value.isnumeric() == False or second_value.isnumeric() == False:
    print('Please enter numbers only.')
    exit()

first_value = int(first_value)
second_value = int(second_value)

sum = first_value + second_value
print('Sum: ' + str(sum))
```

Ejecute la aplicación unas cuantas veces y pruebe varias combinaciones para probar los cambios.

## Resumen

- Con `isnumeric()` puede comprobar si un valor se puede convertir en `int` o `float`.
- La función `isnumeric()` es un ejemplo de *función auxiliar* porque admite el uso de un tipo de datos como `str`. Para acceder a estos tipos de función, use el carácter de punto (**.**) del *operador de descriptor de acceso de miembro*.
- Use la función `exit()` para finalizar la ejecución del programa inmediatamente.
- A veces, puede usar el operador lógico `or` para reducir la cantidad de código que tiene que escribir para implementar las comprobaciones validadas.
- Una función auxiliar trabaja con un valor de un tipo especificado, lo que proporciona utilidades prácticas con las que puede realizar operaciones comunes en valores que pertenecen a ese tipo de datos.
- Todos los tipos de datos admiten algunas funciones auxiliares. Hemos visto brevemente algunas funciones auxiliares `str` con las que comprenderá mejor el contenido de los valores de cadena.

# Ejercicio: Realizar operaciones matemáticas con números

- 6 minutos

Hasta ahora, ha estado interesado en obtener los datos en el formato adecuado para poder realizar operaciones matemáticas en los números. Aparte de una aritmética sencilla, todavía no ha explorado los otros tipos de operaciones que puede realizar con los números.

En esta unidad, veremos varias operaciones matemáticas que usan operadores de Python.

Pero hay otras operaciones más complejas disponibles en el módulo math de Python. Después de aprender a usar otros módulos de la [biblioteca estándar de Python ](https://docs.python.org/3/library/math.html), aprenderá a aprovechar este conjunto de características agregado.

En las bibliotecas de código abierto de terceros, como Pandas, NumPy, SciPy, Matplotlib, entre otras, encontrará otras operaciones matemáticas y las funciones de visualización y ciencia de datos. Después, usará algunas de estas bibliotecas en módulos más avanzados de Microsoft Learn.

En este ejercicio, aprenderá sobre los operadores que permiten realizar operaciones matemáticas típicas con datos numéricos.

### Paso 1: Crear un nuevo archivo

Use las técnicas que ha aprendido en los módulos anteriores para agregar un nuevo archivo de código en la carpeta actual que está dedicada a este módulo. Por ejemplo, puede crear un archivo denominado *exercise3.py*.

### Paso 2: Escribir código que realice varias operaciones matemáticas en el nuevo archivo de código

En el nuevo archivo de código, agregue este código:

PythonCopiar

```python
first_value = 5
second_value = 4

sum = first_value + second_value
difference = first_value - second_value
product = first_value * second_value
quotient = first_value / second_value
modulus = first_value % second_value
exponent = first_value ** second_value 

print('Sum: ' + str(sum))
print('Difference: ' + str(difference))
print('Product: ' + str(product))
print('Quotient: ' + str(quotient))
print('Modulus: ' + str(modulus))
print('Exponent: ' + str(exponent))
```

Muchos de los operadores son obvios pero, si no está seguro, aquí tiene una lista:

- `+`: operador de suma
- `-`: operador de resta
- `*`: operador de multiplicación
- `/`: operador de división
- `%`: operador de módulo, que le da el resto (si existe) después de dividir un valor en otro. Resulta útil para saber si un valor es divisible por el otro.
- `**`: operador de exponente. Por ejemplo, "5 a la cuarta potencia" se expresa como 5 * 5 * 5 * 5.

 Nota

En el siguiente módulo, aprenderá a usar *cadenas de formato* o *cadenas f* para evitar la conversión de datos de nuevo en una cadena.

Al ejecutar el código, debería mostrarse este resultado:

ResultadosCopiar

```output
Sum: 9
Difference: 1
Product: 20
Quotient: 1.25
Modulus: 1
Exponent: 625
```

### Paso 3: Comentar el código anterior y agregar código que le permita controlar el orden predeterminado de las operaciones

Python sigue el acrónimo PEMDAS, que indica el orden en el que se deben realizar las operaciones.

- **P**arentheses (paréntesis): Resuelva primero las operaciones entre paréntesis.
- **E**xponents (exponentes): Resuelva los exponentes.
- **M**ultiplication (multiplicación): Realice la multiplicación de izquierda a derecha.
- **D**ivision (división): Realice la división de izquierda a derecha.
- **A**ddition (suma): Realice la suma de izquierda a derecha.
- **S**ubtraction (resta): Realice la resta de izquierda a derecha.

Para ver esta operación en acción, comente el código anterior del archivo y luego agregue estas líneas de código:

PythonCopiar

```python
print(3 + 4 * 5)
print((3 + 4) * 5)
```

En la primera línea, se permite el orden natural de las operaciones antes de introducir paréntesis para controlar el orden. En la segunda línea, se agregan paréntesis alrededor de los dos primeros valores para forzar que se evalúen primero y, después, se multiplica por el último valor.

Si ejecuta el código, verá este resultado.

ResultadosCopiar

```output
23
35
```

Fíjese por un momento en cómo la posición de los paréntesis cambia el orden y, en última instancia, el resultado de las operaciones matemáticas.

### Paso 4: Comentar el código de los pasos anteriores y agregar código para investigar la división más detenidamente

Vamos a revisar la división por un momento. Al realizar una división, se indica un dividendo y un divisor. Si estos valores son de un tipo de datos `int`, producirán de manera implícita un cociente de tipo `float`.

Para ver esto en acción, comente el código anterior del archivo y luego agregue estas líneas de código:

PythonCopiar

```python
first_value = 5
second_value = 4

quotient = first_value / second_value

print(type(quotient))
print(quotient)
```

Si ejecuta el código, verá este resultado:

ResultadosCopiar

```output
<class 'float'>
1.25
```

Normalmente, podrá trabajar con valores `int` y `float` sin ningún problema. En ocasiones, tendrá que convertir `float` en `int`. A veces, esto ocurre de manera implícita (sin una instrucción explícita). Por lo tanto, puede que le interese tener control sobre ese proceso.

### Paso 5: Comentar el código anterior y agregar código para convertir `float` en `int`

Al convertir un valor `float` en un valor `int`, debe tener en cuenta el truncamiento.

Comente el código de los pasos anteriores y luego agregue al archivo de código esta lista de código:

PythonCopiar

```python
pi = 3.14
print(type(pi))
print(int(pi))

uptime = 99.99
print(type(uptime))
print(int(uptime))
```

Al ejecutar el código, debería mostrarse este resultado:

ResultadosCopiar

```output
<class 'float'>
3
<class 'float'>
99
```

Si nos fijamos en la variable llamada `uptime`, que apenas usa la función `int()`, hace que se quiten los valores después del decimal en lugar de redondear todo el valor hasta el siguiente número entero (100).

Para evitar el truncamiento, puede usar la función integrada `round()`. Actualice el código que escribió en este paso para incluir una llamada a la función `round()`. El código debería coincidir con este de aquí:

PythonCopiar

```python
pi = 3.14
print(type(pi))
print(int(pi))
print(round(pi))

uptime = 99.99
print(type(uptime))
print(int(uptime))
print(round(uptime))
```

Al ejecutar el código, debería mostrarse este resultado:

ResultadosCopiar

```output
<class 'float'>
3
3
<class 'float'>
99
100
```

La función `round()` ofrece una manera de hacer el redondeo y la conversión de un valor `float` en un valor `int`.

### Paso 6: Comentar el código anterior y agregar código que redondee a una posición decimal específica

Puede usar la función integrada `round()` para redondear a un número determinado de posiciones decimales, y no solo al siguiente número entero como ocurrió en el paso anterior.

Para verlo en acción, comente las líneas de código que agregó en los pasos anteriores y luego agregue estas líneas de código:

PythonCopiar

```python
first_value = round(7.654321, 2)
print(first_value)

second_value = round(9.87654, 3)
print(second_value)
```

Al proporcionar un segundo argumento cuando se llama a la función `round()`, se consigue controlar el número de posiciones decimales que se van a redondear.

Para llamar a una función y pasar más de un argumento, se usa una coma (**,**) para separar cada argumento. Conforme vaya profundizando en las funciones, puede crear funciones que tengan parámetros de entrada opcionales. En este caso, si no se proporciona el segundo argumento, la función `round()` tiene como valor predeterminado *0* decimales después de la coma decimal, lo que proporciona un valor de `int`.

Si ejecuta el código, verá este resultado:

ResultadosCopiar

```output
7.65
9.877
```

### Resumen

Estas son algunas ideas importantes de la unidad que debe recordar:

- Los operadores son pequeñas funciones de acceso directo que realizan una operación en uno o más operandos (valores literales o variables, etc.).
- Existen operadores matemáticos integrados para los usos más habituales. En el módulo math de la biblioteca estándar de Python se tratan operaciones matemáticas más avanzadas. Otras bibliotecas de código abierto de terceros tratan una amplia variedad de funciones necesarias para la ciencia de datos, la visualización de datos y el aprendizaje automático.
- El orden de las operaciones matemáticas en Python sigue las reglas de PEMDAS.
- Cuando se convierte a partir de un valor de tipo `float` a un valor de tipo `int`, los valores después del decimal se truncan y se pierden. Use la función `round()` para controlar cómo se redondean los valores.
- Algunas funciones se definen con varios parámetros de entrada. Para pasar varios argumentos a la función, se usa una coma (**,**) entre cada argumento. A veces, los argumentos son opcionales. En estos casos, la función sigue funcionando, pero usa un valor predeterminado o una implementación alternativa.

