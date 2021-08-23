# Collaborative filtering recommender systems

**Texto:** Schafer, J. B., Frankowski, D., Herlocker, J., & Sen, S. (2007). Collaborative filtering recommender systems. In The adaptive web (pp. 291-324). Springer Berlin Heidelberg.

La lectura referenciada, introduce aspectos fundamentales respecto a los Sistemas de recomendación de filtrado colaborativo. En particular, lo define como el proceso de filtrar y evaluar ítems mediante opiniones de otras personas. Nos muestra los algoritmos base para entenderlos, además de comparalos con sistemas alternativos, como el *Content-Bases Filtering*. Además, define distintos métodos de evaluación, aplicaciones a la vida cotidiana, entre otros puntos.

Respecto a las sensaciones luego de leer el paper, consideré muy interesante y apropiada la manera en que se relacionan o se aprovechan distintos comportamientos intrínsecos del ser humano, como la interacción social o el simple hecho de compartir opiniones, en la ciencia de la computación. En particular, para alguien que no necesariamente tiene experiencia previa en sistemas recomendadores, resulta muy agradable comenzar entendiendo la lectura con una contextualización donde se relacionan en cada momento la justificación teórica detrás de las técnicas mostradas, con situaciones cotidianas de interacción social, de las cuales probablemente todo lector se siente identificado, y se facilita el entendimiento de los algoritmos a aplicar. En el mismo sentido, es relevante destacar que el texto es capaz de especificar y delimitar las distintas técnicas y rasgos respecto al *collaborative filtering*, acompañando las explicaciones técnicas de descripciones no necesariamente técncias, que ayudan a guiar la lectura y el entendimiento.

Dicho esto, el paper también presenta puntos débiles que resaltan incluso para un lector principiante en el tema. En primer lugar, al explicar el *Item-Based Nearest Neighbor Algorithms*, se presenta la siguiente fórmula:

![image](https://user-images.githubusercontent.com/42195947/130527787-5ac27c70-d139-47bd-9f49-b9d340e72c57.png)

la cual presenta un error, pues el término r_ui es una constante en dicha fórmula, y su valor debería corresponder a r_uj, explicado por los ítems similares a i. Este es un paso fundamental en el entendimiento del algoritmo, por lo que considero que es un error bastante importante. En caso de que efectivamente esté correcta la fórmula, entonces la explicación no es de la calidad suficiente para relacionarlo con las fórmulas matemáticas.

Por otro lado, se describen los problemas que presentan estos tipos de algoritmos. Si bien son variados los puntos abordados, me llamó la atención en particular el problema del sesgo en las recomendaciones. Se menciona que solo algunos usuarios concentran la mayor parte de los ratings entregados, mientras que la gran masa posee pocas o nulas calificaciones. Esto podría describirse como la distribución Beta, como se puede ver en la figura adjunta, donde la mayor parte del área está centrada por solo una fracción pequeña del eje x, que en este caso serían las personas.

![image](https://user-images.githubusercontent.com/42195947/130527764-a61da1c8-853f-4991-991c-6431ca9035e2.png =100x20)

A mí particularmente me ha tocado trabjar en modelos predictivos donde el sesgo es un tema primordial, al mismo nivel que la precisión de las predicciones. Por lo mismo, me llamó la atención que en este paper no se destacara la importancia de este problema, ni mucho menos se dieran indicios de posibles soluciones o referencias en las que se aborde en mayor profundidad.

