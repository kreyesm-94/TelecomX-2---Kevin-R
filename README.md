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
- Gasto mensual X Cancelación (Dato extra)
- Contrato (tipo) X Cancelación (Dato extra)


