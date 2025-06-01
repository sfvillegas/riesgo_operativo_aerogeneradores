# Predicción del Riesgo Operativo de Aerogeneradores en Condiciones Climáticas Extremas en Tierra del Fuego

## 📚 Descripción General

Este proyecto tiene como objetivo desarrollar un modelo de clasificación multiclase que prediga el **nivel de riesgo operativo** (bajo, medio, alto) de los aerogeneradores del Parque Eólico Río Cullen, ubicado en Tierra del Fuego, Argentina. Se basa en datos operativos de las turbinas y datos meteorológicos históricos de la zona.

El enfoque está orientado a mejorar el mantenimiento preventivo y la eficiencia operativa, anticipando condiciones climáticas adversas que puedan afectar el rendimiento y seguridad de los aerogeneradores.

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

- **SCADA**: Datos simulados o públicos sobre producción y variables operativas de aerogeneradores.
- **Meteostat**: Datos meteorológicos históricos de Río Grande, Tierra del Fuego.

## 🚀 Estado del Proyecto

> **En Desarrollo**: Actualmente en fase de limpieza de datos, pendiente de iniciar el análisis exploratorio de datos (EDA).