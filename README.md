# Predicción de Serie Temporal de AWO Total Sistema

Este proyecto corresponde a una prueba técnica orientada al desarrollo de modelos de predicción sobre datos históricos de ventas y métricas de marketing. El objetivo principal fue estimar la evolución de la variable `AWO total sistema` y evaluar diferentes enfoques de modelado.

---

## 🧩 Metodología

1. **Procesamiento y limpieza de datos**
   - Conversión del identificador temporal de semanas al formato de fecha estándar.
   - Ordenación cronológica y validación de consistencia.
   - Eliminación de registros faltantes y variables irrelevantes.

2. **Análisis exploratorio**
   - Evaluación de correlaciones entre variables exógenas y la variable objetivo.
   - Identificación de multicolinealidad y reducción de dimensionalidad mediante PCA.
   - Análisis de estacionariedad con la prueba ADF.

3. **Feature Engineering**
   - Generación de variables derivadas:
     - Lags históricos de `AWO`.
     - Diferencias semanales.
     - Medias móviles.
   - Incorporación de variables de marketing como predictores exógenos.

4. **Modelado**
   - **ARIMAX**: Modelado autoregresivo con variables exógenas.
   - **Red Neuronal MLP**: Red densa con capas ocultas para capturar relaciones no lineales.
   - Comparativa de desempeño en conjuntos de entrenamiento y prueba.

5. **Evaluación**
   - Métricas utilizadas:
     - RMSE
     - MAE
     - MAPE
     - Precisión estimada
   - Visualización de predicciones frente a valores reales.
   - Análisis de ajuste y generalización.

---

## ⚙️ Tecnologías y herramientas

- Python 3.x
- Pandas
- Numpy
- scikit-learn
- statsmodels
- TensorFlow / Keras
- Matplotlib

---

## ✨ Resultados destacados

- El modelo ARIMAX alcanzó una precisión de **88.9%** con un conjunto de prueba de 20 observaciones, superando el umbral mínimo requerido.
- Tras aplicar **feature engineering**, la precisión se incrementó hasta **92.21%**, mostrando un ajuste más consistente.
- La red neuronal MLP con variables derivadas logró un desempeño comparable y, en algunos casos, superior al modelo clásico autoregresivo.

---

## 📈 Conclusiones

La combinación de ingeniería de atributos y modelos de predicción permitió capturar adecuadamente las dinámicas de la serie temporal, cumpliendo los objetivos establecidos. Se recomienda continuar con iteraciones sobre la selección de features y explorar arquitecturas recurrentes (LSTM) para futuras mejoras.


