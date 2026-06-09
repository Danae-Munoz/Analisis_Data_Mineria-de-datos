# Predicción de Precios de Vinos con Machine Learning

---

## Descripción

Este proyecto desarrolla un análisis de datos sobre el mercado vitivinícola utilizando un dataset real de vinos obtenido desde Kaggle, basado en información de la plataforma Vivino.com. El objetivo principal es identificar los factores que influyen en el precio de los vinos y construir modelos predictivos basados en Machine Learning que permitan estimar el valor de un vino según sus características.

---

## Fuente de datos

El dataset utilizado proviene de Kaggle:

https://www.kaggle.com/datasets/budnyak/wine-rating-and-price

Este conjunto de datos contiene información de vinos obtenida desde Vivino.com y se encuentra dividido originalmente en distintos archivos CSV, correspondientes a diferentes tipos de vino:

* `Red.csv`: vinos tintos.
* `White.csv`: vinos blancos.
* `Sparkling.csv`: vinos espumantes.
* `Rose.csv`: vinos rosé.
* `Varieties.csv`: archivo no utilizado, debido a que contiene una sola columna y no aporta información relevante al modelamiento.

Para el desarrollo del proyecto, se trabajó con los archivos Red, White, Sparkling y Rose, los cuales fueron integrados en un único dataset consolidado.

---

## Variables principales

El dataset incluye las siguientes variables relevantes:

* `Country`: país de origen del vino.
* `Rating`: calificación promedio del vino.
* `NumberOfRatings`: cantidad de valoraciones recibidas.
* `Price`: precio del vino en euros.
* `Year`: año de producción del vino.
* `WineStyle`: tipo de vino, como red, white, sparkling o rose.

Estas variables permiten analizar el comportamiento del mercado de vinos y evaluar qué características tienen mayor relación con el precio final del producto.

---

## Objetivo

Desarrollar un modelo de análisis y predicción que permita:

* Identificar los factores que influyen en el precio de los vinos.
* Analizar la relación entre variables numéricas y categóricas.
* Preparar los datos para su uso en modelos de Machine Learning.
* Comparar el desempeño de distintos modelos predictivos.
* Predecir el precio de un vino según sus características principales.

---

## Metodología

El proyecto sigue la metodología **CRISP-DM**:

1. **Comprensión del negocio**
   Definición del problema: predicción de precios de vinos mediante Machine Learning.

2. **Comprensión de los datos**
   Exploración del dataset y análisis de variables como precio, calificación, país, año, cantidad de valoraciones y tipo de vino.

3. **Preparación de los datos**

   * Integración de los archivos CSV de vinos.
   * Limpieza de valores nulos.
   * Conversión de la variable `Year` a formato numérico.
   * Tratamiento del valor `N.V.` en los años.
   * Eliminación de variables con alta cardinalidad.
   * Codificación de variables categóricas.

4. **Modelado**
   Preparación del dataset y entrenamiento de modelos predictivos.

5. **Evaluación**
   Evaluación de los modelos mediante métricas como MAE, RMSE y R².

6. **Entrenamiento**
   Se entrena un modelo de Regresión Lineal. Luego, debido a sus resultados limitados, se prueban otros modelos como Árbol de Decisión y Random Forest.

---

## Modelos predictivos

* Regresión Lineal.
* Árbol de Decisión.
* Random Forest Regressor.

---

## Errores durante el proceso

* Valores nulos en la variable `Year`.
* Valor `N.V.` en la columna de año, lo que impedía convertirla directamente a número.
* Variables categóricas que debieron ser codificadas para el modelo.
* Bajo porcentaje de predicción en el modelo de Regresión Lineal.
* Bajo rendimiento del modelo de Árbol de Decisión.
* Presencia de outliers en variables como `Price` y `NumberOfRatings`.

---

## Tecnologías utilizadas

* Python.
* Pandas.
* NumPy.
* Matplotlib.
* Seaborn.
* Scikit-learn.
* Google Colab.
* Kaggle.

---

## Estructura del proyecto

```bash
MachineLearning-MineriadeDatos/
├── Analisis_Data.ipynb
├── Evaluación_1_Danae_Muñoz.ipynb
├── Evaluación_Danae_Muñoz.ipynb
├── Segunda_opcion.ipynb
└── README.md
```
