# Proyecto-ia-eSports

# Definición del Problema
El problema que seleccionamos para resolver es la predicción de las ganancias totales de un jugador profesional de eSports.

La relevancia de este problema es multifacética, ya que para algunas organizaciones y patrocinadores, un modelo predictivo de ganancias puede servir como una herramienta inicial para identificar talentos emergentes y así optimizar las inversiones en fichajes. Para los jugadores aspirantes, ofrece una perspectiva cuantitativa sobre qué factores (como el juego elegido o el género del mismo) son más determinantes para el éxito financiero que pueden lograr en la industria. Finalmente, para los analistas de la industria de los eSports, este modelo puede ayudarles a entender las dinámicas económicas del mercado y cómo se distribuyen las ganancias entre los diferentes competidores.

# Plan de Acción
Descripción del Dataset:
Fuente: Nuestro proyecto utilizará el dataset "eSports Earnings" obtenido de Kaggle.
Contenido: Este conjunto de datos contiene información histórica sobre las ganancias de jugadores y equipos en diversos torneos de eSports, incluyendo variables categóricas como Game (videojuego específico), Genre (género del videojuego) y Country (nacionalidad del jugador), así como variables numéricas como TotalUSDPrize (ganancias totales del jugador).

# Modelo Seleccionado:
Tras analizar el conjunto de datos, decidimos utilizar dos modelos de regresión para abordar el problema, permitiendo una comparación de rendimiento:

Modelo Base: Decision Tree Regressor.

Modelo Avanzado: Random Forest Regressor.

Estrategia de Evaluación y Metodología Aplicada:
El plan de trabajo se ejecutará en un notebook.ipynb y seguirá los siguientes pasos:

Análisis Exploratorio de Datos (EDA): Inspección inicial para entender la distribución de las variables, identificar valores atípicos, visualizar correlaciones y manejar posibles datos faltantes.

Ingeniería y Selección de Características: Transformación de variables categóricas (como Game y Genre) a formato numérico mediante técnicas como one-hot encoding, y selección de características relevantes para evitar ruido y mejorar el rendimiento.

Entrenamiento del Modelo: División del dataset en conjunto de entrenamiento (80%) y prueba (20%). Ambos modelos (Decision Tree y Random Forest) se entrenarán con el conjunto de entrenamiento.

Evaluación y Testeo: Medición del rendimiento sobre el conjunto de prueba usando métricas estándar para regresión:

Error Cuadrático Medio (MSE)

Raíz del Error Cuadrático Medio (RMSE)

Coeficiente de Determinación (R2)

Documentación: Todo el proceso, código y resultados serán documentados en el repositorio de GitHub, principalmente en el archivo README.md y en los comentarios del notebook.

# Justificación del Modelo
La elección de los modelos responde a una estrategia por etapas para resolver el problema de predicción de ganancias:

# Decision Tree Regressor:
Pertinencia y Ventajas: Elegimos este modelo como punto de partida por su capacidad para manejar variables categóricas y numéricas, y por su facilidad de interpretación. Los árboles de decisión permiten visualizar claramente cómo se toman las decisiones, lo que facilita entender qué variables y valores impactan las ganancias. Además, se adaptan bien a relaciones no lineales y son rápidos de entrenar.

Limitaciones: Su principal desventaja es la tendencia a sobreajustar (overfitting) los datos de entrenamiento, lo que puede afectar la generalización a nuevos datos.

# Random Forest Regressor:
Pertinencia y Ventajas: Lo seleccionamos como modelo avanzado y robusto. Al ser un conjunto (ensemble) de múltiples árboles de decisión, reduce el riesgo de sobreajuste y captura relaciones complejas y no lineales entre las variables. Es menos sensible a valores atípicos y suele ofrecer mayor precisión predictiva. Además, permite evaluar la importancia de cada característica, lo que enriquece la interpretación de los resultados.

Limitaciones: Funciona como una "caja negra" (black box), siendo menos interpretable que un árbol individual. Requiere más recursos computacionales y tiempo de entrenamiento.

# Resultados
En esta sección, se presentan los hallazgos obtenidos tras el entrenamiento y la evaluación de los modelos de regresión. Se analizaron tanto las métricas de rendimiento como los resultados gráficos para interpretar el comportamiento del modelo predictivo.

# Rendimiento de los Modelos
Se entrenaron dos modelos, un Decision Tree como modelo base y un Random Forest como modelo avanzado. A continuación se muestran sus métricas de rendimiento sobre el conjunto de prueba, el Decision Tree obtuvo un Error Cuadrático Medio (RMSE) de $394,241.62 y un Coeficiente de Determinación (R²) de 0.6491. Por su parte, el Random Forest presentó un RMSE de $398,781.26 y un R² de 0.6410. Esto indica que ambos modelos tienen un desempeño similar, con el Decision Tree ligeramente mejor en estas métricas.

# Interpretación de las métricas
El Coeficiente de Determinación (R²) fue de aproximadamente 0.65 para el Decision Tree, lo que indica que nuestro modelo es capaz de explicar cerca del 65% de la variabilidad en las ganancias de los jugadores de eSports siendo un resultado moderadamente fuerte.

El Error Cuadrático Medio (RMSE) se sitúa en torno a los $395,000 USD. Esto significa que, en promedio, las predicciones del modelo se desvían de las ganancias reales en esa cantidad. Si bien el modelo capta la tendencia general, esta cifra refleja la alta dispersión y los valores extremos en los datos de ganancias, como se observó en el análisis exploratorio.

Un hallazgo inesperado es que el Decision Tree superó marginalmente al Random Forest. Esto nos indica que, para este conjunto de datos y con la configuración de hiperparámetros utilizada, el aumento de la complejidad del modelo no nos garantiza una mejora en el rendimiento.

# Discusión de los Hallazgos Gráficos 
Los gráficos obtenidos nos dieron una visión mucho más profunda de los resultados.

Ganancias Reales vs. Predichas: El gráfico de dispersión "Random Forest: Ganancias Reales vs. Predichas"  muestra que los puntos tienden a seguir la línea diagonal roja, lo que confirma la correlación positiva entre los valores reales y los predichos. Sin embargo, también se observa que:

El modelo tiene un mejor rendimiento para el grupo de jugadores con ganancias bajas y medias (la zona más densa de puntos).

El modelo tiende a subestimar las ganancias de los jugadores con mayores ingresos (los outliers). Esto es evidente en los puntos ubicados muy a la derecha del gráfico, que se encuentran significativamente por debajo de la línea de predicción perfecta.

Para analizar con mayor detalle el rendimiento del modelo en los casos más comunes, se generó un segundo gráfico que filtra el 5% de los jugadores con mayores ganancias (superiores a $1,110,703.71 USD). En esta visualización "ampliada", se aprecia con mayor claridad la tendencia positiva y la concentración de los datos. Aun así, se mantiene una dispersión considerable alrededor de la línea de predicción perfecta, lo que confirma que, incluso para el 95% de los jugadores, predecir las ganancias exactas sigue siendo una tarea compleja.




