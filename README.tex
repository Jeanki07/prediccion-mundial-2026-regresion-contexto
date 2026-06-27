MODELO MUNDIAL 2026 - COMPETENCIA DE MODELOS Y CONTEXTO COMPETITIVO

Este proyecto construye un modelo predictivo para estimar resultados de partidos del Mundial 2026.
El sistema entrena varios modelos de regresión, predice goles esperados para cada equipo y 
luego ajusta esas predicciones usando contexto competitivo de fase de grupos.

El modelo genera:

- Competencia entre modelos.
- Mejor modelo según MAE promedio.
- Predicciones de goles esperados.
- Probabilidades de victoria local, empate y victoria visitante.
- Top 10 marcadores más probables.
- Ajuste por contexto competitivo.
- Gráficos y tablas por partido.

============================================================
ESTRUCTURA ESPERADA
============================================================

modelo regresion/
│
├── data/
│   ├── results.csv
│   ├── fifa_ranking.csv
│   ├── elo_ranking.csv
│   ├── fixtures_2026.csv
│   ├── fixtures_2026_group_stage.csv
│   ├── data_modelo.csv
│   ├── fixtures_modelo.csv
│   └── fixtures_contexto_grupos.csv
│
├── outputs/
│   ├── competencia_modelos.csv
│   ├── mejor_modelo.txt
│   ├── modelo_home.pkl
│   ├── modelo_away.pkl
│   ├── predicciones_fixture.csv
│   ├── predicciones_todos_modelos.csv
│   ├── top10_marcadores.csv
│   ├── top10_todos_modelos.csv
│   └── graficos generados
│
├── 00_actualizar_results_mundial.py
├── 01_construir_data_modelo.py
├── 02_entrenar_predecir_modelos.py
├── 03_visualizar_partido_modelos.py
├── 04_mostrar_modelo_final.py
├── 05_crear_contexto_grupos.py
├── requirements.txt
└── README.txt

============================================================
REQUISITOS
============================================================

Instalar las librerías necesarias:

pip install -r requirements.txt

Contenido mínimo de requirements.txt:

numpy
pandas
scipy
scikit-learn
matplotlib
joblib

============================================================
FLUJO DE EJECUCIÓN
============================================================

1) Entrar a la carpeta del proyecto:

cd "/home/jeanki/Escritorio/modelo regresion"

2) Actualizar resultados reales del Mundial:

python 00_actualizar_results_mundial.py

Este script actualiza:

data/results.csv

3) Construir la data del modelo:

python 01_construir_data_modelo.py

Genera:

data/data_modelo.csv
data/fixtures_modelo.csv

4) Crear contexto competitivo de fase de grupos:

python 05_crear_contexto_grupos.py

Genera:

data/fixtures_contexto_grupos.csv

Este archivo calcula variables como:

- puntos actuales del grupo
- posición actual
- mejor posición posible
- peor posición posible
- si el equipo necesita ganar
- si necesita resultado
- si pelea el primer lugar
- si puede caer a tercer lugar
- si puede rotar
- si necesita diferencia de goles

5) Entrenar modelos y generar predicciones:

python 02_entrenar_predecir_modelos.py

Genera:

outputs/competencia_modelos.csv
outputs/mejor_modelo.txt
outputs/modelo_home.pkl
outputs/modelo_away.pkl
outputs/predicciones_fixture.csv
outputs/predicciones_todos_modelos.csv
outputs/top10_marcadores.csv
outputs/top10_todos_modelos.csv

6) Visualizar un partido específico:

python 03_visualizar_partido_modelos.py

Este script permite visualizar un partido por MATCH_ID.

Dentro del archivo se puede cambiar:

MATCH_ID = 60

por el número del partido que se desea analizar.

El script muestra:

- partido seleccionado
- equipo local
- equipo visitante
- contexto competitivo
- comparación de predicciones por modelo
- top 10 marcadores por modelo
- gráfico comparativo de probabilidades
- gráfico pastel del modelo ganador
- tabla visual del contexto competitivo

7) Mostrar el modelo final:

python 04_mostrar_modelo_final.py

Este script muestra:

- modelo ganador
- coeficientes si el modelo es lineal
- importancia de variables si el modelo lo permite
- ecuación o interpretación del modelo final

============================================================
ORDEN CORRECTO DE EJECUCIÓN
============================================================

python 00_actualizar_results_mundial.py
python 01_construir_data_modelo.py
python 05_crear_contexto_grupos.py
python 02_entrenar_predecir_modelos.py
python 03_visualizar_partido_modelos.py
python 04_mostrar_modelo_final.py

============================================================
DESCRIPCIÓN DEL MODELO
============================================================

El sistema entrena varios modelos para predecir goles esperados:

- Regresión Lineal
- Ridge
- Random Forest Regressor
- Gradient Boosting Regressor
- Poisson Regressor

Cada modelo se entrena dos veces:

- modelo_home: predice goles del equipo local
- modelo_away: predice goles del equipo visitante

Luego, los goles esperados se transforman en probabilidades usando una matriz 
de Poisson con ajuste Dixon-Coles.

============================================================
VARIABLES PRINCIPALES DEL MODELO BASE
============================================================

Las variables principales usadas para el entrenamiento son:

- home_gf12
- home_ga12
- home_pts12
- home_prev_matches
- away_gf12
- away_ga12
- away_pts12
- away_prev_matches
- diff_fifa
- diff_elo
- h2h
- neutral
- home_advantage

Estas variables representan forma reciente, goles, puntos, ranking FIFA, Elo, 
historial directo y localía.

============================================================
CONTEXTO COMPETITIVO
============================================================

El contexto competitivo no se usa directamente en el entrenamiento porque la data histórica 
no contiene esas variables.

Se aplica como ajuste posterior sobre los goles esperados.

Primero, el modelo predice:

lambda_home_base
lambda_away_base

Luego el contexto ajusta:

lambda_home_final = lambda_home_base * factor_contexto_home
lambda_away_final = lambda_away_base * factor_contexto_away

Finalmente, con las lambdas ajustadas se calculan:

- probabilidad de victoria local
- probabilidad de empate
- probabilidad de victoria visitante
- top 10 marcadores más probables

============================================================
EJEMPLO DE INTERPRETACIÓN DEL CONTEXTO
============================================================

Si un equipo necesita ganar, su factor contextual puede ser mayor que 1.

Ejemplo:

factor_contexto_home = 1.15

Esto significa que el contexto aumenta la intensidad ofensiva estimada del equipo local.

Si un equipo ya está clasificado y no pelea el primer lugar, puede tener:

factor_contexto_home = 0.90

Esto significa que el contexto reduce su intensidad ofensiva por posible rotación.

Si no hay ajuste contextual:

factor_contexto_home = 1.00

============================================================
SALIDAS PRINCIPALES
============================================================

competencia_modelos.csv:
Contiene el rendimiento de cada modelo usando MAE, RMSE, R2 y accuracy del resultado.

mejor_modelo.txt:
Guarda el nombre del modelo ganador según MAE promedio.

predicciones_todos_modelos.csv:
Contiene predicciones de todos los modelos para todos los partidos.

predicciones_fixture.csv:
Contiene las predicciones del mejor modelo.

top10_todos_modelos.csv:
Contiene los 10 marcadores más probables por partido y por modelo.

top10_marcadores.csv:
Contiene los 10 marcadores más probables del mejor modelo.

============================================================
NOTA FINAL
============================================================

El modelo no garantiza el resultado real de los partidos.
Su objetivo es estimar probabilidades usando información histórica, forma reciente, 
ranking, Elo, historial y contexto competitivo del grupo.
