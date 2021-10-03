# Interactive recommender systems: A survey of the state of the art and future research challenges and opportunities

Este texto corresponde a una recopilación del estado de arte de los sistemas recomendadores interactivos. Particularmente, desarrolla distintos objetivos considerados importantes para lograr la aceptación de las recomendaciones, evalúa el cumplimiento de los mismos en distintas investigaciones, además de aportar con un análisis y distintas oportunidades de mejora e investigación. Particularmente, analizan los sistemas de recomendación interactivos y su soporte
para abordar los siguientes desafíos: (1) transparencia y justificación, (2) control del usuario sobre el sistema de recomendación, (3) falta de
diversidad, (4) problemas de arranque en frío y (5) adquisición y representación de información contextual. De esta manera, plantean tres contribuciones a la investigación:
1. Presentar un marco de visualización interactivo para sistemas recomendados.
2. Análisis de los sistemas de recomendación interactivos abarcados.
3. Desafíos futuros de la investigación y oportunidades para avanzar en el campo de la investigación.

Dentro del análisis de los objetivos del framework, me parece que para lograr el objetivo de transparencia que buscan cumplir, no basta con los múltiples ejemplos evidenciados en esta sección. Particularmente, en ninguno de los ejemplos se presenta alguna visualización que sea capaz de mostrar cómo funcionan los algoritmos bases de los sistemas recomendadores, de forma que el usuario pueda tener una noción de cómo se usa la información extraída de él mismo. Si bien la figura 8 intenta evidenciar la similitud entre el funcionamiento de distintos agentes, en ningún caso transparente a través de alguna figura el concepto o funcionamiento de alguno de ellos, como se hubiese esperado.
Un ejemplo que me pareció bastante bueno y evidentemente útil, fue lograr justificar recomendaciones transparentando, de manera ilustrativa y no matemática, los argumentos para la elección. Con esto me refiero especialmente a la figura 13, que genera un nexo entre el comportamiento o evaluaciones del usuario anteriores, con la recomendación elegida y sus características. Sin duda, esta es la forma más simple pero útil de visualizar el concepto, a diferencia de la mayoría de las figuras de transparencia, que podrían recurrir un profundo análisis para lograr un entendimiento íntegro de lo que buscaban reflejar.

De esta manera, en general, la sección que encontré de menor utilidad fue la de análisis. Por el nombre de esta, me esperaba, ya sea una crítica o aportes acerca de lo recopilado en las secciones anteriores. Sin embargo, considero que se presentan directamente como recopilación de si las distintas investigaciones cumplen o no cumplen el objetivo, presentando la proporción que contempla cada temática dentro de la investigación. Sin embargo, creo, a nivel personal, que esto no aporta mucho al aprendizaje o conocimiento del lector, pudiendo haberse resumido en una simple nota. En esta sección esperaba comentarios como, posibles causas del porqué tan pocas investigaciones abarcaron la diversidad (solo una de las presentadas), qué tecnologías o innovaciones están liderando actualmente la mejora continua de cada temática, etc.
Por ejemplo, otro punto que me interesó mucho fue que la efectividad de los sistemas recomendadores va más allá de la precisión empírica o numérica, sino que esta depende de la utilidad que genera al usuario, y que se puede lograr considerando los distintos objetivos del framework enumerados en el paper. Creo que, como parte del análisis, hubiese sido interesante ahondar en este tema de manera explícita a través de algunos 

Una lectura que se complementa de muy buena manera con este paper, es *Inspectability and control in social recommenders*, de los autores Knijnenburg, Bostandjiev, O'Donovan, y Kobsa (2012). Particularmente respecto al último punto que destaqué en los comentarios, y que me interesaba bastante profundizar, este texto detalla y explicita que no solo les interesa la calidad de las recomendaciones, sino también la satisfacción de los usuarios con el sistema como
entero. De esta manera, plantea los conceptos de comprensibilidad y control percibido para explicar cómo la inspeccionabilidad y
el control influye en la experiencia de los usuarios. Con estos antecedentes, los autores plantean un *framework* para realizar recomendaciones de música a partir de datos de interacciones sociales en Facebook. Este sistema analizado se denomina TasteWeights, cuyo algoritmo de recomendación consta de dos pasos: primero computa los pesos para cada amigo de Facebook, basado en la similaridad, definida por el coeficiente de correlación de Pearson. Posteriormente, se le asignan pesos a todos los ítems (musicales) de los amigos del usuario activo. De esta manera, el peso de cada recomendación viene dado por:

![image](https://user-images.githubusercontent.com/42195947/135738318-ea72068b-158d-4638-9979-3e4998aa323b.png)

Donde las recomendaciones serán en orden de estos pesos.

De esta manera, el usuario tiene un control mucho mayor, tanto pudiendo ajustar los pesos de sus amigos ítems inicialmente, como de los amigos.

Esto se ve reflejado en la siguiente figura, la cual complementa a la ya mostrada dentro del texto de He, Parra y verbert.

![image](https://user-images.githubusercontent.com/42195947/135738421-aa81b728-4dbf-489c-8fce-8cd106817e13.png)


**Referencia base:** 

- He, C., Parra, D., & Verbert, K. (2016). Interactive recommender systems: A survey of the state of the art and future research challenges and opportunities. Expert Systems with Applications, 56, 9-27.

**Referencias complementarias:** 

- Knijnenburg, B., Bostandjiev, S., O'Donovan, J., and Kobsa, A. (2012). Inspectability and control in social recommenders. RecSys'12 - Proceedings of the 6th ACM Conference on Recommender Systems.
