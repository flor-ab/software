# software

Terminar depuración y primera pregunta:
  PARA PILLAR LOS PARTIDOS QUE FALTABAN
  - he añadido \\b antes y después de cada palabra que quería mirar para que PARTIDO MINERO POPULAR no coincidiera con PP (es un ejemplo, pero pasaba)
  - bloque nacionalista galego // partido de la ciudadania y con tilde // psoe 
  - Cambio a str_detect para los partidos múltiples porque algunos (EZKER BATUA) aparecía seguido de guiones y no lo podía captar
  - Se incluyen partidos formados por coaliciones, p.ej. para esquerra republicana de catalunya

    SOBRE CAMBIO REAGRUPAR VOTOS
    - Con el método anterior se suman mesas, votos en blanco, censos, etc. Si no hubiera filas duplicadas de pej EH - BILDU daría igual, pero al no ser el caso (ya que en los datos originales
      había varias filas por cada partdio de los que son ahora EH - BILDU) estos valores, aunque no los votos totales, se inflan

    TERMINAR DE AJUSTAR DATOS ENCUESTAS
    - Quito aquellas con un día o menos de trabajo de campo y las que fueron a pie de urna

    CREACIÓN DE TABLA_MAESTRA
    - Para tener los nombres de los municipios y sus códigos de municipios, además de las siglas de cada partido
    
    PRIMERA PREGUNTA
    - Tengo los resultados en forma de tabla
    - Para mañana pretendo hacer un gráfico:
          - Por cada elección un gofre
          - Un cuadrado por cada municipio con más de 100.000 hab.
          - Color del cuadrado dependiente de qué partido recibió más votos

    SEGUNDA PREGUNTA
    - Aprovecho lo que hizo jazmín para la primera pregunta y repito los gráficos de gofre. Podemos buscar otros gráficos si queréis innovar
   
    TERCERA PREGUTNA
    - No estoy muy convencida de como está, os lo subo para que podáis seguir avanzando pero voy a ir dándole una vuelta en paralelo.
    - Básicamente he calculado el porcentaje de votos de cada partido en cada elección y el porcentaje de votos de cada partido en las encuestas de cada elección. Con eso, obtengo un error absoluto para ver en cuántos puntos se pasan las encuestas. He hecho un gráfico con los resultados de las elecciones y comaprado con los datos que hay de resumen en Wikipedia y parece que está OK. Para los errores, he hecho boxplot. Me gustaría darle una vuelta porque no me aprece que esté cerrada del todo la pregunta, y además le voy a preguntar a javi por lo de la intención de voto que comentamos ayer.
    - Alternativamente, un gráfico tipo gofre en lugar de uno de barras


  CUARTA PREGUNTA
  - Se ha calculado la correlación entre el censo y los votos totales por partido utilizando la función cor. El resultado es correlación de 0.8238768, indicando una fuerte relación positiva entre ambas variables.
la relación entre los votos totales por partido y el censo, ha obtenido un valor de 0.1747194. Esto indica que, en promedio, los votos totales representan aproximadamente el 17.47% del censo.
El modelo tiene un ajuste bastante bueno, con un R-cuadrado de 0.6788, lo que sugiere que más del 67% de la variabilidad de los votos totales por partido es explicada por el censo.
- Se observa una dispersión de los datos, aunque parece ver un parece haber un patrón no aleatorio en los residuos, especialmente en los valores extremos del eje  x (valores ajustados). Esto puede indicar que la relación entre el censo y los votos no es completamente lineal y que podría haber heterocedasticidad. También es visible que hay puntos que parecen muy alejados del eje horizontal (residuos grandes, tanto positivos como negativos).

- Se filtraron los datos para incluir únicamente las zonas clasificadas como "rural" y "semi_rural". Luego, se calcularon los porcentajes de votos por partido en estas zonas, agrupando los datos por partido y sumando los votos totales para cada uno. Posteriormente, se calculó el porcentaje de votos que representa cada partido sobre el total de votos en las zonas rurales.


