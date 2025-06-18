![image](https://github.com/user-attachments/assets/dd536d74-e3e5-455c-9d58-a9f3d8ea0a04)
![modif port](https://github.com/user-attachments/assets/0dce16f3-3d50-4db7-adfb-71b7b3cd69e7)

Carrera: Técnico en Ciencia de Datos e Inteligencia Artificial

Bloque: Aprendizaje Automático

Docente a cargo: Mirabete, Martín

Autor: Villegas, Sabrina

# Predicción del Riesgo Operativo de Aerogeneradores en Condiciones Climáticas Extremas en Tierra del Fuego

VIDEO:  [Ver presentación en Google Drive]https://drive.google.com/file/d/1ytP0ts7k9qRphFSUDwLL4jBcXhZkfmPS/view?usp=sharing

## ENTREGA 1:
##  Objetivo General

Desarrollar un modelo de clasificación multiclase utilizando técnicas de Aprendizaje Automático supervisado, con el objetivo de predecir el nivel de riesgo operativo (bajo, medio o alto) de los aerogeneradores del Parque Eólico Río Cullen, en Tierra del Fuego, Argentina. El modelo se basará en datos operativos de turbinas y variables meteorológicas históricas, orientado a mejorar el mantenimiento preventivo y optimizar la eficiencia operativa, anticipando condiciones climáticas adversas que puedan afectar el rendimiento y la seguridad de los aerogeneradores.

## Contexto - Relevancia Local y Problema a abordar

Tierra del Fuego está dando importantes pasos en la transición energética mediante la instalación del parque eólico de Río Cullen, cercano a la ciudad de Río Grande. Sin embargo, las condiciones climáticas extremas de la región caracterizadas por fuertes vientos, bajas temperaturas y alta humedad representan desafíos operativos significativos. La aplicación de modelos predictivos basados en Aprendizaje Automático permitirá: 

1. Detectar tempranamente condiciones de riesgo.

2. Optimizar estrategias de mantenimiento predictivo.

3. Reducir costos operativos y prevenir fallas.

4. Asegurar la sostenibilidad y el rendimiento del parque eólico.

Además, el éxito de este proyecto podría servir de modelo para replicar en otras regiones del país con condiciones similares.

Este proyecto aborda un problema de clasificación multiclase supervisada como se ha comentado al principio, ya que busca etiquetar situaciones de operación de los aerogeneradores en tres niveles de riesgo: bajo, medio o alto.  Los modelos de Aprendizaje Automático a utilizar son los siguientes modelos de clasificación: 
• Random Forest: buen desempeño en datos ruidosos y de tamaño medio. 
• SVM: útil en datos bien estructurados, con alta precisión. 
• Árbol de Decisión y K-NN también serán considerados en fases exploratorias.

This study investigates a machine-learning model that classifies the operational risk level (low, medium, or high) of wind turbines exposed to extreme weather in the Río Cullen wind farm, Tierra del Fuego. Historical SCADA and meteorological data—including wind speed, active power, temperature, and wind direction—were aligned by timestamp, cleaned, balanced, and split (80%) into training and (20%) testing sets. The model was trained and evaluated using Decision Tree, Random Forest, K-Nearest Neighbors, and Support Vector Machine (SVM) algorithms. Although Random Forest reached 95 % accuracy, it under-detected the minority high-risk class; therefore, the SVM, which achieved 92 % accuracy and a macro F1-score of 0.75, was selected for its robustness to imbalanced multiclass data. The model can flag high-risk conditions early, and this enables operators to schedule preventive maintenance and avoid costly downtime in remote, harsh environments. In conclusion, predictive classification models improve the safety, reliability, and efficiency of renewable energy systems. These findings suggest that machine learning may accelerate Argentina’s energy transition by optimizing maintenance and ensuring continuous turbine operation.

## Preguntas claves
## •	¿Qué variables climáticas y operativas tienen mayor correlación con situaciones de riesgo en los aerogeneradores?
El análisis exploratorio identificó a la velocidad del viento (Wind Speed) y la potencia activa (LV ActivePower) con alta variabilidad y correlación directa. Además variables térmicas como tavg, tmin, tmax evidencian un entorno frío característico de Tierra del Fuego que puede influir en el rendimiento y riesgo operativo. Estas variables se consideran altamente relevantes debido a su impacto en el funcionamiento mecánico de las turbinas bajo condiciones extremas.

## •	¿Puede un modelo de clasificación predecir eficazmente el nivel de riesgo en condiciones reales?
Sí. los modelos desarrollados como el SVM demostraron una capacidad predictiva sólida alcanzando un F1-score macro superior a 0.75. Esta métrica, adecuada para contextos con clases desbalanceadas indica que el modelo puede predecir eficazmente los niveles de riesgo "Bajo", "Medio" y parcialmente "Alto". Aun así, se evidenció que las clases minoritarias como “Alto” siguen siendo un desafío lo que sugiere mejoras.

## •	¿Qué algoritmo de clasificación ofrece el mejor desempeño ante este tipo de datos?
El algoritmo de Máquinas de Vectores de Soporte (SVM) fue el que alcanzó el mejor equilibrio entre precisión y recall de todas las clases, según la métrica F1-score macro. Superó a modelos como Árbol de Decisión, Random Forest y K-Nearest Neighbors, lo que confirma su robustez en escenarios multiclase con distribución desigual.

## 🗂️ Estructura del Proyecto

- `data/raw/`:
  - Datos originales sin procesar.
  - **T1.csv**: Datos operativos de aerogeneradores (SCADA).
  - **export.csv**: Datos meteorológicos históricos de Río Grande.
  
- `data/processed/`:
  - Datos limpios y transformados listos para el modelado.
  - **dataset_final_limpio.csv**.

- `notebooks/`:
  - Notebooks de exploración, limpieza de datos, entrenamiento de modelos y evaluación.
  - **modelo_aerogeneradores.ipynb**

- `src/`:
  - Código fuente del proyecto (scripts para preprocesamiento y modelado).
  
- `models/`:
  - Modelos entrenados y serializados (`.pkl`, `.joblib`).

- `reports/`:
  - Visualizaciones, resultados de análisis y métricas del modelo.

- `docs/`:
  - Documentación adicional y PDFs del proyecto.

## 🛠️ Tecnologías Utilizadas

- Python 3.11
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

## 📈 Proceso de Trabajo (Planificado)

1. **Adquisición de Datos**:
   - Recopilación de datos SCADA de aerogeneradores.
   - Obtención de datos meteorológicos históricos de Meteostat.

2. **Preprocesamiento**:
   - Limpieza de datos: eliminación de valores nulos y duplicados.
   - Conversión de formatos de fecha/hora y unificación de ambos datasets.

3. **Análisis Exploratorio de Datos (EDA)** (Pendiente de realizar):
   - Análisis de la distribución de variables mediante histogramas y boxplots.
   - Análisis de correlaciones y relaciones bivariadas entre variables operativas y climáticas.
   - Análisis de series temporales para identificar tendencias y estacionalidades.
   - Tratamiento de valores atípicos y selección de variables relevantes.
   
4. **Ingeniería de Características**:
   - Generación de nuevas variables relevantes para la predicción.
   - Normalización y escalado si es necesario.

5. **Modelado**:
   - Aplicación de modelos de clasificación supervisada: Árboles de Decisión, Random Forest, etc.
   - Ajuste de hiperparámetros mediante técnicas como Grid Search.

6. **Evaluación**:
   - Evaluación del desempeño del modelo utilizando métricas como Precisión, Recall, F1-Score y Matriz de Confusión.
   - Interpretación de la importancia de características.

7. **Conclusiones**:
   - Interpretación de los resultados.
   - Recomendaciones para optimizar la gestión del riesgo operativo.

## ENTREGA 2: 

## 📄 Origen de los Datos

- **SCADA**:
  PROCESO DE RECOPILACION: Datos históricos de sensores SCADA de aerogeneradores, sobre producción y variables operativas de aerogeneradores.
  FUENTE: [Ver Página de Referencia (Kaggle Dataset)](https://www.kaggle.com/datasets/berkerisen/wind-turbine-scada-dataset)
  FECHA DE ADQUISICION: 31 de mayo de 2025
  PERIODO DE TIEMPO del DATASET: desde el año 2018

- **Meteostat**:
  PROCESO DE RECOPILACION: Extracción de datos meteorológicos historicos de Río Grande, Tierra del Fuego públicos vía plataforma web.
  FUENTE: [Ver Meteostat](https://meteostat.net/es/place/ar/rio-grande?s=87934&t=2018-01-01/2018-12-18)
  FECHA DE ADQUISICION: 31 de maayo de 2025 
  PERIODO DE TIEMPO del DATASET: desde 01-01-2018 hasta 18-12-2018

## Descripción de los Datasets 
1. Dataset Operativo (SCADA) : Contiene registros operativos de aerogeneradores, medidos a intervalos de 10 minutos,  con información sobre producción de energía y condiciones de operación. 
   Cantidad de instancias: 50,530 filas. 
   Características (columnas):
   
   ![image](https://github.com/user-attachments/assets/a87327be-8364-4f48-b567-a30004e90cff)
   
   Tipo de datos: Mixtos: datetime y float64.
   Observaciones relevantes:
                     o No hay valores nulos en el dataset después del preprocesamiento. 
                     o Se eliminaron filas duplicadas. 
                     o Se realizaron conversiones de fecha y hora al tipo datetime.

   
3. Dataset Meteorológico : Contiene datos climáticos históricos de Río Grande, Tierra del Fuego, obtenidos de Meteostat.org, con variables meteorológicas diarias.
  Cantidad de instancias: 352 días.
  Características (columnas):

  ![image](https://github.com/user-attachments/assets/143792de-3db3-4610-b764-e5578678114c)
  
  Tipo de datos: datetime y float64. 
  Observaciones relevantes: 
                   o Se eliminaron variables con muchos valores nulos como snow y tsun. 
                   o Se eliminaron duplicados. 
                   o Se estandarizaron los tipos de datos.

NOTAS DE PREPROCESAMIENTO: 
- Se convirtieron las columnas de fecha y hora a datetime
- Se eliminaron duplicados en ambos datasets
- Se eliminaron valores nulos de columnas irrelevantes para el modelo
- Se unificaron ambos datasets por fecha (Date/time y date) para su posterior analisis y modelado correcto


## 📂 Acceso a los Datos Originales

Los datasets utilizados en este proyecto están disponibles en:

- Carpeta: `data/raw/`
  - `T1.csv`: Dataset SCADA de aerogeneradores.
  - `export.csv`: Dataset meteorológico histórico.

> ⚠️ **Nota importante:** Debido al tamaño de los archivos no se pueden visualizar directamente pero están correctamente almacenados en el repositorio y disponibles para su descarga.

## Conclusiones
En el presente trabajo se desarrolló un análisis de clasificación multiclase sobre datos operativos y meteorológicos de aerogeneradores, orientado a predecir el nivel de riesgo operativo (Bajo, Medio o Alto) bajo condiciones climáticas extremas. Se entrenaron y evaluaron cuatro modelos de clasificación: Árbol de Decisión, Random Forest, SVM y K-Nearest Neighbors. A través de un enfoque basado en la métrica F1-Score macro, que es especialmente adecuada para contextos de clases desbalanceadas, el modelo SVM se destacó por alcanzar el mejor equilibrio entre precisión y exhaustividad en las predicciones superando en desempeño a los otros modelos evaluados. No obstante, se identificó que la predicción de las clases minoritarias, en particular la clase "Alto", continúa siendo un desafío. En consecuencia, se sugiere como línea de trabajo futura la optimización de hiperparámetros mediante técnicas de búsqueda como GridSearchCV, así como la implementación de métodos de balanceo más sofisticados como SMOTE-Tomek Links o ADASYN.
Estas mejoras potenciales podrían incrementar significativamente la capacidad predictiva del modelo, contribuyendo al objetivo de optimizar el mantenimiento preventivo de los aerogeneradores en contextos climáticos adversos y, por ende, mejorar la eficiencia operativa y la seguridad en el parque eólico.

## Cierre del Análisis
el análisis realizado permitió identificar el modelo más adecuado para la predicción del riesgo operativo de aerogeneradores en condiciones climáticas extremas. El modelo SVM demostró un desempeño superior en términos de balance entre precisión y recall para las distintas clases, destacándose como la mejor alternativa dentro de los algoritmos evaluados.
A pesar de los resultados alentadores, se identificaron oportunidades de mejora, particularmente en la clasificación de las clases minoritarias. La aplicación de técnicas avanzadas de ajuste de hiperparámetros y métodos de balanceo más sofisticados constituyen líneas de trabajo futuro recomendadas.
Estos avances no solo permitirán mejorar la capacidad predictiva del modelo, sino que también aportarán valor en la optimización del mantenimiento preventivo, aumentando la confiabilidad y eficiencia del parque eólico analizado.


