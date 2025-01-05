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
  -He calculado la relación entre los votos totales y el censo total para cada comunidad autónoma, mostrando cómo el porcentaje de votos sobre el censo ha evolucionado a lo largo de los años. Luego, he visualizado esta relación en un gráfico de líneas con diferentes colores para cada comunidad autónoma, utilizando una paleta de colores viridis para una mejor legibilidad.
  
- Después he animado el gráfico

- Para calcular la diferencia entre zonas rurales de urbanas, he calculado la relación entre el censo total y los votos totales por comunidad autónoma, agrupando los datos por año, mes y comunidad. La gráfica muestra cómo varía el porcentaje de votos sobre censo en el tiempo y se agrupan las comunidades autónomas en facetas según los rangos de porcentaje de votos.

Se distingue entre las zonas rurales y urbanas, asignando una categoría según el censo (rural si es menor a 10,000). Luego, se comparan los porcentajes de votos obtenidos en ambas zonas para los principales 10 partidos, y se visualiza esta distribución mediante un gráfico de barras, donde se muestran los porcentajes de votos rurales y urbanos para cada partido.
