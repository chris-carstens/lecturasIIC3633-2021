# Deep Learning based Recommender System: A Survey and New Perspectives

Este artículo entrega una recopilación e investigación del estado de arte de los sistemas recomendadores
basados en aprendizaje profundo. Particularmente, muestra cómo es posible integrar estos conceptos y herramientas
de aprendizaje profundo a los métodos tradicionales, como también presentando métodos novedosos y que entregan
una perspectiva nueva a los clásicos sistemas recomendadores introducidos.

Una temática que particularmente me llamó la atención, por el hecho principal que obliga a hacer una asociación del funcionamiento tradicional con las técnicas de aprendizaje profundo, es la de *Neural Collaborative Filtering* (NCF). Primero, tomando en cuenta el método tradicional de Factorización Matricial en los sistemas recomendadores, donde se generan *embeddings* tanto para el usuario como para los ítems, que posteriormente son multiplicados o trabajados de manera lineal con una transformación lineal, resulta interesante asociar o entender que este podría ser visto como un caso específico del NCF, que se puede apreciar en la siguiente figura proveniente del artículo:

![image](https://user-images.githubusercontent.com/42195947/134971785-91261b70-07a9-42ea-b24e-73c099cc71b6.png)

Paritcularmente, la transformación lineal que se realizar mediante la multiplicación de los vecotes lineales con una matriz, en este caso se transforma en una transformación no lineal, dada por la *Neural CF Layer* que se aprecia en la figura. Esto demuestra, como también en los siguientes ejemplos del texto, que los conceptos no son enteramente distantes, sino más bien, son distintos medios para realizar el mismo fin,

A través de esta nueva versión del método de MF, usando aprendizaje profundo, la clálica función para predecir el rating en factorización matricial, en función de ambos vectores latentes,
se transforma esta vez a través de una función *f* representada por el perceptrón multicapa:

![image](https://user-images.githubusercontent.com/42195947/134972571-a359547a-7ee4-4bfa-93a9-51f0bd9eee81.png)

A pesar de las completas referencias, me hubiese gustado abarcar un poco más las desventajas o requisitos de cada método de aprendizaje profundo en específico, como el recíen mostrado. Particularmente, con el enfoque comparativo de métodos tradicionales vs métodos de aprendizaje profundo, pues dadas condiciones conocidas como la necesidad de de grandes cantidades de datos o sensibilidad de los hiperparámetros en estos últimos, resulta importante conocer el umbral dentro del cual un método de aprendizaje profundo puede empeorar los resultados frente a un método tradicional, dada la impropicia que podría surgir dentro del contexto en que se implemente.

Una referencia que me pareció interesante dentro de lo mencionado, y de particularmente el problema del *cold-start* que predomina en los métodos de filtrado colaborativo, esencialmente ante la escasez de datos, es la entregada por Bansal, Belanger y McCallum (2016) en el paper denominado Ask the GRU: Multi-task Learning for
Deep Text Recommendations. Como el aprendizaje produndo es conocido por su voracidad de datos, se recalca este problema del *cold-start*. Para lo mismo, este paper, en primer lugar, presenta distintas opciones en la bibliografía que buscan aterrizar estos métodos para mejorar este problema, como el uso de un codificador automático de *bag of words* en
el modelo dentro de un marco bayesiano (para recomendaciones en base a texto), el uso de redes neuronales para conocer la función de similitud entre el usuario y los factores latentes del elemento, entre otros métodos. El paper entonces, propone un nuevo enfoque denominado *Multi-task learning*, que mejora las métricas dentro del problema de *cold-start* para las recomendaciones por texto.

**Referencia base:** 

- Zhang, S., Yao, L., Sun, A., & Tay, Y. (2019). Deep learning based recommender system: A survey and new perspectives. ACM Computing Surveys (CSUR), 52(1), 1-38.

**Referencias complementarias:** 

- Bansal, T., Belanger, D., & McCallum, A. (2016). Ask the gru: Multi-task learning for deep text recommendations. In Proceedings of the 10th ACM Conference on Recommender Systems (pp. 107-114).

