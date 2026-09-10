Fundamentos-de-ciencia-de-datos

Este repositorio reúne los desafíos y proyectos desarrollados durante el bootcamp de Fundamentos de Ciencia de Datos (Talento Digital), cubriendo el ciclo completo de un proyecto de datos: exploración y limpieza (pandas, NumPy, EDA, estadística y probabilidad), modelado predictivo supervisado y no supervisado (regresión logística, Random Forest, GridSearchCV, K-means, DBSCAN, PCA, t-SNE) y procesamiento a escala con Apache Spark y MLlib.

Como Ingeniero Civil de Minas con formación en geoestadística (kriging, simulación condicional) y planificación minera (optimización de pit con Lerchs-Grossmann, Vulcan, Datamine), uso también este espacio para explorar el punto de encuentro entre ambos mundos: cómo técnicas de machine learning como Random Forest y validación cruzada pueden complementar o contrastar con los métodos geoestadísticos clásicos en la estimación de recursos minerales.

Proyecto destacado: Estimación de recursos en presencia de incertidumbre geológica

Port a Python de mi memoria de título de Ingeniería Civil de Minas (Universidad de Concepción, 2019): "Estimación de recursos en presencia de incertidumbre geológica".

El trabajo original se desarrolló en R (RStudio), usando spMC para simular variables geológicas categóricas (tipo de roca, alteración, textura) y gstat para el kriging. Este notebook recodifica todo el flujo de trabajo en Python, reemplazando además el motor de simulación categórica de spMC por un enfoque de Machine Learning (Random Forest).

De R a Python — qué cambió
Paso de la memoria (R)	Herramienta original	Implementación en Python
Simulación de variables categóricas (roca, alteración, textura)	spMC (cadenas de Markov espaciales, transiogramas)	RandomForestClassifier (scikit-learn)
Kriging de variables continuas (Cu, Mo, Fe) con deriva geológica	gstat	Regression kriging: regresión sobre dummies de la variable categórica + kriging ordinario de residuos (GSTools)
Categorización de recursos (Medido/Indicado/Inferido)	Varianza de kriging (gstat)	Igual criterio, sobre la varianza de kriging calculada con GSTools
Curvas tonelaje-ley e inventario de recursos	Scripts R a medida	pandas / numpy
Análisis económico y sensibilidad a la ley de corte	Scripts R a medida	pandas / numpy / matplotlib
Por qué Machine Learning en vez de spMC

spMC no tiene una librería equivalente en Python. En vez de reconstruir su marco teórico (cadenas de Markov espaciales y transiogramas) desde cero, se optó por una alternativa más simple de mantener y más rápida: un Random Forest aprende la relación entre la configuración de los vecinos más cercanos (distancia + categoría) y la categoría en un punto no muestreado, y esa relación se usa para simular nuevas realizaciones.

El notebook incluye dos modos de simulación:

sequential — encadena la información entre nodos simulados (más continuidad espacial, más lento).
batch — predice y sortea todos los nodos de una vez (~100-300x más rápido; recomendado para grillas grandes o análisis que necesitan repetir la simulación muchas veces).
Estructura del notebook
Motor de simulación categórica basado en Random Forest
Caso ficticio — datos 100% sintéticos, replicando el caso de prueba de la memoria original
Caso real — depósito de fierro de la memoria original, configurable para cargar cualquier base de datos propia (solo se editan los nombres de columnas)
Conclusiones y notas de uso
Tecnologías

Python · NumPy · SciPy · pandas · scikit-learn · GSTools · Matplotlib

Contexto

Memoria de título: "Estimación de recursos en presencia de incertidumbre geológica", Ingeniería Civil de Minas, Universidad de Concepción, Chile (2019). Profesor patrocinante: Roberto Fustos Toribio.

Autor: Eric Rodríguez Acuña — linkedin.com/in/ericrodrigueza
