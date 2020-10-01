# Manipulación y formato de datos de cadena para su visualización en Python

Use las características integradas de la clase de cadena y otros métodos auxiliares para controlar los datos de cadena.

## Learning Objectives

Objetivos de este módulo:

- Usar caracteres de escape en cadenas literales para agregar nuevas líneas y pestañas.
- Usar las características de la función `print()` para dar formato a las cadenas para su visualización.
- Llamar a una de las numerosas funciones integradas para eliminar espacios vacíos, agregar relleno y buscar y reemplazar subcadenas.
- Usar la función `format()` para crear una cadena de formato que contenga una serie de campos de reemplazo.

## Requisitos previos

- Saber cómo crear una carpeta de trabajo y agregar archivos de código.
- Saber cómo ejecutar un archivo de código de Python mediante la compatibilidad con herramientas en Visual Studio Code o la línea de comandos.
- Comprender la forma de pasar valores como argumentos a una función.
- Tener experiencia con la función `print()`, las variables y las cadenas literales, así como con los datos numéricos.
- Saber distinguir la llamada a funciones auxiliares en un tipo de datos, un valor literal y una variable.

# Introducción

- 1 minuto

La mayoría de los programas que se compilan muestran el resultado de la cadena, reciben entradas de cadena o manipulan cadenas de alguna manera. Python proporciona una amplia gama de características integradas para la manipulación y el formato de cadenas.

Supongamos que necesita transformar los datos que se van a usar en el programa. Los datos pueden tener caracteres alfanuméricos o caracteres de espacio vacío extraños, o pueden estar en mayúscula o minúscula de forma incorrecta. O quizás tenga que dar formato a los datos para mostrarlos al usuario final. Es posible que tenga que agregar pestañas, agregar nuevas líneas, cambiar las mayúsculas o minúsculas o cambiar la alineación.

En este módulo, usará características especiales de cadenas literales para agregar códigos de escape para insertar caracteres especiales y crear cadenas de varias líneas. Pasará argumentos opcionales adicionales a la función `print()` para modificar el modo en que se muestran las cadenas. Usará más de una docena de métodos auxiliares de cadena diferentes para buscar y reemplazar subcadenas, agregar relleno y cambiar la alineación. Y aprenderá a evitar la concatenación de cadenas mediante una sintaxis de plantillas de cadena especial.

Al final de este módulo, podrá compilar con confianza programas que pueden manipular y dar formato a cadenas.

## Objetivos de aprendizaje

En este módulo, aprenderá a:

- Usar caracteres de escape en cadenas literales para agregar nuevas líneas y pestañas.
- Usar las características de la función `print()` para dar formato a las cadenas para su visualización.
- Llamar a una de las numerosas funciones integradas para eliminar espacios vacíos, agregar relleno y buscar y reemplazar subcadenas.
- Usar la función `format()` para crear una cadena de formato que contenga una serie de campos de reemplazo.

## Requisitos previos:

- Debe saber cómo crear una carpeta de trabajo y agregar archivos de código.
- Debe saber cómo ejecutar un archivo de código de Python mediante la compatibilidad con herramientas en Visual Studio Code o la línea de comandos.
- Debe comprender cómo puede pasar valores como argumentos a una función.
- Debe haber trabajado con la función `print()`, las variables y las cadenas literales, así como los datos numéricos.
- Debe saber distinguir que puede llamar a funciones auxiliares en un tipo de datos, un valor literal y una variable.

Si no está seguro de cómo realizar cualquiera de estas tareas, dedique un tiempo a revisar todos los módulos anteriores en esta ruta de aprendizaje.



# Ejercicio: literales de cadena de formato

- 6 minutos

Las cadenas de Python tienen muchas características integradas, incluidas algunas que podrían no ser obvias. Antes de explorar algunos formatos de cadena avanzados que usan funciones especiales, vamos a hacer uso de todo lo que las cadenas pueden hacer por sí solas.

### Paso 1: Crear una nueva carpeta de trabajo y un archivo de código de Python

Con las técnicas que aprendió en los módulos anteriores, cree una nueva carpeta para su trabajo en este módulo. Por ejemplo, puede crear una carpeta denominada `python-format-strings`.

Dentro de esa carpeta, cree un archivo para este ejercicio. Por ejemplo, puede crear un archivo denominado `exercise1.py`.

A la hora de ejecutar el código, use las herramientas de Python para la integración con Visual Studio Code. Como alternativa, puede usar un comando en el terminal integrado mediante las técnicas que hemos aprendido en módulos anteriores.

### Paso 2: Agregar código para comparar cadenas literales definidas mediante comillas simples y dobles

Defina cadenas literales mediante un par de símbolos de comillas simples (`'`) o un par de símbolos de comillas dobles (`"`). Agregue las siguientes líneas de código al nuevo archivo de código:

PythonCopiar

```python
first_string = 'A literal string'
second_string = "A literal string"
print(second_string == first_string)
```

Al ejecutar el código, verá el resultado siguiente:

ResultadosCopiar

```output
True
```

Puede usar comillas simples o dobles. En este caso, normalmente usaremos comillas simples.

### Paso 3: Comentar el código anterior y agregar el código que usa comillas dentro de otras comillas

Si necesita usar una comilla simple o doble en la propia cadena, puede usar comillas dobles dentro de un conjunto de comillas simples, y viceversa.

Comente el código del paso anterior y agregue el código siguiente al archivo de código:

PythonCopiar

```python
third_string = 'A single quoted literal string with a " double quote'
fourth_string = "A double quoted literal string with a ' single quote"
print(third_string)
print(fourth_string)
```

En este caso, `third_string` apunta a una cadena literal que inserta comillas dobles dentro de una cadena definida con comillas simples. Por el contrario, `fourth_string` apunta a una cadena literal que incrusta una comilla simple dentro de una cadena definida con comillas dobles.

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
A single quoted literal string with a " double quote
A double quoted literal string with a ' single quote
```

### Paso 4: Comentar el código anterior y agregar código que usa secuencias de escape

Pero, ¿qué ocurre si necesita insertar una comilla simple en una cadena literal y quiere definir la cadena con comillas simples? ¿O, por el contrario, usar una comilla doble dentro de una cadena literal definida con comillas dobles? En este caso, puede usar el carácter `\` para crear una secuencia de escape.

Hay varias secuencias de escape disponibles para las cadenas de Python. Comente el código de los pasos anteriores y, posteriormente, agregue el código en la lista de código siguiente:

PythonCopiar

```python
fifth_string = 'A single quoted literal string with an \' escaped single quote'
sixth_string = "A double quoted literal string with a \" double quote"
seventh_string = 'A literal string with a \n new line character'
eighth_string = 'A literal string with a \t tab character'

print(fifth_string)
print(sixth_string)
print(seventh_string)
print(eighth_string)
```

Tal y como se sugiere en el contenido de las cadenas literales, la secuencia de escape `\n` crea una línea nueva y la secuencia de escape `\t` agrega una tabulación a la cadena cuando se muestra.

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
A single quoted literal string with an ' escaped single quote
A double quoted literal string with a " double quote
A literal string with a
 new line character
A literal string with a          tab character
```

Existen otras secuencias de escape, pero estas son las más populares.

### Paso 5: Comentar el código anterior y agregar código que muestra cadenas sin formato

Pero, ¿qué ocurre si necesita mostrar el contenido de una secuencia de escape sin realizar el comando de la secuencia de escape? En otras palabras, ¿qué ocurre si necesita mostrar literalmente el valor `\n`? En ese caso, debe prefijar una cadena literal con el carácter `r` para producir un resultado sin procesar, sin escape. Esto resulta útil si necesita omitir las secuencias de escape y mostrar toda la cadena tal como aparece en el código.

Comente el código que agregó en los pasos anteriores y, posteriormente, agregue el código siguiente al archivo de código:

PythonCopiar

```python
nineth_string = r"A literal string with a \n new line character printed raw"

print(nineth_string)
```

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
A literal string with a \n new line character printed raw
```

### Paso 6: Comentar el código anterior y agregar código que usa cadenas de varias líneas

Si necesita mostrar una cadena en varias líneas, puede usar la nueva secuencia de escape de línea que acabamos de aprender. Como alternativa, puede crear una cadena de varias líneas definiendo la cadena con un conjunto de tres comillas simples o un conjunto de tres comillas dobles.

Comente el código del paso anterior y agregue el código de la lista de código siguiente:

PythonCopiar

```python
tenth_string = '''A literal string
on more than one line
sometimes known as a verbatim string'''

eleventh_string = """Another literal string
     on more than one line
using double quotes"""

print(tenth_string)
print(eleventh_string)
```

En algunos lenguajes de programación, este tipo de cadena de varias líneas que conserva su formato se denomina "cadena textual".

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
A literal string
on more than one line
sometimes known as a verbatim string
Another literal string
     on more than one line
using double quotes
```

Observe que la cadena literal a la que apuntamos con la variable `eleventh_string` incluye varios espacios vacíos. Se conservan con fidelidad cuando se imprime la cadena unas cuantas líneas más adelante.

### Paso 7: Comentar el código anterior y agregar el código que da formato a la cadena mediante la función `print()`

En este ejercicio, se han usado varias técnicas inherentes a las cadenas para influir en el formato. La función `print()` también tiene algunas características integradas que nos permiten concatenar cadenas e influir en su formato.

Comente el código de los pasos anteriores y, posteriormente, agregue el código en la lista de código siguiente. Esto muestra cómo puede proporcionar la función `print()` con argumentos adicionales para modificar el resultado.

PythonCopiar

```python
first = 'Conrad'
second = 'Grant'
third = 'Bob'
print(first, second)
print(first, second, third)
print(first, second, third, sep='-')
print(first, second, third, sep='-', end='.')
```

La primera y la segunda llamada de la función `print()` concatenan cadenas antes de mostrarlas en la consola. La función `print()` se define de tal forma que se puede enviar en un número variable de argumentos (dos, tres, cuatro, o más). Todas ellas se concatenarán juntas, separadas entre sí por un espacio vacío, y se mostrarán en la consola.

La tercera llamada a la función `print()` agrega un argumento con nombre opcional `sep`. Define el carácter que se quiere usar para separar las cadenas a medida que se concatenan para su visualización.

La cuarta llamada a la función `print()` agrega otro argumento con nombre opcional `end`. Define el carácter que se quiere usar al final de la secuencia.

Al ejecutar el código, verá el resultado siguiente.

ResultadosCopiar

```output
Conrad Grant
Conrad Grant Bob
Conrad-Grant-Bob
Conrad-Grant-Bob.
```

### Funciones con argumentos de variable y con nombre

En un módulo anterior, hemos aprendido cómo puede definir funciones con parámetros de entrada opcionales. Estos parámetros permiten al llamador decidir si acepta el valor o la implementación predeterminados, o proporcionar el argumento con un valor.

Del mismo modo, puede definir funciones con parámetros variables. Esto permite que el llamador pase tantos argumentos como sea necesario y la función procese cada parámetro.

Los parámetros con nombre permiten al llamador usar la convención `name=value`. Esto nos permite enviar los argumentos en cualquier orden, por lo que el propósito de esos argumentos será más claro para quienes puedan leer el código en el futuro.

En otro módulo, aprenderá a agregar variables y parámetros con nombre a las funciones que defina al crear sus propias funciones.

## Resumen

En este ejercicio, ha aprendido algunos detalles importantes sobre cómo trabajar con cadenas:

- Puede definir una cadena literal mediante un conjunto de símbolos de comillas simples o dobles.
- Puede agregar una secuencia de escape para usar un carácter especial dentro de la cadena, como una secuencia de escape de comillas simples (`\'`), una secuencia de escape de comillas dobles (`\"`), una secuencia de escape de línea nueva (`\n`) o una secuencia de escape de tabulación (`\t`).
- Puede imprimir el resultado sin formato de una cadena prefijándola con el carácter `r`.
- Puede definir una cadena textual de varias líneas mediante un conjunto de tres caracteres de comillas simples (`'''`) o un conjunto de tres caracteres de comillas dobles (`"""`).
- La función `print()` puede concatenar un número variable de cadenas enviadas como argumentos en la función. Puede especificar el carácter que quiere usar para separar cada argumento, así como el carácter final.

# Ejercicio: usar funciones auxiliares de cadena

- 6 minutos

En un módulo anterior, hemos aprendido los detalles de una función auxiliar, `isnumeric()`, que nos permite comprender el contenido de una cadena y saber si podemos convertir esa cadena en un valor `int` o `float`. Un método auxiliar es una función que está disponible para los valores de un tipo de datos determinado y proporciona una funcionalidad adicional. Hemos repasado brevemente unos cuantos métodos auxiliares de cadena de estilo `is___()`.

Hay muchos otros métodos auxiliares disponibles para las cadenas; en este ejercicio trabajaremos con más de una docena ellos, que probablemente usará al compilar programas Python del mundo real.

### Paso 1: Crear un nuevo archivo de código para este ejercicio

Use las técnicas que ha aprendido en los módulos anteriores para agregar un nuevo archivo de código en la carpeta actual dedicada a este módulo. Por ejemplo, puede crear un nuevo archivo denominado `exercise2.py`.

### Paso 2: Agregar código para llamar a la función `capitalize()` mediante tres técnicas diferentes

Agregue el código de la siguiente lista al nuevo archivo:

PythonCopiar

```python
message = str.capitalize('first message')
print(message)

message = 'second message'.capitalize()
print(message)

message = 'third message'
print(message.capitalize())
```

La función `capitalize()` garantiza que el primer carácter de una cadena esté en mayúscula. Solo se escribe en mayúscula la primera letra de la cadena. Si la cadena contiene varias palabras separadas por caracteres vacíos, solo se escribe en mayúscula el primer carácter.

Aunque la función `capitalize()` es útil, preste atención a las tres formas diferentes que usamos para llamarla.

La primera vez la llamamos como miembro de la clase `str`. En otras palabras, tenemos acceso al método auxiliar `str` mediante el operador de acceso a miembros, un símbolo de punto (`.`), en el nombre del propio tipo de datos. Posteriormente, llamamos al nombre de la función y pasamos nuestra cadena literal como argumento.

La segunda vez llamamos a la función como miembro de la cadena literal. En otras palabras, tenemos acceso al método auxiliar `str` mediante el operador de acceso a miembros en el propio valor de la cadena literal. Cuando hacemos esto, no es necesario pasar nada como argumento. La función opera en la propia cadena literal.

La tercera vez llamamos a la función como miembro de una variable. Al igual que en el ejemplo anterior, tenemos acceso al método auxiliar `str` mediante el operador de acceso a miembros en la variable que apunta a una cadena literal. De nuevo, no es necesario pasar nada como argumento porque la función opera en la cadena a la que apunta la variable.

Hay varias maneras de llamar a estos métodos auxiliares, y probablemente usará el que sea más conveniente en un contexto determinado.

En el resto de este ejercicio, normalmente usaremos el tercer ejemplo. Sin embargo, la conclusión importante es comprender que hay maneras distintas de lograr el mismo resultado cuando se escribe código. Incluso si no lo mostramos aquí, puede usar uno de los distintos estilos al llamar a estos métodos.

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
First message
Second message
Third message
```

### Paso 3: Comentar el código anterior y agregar código para llamar a funciones que modifican las mayúsculas y minúsculas de la cadena

De forma similar a la función `capitalize()`, existen funciones que cambian el uso de mayúsculas a minúsculas, o viceversa.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
message = 'hello world'
print(message.lower())
print(message.upper())

message = message.title()
print(message)
print(message.swapcase())
```

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
hello world
HELLO WORLD
Hello World
hELLO wORLD
```

### Paso 4: Comentar el código anterior y agregar el código que cuenta el número de veces que una cadena se encuentra en otra

El método `count()` proporciona un recuento del número de veces que se usa un carácter especificado en una cadena.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
location = 'Mississippi'
print(location.count('s'))
```

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
4
```

¿Y si quiere saber cuántas letras hay en una cadena? En ese caso, use un método denominado `len()`. Tenga en cuenta que no se trata de un método auxiliar en la forma en que se define, ya que funciona en algo más que solo los valores de cadena.

Comente el código anterior en este paso y agregue la siguiente lista de código:

PythonCopiar

```python
print(len('how many letters in this string?'))
```

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
32
```

### Paso 5: Comentar el código anterior y agregar el código que llama a las funciones que inspeccionan el contenido de la cadena

Llame a las funciones `startswith()` y `endswith()` para inspeccionar el contenido de una cadena de cara a averiguar si coincide con lo que esperaba que comenzara o finalizara, respectivamente.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
message = 'racecar'
print(message.startswith('r'))
print(message.startswith('a'))
print(message.startswith('ra'))

print(message.endswith('r'))
print(message.endswith('a'))
print(message.endswith('ar'))
```

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
True
False
True
True
False
True
```

### Paso 6: Comentar el código anterior y agregar el código que encuentra la posición de una cadena dentro de otra cadena

El método `find()` busca la posición de base cero de una cadena dentro de otra. En otras palabras, empezando por el número `0`, el método le indica dónde se encuentra la cadena de búsqueda. Si no encuentra la cadena, devuelve `-1`.

Puede usar la función `find()` para dividir una cadena en un lugar específico, de cara a realizar modificaciones adicionales en la cadena. En un próximo módulo, aprenderá una técnica denominada *segmentación* que puede usar la posición del carácter para recuperar parte de una cadena más larga.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
message = 'The quick brown fox jumps over the lazy dog'
print(message.find('q'))

print(message.find('t'))
print(message.find('T'))
```

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
4
31
0
```

Observe que el método `find()` distingue entre mayúsculas y minúsculas. La posición de la `t` minúscula y de la `T` mayúscula es diferente.

### Paso 7: Comentar el código anterior y agregar el código que elimina los caracteres vacíos de la izquierda, los de la derecha, o ambos

Python proporciona `lstrip()` para quitar los caracteres de espacio vacío del lado izquierdo de una cadena y la función `rstrip()` para quitarlos del lado derecho de una cadena. O también puede usar la función `strip()` para quitar ambos.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
message = '    middle     '
print('.' + message.lstrip() + '.')
print('.' + message.rstrip() + '.')
print('.' + message.strip() + '.')
```

Aquí, concatenamos una cadena literal que contiene un símbolo de punto (`.`) antes y después de la variable `message` y la llamada a una de las funciones de eliminación. Esto le permite ver cómo afecta al contenido de la cadena.

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
.middle     .
.    middle.
.middle.
```

### Paso 8: Comentar el código anterior y agregar el código que reemplaza a una cadena encontrada en otra cadena

La función `replace()` intercambia cada instancia de una cadena por una cadena diferente.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
message = 'brevity is the essence of wit'
message = message.replace('essence', 'soul')
print(message)
```

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
brevity is the soul of wit
```

### Paso 9: Comentar el código anterior y agregar código que justifique una cadena agregando caracteres de espacio vacío

Los métodos `rjust()` y `ljust()` agregan caracteres de espacio vacío a una cadena para proporcionar justificación a la derecha o a la izquierda, respectivamente.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
message = 'howdy'
print(message.rjust(20))
print(message.rjust(20, '-'))
print(message.ljust(20))
print(message.ljust(20, '-'))
```

Tenga en cuenta que, en ambos casos, puede agregar un segundo argumento. Este argumento usa un carácter diferente, en lugar de un espacio vacío, para agregar caracteres iniciales o finales, respectivamente.

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
               howdy
---------------howdy
howdy
howdy---------------
```

## Resumen

Python proporciona muchas funciones auxiliares para dar formato a las cadenas o modificar su contenido. Si necesita modificar una cadena, antes de empezar a escribir código para manipular una cadena, compruebe si puede usar una función que ya existe. Dedique unos instantes a repasar la documentación de Python o busque el método auxiliar adecuado para lograr el resultado que quiere.



# Ejercicio: usar la función de `format()` y cadenas de formato

- 6 minutos

Python ha evolucionado a lo largo de los años. Puede ver ejemplos de código que dan formato a cadenas de muchas maneras diferentes. En este ejercicio, nos centraremos en las mejoras más recientes en el formato de cadena.

La función auxiliar `format()` combina valores en una plantilla de cadena literal, sin necesidad de una concatenación de cadenas desordenada. También puede dar formato a los valores combinados para su visualización adecuada, como en el caso de números, fechas y horas.

En la versión 3.6 de Python, los desarrolladores simplificaron el método `format()` en un prefijo de cadena, la letra `f`. Esto realiza prácticamente la misma funcionalidad, con menos escritura.

### Paso 1: Crear un nuevo archivo de código para este ejercicio

Use las técnicas que ha aprendido en los módulos anteriores para agregar un nuevo archivo de código en la carpeta actual dedicada a este módulo. Por ejemplo, puede crear un nuevo archivo `exercise3.py`.

### Paso 2: Agregar el código siguiente para mostrar la característica de combinación de la función `format()`

Agregue el siguiente código al archivo nuevo.

PythonCopiar

```python
medicine = 'Coughussin'
dosage = 5
duration = 4.5

instructions = '{} - Take {} ML by mouth every {} hours'.format(medicine, dosage, duration)
print(instructions)

instructions = '{2} - Take {1} ML by mouth every {0} hours'.format(medicine, dosage, duration)
print(instructions)

instructions = '{medicine} - Take {dosage} ML by mouth every {duration} hours'.format(medicine = 'Sneezergen', dosage = 10, duration = 6)

print(instructions)
```

En este ejemplo de código, se define una cadena de formato que contiene una serie de campos de reemplazo, tal como se define en un conjunto de llaves `{}`.

En el primer ejemplo, los campos de reemplazo no contienen valores. Mediante el operador de acceso a miembros, llamamos a la función `format()`. Pasamos los valores que queremos sustituir en cada campo de reemplazo, en el orden en que aparecen.

En el segundo ejemplo, se rellenan los campos de reemplazo con un valor numérico de base cero, que tiene acceso al argumento pasado a la función `format()`. Hemos mezclado intencionadamente el orden para mostrar que puede usar los argumentos en cualquier posición de la cadena de formato. Para ello, cambie la posición ordinal en el campo de reemplazo.

En el tercer ejemplo, se rellenan los campos de reemplazo con nombres de variable. Esos mismos nombres de variable se pasan como argumentos con nombre en la función `format()`.

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
Coughussin - Take 5 ML by mouth every 4.5 hours
4.5 - Take 5 ML by mouth every Coughussin hours
Sneezergen - Take 10 ML by mouth every 6 hours
```

### Paso 3: Comentar el código anterior y agregar código para usar literales de cadena con formato o "cadenas f"

La función `format()` es eficaz y flexible. Puede lograr la misma funcionalidad, con menos escritura, mediante el uso de literales de cadena con formato, también conocidos como *cadenas f*.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
name = 'World'
message = f'Hello, {name}.'
print(message)

count = 10
value = 3.14
message = f'Count to {count}.  Multiply by {value}.'
print(message)
```

En el primer ejemplo, creamos campos de reemplazo como hicimos con la función `format()`. Rellenamos el campo de reemplazo con el nombre de la variable que queremos sustituir en la cadena de formato.

En el segundo ejemplo, la variable `count` está establecida en un valor `int` y la variable `value` está establecida en un valor `float`. La cadena de formato se encarga de la conversión del tipo de datos, por lo que no es necesario llamar a `str()` alrededor de esos valores.

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
Hello, World.
Count to 10.  Multiply by 3.14.
```

### Paso 4: Comentar el código anterior y agregar código para evaluar expresiones simples en el campo de reemplazo de una cadena f

Puede realizar prácticamente cualquier expresión dentro de un campo de reemplazo. En el ejemplo siguiente, realizaremos cálculos directamente dentro del campo de reemplazo. Quizás prefiera no hacerlo, ya que es menos legible que crear una variable temporal para realizar los cálculos. Pero es útil conocer todas las posibilidades.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
width = 5
height = 10

print(f'The perimeter is {(2 * width) + (2 * height)} and the area is {width * height}.')
```

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
The perimeter is 30 and the area is 50.
```

### Paso 5: Comentar el código anterior y agregar código para definir especificadores de formato para controlar la alineación y el relleno

Los campos de reemplazo de literal de cadena de formato tienen una sintaxis especial de especificador de formato que es prácticamente un pequeño lenguaje de programación. En este paso del ejercicio, simplemente vamos a ver aspectos superficiales de lo que es posible. Puede usar la sintaxis del especificador de formato para dar formato a números, fechas, horas, porcentajes y exponentes.

En este paso, usaremos la sintaxis del especificador de formato para agregar alineación y relleno a las cadenas de formato.

Comente el código del paso anterior y agregue la lista de códigos siguiente:

PythonCopiar

```python
value = 'hi'

print(f'.{value:<25}.')
print(f'.{value:>25}.')
print(f'.{value:^25}.')
print(f'.{value:-^25}.')
```

Un especificador de formato usa un signo de dos puntos (`:`) después del nombre de la variable, para especificar cómo se debe dar formato a ese valor.

En la primera cadena f, usamos el símbolo menor que (`<`) para alinear el texto a la izquierda de una cadena que tiene un total de 25 caracteres de ancho. La cadena `hi` ocupa dos de los 25 caracteres en total. Agregamos símbolos de punto (`.`) a la izquierda y a la derecha del campo de reemplazo para ayudarnos a ver el ancho total de la cadena.

En la segunda cadena f, usamos el símbolo mayor que (`>`) para alinear el texto a la derecha de una cadena que tiene un total de 25 caracteres de ancho.

En la tercera cadena f, usamos el símbolo de intercalación (`^`) para centrar el texto en el medio de una cadena que tiene un total de 25 caracteres de ancho.

En la cuarta cadena f, usamos de nuevo el símbolo de intercalación (`^`). Pero esta vez, anteponemos un símbolo de guion (`-`) que se va a usar en lugar de un espacio vacío para rellenar el ancho restante de la cadena.

Al ejecutar el código, debería ver el resultado siguiente:

ResultadosCopiar

```output
.hi                       .
.                       hi.
.           hi            .
.-----------hi------------.
```

Para obtener más información, consulte la [documentación de Python ](https://docs.python.org/3/library/string.html#formatspec?azure-portal=true).

## Resumen

- La función `format()` permite definir una cadena de formato (básicamente, una plantilla). La cadena contiene una serie de campos de reemplazo que se sustituyen por los argumentos que se pasan a la función.
- El nuevo literal de cadena de formato, o cadena f, reduce las pulsaciones de tecla del método `format()`. Esto le permite usar variables o expresiones en los campos de reemplazo.
- Los especificadores de formato son una sintaxis compacta que permite dar formato a números, fechas y porcentajes, así como alineación y espaciado.
