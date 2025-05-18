# # Optimización de Árbol de Decisión con Random Search y Grid Search

Este repositorio contiene un análisis para optimizar un modelo de árbol de decisión usando técnicas de búsqueda de hiperparámetros: Random Search y Grid Search.

## Contenido

- `Optimizacion-Hiperparametros-deber.ipynb`: Notebook con el código de carga, entrenamiento, optimización y evaluación del modelo.
- `modelo_arbol_decision_optimo.joblib`: Modelo final entrenado con los mejores hiperparámetros y guardado para uso posterior.

## Datos

El conjunto de datos utilizado contiene información médica de pacientes, con el objetivo de predecir si una persona tiene o no diabetes. Cada fila representa un paciente, y las columnas incluyen variables clínicas y biométricas como:

- Glucose: Nivel de glucosa en sangre.

- BMI: Índice de masa corporal (Body Mass Index).

- Age: Edad del paciente.

- BloodPressure: Presión arterial diastólica (mm Hg).

- DiabetesPedigreeFunction: Función de pedigrí de diabetes (representa la probabilidad hereditaria).

- Outcome: Variable objetivo (0 = no tiene diabetes, 1 = tiene diabetes).

Esta información se utiliza para entrenar y evaluar modelos de clasificación, específicamente un árbol de decisión, con técnicas de búsqueda de hiperparámetros para optimizar su rendimiento.

## Resultados

- Se encontró que el mejor modelo por Random Search obtiene un accuracy de aproximadamente 0.76.
- El mejor modelo por Grid Search obtiene un accuracy de aproximadamente 0.74.
- Se seleccionó el modelo optimizado con Random Search para entrenar el modelo final y guardarlo.

## Mejor modelo
Se utilizaron técnicas de optimización de hiperparámetros mediante GridSearchCV y RandomizedSearchCV para mejorar el rendimiento del modelo de árbol de decisión. Luego de evaluar múltiples combinaciones con validación cruzada, se seleccionaron los mejores parámetros y se reentrenó el modelo final.

Mejores hiperparámetros seleccionados:
{'criterion': 'entropy', 'max_depth': None, 'max_features': 'sqrt', 'min_samples_leaf': 18, 'min_samples_split': 10}

Accuracy del modelo final en el conjunto de prueba: 0.7208

Este resultado indica que el modelo tiene una precisión del 72.08% para predecir correctamente si una persona tiene o no diabetes, basado en los datos disponibles.

## Licencia

Este proyecto está bajo la licencia MIT - ver el archivo LICENSE para más detalles.
