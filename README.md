# Sesgos en Noticias
## Descripción del corpus utilizado
Para este ejercicio se utilizó el dataset Spanish News Classification, 
que contiene noticias reales en español distribuidas en distintas categorías 
temáticas (como política, economía, sociedad, deportes, entre otras). En total, el 
corpus cuenta con más de 15.000 noticias, lo que permite analizar el lenguaje 
periodístico desde diferentes enfoques. Durante la exploración se observaron 
tendencias en el uso de ciertos términos asociados al género y al estatus 
socioeconómico, lo cual motivó el análisis de posibles sesgos en las relaciones 
semánticas entre palabras.

## Palabras seleccionadas y razones

Las palabras elegidas fueron: hombre, mujer, rico, rica, pobre.
Estas se seleccionaron porque permiten explorar dos ejes sensibles de 
sesgo comunes en el discurso mediático: Género: comparación entre “hombre” 
y “mujer”.

Condición económica: comparación entre “rico/rica” y “pobre”.
El objetivo fue observar si los embeddings (representaciones vectoriales 
del lenguaje) reflejan diferencias en cómo estos conceptos se utilizan en el corpus.

## Visualización e interpretación
En el siguiente mapa 2D de embeddings (PCA) se muestran las 
relaciones entre los términos seleccionados:

<img width="714" height="548" alt="image" src="https://github.com/user-attachments/assets/4d1f96b1-911f-467e-889c-154dc2d32e61" />

Se observa que “hombre” y “rico” aparecen próximos entre sí, mientras que “mujer” y “rica” 
se ubican más alejadas. Además, “pobre” ocupa una posición separada, lo que indica diferencias 
en los contextos donde se utilizan estas palabras en las noticias.

## Observaciones de sesgo

El resultado sugiere la presencia de sesgos de género y clase:
“Rico” se asocia más con lo masculino (“hombre”), mientras que “rica” y “mujer” 
aparecen en espacios semánticos distintos, lo que puede reflejar un uso 
desigual o connotaciones diferentes según el género.

“Pobre” está distanciado de ambos géneros, posiblemente relacionado con 
contextos negativos o marginales en el discurso periodístico.

Estos patrones indican que el corpus de noticias reproduce estereotipos 
sociales que luego pueden trasladarse a los modelos de lenguaje.

## Reflexión ética

El sesgo en modelos de procesamiento de lenguaje natural (PLN) es un problema 
serio cuando se aplica a noticias, porque influye en la forma en que las personas reciben 
y perciben la información. Si un modelo refuerza asociaciones entre “hombre” y “riqueza”, 
o entre “mujer” y contextos distintos o menos favorables, puede distorsionar la realidad 
social y perpetuar desigualdades.

## Conclusión

El análisis muestra cómo los modelos de lenguaje pueden reflejar y amplificar sesgos presentes en los datos reales. La ética en inteligencia artificial requiere revisar críticamente los corpus y aplicar estrategias de mitigación para asegurar un tratamiento justo y responsable del lenguaje en el ámbito informativo.
