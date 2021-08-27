# Comentarios semana 2: Técnicas de factorización matricial para sistemas recomendadores.

**Paper:** Koren, Y., Bell, R., & Volinsky, C. (2009). Matrix factorization techniques for recommender systems. Computer, 42(8), 30-37.

El presente paper presenta técnicas filtrado colaborativo (CF) basado en técnicas de factorización matricial, en particular el método *SVD*. Estas fueron introducidas en este conexto durante la competencia del *Netflix Price*. Los modelos de factorización matricial surgen a partir de las ideas que establecen los modelos latentes, los cuales buscan transformar los datos con el objetivo de construir características o dimensiones (ocultas o latentes) que permitan entender los patrones de la data original. Estos moodelos, significan una mejora general de accuracy con respecto a los modelos (CF) basados en KNN, y además son más flexibles para incorporar información adicional como *implicit feedback*

La principal crítica que les hago a los autores es que introducen el método como uno cercano a *SVD* pero no describen por qué, ni que características o intuición comparten y menos cuales serían las bondades del método propuesto versus uno clásico. Para enmendar aquello realice una estudio más profundo de *SVD* basado principalmente en el post original de [FunkSVD](https://sifter.org/~simon/journal/20061211.html).
