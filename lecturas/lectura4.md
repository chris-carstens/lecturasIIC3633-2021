# Content-Based Recommendation Systems

Este paper secciona los puntos importantes para elaborar un sistema recomendador basado en contenido, con un enfoque principal en texto.
Se presenta el uso de datos estructurados y no estructurados, para representar un ítem. 
Particularmente, en el caso de los datos no estructurados (por ejemplo, entradas de texto irrestrictas), se plantean limitaciones 
que pueden darse en su uso, por ejemplo, al convertir la data no estructurada en estructurada. 
Aquí, utilizando estadísticas de frecuencia de aparición de palabras en el texto, se obtiene una representación que no captura el contexto en que las palabras fueron usadas, lo que puede llevar a una interpretación errónea.
Se da el ejemplo de que, si escribo que una parrilla no tiene ningún menú vegetariano, la aparición de esa palabra puede concluir en exactamente lo contrario. 
Por lo mismo también existen variantes que utilizan palabras contiguas para formar pesos en las apariciones, y no palabras individuales como el ejemplo mencionado.

En el apartado de *Learning a User model*, se explica de manera general la forma en que se modelan las preferencias del usuario, quedando bastante claro en términos 
conceptuales, tanto mediante el uso de ratings explícitos como implícitos. Sin embargo, en términos empíricos o de implementación, no se explica cómo se arma el perfil del 
usuario con el cual posteriormente se calculará la similitud respecto a los ítems, o el *embedding* que lo representa y sus formas de calcularlo. 
Además, creo que habría sido interesante analizar cómo se determina empíricamente la relevancia de los ratings, ya sean directos o indirectos. 
Analizar la sensibilidad según distintos márgenes de relevancia, o cómo se ven impactados los resultados, más allá de definir como relevante el simplemente haber 
interactuado con un ítem.
Por otro lado, al final de este apartado retoman el punto del uso de campos de texto libre, que implica una fuente de datos no estructurada, la cual se convierte posteriormente en fuentes de datos estrcturados mediante mecanismos no mencionados explícitamente en este punto. 
Sin embargo, no se retoman los problemas que generan estos datos y que fueron inicialmente planteados, por lo que genera la duda de si efectivamente se puede lograr un sistema recomendador eficiente con este tipo de datos, 
o si existen técnicas más avanzadas para resolverlo.

A continuación, se entregan ejemplos de algoritmos utilizados por sistemas recomendadores, particularmente enfocados en aquellos útiles para clasificar texto. 
Este apartado lo encuentro realmente útil, permitiendo al lector concluir qué métodos pueden ser los más apropiados en este contexto. 
Particularmente, concluye que el SVM es especialmente útil dentro de los clasificadores lineales, para clasificaciones de texto. 
Por otro lado, introduce y muestra de manera convincente el método de Naïve Bayes, y lo recalca como especialmente útil para este caso, 
a pesar de que se viole el supuesto de independencia de clases cuando es utilizado en el contexto de clasificador de texto. 
Incluso, entrega una referencia y explicación respecto al porqué esto ocurriría. 
Sin duda alguna, creo que estos apartados son especialmente útiles para un lector que busque una implementación empírica en el contexto de clasificadores o recomendaciones en base a contenido de texto.

Dichos estos puntos respecto al paper, considero que otro texto que se complementa de muy buena manera, es el de Celma y Herrera (2008). Particularmente, dado que en el paper leído no se hablan de las métricas para evaluar un sistema recomendador basado en contenido, la sección de este paper complementario, llamada *Item-Centric Evaluation*, permite definir empíricamente distintas métricas para analizar las propuestas. En este punto, plantea métricas asociadas a la navegación, como la *average shortest path*, que mide la distancia entre dos ítems, y a la conectividad, como el *degree distribution*, que es el número de ítems similares a un ítem de referencia. 

**Referencia base:** 
- Pazzani, M. J., & Billsus, D. (2007). Content-based recommendation systems. In The adaptive web (pp. 325-341).

**Referencias complementarias**
- Celma, Ò., & Herrera, P. (2008). A new approach to evaluating novel recommendations. Proceedings of the 2008 ACM Conference on Recommender Systems - RecSys  ’08. doi:10.1145/1454008.1454038 
