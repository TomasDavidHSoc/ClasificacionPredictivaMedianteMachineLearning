# Clasificación Predictiva de Diabetes - Machine Learning Clínico

Este repositorio contiene el análisis completo para la detección temprana de diabetes utilizando la base de datos `PimaIndiansDiabetes2`. El proyecto se centra en la aplicación rigurosa de técnicas de ciencia de datos, desde la limpieza de datos hasta la selección del modelo clínico más ético y eficiente.

## 📋 Metodología
El análisis sigue un flujo de trabajo profesional de extremo a extremo:
1. **Limpieza y Preprocesamiento**: Imputación de valores faltantes mediante técnicas de **MICE** (Multivariate Imputation by Chained Equations) para preservar el 100% de la muestra original.
2. **Análisis Exploratorio y PCA**: Reducción de dimensionalidad para identificar patrones de separabilidad en los indicadores clínicos (PC1, PC2, PC3).
3. **Modelado Predictivo**: Evaluación comparativa de 9 modelos:
   - Regresiones Logísticas (Efectos principales e interacciones).
   - Selección de variables mediante regularización **Lasso**.
   - Modelos de clasificación supervisada: **Naive Bayes, LDA, QDA, K-NN**.
   - Métodos de ensamble: **Random Forest** (optimizado con 200 árboles).
4. **Validación Robusta**: Implementación de *Repeated Holdout Method* (B=50) para garantizar la estabilidad de las métricas de desempeño.

## 📊 Hallazgos Principales
Tras evaluar el desempeño global, se determinó que:
- **Priorización Clínica**: Se seleccionó **Naive Bayes** como el modelo de producción. Aunque otros algoritmos presentan una exactitud global ligeramente superior, Naive Bayes ofrece la **Sensibilidad (Recall) más alta (61.50%)**, reduciendo el riesgo crítico de falsos negativos en el diagnóstico de pacientes con diabetes.
- **Interpretabilidad**: Se optó por modelos basados en variables clínicas originales en lugar de componentes abstractos (PCA) para garantizar la utilidad del diagnóstico en entornos médicos accionables.

## 🛠 Tecnologías Utilizadas
- **Lenguaje**: R
- **Entorno**: RMarkdown (PDF Report)
- **Machine Learning**: `caret`, `glmnet`, `randomForest`, `e1071`, `MASS`, `class`.
- **Análisis Estadístico**: `mice`, `metrica`, `FactoMineR`.

## 📂 Estructura del Repositorio
- `Clasificación-Predictiva-mediante-Machine-Learning.Rmd`: Código fuente completo con los bloques de modelado y visualización.
- `Clasificación-Predictiva-mediante-Machine-Learning.pdf`: Reporte técnico final con conclusiones y tablas comparativas.
