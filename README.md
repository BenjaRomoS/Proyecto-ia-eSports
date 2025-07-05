# Proyecto-ia-eSports

# Definición del Problema
El problema que seleccionamos para resolver, es la predicción de las ganancias totales de un jugador profesional de eSports.

La relevancia de este problema es multifacética, ya que para algunas organizaciones y patrocinadores, un modelo predictivo de ganancias puede servir como una herramienta inicial para identificar talentos emergentes y así optimizar las inversiones en fichajes. Para los jugadores aspirantes, ofrece una perspectiva cuantitativa sobre qué factores (como el juego elegido o el género del mismo) son más determinantes para el éxito financiero que pueden lograr en la industria. Finalmente, para los analistas de la industria de los eSports, este modelo puede ayudarles a entender las dinámicas económicas del mercado y cómo se distribuyen las ganancias entre los diferentes competidores.

# Plan de Acción
# Descripción del Dataset:
Fuente: Nuestro proyecto utilizará el dataset "eSports Earnings" obtenido de Kaggle.

Contenido: Este conjunto de datos contiene información histórica sobre las ganancias de jugadores y equipos en diversos torneos de eSports. Incluyendo variables categóricas como Game (videojuego específico), Genre (género del videojuego) y Country (nacionalidad del jugador), así como variables numéricas como TotalUSDPrize (ganancias totales del jugador).

# Modelo(s) Seleccionado(s): 
Tras analizar el conjunto de datos, decidimos utilizar dos modelos de regresión para abordar el problema, permitiendo una comparación de rendimiento:

Modelo Base: Regresión Lineal.

Modelo Avanzado: Random Forest Regressor.

# Estrategia de Evaluación y Metodología Aplicada:
El plan de trabajo se ejecutará en un notebook.ipynb y seguirá los siguientes pasos:
Análisis Exploratorio de Datos (EDA): Haremos una inspección inicial de los datos para entender la distribución de las variables, para identificar valores atípicos, visualizar correlaciones entre las ganancias y otras características, y manejar posibles datos faltantes.

Ingeniería y Selección de Características (Feature Engineering & Selection): Transformaremos variables categóricas (como Game y Genre) a un formato numérico mediante técnicas como one-hot encoding y seleccionaremos las características más relevantes para el modelo con el fin de evitar el ruido y mejorar el rendimiento.

Entrenamiento del Modelo: Dividiremos el dataset en un conjunto de entrenamiento (80%) y uno de prueba (20%). Ambos modelos (Regresión Lineal y Random Forest) se entrenarán con el conjunto de entrenamiento.

Evaluación y Testeo: Mediremos el rendimiento de los modelos sobre el conjunto de prueba utilizando métricas estándar para problemas de regresión:
Error Cuadrático Medio (MSE): Para penalizar los errores grandes.

Raíz del Error Cuadrático Medio (RMSE): Para interpretar el error en las mismas unidades que la variable objetivo (USD).

Coeficiente de Determinación (R2): Para medir qué proporción de la varianza en las ganancias es predecible a partir de las características.

Documentación: Todo el proceso, código y resultados serán documentados en el repositorio de GitHub, principalmente en el archivo README.md y en los comentarios del notebook.




# Agregar los archivos modificados al área de preparación
git add .

# Luego haces el commit con un mensaje.
git commit -m "Mensaje descriptivo"

# Finalmente haces push para subir los cambios.
git push origin main

# Para actualizar tu repositorio local con los cambios realizados en el repositorio remoto de GitHub, debes usar el comando:
git pull origin main

# Recuerda que no estas solo en el proyecto, avisa cuando cambies el nombre del repositorio.
