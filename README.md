![image](https://github.com/user-attachments/assets/dd536d74-e3e5-455c-9d58-a9f3d8ea0a04)
![modif port](https://github.com/user-attachments/assets/0dce16f3-3d50-4db7-adfb-71b7b3cd69e7)

Carrera: Técnico en Ciencia de Datos e Inteligencia Artificial

Bloque: Aprendizaje Automático

Docente a cargo: Mirabete, Martín

Autor: Villegas, Sabrina

# Predicción del Riesgo Operativo de Aerogeneradores en Condiciones Climáticas Extremas en Tierra del Fuego

##  Objetivo General

Desarrollar un modelo de clasificación multiclase utilizando técnicas de Aprendizaje Automático supervisado, con el objetivo de predecir el nivel de riesgo operativo (bajo, medio o alto) de los aerogeneradores del Parque Eólico Río Cullen, en Tierra del Fuego, Argentina. El modelo se basará en datos operativos de turbinas y variables meteorológicas históricas, orientado a mejorar el mantenimiento preventivo y optimizar la eficiencia operativa, anticipando condiciones climáticas adversas que puedan afectar el rendimiento y la seguridad de los aerogeneradores.

## Contexto - Relevancia Local y Problema a abordar

Tierra del Fuego está dando importantes pasos en la transición energética mediante la instalación del parque eólico de Río Cullen, cercano a la ciudad de Río Grande. Sin embargo, las condiciones climáticas extremas de la región caracterizadas por fuertes vientos, bajas temperaturas y alta humedad— representan desafíos operativos significativos. La aplicación de modelos predictivos basados en Aprendizaje Automático permitirá: 

1. Detectar tempranamente condiciones de riesgo.

2. Optimizar estrategias de mantenimiento predictivo.

3. Reducir costos operativos y prevenir fallas.

4. Asegurar la sostenibilidad y el rendimiento del parque eólico.

Además, el éxito de este proyecto podría servir de modelo para replicar en otras regiones del país con condiciones similares.

Este proyecto aborda un problema de clasificación multiclase supervisada, ya que busca etiquetar situaciones de operación de los aerogeneradores en tres niveles de riesgo: bajo, medio o alto.  Los modelos de Aprendizaje Automático a Utilizar Se consideran los siguientes modelos de clasificación: 
• Random Forest: buen desempeño en datos ruidosos y de tamaño medio. 
• XGBoost: eficiente y potente, aunque requiere ajustes. 
• SVM: útil en datos bien estructurados, con alta precisión. 
• Árbol de Decisión y K-NN también serán considerados en fases exploratorias.


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

## 📄 Origen de los Datos

- **SCADA**: Datos históricos de sensores SCADA de aerogeneradores, sobre producción y variables operativas de aerogeneradores. [Ver Página de Referencia (Kaggle Dataset)](https://www.kaggle.com/datasets/berkerisen/wind-turbine-scada-dataset)

- **Meteostat**: Datos meteorológicos históricos de Río Grande, Tierra del Fuego. [Ver Meteostat](https://meteostat.net/es/place/ar/rio-grande?s=87934&t=2018-01-01/2018-12-18)

  
## 🚀 Estado del Proyecto

> **En Desarrollo**: Actualmente en fase de limpieza de datos, pendiente de iniciar el análisis exploratorio de datos (EDA).
>
## 📂 Acceso a los Datos Originales

Los datasets utilizados en este proyecto están disponibles en:

- Carpeta: `data/raw/`
  - `T1.csv`: Dataset SCADA de aerogeneradores.
  - `export.csv`: Dataset meteorológico histórico.

> ⚠️ **Nota importante:** Debido al tamaño de los archivos no se pueden visualizar directamente pero están correctamente almacenados en el repositorio y disponibles para su descarga.

---
Project Organization

Project Organization
├── LICENSE
├── Makefile <- Makefile with commands like make data or make train
├── README.md <- The top-level README for developers using this project.
├── data
│ ├── external <- Data from third party sources.
│ ├── interim <- Intermediate data that has been transformed.
│ ├── processed <- The final, canonical data sets for modeling.
│ └── raw <- The original, immutable data dump.
│
├── docs <- A default Sphinx project; see sphinx-doc.org for details
│
├── models <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks <- Jupyter notebooks. Naming convention is a number (for ordering),
│ the creator's initials, and a short - delimited description, e.g.
│ 1.0-jqp-initial-data-exploration.
│
├── references <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports <- Generated analysis as HTML, PDF, LaTeX, etc.
│ └── figures <- Generated graphics and figures to be used in reporting
│
├── requirements.txt <- The requirements file for reproducing the analysis environment, e.g.
│ generated with pip freeze > requirements.txt
│
├── setup.py <- makes project pip installable (pip install -e .) so src can be imported
├── src <- Source code for use in this project.
│ ├── init.py <- Makes src a Python module
│ │
│ ├── data <- Scripts to download or generate data
│ │ └── make_dataset.py
│ │
│ ├── features <- Scripts to turn raw data into features for modeling
│ │ └── build_features.py
│ │
│ ├── models <- Scripts to train models and then use trained models to make
│ │ │ predictions
│ │ ├── predict_model.py
│ │ └── train_model.py
│ │
│ └── visualization <- Scripts to create exploratory and results oriented visualizations
│ └── visualize.py
│
└── tox.ini <- tox file with settings for running tox; see tox.readthedocs.io

