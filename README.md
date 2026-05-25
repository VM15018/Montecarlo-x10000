# Montecarlo-x10000
# El Oráculo del Balón: Predicción del Mundial FIFA 2026

## Descripción del Proyecto
Este proyecto es un *pipeline* completo de Ciencia de Datos y Machine Learning desarrollado para predecir al campeón de la **Copa Mundial de la FIFA 2026**. 

A diferencia de modelos tradicionales que intentan predecir directamente al campeón (lo cual genera un desbalance masivo de clases), este modelo estocástico evalúa las probabilidades de victoria a nivel de **partido individual**. Utilizando un algoritmo de **XGBoost** calibrado, el modelo alimenta una simulación de **Monte Carlo (10,000 iteraciones)** adaptada al nuevo formato expansivo de 48 selecciones.

## Características Principales (Feature Engineering)
* **Web Scraping Dinámico:** Extracción de datos en vivo evadiendo bloqueos anti-bot (Calidad de plantilla y PIB PPA).
* **Motor Matemático ELO:** Cálculo iterativo y cronológico del rating ELO desde cero usando resultados desde el año 2000.
* **Time Decay:** Función de decaimiento exponencial para restar peso predictivo a partidos antiguos.
* **Momentum Deportivo:** Cálculo de la racha de rendimiento en los últimos 5 encuentros.
* **Métricas Profesionales:** Evaluación del modelo utilizando *Log-Loss* y *Multiclass Brier Score*, descartando el *Accuracy* tradicional.

## Estructura del Proyecto
El proyecto está consolidado para su fácil ejecución y auditoría académica:

```text
/
├── Mundial.ipynb                # Cuaderno Jupyter maestro (Pipeline End-to-End)
├── requirements.txt             # Dependencias del proyecto
├── README.md                    # Documentación
└── El Oráculo del Balón.pdf     # Reporte técnico detallado (Análisis y Limitaciones)
