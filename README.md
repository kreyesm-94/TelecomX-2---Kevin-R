# TelecomX-2---Kevin-R

# *Curso de estadistica con Machine Learning* #

🎯 Misión

Tu nueva misión es desarrollar modelos predictivos capaces de prever qué clientes tienen mayor probabilidad de cancelar sus servicios.
La empresa quiere anticiparse al problema de la cancelación, y te corresponde a ti construir un pipeline robusto para esta etapa inicial de modelado.


🧠 Objetivos del Desafío

Preparar los datos para el modelado (tratamiento, codificación, normalización).
Realizar análisis de correlación y selección de variables.
Entrenar dos o más modelos de clasificación.
Evaluar el rendimiento de los modelos con métricas.
Interpretar los resultados, incluyendo la importancia de las variables.
Crear una conclusión estratégica señalando los principales factores que influyen en la cancelación.


🧰 Habilidades que se van a prácticar en este TelecomX 2

✅ Preprocesamiento de datos para Machine Learning

✅ Construcción y evaluación de modelos predictivos

✅ Interpretación de resultados y entrega de insights

✅ Comunicación técnica con enfoque estratégico


# *Creación de repositorio en GitHub para almacenar el análisis* #

¡Organizar tu proyecto desde el principio facilita el desarrollo y garantiza buenas prácticas en el control de versiones! 🚀
- Repositorio Kevin Reyes / Nombre: TELECOMx-2 Kevin R

# *Extracción del Archivo Tratado* #

En el proyecto de TelecomX-1 se realizo un análisis exploratorio de los datos, logrando identificar insight importantes para la empresa y para la toma de decisiones. Para este proyecto se trabajaría con el archivo final que se obtuvo del TelecomX-1, sera la base e insumo necesario para poder llevar acabo el análisis deseado en el TelecomX-2

- Creación de nuevo cuaderno de Colaboraty Colab
- Carga de archivo CSV / "df_final_kev_TelecomX 2

# *Eliminación de columnas innecesarias y tratamiendo de columnas* #
En todo proyecto es necesario realizar un análisis generar de la data con la que contamos, esto para asegurar que solo almacenemos la información necesaria. Si es necesario eliminar columnas o filas poder hacerlo y si es necesario realizar el tratamiento de columnas también poder hacerlo

- Eliminamos la fila de "customer ID"
- Ejecutamos código para validar la correlación de cuentas y correlación del tenere total

# *Ejecusión del Encoding* #
Nos permite transforma las variables categóricas a formato numérico para hacerlas compatibles con los algoritmos de machine learning.

- Importamos bibliotecas OneHotEncoder / ColumnTransformer
- Transformación de variables a numéros

# *Ejecusión de la verificación de la proporción de cancelación (Churn)* #
Calcula la proporción de clientes que cancelaron en relación con los que permanecieron activos. Evalúa si existe un desbalance entre las clases, ya que esto puede impactar en los modelos predictivos y en el análisis de los resultados
Este paso es muy importante antes de entrenar, porque si la proporción está muy desbalanceada, el modelo puede aprender a “predecir siempre la clase mayoritaria” y aun así tener un accuracy alto pero inútil.

# *Balanceo de clases* #
Es necesario aplicar técnicas de balanceo como undersampling o oversampling. En situaciones de fuerte desbalanceo, herramientas como SMOTE pueden ser útiles para generar ejemplos sintéticos de la clase minoritaria.
Debemos asegurarnos de que todas las columnas sean numéricas.

# *Estandarización* #
La estandarización evalúa la necesidad de normalizar o estandarizar los datos, según los modelos que se aplicarán. Modelos basados en distancia, como KNN, SVM, Regresión Logística y Redes Neuronales, requieren este preprocesamiento. Por otro lado, modelos basados en árboles, como Decision Tree, Random Forest y XGBoost, no son sensibles a la escala de los datos.

# *Análisis de correlación* #
Visualiza la matriz de correlación para identificar relaciones entre las variables numéricas. Presta especial atención a las variables que muestran una mayor correlación con la cancelación, ya que estas pueden ser fuertes candidatas para el modelo predictivo.

Ya que transformamos las variables categóricas en numéricas, podemos calcular y visualizar la matriz de correlación para ver qué tan relacionadas están con la cancelación

# *Análisis dirigido* #
Variables especificas que se relacionan directamente con el;

- Tiempo de contrato × Cancelación
- Gasto total × Cancelación
Adicional se agregaron dos opciones más;
- Gasto mensual X Cancelación (Dato extra)
- Contrato (tipo) X Cancelación (Dato extra)

# *Separación de datos* #

Se devide el conjunto de datos en entrenamiento y prueba para evaluar el rendimiento del modelo. Una división común es 70% para entrenamiento y 30% para prueba, o 80/20, dependiendo del tamaño de la base de datos.

# *Creación de modelos* #
Se crearon dos modelos;

Modelo logístico: Se aplico la normalización

Random forest: No se aplico normalización

# **Justificación del preprocesamiento** #

Para la Regresión Logística, aplicamos normalización porque es un modelo basado en optimización matemática (gradiente descendente). Si no escalamos, variables con rangos grandes podrían dominar el entrenamiento.

Para Random Forest, no aplicamos normalización porque los árboles se basan en umbrales de partición (ej. “edad < 30”), lo que hace irrelevante la escala de la variable.

Realizmos una comparación de resultados con los datos extraidos;
a Regresión Logística obtuvo una accuracy de ~0.85 y un buen recall en la clase positiva (clientes que cancelan).

El Random Forest superó ligeramente con accuracy de ~0.87, mostrando mayor balance entre precisión y recall.

# **Evaluación de modelos** #

Realizar una evaluación para los diferentes modelos aplicados en el análisis ayuda a identificar que metricas importantes para el negocio se mueven a favor o en contra, de esta manera se puede preveenir o mejorar de alguna manera antes de que suceda la cancelación.


_Regresión Logística_
Predijo bien la mayoría de cancelaciones (recall = 0.98).
Falló más en clientes que no cancelan, generando falsos positivos (predijo cancelación cuando no era).

_Random Forest_
Más equilibrado entre clases.
No favorece en exceso a los clientes que cancelan o los que permanecen.


Se realizo un análisis de comparación determinando que el modelo que presento mejor rendimiendo es el Random Forest (accuracy 0.87), teniendo una mejor interpretación de los datos y balance entre las descripciones de la base.

# **Ejecusión de curva de ROC** #

Ambos modelos tienen curvas muy por encima de la línea aleatoria, indicando alta capacidad de clasificación.
Conclusión final:
- La Regresión Logística es el modelo ganador en este caso:
- Tiene mejor AUC (0.98).
- Es más simple de implementar e interpretar.
- Generaliza mejor en este dataset que Random Forest.

# **Análisis de la Importancia de las Variables** #

Después de elegir los modelos es importante que se realice el análisis de las variables más relevantes para la predicción de la cancelación.
Se realizo una gráfica con las 15 variables mas significativas de la data, dato importante para determinar en que descripción enfocalizarse.


# **Conclusión** #

Se brinda una conclusión detallada analizando las varibles establecidas y modelos utilizados, de esta manera se concluye que el modelo que mejor predice es el Random Forest, sin descartar que el modelo de Regresión Logística, permite no solo predecir cancelaciones con un 87% de exactitud, si no también entender que tipo de factores las impulsan.

Adicional se brinda una recomendación general de estrategías de permanecia que podrían ayudar a la empresa con la retención de clientes.
