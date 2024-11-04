# Predicción de Precios de Bienes Raices en Australia - Regresión Avanzada

## Índice

- [Índice](#índice)
- [Introducción](#introducción)
  - [Métodos Utilizados](#métodos-utilizados)
  - [Tecnologías](#tecnologías)
- [Descarga y Configuración](#descarga-y-configuración)
  - [Requisitos Previos](#requisitos-previos)
  - [Cómo Ejecutar](#cómo-ejecutar)
- [Declaración del Problema](#declaración-del-problema)
  - [Objetivo Comercial](#objetivo-comercial)
  - [Preparación de Datos:](#preparación-de-datos)
  - [Construcción y Evaluación del Modelo](#construcción-y-evaluación-del-modelo)
  - [Conclusiones](#conclusiones)
    - [Regresión Ridge](#regresión-ridge)
    - [Regresión Lasso](#regresión-lasso)
    - [Regresión ElasticNet](#regresión-lasso)
    - [Las Variables Más Significativas Son:](#las-variables-más-significativas-son)

## Introducción

El presente proyecto analiza la prediccion de los precios de las casas en el mercado inmobiliario en Australia. En el presente conjunto de datos busca aplicar de modelado de regresión avanzadas. El DataSet presenta multiples caracteristicas (Features), la informacion envulven caracteristicas de las viviendas para ser implementado en modelos de regresión para predecir el precio de venta. 

### Métodos Utilizados
* Análisis Exploratorio de Datos (EDA): Para comprender las características del conjunto de datos y detectar patrones.
* Limpieza de Datos: Manejo de valores nulos y datos inconsistentes.
* Ingeniería de Características: Creación de nuevas variables y transformación de datos existentes para mejorar el rendimiento del modelo.
* Modelado Predictivo: Aplicación de técnicas de regresión lineal, así como de modelos de regularización como Ridge, Lasso y ElasticNet.
* Validación de Modelos: Uso de técnicas como la validación cruzada para evaluar el rendimiento de los modelos.

### Tecnologías
* Python: Lenguaje de programación principal para el análisis de datos y modelado.
* Pandas: Biblioteca para la manipulación y análisis de datos.
* NumPy: Biblioteca para operaciones numéricas.
* Scikit-learn: Biblioteca para machine learning que proporciona herramientas para modelado y evaluación.
* Matplotlib y Seaborn: Bibliotecas para visualización de datos.
* Statsmodels: Para análisis estadísticos y modelos de regresión
* Colap Notebook: Entorno interactivo para ejecutar y documentar el código.

## Descarga y Configuración
### Requisitos Previos

Este proyecto necesita que Anaconda esté instalado en la computadora.

Para más detalles sobre la instalación, visite: https://docs.anaconda.com/anaconda/install/index.html

### Cómo Ejecutar

Puede descargar el código fuente clonando este repositorio usando Git:

1. Abra su aplicación Terminal favorita (Unix, Linux o Macos), como Terminal, Comando, Consola, iTerm2, etc.

2. Clone el repositorio

```
git clone <GITHUB_REPO_URL>
```

3. Abra el archivo notebook ** *.ipynb** en Anaconda.

```
jupyter notebook <FILE.ipynb
```


## Declaración del Problema

Una empresa de vivienda con sede en EE. UU. llamada Surprise Housing ha decidido ingresar al mercado australiano. La empresa utiliza el análisis de datos para comprar casas a un precio inferior a sus valores reales y venderlas a un precio más alto. Con el mismo propósito, la empresa ha recopilado un conjunto de datos de la venta de casas en Australia. Los datos se proporcionan en el archivo CSV a continuación.

La compañía está buscando posibles propiedades para comprar e ingresar al mercado. Debe construir un modelo de regresión utilizando la regularización para predecir el valor real de las posibles propiedades y decidir si invertir en ellas o no.

La empresa quiere saber:

* Qué variables son significativas para predecir el precio de una casa, y
* Qué tan bien esas variables describen el precio de una casa.

Además, determine el valor óptimo de lambda para la regresión de Ridge y Lasso.
### Objetivo Comercial

Debe modelar el precio de las casas con las variables independientes disponibles. Luego, la gerencia utilizará este modelo para comprender cómo varían exactamente los precios con las variables. En consecuencia, pueden manipular la estrategia de la empresa y concentrarse en áreas que generarán altos rendimientos. Además, el modelo será una buena manera para que la gerencia entienda la dinámica de precios de un nuevo mercado.
---

### Preparación de Datos:

1. Limpieza de Datos y Análisis de Datos Faltantes.
2. Análisis y Tratamiento de Valores Atípicos.
3. Derivación de Columnas Categóricas.
4. Análisis Univariable.
5. Análisis Bivariable.

### Construcción y Evaluación del Modelo

1. División de datos de entrenamiento y prueba.
2. Escalado de Características - StandardScaler.
3. Ingeniería y Selección de Características usando RFE y el Factor de Inflación de Varianza.
4. Preparación del modelo usando OLS & Regresión Lineal.
5. Modelos de Regularización Ridge, Lasso y ElasticNet.
6. Análisis de Residuos.
7. Evaluación y Valoración del Modelo.
8. Predicción.
9. Conclusión y Análisis Final.

### Conclusiones
El análisis de precios de casas en el mercado inmobiliario australiano ha permitido aplicar diferentes modelos de regresión para predecir el precio de venta. A través de técnicas de validación y ajuste de hiperparámetros, se han obtenido resultados significativos que reflejan el rendimiento de cada modelo.

### Conclusions

R2_Score for Ridge regresion: 0.8778
R2_Score for Lasso regresion: 0.7845
R2_Score for ElasticNet regresion: 0.8673

Ridge Regression
Optimal Lambda Value: 10.0
R2 Score Train: 0.8941
R2 Test Score: 0.8778
RMSE Test: 30616.1488
Interpretación: El modelo de Ridge muestra un buen ajuste tanto en el conjunto de entrenamiento como en el de prueba, con un R² relativamente alto que indica que el modelo puede explicar una buena parte de la variabilidad del precio de venta. Sin embargo, el RMSE sugiere que, aunque el modelo tiene un buen rendimiento, hay un margen de error considerable en las predicciones.

Lasso Regression
Optimal Lambda Value: 10.0
R2 Score Train: 0.9306
R2 Test Score: 0.7845
RMSE Test: 40655.8097
Interpretación: El modelo Lasso presenta un R² más alto en el conjunto de entrenamiento, lo que sugiere un buen ajuste, pero su desempeño en el conjunto de prueba es significativamente inferior. Esto podría indicar sobreajuste, donde el modelo se ajusta demasiado a los datos de entrenamiento y no generaliza bien a nuevos datos. El RMSE también es más alto en comparación con Ridge, lo que refuerza esta conclusión.

ElasticNet Regression
Optimal Lambda Value: 0.1
R2 Score Train: 0.8686
R2 Test Score: 0.8673
RMSE Test: 31907.7243
Interpretación: El modelo de ElasticNet muestra un equilibrio entre el ajuste del conjunto de entrenamiento y el de prueba, con un R² que indica un buen rendimiento general en ambas partes. El RMSE es intermedio entre Ridge y Lasso, sugiriendo que tiene un buen rendimiento, aunque todavía hay espacio para mejorar.
#### Ridge Regression
* **Optimal Lambda Value: 10.0
* **R2 Score Train:** 0.8941
* **R2 Test Score:**  0.8778
* **RMSE Test:**      30616.1488

#### Lasso Regression
* **Optimal Lambda Value:** 10.0
* **R2 Score Train:**  0.9306
* **R2 Test Score:**   0.7845
* **RMSE Test:**       40655.8097

#### ElasticNet Regression
* **Optimal Lambda Value:** 0.1
* **R2 Score Train:**  0.8686
* **R2 Test Score:**   0.8673
* **RMSE Test:**       31907.7243

#### Las Variables Más Significativas Son:
* YearBuilt
* YearRemodAdd
* YrBltAndRemod
* Condition2_PosA
* RoofMatl_CompShg
* RoofMatl_Metal
* RoofMatl_Roll
* RoofMatl_Tar&Grv
* RoofMatl_WdShake
* RoofMatl_WdShngl
