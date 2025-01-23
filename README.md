# Predicción del Precio de Vehículos con Regresión Lineal

Este proyecto tiene como objetivo predecir el precio de los vehículos a partir de sus características utilizando un modelo de regresión lineal. A continuación, se presenta una descripción detallada del análisis realizado y los pasos seguidos en todo el proceso.

## 📖 Tabla de Contenidos
1. [Descripción del Problema](#descripción-del-problema)
2. [Análisis Exploratorio de Datos (EDA)](#análisis-exploratorio-de-datos-eda)
   - [Carga de Datos](#carga-de-datos)
   - [Resumen de los Datos](#resumen-de-los-datos)
   - [Valores Faltantes](#valores-faltantes)
3. [Preprocesamiento de Datos](#preprocesamiento-de-datos)
4. [Construcción del Modelo](#construcción-del-modelo)
5. [Evaluación del Modelo](#evaluación-del-modelo)
6. [Conclusiones](#conclusiones)
7. [Requisitos](#requisitos)

## 🕵️ Descripción del Problema

El objetivo de este análisis es crear un modelo predictivo que permita estimar el precio de un vehículo basado en sus características principales, tales como el año, kilometraje, tipo de combustible, tipo de vendedor, transmisión, propietario, consumo de combustible, cilindrada, potencia máxima, torque y número de asientos.

## 🔎 Análisis Exploratorio de Datos (EDA)

### Carga de Datos

Se ha utilizado un conjunto de datos que contiene información sobre diversas características de los vehículos, incluyendo el precio. Los datos se cargan en un DataFrame de pandas:

```python
import pandas as pd

df = pd.read_csv("Car details v3.csv")
```

### Resumen de los Datos

Se realiza un resumen inicial de los datos para comprender mejor las características y su distribución:

```python
df.head(5)
```

El resumen muestra las primeras filas del conjunto de datos, proporcionando una visión general de las variables disponibles.

### Valores Faltantes

Se identifican las columnas que contienen valores nulos y se analiza la cantidad de valores faltantes por variable:

```python
df.isna().sum()
```

Se observa que las columnas `mileage`, `engine`, `max_power`, `torque` y `seats` presentan valores nulos.

## ⚒️ Preprocesamiento de Datos

Para manejar los valores faltantes, se pueden seguir dos enfoques:
- Eliminar las observaciones o variables que contengan valores nulos.
- Imputar los valores faltantes utilizando técnicas como la media, mediana, moda o métodos más avanzados

En este análisis, se opta por imputar los valores faltantes para no perder información valiosa que pueda afectar negativamente el análisis.

## ⭐ Construcción del Modelo

Se construye un modelo de regresión lineal utilizando las siguientes librerías:

```python
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
import statsmodels.api as sm
from sklearn import metrics
```

Se divide el conjunto de datos en conjuntos de entrenamiento y prueba, se escalan las características y se ajusta el modelo de regresión lineal.

## 📈 Evaluación del Modelo

El modelo se evalúa utilizando métricas de desempeño como el R-cuadrado y el error cuadrático medio (MSE). Estas métricas permiten determinar la precisión del modelo y su capacidad para predecir el precio de los vehículos.

## 🏁 Conclusiones

El modelo de regresión lineal proporciona una estimación del precio de los vehículos basada en sus características. Ofrece una base sólida para entender cómo diferentes características afectan el precio de los vehículos.

## Requisitos

Las librerías utilizadas en este análisis son:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- statsmodels

Para instalar las librerías necesarias, puedes ejecutar:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

## ✍️ Contacto

Si tienes alguna pregunta o sugerencia, no dudes en contactarme a través de mi [perfil de GitHub](https://github.com/Andersoncrs).

---

¡Gracias por revisar este proyecto! Espero que encuentres útil la información y el análisis presentado.
