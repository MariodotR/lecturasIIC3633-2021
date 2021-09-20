# Comentarios semana 5: Combinando predictores

**Paper:** Jahrer, M., Töscher, A. and Legenstein, R. (2010). Combining predictions for accurate recommender systems. In Proceedings of the 16th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, 693-702. ACM.

En este trabajo se demuestra empíricamente (data set de Netflix) que la performance (RMSE) de una combinación adecuada de modelos es superior a la marginal de cada uno de ellos. Los método usados son los conocidos KNN item; KNN user; SVD y tres variaciones: AFM (asymmetric factor model), se enfoca en caracterizar a los usuarios por medio sus ítems consumidos. SVDe (SVD extended), añade característica de frecuencia de votos y GE (global effects), una factorización matricial con un diseño de característica hecho a mano. Además se condidera un modelo generativo (busca aprender la distribución de probabilidad de los datos) con neuronas estocásticas y optimizando la consistencia ("energía"), llamado RBM ( restricted bolzmann machine). 

Los modelos de mezclas utilizados fueron: LR (linear regression), el cual combina los métodos a través de pesos óptimos vía minimos cuadrados. Binned Linear Regression, para evitar muestras muy grandes realiza mezclas sobre particiones. NN (neuronal network) con SGD, sigmoide y una transformación para entregar escalar los ratings. BGBDT (bagged gradient boosted decision tree), combina una ténica de bagging (búsqueda de divisiones óptimas), gradient boosting (todos los predictores aportan aprendiendo una proporción del objetivo) y selección aleatoria de subespacios óptimos. KRR (kernel ridge regression blending), promedia modelos que invierten la matriz Grammiana con un kernel Gaussiano. KNN, promedio de una combinación por similaridad de modelos entrenados sobre un subconjunto de entrenamiento. 



*la unión hace la fuerza* 
