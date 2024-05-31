# Análisis Final de la Red Neuronal

La red neuronal desarrollada se compone de cuatro capas principales: una capa de entrada, dos capas ocultas y una capa de salida. El modelo ha sido entrenado para clasificar la satisfacción de los pasajeros de avión, logrando una precisión del 93%, lo cual indica un alto nivel de exactitud en sus predicciones.

### Arquitectura del Modelo

**Capa de Entrada:** (16 neuronas por las 16 columnas de entrada) Recibe las características iniciales de los datos de los pasajeros, incluyendo factores como el tipo de cliente, el tipo de vuelo, la clase, la distancia del vuelo y diversos servicios ofrecidos durante el vuelo.

**Primera Capa Oculta:** (12 neuronas) Procesa las entradas aplicando una función de activación ReLU para capturar relaciones no lineales complejas.
    
**Segunda Capa Oculta:** (8 neuronas) Realiza un procesamiento adicional de las características transformadas por la primera capa oculta, también usando la función de activación ReLU.
    
**Capa de Salida:** (1 neurona) Genera las predicciones finales aplicando una función de activación logística para producir probabilidades de satisfacción (satisfecho o neutral y no satisfecho).

### Proceso de Entrenamiento

**1. Inicialización:** Los pesos y sesgos del modelo se inicializan aleatoriamente.

**2. Propagación hacia Adelante ('forward_prop'):**
    - Los datos de entrada pasan por cada capa de la red.
    - Las funciones de activación ReLU se aplican en las capas ocultas para introducir no linealidad.
    - La capa de salida aplica la función de activación logística para generar las predicciones.

**3. Cálculo de la Pérdida:** Se utiliza una función de costo cuadrática para medir la diferencia entre las predicciones del modelo y las etiquetas reales de satisfacción.

**4. Propagación hacia Atrás:**
    - Se calcula el gradiente de la función de costo con respecto a cada peso y bias en la red.
    - Se ajustan los pesos y biases utilizando (un algoritmo de optimización) Descenso de Gradiente Estocástico para minimizar la función de costo.

## Resultados y Evaluación

**Precisión del 93%:** 
El modelo demuestra un alto grado de precisión, haciendo predicciones correctas sobre la satisfacción de los pasajeros en la gran mayoría de los casos.
El rendimiento del modelo sugiere una buena capacidad de generalización a nuevos datos de pasajeros, evitando el sobreajuste.

### Conclusión
El proyecto cumple con los objetivos y requisitos del TP. Se implemento y entreno una red neuronal desde cero utilizando NumPy y Pandas, y la red alcanzó una precisión alta del 93%. Además, la comparación con una implementación estándar utilizando scikit-learn muestra resultados consistentes, lo que valida dicha precisión. 