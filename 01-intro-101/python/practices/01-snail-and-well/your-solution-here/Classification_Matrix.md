Una matriz de confusión es una tabla que a menudo se usa para describir el rendimiento de un modelo de clasificación (o "clasificador") en un conjunto de datos de prueba para los que se conocen los valores verdaderos. La matriz de confusión en sí misma es relativamente simple de entender, pero la terminología relacionada puede ser confusa. 

Para poder llegar al resultado, necesitaríamos de un lado los datos de entrenamiento, variables predictoras (X), y de otro la variable a predecir (Y). Si realizamos las tareas de separar el conjunto de entrenamiento de forma manual o bien a través del cross-fold validation (técnica iterativa), obtendremos una matriz más grande para entrenar el modelo (generalmente 70-80%) y la restante parte para validar el resultado.

Veámos un ejemplo aplicado a un caso de uso si un paciente tiene o no una enfermedad, aplicaremos un algoritmo con función logística, donde el resultado será de tipo binario  (0= NO y 1= SI).

Ahora definamos los términos más básicos:

**Positivos Verdaderos (TP):** estos son casos en los que predijimos que sí (tienen la enfermedad) y tienen la enfermedad.
**Negativos Verdaderos (TN):** predijimos que no, y no tienen la enfermedad.
**Falsos Positivos (PF):** predijimos que sí, pero en realidad no tienen la enfermedad. (También conocido como "error tipo I")
**Falsos Negativos (FN):** predijimos que no, pero en realidad tienen la enfermedad. (También conocido como "error de tipo II")

Ahora que tenemos nuestra matriz (fig. 1), veámos el listado de ratios que podemos obtener:

Precisión: en general, ¿con qué frecuencia es correcto el clasificador?
(TP + TN) / total = (100 + 50) / 165 = 0,91
Tasa de clasificación errónea: En general, ¿con qué frecuencia está mal?
(FP + FN) / total = (10 + 5) / 165 = 0.09
equivalente a 1 menos precisión
también conocido como "Tasa de error"
Tasa positiva verdadera: cuando en realidad es sí, ¿con qué frecuencia predice sí?
TP / real sí = 100/105 = 0.95
también conocido como "Sensibilidad" o "Recuperación"
Tasa de falso positivo: cuando en realidad es no, ¿con qué frecuencia predice que sí?
FP / real no = 10/60 = 0.17
Tasa negativa verdadera: cuando en realidad no, ¿con qué frecuencia predice que no?
TN / no real = 50/60 = 0,83
equivalente a 1 menos tasa de falsos positivos
también conocido como "especificidad"
Precisión: cuando predice sí, ¿con qué frecuencia es correcto?
TP / predicho sí = 100/110 = 0.91
Prevalencia: ¿Con qué frecuencia ocurre realmente la condición sí en nuestra muestra?
real sí / total = 105/165 = 0.64