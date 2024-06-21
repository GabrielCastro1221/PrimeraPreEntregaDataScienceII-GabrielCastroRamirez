# _***Prediccion de enfermedades cardiacas***_

Para este analisis se dispone de un conjunto de datos en formato `csv` que contiene la informacion de varias métricas de salud de pacientes cardíacos, este conjunto de datos incluye datos como la edad, la presión arterial, la frecuencia cardíaca, colesterol, gleusemia entre otros.
El objetivo de este analisis es desarrollar una prediccion capaz de identificar con precisión a personas con enfermedades cardíacas.
Por medio de varios procesos de limpieza de datos y calculos entre los valores de cada campo del conjunto de datos, se garantizara que el modelo identificara a todos los pacientes potenciales.

## _***Objetivos:***_

+ Identificar el tipo de dato de cada uno de los campos que contienen los registros de la informacion de las personas en el conjunto de datos y asi porder realizar las tranformaciones respectivas para una analisis optimo de la problematica a evaluar.
+ Identificar el rango y el promedio de cada uno de los registros que se encuentran el los campos del conjuntode datos para poder deducir en que personas es mas frecuente encontrar enfermedades cardiacas.
+ Efectuar un analisis univariado para comprender saber como es el comportamiento de las caracteriscas y mirar como es su distribución en el conjunto de datos.
+ Visualizar los datos categoricos para analizar como es la frecuencia de las categorias de cada campo del conjunto de datos.
+ Efectuar un analisis bivariado para comprender la relacion entre la distribución de las caracteriscas de los campos categoricos con los objetivos.

## _***Fuente de datos***_

En la siguiente url se encuentran alojados los datos de las personas con problemas cardiacos que ayudaran a hacer el analisis de la problematica. Esta url pertenece a la plataforma GitHub y servira para cargar el conjunto de datos en el notebook.

```
https://raw.githubusercontent.com/GabrielCastro1221/csv_dataScience/main/heart1.csv
```

## _***Información sobre el conjunto de datos***_

CAMPO            | DESCRIPCION
-----------------|------------------------------------------------------------------------
_***AGE***_      | Edad del paciente
_***SEX***_      | Sexo del paciente: 0 = Hombre - 1 = Mujer
_***CP***_       | Tipo de dolor en el pecho: 0 = angina tipica - 1 = angina atipica - 2 dolor no anginoso - 3 = asintomatico
_***TRESTBPS***_ | Presión arterial en reposo en mm Hg
_***CHOL***_     | Colesterol sérico en mg/dl
_***FBS***_      | Nivel de azúcar en la sangre en ayunas, clasificado como superior a 120 mg/dl: 1 = Verdadero - 0 = Falso
_***RESTECG***_  | Resultados electrocardiográficos en reposo: 0 = Normal - 1 = Tener anomalía de la onda ST-T - 2 = Mostrando hipertrofia ventricular izquierda probable o definitiva.
_***THALACH***_  | Frecuencia cardíaca máxima alcanzada durante una prueba de esfuerzo
_***EXANG***_    | Angina inducida por el ejercicio: 1 = Si - 0 = No
_***OLDPEAK***_  | Depresión del ST inducida por el ejercicio en relación con el reposo
_***SLOPE***_    | Pendiente del segmento ST del ejercicio máximo: 0 = pendiente ascendente - 1 = Plana - 2 = pendiente descendente
_***CA***_       | Número de vasos principales (0-4) coloreados por fluoroscopia
_***THAL***_     | Resultado de la prueba de esfuerzo con talio: 0 = Normal - 1 = Defecto solucionado - 2 = defecto reversible - 3 = No descrito
_***TARGET***_   | Estado de enfermedad cardíaca: 0 = Sano - 1 = Enfermo

## _***Librerias utilizadas en el Notebook***_

+ `Warnings`: se utiliza para controlar los mensajes de advertencia
+ `Pandas`: permite trabajar con datos estructurados de manera eficiente.
+ `Numpy`: Permite crear vectores y matrices grandes multidimensionales, junto con una gran colección de funciones matemáticas de alto nivel.
+ `MatplotLib`: Permite generar gráficos en dos dimensiones, a partir de datos contenidos en listas o diccionarios de datos.
+ `seaborn`: Proporciona una interfaz de alto nivel para crear gráficos estadísticos informativos.

## _***Metodos Utilizados en el Notebook***_

+ `pd.read_csv`: Este metodo de la libreria `pandas` permite cargar el conjunto de datos proveniente de la URL de github en el proyecto.
+ `info`: Este metodo de la libreria `pandas` proporciona información detallada del conjunto de datos.
+ `astype`: Este metodo de la libreria `pandas` permite hacer tranformaciones de datos sobre el conjunto de datos en el que se esta trabajando.
+ `describe`: Este metodo de la libreria `pandas` muestra los datos estadisticos de los datos numericos del conjunto de datos.
+ `describe(include="object")`: Este metodo de la libreria pandas muestra el resultado de los datos categoricos del conunto de datos.
+ `plt.subplots`: Este metodo de la libreria `MatPlotLib` le asigna las dimensiones a la visualización
+ `np.floor & np.ceil`: Este metodo de la libreria `numpy` en este analisis servira para darle un rango de columnas y celdas a las visualizaciones generadas.
+ `sns.histplot`: Este metodo de la libreria `seaborn` permite crear una visualizacion tipo histograma.
+ `plt.suptitle`: Este metodo de la libreria `MatPlotLib` permite agregarle un subtitulo alucivo a lo que se representa en los graficos.
+ `plt.tight_layout`: Este metodo de la libreria `MatPlotLib` permite automatizar la distribucion de los datos en la visualización
+ `plt.subplots_adjust`: Este metodo de la libreria `MatPlotLib` permite agregar espaciado perzonalido a las visualizaciones.
+ `plt.show`: Este metodo de la libreria `MatPlotLib` permite mostrar el grafico en el notebook.
+ `difference`: Este metodo de la libreria `pandas` permite hacer la diferencia de entre conjuntos de datos.
+ `value_counts`: Este metodo de la libreria `pandas` se utiliza para contar la frecuencia de valores unicos en una serie de datos.
+ `sort_values`: Este metodo de la libreria `pandas` Sirve pa ordenar valores de una o mas columnas.
+ `set_palette`: Este metodo de la  libreria `seaborn` Sirve pa asignar colores personalizados a las visualizaciones.
+ `sns.barplot`: Este metodo de la libreria `seaborn` permite crar una visualización de barras.
+ `sns.kdeplot`: Este metodo de la libreria `seaborn` permite ajustar la apariencia del grafico segun la probabilidad de las variables basadas en la serie de datos.

## _***Glosario***_

1. _***Data wrangling (Limpieza de datos)***_: también conocido como data munging, es el proceso de limpiar, estructurar y enriquecer conjuntos de datos crudos en formatos más utilizables para análisis. Implica transformar datos en diferentes formatos, fusionar conjuntos de datos, detectar y corregir errores en los datos, así como manejar valores faltantes y asegurar que los datos estén en el formato adecuado para su análisis.

2. _***Datos categoricos***_: son un tipo de datos que representan características y cualidades, en lugar de cantidades numéricas. Estos datos se dividen en categorías o grupos discretos y finitos.

3. _***Datos continuos***_: son otro tipo de datos que representan valores numéricos que pueden tomar cualquier valor dentro de un intervalo específico.

4. _***Exploratory data analysis (EDA)***_: Es una etapa fundamental en el proceso de análisis de datos, donde se utilizan técnicas estadísticas y gráficas para explorar y entender los datos antes de aplicar métodos más avanzados o realizar inferencias.

5. _***Analisis univariado***_: Es una técnica estadística que se centra en analizar una sola variable a la vez. Es decir, examina las características y propiedades de una variable sin considerar otras variables simultáneamente. Este tipo de análisis es fundamental en estadística descriptiva y suele ser el primer paso en la exploración de datos.

6. _***Analisis bivariado***_: Es una técnica estadística que se centra en estudiar la relación entre exactamente dos variables al mismo tiempo. A diferencia del análisis univariado, que se enfoca en una sola variable a la vez, el análisis bivariado explora cómo varía una variable en relación con otra.