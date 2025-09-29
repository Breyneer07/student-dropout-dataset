# Synthetic Student Dropout Dataset

Este repositorio contiene un dataset sintético diseñado para la Actividad 1 – SUPERVISED vs UNSUPERVISED LEARNING de la asignatura Data Mining (Universidad de la Costa). El objetivo es simular un conjunto de datos que represente el fenómeno de deserción estudiantil en programas de pregrado, con variables demográficas, académicas y financieras.

## Descripción del dataset

- Archivo: Synthetic_Student_Dropout.csv
- Número de registros: más de 500
- Formato: CSV (valores separados por comas)

### Variables incluidas

| Variable              | Tipo       | Descripción |
|-----------------------|-----------|-------------|
| Age                   | Numérico  | Edad del estudiante (16 – 30 años) |
| Gender                | Categórico| Género del estudiante (Male, Female, Other) |
| Origin                | Categórico| Lugar de procedencia (Urban, Rural) |
| HighSchool_Avg        | Numérico  | Promedio de calificaciones en secundaria (0 – 100) |
| Admission_Test        | Numérico  | Puntaje de examen de admisión (0 – 100) |
| First_Semester_Grades | Numérico  | Promedio del primer semestre universitario (0 – 100) |
| Socioeconomic_Level   | Categórico| Nivel socioeconómico (Low, Medium, High) |
| Scholarship           | Binario   | Indica si cuenta con beca (Yes, No) |
| Loan                  | Binario   | Indica si cuenta con crédito educativo (Yes, No) |
| Financial_Aid         | Binario   | Indica si recibe apoyo financiero (Yes, No) |
| Dropout               | Binario   | Variable objetivo: indica si desertó (Yes, No) |

## Datos nulos y outliers

- Se incluyeron valores vacíos en variables como HighSchool_Avg, Admission_Test y First_Semester_Grades para simular información faltante real.
- Se generaron valores atípicos en variables numéricas (por ejemplo, calificaciones fuera del rango habitual y edades extremas) con el fin de enriquecer el preprocesamiento de datos.

## Objetivo del dataset

Este dataset fue creado con fines académicos y de práctica en Machine Learning, específicamente para:

- Comparar enfoques supervisados vs no supervisados.
- Entrenar y evaluar modelos de clasificación supervisada (Regresión Logística, Árboles de Decisión, Random Forest, SVM).
- Analizar la problemática de la deserción estudiantil y explorar estrategias de predicción temprana.

## Ejemplo de uso en Python

```python
import pandas as pd

# Cargar el dataset
df = pd.read_csv("Synthetic_Student_Dropout.csv")

# Mostrar las primeras filas
print(df.head())

# Información general
print(df.info())

# Distribución de la variable objetivo
print(df['Dropout'].value_counts())
```

## Referencias

- Actividad propuesta en el curso Data Mining – Universidad de la Costa
- Synthetic Data Generation with Python – DataCamp: https://www.datacamp.com/tutorial/synthetic-data-generation
