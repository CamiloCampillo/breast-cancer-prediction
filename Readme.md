# 🤖 Predicción de cáncer de mama con algoritmo de machine learning

## 🌐 Visita el sitio web en Quarto Pubs

**Link** 

https://camiloc07.quarto.pub/breast-cancer-predict/

## 📍 Introducción

El cáncer de mama representa una de las principales preocupaciones de salud a nivel global, afectando a millones de mujeres cada año. La detección temprana es fundamental para mejorar las tasas de supervivencia y éxito del tratamiento. Este proyecto tiene como objetivo crear un modelo predictivo utilizando técnicas de aprendizaje automático para clasificar tumores como benignos o malignos. A través de este enfoque, se busca asistir a los profesionales médicos en el diagnóstico precoz, optimizando los resultados clínicos y, en última instancia, contribuyendo a salvar vidas.

---

## 💡 Objetivo del proyecto

El propósito principal de este proyecto es desarrollar un modelo de aprendizaje automático preciso y confiable para clasificar tumores de mama como benignos o malignos. El objetivo es ofrecer a los profesionales de la salud una herramienta efectiva para la detección temprana del cáncer, facilitando intervenciones oportunas y mejorando la atención al paciente. Al identificar las características relevantes de los tumores, este modelo actúa como un apoyo esencial para los oncólogos y otros profesionales médicos en su toma de decisiones clínicas.

---

## 📊 Información del dataset

El proyecto utiliza el conjunto de datos de diagnóstico de cáncer de mama de Wisconsin, que incluye características médicas clave extraídas de biopsias de tumores mamarios. Este conjunto es ampliamente reconocido y utilizado en investigaciones sobre cáncer de mama y en la creación de modelos predictivos, contribuyendo a la mejora de diagnósticos tempranos y el desarrollo de soluciones más precisas en el campo de la oncología.

**Dataset:** Puedes obtener el conjunto de datos alojado en *UCI Machine Learning Repository*.

Cada registro está etiquetado con como **benigno (2)** o **maligno (4)**.

Las variables que contiene el dataset son:

| Variable                 | Descripción                                    | Rango        |
|--------------------------|------------------------------------------------|--------------|
| SampleCodeNumber         | Identificación única del tumor                 | ID           |
| ClumpThickness           | Espesor del grupo de células                   | 1 - 10       |
| UniformityCellSize       | Uniformidad en el tamaño de las células.       | 1 - 10       |
| UniformityCellShape      | Uniformidad en la forma de las células         | 1 - 10       |
| MarginalAdhesion         | Adhesión marginal de las células               | 1 - 10       |
| SingleEpithelialCellSize | Tamaño de una sola célula epitelial            | 1 - 10       |
| BareNuclei               | Presencia de núcleos desnudos (sin citoplasma) | 1 - 10       |
| BlandChromatin           | Cantidad de cromatina blanda en los núcleos    | 1 - 10       |
| NormalNucleoli           | Presencia de nucléolos normales                | 1 - 10       |
| Mitoses                  | Número de mitosis observadas                   | 1 - 10       |
| Class                    | Indica si el tumor es benigno o malingno       | 2 = benigno  4 = maligno  |
---

## 🔧 Preprocesamiento de Datos

Para asegurar un rendimiento óptimo del modelo de aprendizaje automático, se realizaron pasos clave de preprocesamiento en el conjunto de datos. Estos incluyen:

- **Manejo de valores con carácteres extraños:** se realizó la imputación o eliminación de datos erróneos para evitar brechas que pudieran generar imprecisiones en las predicciones.

- **Manejo de valores duplicados:** se hizo la respectiva limpieza del dataset para eliminar los valores duplicados.

- **Codificación de variables categóricas:** la variable objetivo fue codificada convirtiéndolas en factores que permitieran un correcto análisis.

- **Entrenamiento y test:** se realizó la división del conjunto de datos en datos de entrenamiento y datos de prueba para garantizar que el modelo fuera probado con datos que para este fueran desconocidos.

---

## 💻 Desarrollo y Metodología

La metodología que se usó para este proyecto fue la siguiente: 

- **Análisis Exploratorio de Datos:** Se realizó un análisis exploratorio para comprender mejor las características del conjunto de datos. Este paso incluyó la visualización de distribuciones y la identificación de patrones que pudieran influir en el modelo predictivo.

- **Modelo de Regresión Logística:** Se utilizó un modelo de regresión logística para predecir la probabilidad de que un paciente tenga cáncer de mama. Este enfoque es adecuado para problemas de clasificación binaria, como el diagnóstico (benigno o maligno).

- **Validación Cruzada:** Para evaluar la robustez del modelo, se implementó una técnica de validación cruzada. Esto permitió dividir el conjunto de datos en múltiples subconjuntos, entrenando el modelo en diferentes combinaciones y evaluando su rendimiento en datos no vistos. La validación cruzada ayuda a prevenir el sobreajuste y proporciona una estimación más precisa del rendimiento del modelo.

---

## 📈 Métricas de evaluación

Para este proyecto, las medidas de desempeño utilizadas fueron las siguientes:

- **Precisión (Accuracy):** mide la proporción de casos que son clasificados correctamente por el modelo. Sin embargo, en los diagnósticos médicos, la precisión por sí sola no es suficiente.

- **Sensibilidad (Sensitivity):** mide la proporción de casos que el modelo clasificó correctamente como el caso positivo con respecto a todos las predicciones positivos. Esta métrica es vital porque nos indica la capacidad del modelo de identificar a los pacientes que realmente tienen el tumor maligno.

- **Especificidad (Specificity):** mide la proporción de casos que el modelo clasificó como negativos correctamente. Esta métrica es importante porque nos indica la capacidad del modelo de clasificar a las personas que no tienen en tumor maligno. Así evitando los falso negativos (Personas que tiene cáncer pero son clasificadas como negativo).

- **Curva ROC y área bajo la curva (AUC):** esta métrica mide la capacidad del modelo para diferenciar entre casos benignos y malignos en diferentes valores de umbral, mostrando qué tan bien funciona el modelo independientemente de la distribución de clases.

---

## 📈 Resultados

Luego de evaluar el modelo de regresión logística con validación cruzada, las métricas de desempeño fueron:

- **Precicisón:** $0.9652$

- **Sensibilidad:** $0.9857$

- **Especificidad:** $0.9542$

- **AUC:** $0.9933428$

Estas métricas indican que el modelo es muy confiable para distinguir entre casos benignos y malignos. Minimizando los falsos positivos y los falsos negativos manteniendo una excepcional precisión. 

---

## 💡 Líneas futuras

Para el futuro, se pueden explorar varias áreas de mejora en este proyecto:

- **Optimización del modelo:** Ajuste de parámetros y prueba de técnicas avanzadas, como redes neuronales y/o otros modelo de machine learning, para mejorar la precisión y el rendimiento del modelo.

- **Generación de nuevas características:** Incluir más variables clínicas o crear nuevas a partir de las existentes podría incrementar la efectividad predictiva.

- **Aplicación clínica:** Desarrollar una interfaz amigable para facilitar la integración del modelo en el entorno médico, apoyando decisiones en tiempo real.

- **Validación en diferentes conjuntos de datos:** Probar el modelo en otros datasets para asegurar su validez en diversas poblaciones.

---

## 📢 Contacto

¿Tienes preguntas, comentarios o sugerencias? No dudes en contactarme:

**Correo:** camilocampillo07@gmail.com

**LinkedIn:** [Camilo Campillo](https://www.linkedin.com/in/camilo-campillo-mart%C3%ADnez/)





 





