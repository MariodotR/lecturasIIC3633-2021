# Comentarios semana 1: Sistemas recomendadores basados en filtrado colaborativo

**Paper:** Schafer, J. B., Frankowski, D., Herlocker, J., & Sen, S. (2007). Collaborative filtering recommender systems. In The adaptive web (pp. 291-324). Springer Berlin Heidelberg.

Vivimos en un mundo de sobre información, por lo que se debe seleccionar que contenidos se nos presentan. El presente paper es una introducción
de los sistemas recomendadores y los principales conceptos relacionados con el filtrado colaborativo (CF). El (CF) se define como
el proceso de filtrado de items (a recomendar) usando las opiniones de otra gente. La decisión fundamental es el diseño de la selección de opiniones o ranking
más apropiados para elaborar una recomendación personalizada para un cierto usuario. Desde un punto de vista algebraico, este problema se puede describir como
la completación de una matriz de usuarios-items. Existen ratings tanto explicitos como implicitos. Las interrogantes de los sitemas (CF) que se abordan son: Dominios de aplicación
apropiados, algoritmos, tipos de ratings, evalución/comparación de sistemas recoemndadores, diseño de interfaces sociales más interactivas y explicitas, privacidad
y algunas otras preguntas abiertas.

Sobre lo planteado por los autores acerca de los usos del (CF) destacan que a la fecha, muchas investigaciones se centran en resolver tareas más específicas y más abstractas
como la recomendación de items nuevos. Sin embargo, no se ha profundizado en el diseño de tareas que tienen un objetivo claro para un cierto contexto. Todos los métodos
presentados se basan en la interacción natural usuario-item, pero no se está considerando en esta interación, el contexto situacional. Los usuarios de sistemas 
asociados a la recomendación, se encuentran en búsqueda de los mejores items sujeto su comodidad/tiempo/espacio actual. Así yo propondría la **integración del contexto,
tanto de manera explícita como implícita**. Por ejemplo; Explícitamente, el usuario podría estar buscando recomendaciones para una primera cita, un matrimonio o
simplemente un sabádo por la tarde. Implícitamente, podría afirmar que las recomendaciones dependen de la estacionalidad del año, de la hora y día en que se realiza
la consulta, y también del dispositivo desde dónde se realiza la consulta. Esto último se debería estudiar dependiendo del dominio y comunidad específica.
En un contexto típico de péliculas, podríamos encontrar patrones de comportamiento diferentes, si el usuario accede desde el televisor versus el teléfono. La  incorporación
del contexto induce un tradeoff, pues si bien ayuda a entregar recomendaciones más personalizadas, incluso en situaciones críticas como cuando existe poca información del usuario,
estas recomendaciones estarán sesgadas a las modas de la comunidad en aquellos contextos.

Dentro de los métodos probabilísticos, los autores destacan el desarrollo de técnicas de reducción de dimensionalidad o generación de clusters desde un punto de vista
probabilísto, esto es, que através de una variable latente $z$ podemos calcular la probabilidad de que un usuario $u$ califique un ítem $i$ con valor $r$:

$$ p(r|u,i)= \sum_z p(r|i,z)p(z|u) $$

Con lo cual se puede entregar como predicción el valor esperado de la calificación $r$.

