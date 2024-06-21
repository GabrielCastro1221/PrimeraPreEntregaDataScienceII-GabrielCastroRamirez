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

## _***Información sobre el conjunto de datos:***_

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

## _***Librerias utilizadas:***_

+ `Warnings`: se utiliza para controlar los mensajes de advertencia
+ `Pandas`: permite trabajar con datos estructurados de manera eficiente.
+ `Numpy`: Permite crear vectores y matrices grandes multidimensionales, junto con una gran colección de funciones matemáticas de alto nivel.
+ `MatplotLib`: Permite generar gráficos en dos dimensiones, a partir de datos contenidos en listas o diccionarios de datos.
+ `seaborn`: Proporciona una interfaz de alto nivel para crear gráficos estadísticos informativos.
