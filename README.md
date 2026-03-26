# 🧬 Predicción de Diagnóstico Médico

Este proyecto implementa distintos modelos de Machine Learning para predecir diagnóstico binario (Maligno vs Benigno), optimizando el umbral de decisión en base al F1-score.

## 🎯 Objetivo
Comparar modelos y encontrar el umbral óptimo de clasificación que maximiza el F1-score, priorizando un buen balance entre precisión y recall.

## 🧠 Modelos utilizados
- Regresión Logística
- Random Forest
- Gradient Boosting
- Support Vector Machine (SVM)

## ⚙️ Pipeline

1. Carga de datos
2. Separación en train y validación externa (80/20)
3. Preprocesamiento:
   - Escalado (solo para SVM)
4. Validación cruzada estratificada (5 folds)
5. Evaluación por threshold:
   - Se testean umbrales entre 0 y 1
   - Se calculan F1, Precision y Recall
6. Selección de threshold óptimo (máximo F1 promedio)
7. Evaluación final en conjunto de validación

## 📊 Métricas
- F1 Score (principal)
- Precision
- Recall

## 📈 Output
- Curvas F1 / Precision / Recall vs threshold
- Umbrales óptimos por modelo
- Comparación final de modelos en validación externa

## 📁 Estructura del proyecto
- Script_PrecicciónCM.py → Script principal
- Script.ipynb → Versión notebook
- Datos_Medias.csv → Dataset

## 🚀 Uso

Ejecutar el script principal:

python Script_PrecicciónCM.py

## 📦 Requisitos

Ver requirements.txt
