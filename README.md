# Taller-2---Causal-Inference / Data

Utilicen la base de datos "medicaid_did.dta".

Las variables son las siguientes:
  stfips: nombre de estado.
  year: año.
  dins: outcome.
  yexp2: año en que se aplicó el Medicare en caso de que haya recibido el programa.
  W: clave de estado.

Para los problemas 1 y 2 será necesario realizar la siguiente limpieza a los datos. Estos cambios nos permitirán analizar el Medicare como un Non-staggered DiD, contrario a la pregunta 3.
  Tire los años estrictamente mayores a 2015.
  Tire los tres estados que expandieron la ayuda en 2015.
