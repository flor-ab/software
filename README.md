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
    - Alternativamente, un gráfico tipo gofre en lugar de uno de barras
  
