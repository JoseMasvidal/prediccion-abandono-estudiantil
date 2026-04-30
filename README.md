# Predicción de Abandono Estudiantil

## Descripción del problema de negocio
La deserción estudiantil representa un desafío académico, social y financiero para las instituciones educativas. Cuando un estudiante abandona sus estudios, la institución pierde continuidad en su misión formativa, disminuye sus indicadores de retención y puede enfrentar impactos en planeación presupuestal.

En este proyecto se plantea un caso aplicado de análisis predictivo para identificar estudiantes con alto riesgo de abandono de manera temprana, con el fin de apoyar decisiones de acompañamiento y prevención.

## Objetivo del modelo de Machine Learning
Desarrollar un modelo de Machine Learning que estime la probabilidad de abandono estudiantil para cada alumno, permitiendo:

- Detectar perfiles de riesgo de forma oportuna.
- Priorizar intervenciones institucionales (tutorías, apoyo financiero, orientación psicosocial, etc.).
- Apoyar la toma de decisiones basada en datos para mejorar la retención.

## Datos necesarios
Para construir un modelo útil, se requiere información histórica de estudiantes, idealmente anonimizada y consolidada por periodos académicos. Ejemplos de variables:

- **Datos académicos:** promedio, materias reprobadas, avance curricular, asistencia.
- **Datos sociodemográficos:** edad, género, lugar de residencia, condición laboral.
- **Datos económicos:** tipo de beca, nivel socioeconómico, mora en pagos.
- **Datos institucionales:** programa académico, jornada, modalidad.
- **Variable objetivo:** indicador de abandono (sí/no) en un periodo definido.

## Tipo de Machine Learning a utilizar
Este caso se aborda principalmente como un problema de **aprendizaje supervisado de clasificación binaria**, donde la etiqueta objetivo es si un estudiante abandona o no.

También podrían explorarse enfoques complementarios (por ejemplo, segmentación de perfiles), pero el alcance inicial se centra en clasificación.

## Algoritmos posibles
Para una primera fase, se pueden comparar modelos con distintos niveles de complejidad:

- Regresión logística (línea base interpretable).
- Árboles de decisión.
- Random Forest.
- Gradient Boosting (XGBoost, LightGBM, CatBoost).
- Support Vector Machines (SVM).

La selección final dependerá de desempeño, interpretabilidad y facilidad de implementación institucional.

## Métricas posibles
Dado que suele existir desbalance entre estudiantes que abandonan y los que no, conviene evaluar más allá de la exactitud:

- **Recall (sensibilidad):** capacidad de detectar casos de abandono.
- **Precision:** proporción de alertas correctas.
- **F1-score:** equilibrio entre precision y recall.
- **ROC-AUC:** calidad de discriminación global.
- **PR-AUC:** útil cuando hay fuerte desbalance de clases.
- **Matriz de confusión:** interpretación operativa de aciertos y errores.

## Justificación: por qué Machine Learning sí aporta valor
Machine Learning aporta valor en este contexto porque:

1. **Permite anticipar riesgos** antes de que el abandono ocurra.
2. **Escala el análisis** a miles de estudiantes de forma sistemática.
3. **Detecta patrones complejos** que no son evidentes con reglas simples.
4. **Mejora la asignación de recursos** de intervención hacia quienes más lo necesitan.
5. **Fortalece la gestión basada en evidencia**, facilitando mejora continua.

En síntesis, el modelo no reemplaza decisiones humanas, sino que funciona como herramienta de apoyo para estrategias de permanencia estudiantil.

## Estructura inicial del proyecto
```text
prediccion-abandono-estudiantil/
├── data/          # Datos crudos y procesados (sin versionar archivos sensibles)
├── notebooks/     # Análisis exploratorio y experimentos
├── reports/       # Informes, visualizaciones y entregables
├── src/           # Código fuente del proyecto
├── .gitignore
├── requirements.txt
└── README.md
```
