### Taller-2---Causal-Inference / Data
#   PARTE 2
Utilicen la base de datos "medicaid_did.dta".

Las variables son las siguientes:

- `stfips`: nombre de estado.
- `year`: año.
- `dins`: outcome.
- `yexp2`: año en que se aplicó el Medicaid en caso de que haya recibido el programa.
- `W`: clave de estado.

Para los problemas 1 y 2 será necesario realizar la siguiente limpieza de los datos. Estos cambios nos permitirán analizar el Medicaid como un Non-staggered DiD, contrario a la pregunta 3.
  -Tire los años estrictamente mayores a 2015.
  -Tire los tres estados que expandieron la ayuda en 2015.

# PARTE 3

Utilicen la base de datos "Muralidharan_Prakash_2013.csv".

Las variables son las siguientes:

- `enrollment_secschool`: outcome; 1 si el individuo está inscrito en secundaria.
- `treat1`: 1 si tiene 14 o 15 años (cohorte expuesta); 0 si tiene 16 o 17 años (no expuesta).
- `female`: 1 si es mujer.
- `bihar`: 1 si vive en Bihar (estado con el programa); 0 si vive en Jharkhand.
- `village`: clave de aldea.
- `hhwt`: ponderador del hogar.
- Controles del hogar: `hhheadmale` (jefe del hogar hombre), `hhheadschool` (escolaridad del jefe del hogar), `sc`, `st`, `obc` (casta o tribu), `hindu`, `muslim`, `electricity`, `media`, `land`, `bpl` (debajo de la línea de pobreza).
- Controles de la aldea: `middle` (escuela de nivel medio), `postoff` (oficina de correos), `bank` (banco), `lcurrpop` (log de la población).

Antes de empezar será necesario realizar la siguiente limpieza de los datos:

- Quédense solo con las observaciones con `treat1` no faltante (individuos de 14 a 17 años; 30,295 observaciones).
- Recodifiquen como faltante el valor 99 de `hhheadschool`.

Para todas las estimaciones utilicen `hhwt` como ponderador y agrupen los errores estándar a nivel de `village`.
