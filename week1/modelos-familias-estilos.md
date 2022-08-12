# Modelos y familias de estilos
Existen muchas formas de afrontar el diseño de una arquitectura:

## Proceso ad-hoc
- Procesos de diseño de manera informal, no son repetibles y tampoco mejorables
- Demandan un bajo esfuerzo para su gestión
- No aporta información que permita anlizar y mejorar sus actividades y productos

## Proceso tradicional
- Concibe el proceso de diseño como un proceso de contrucción del software(solo cuando la arquitectura esté finalizada se empieza con el proceso de diseño detallado y construcción)
- Ventaja de analizar todos los aspectos relevantes antes de empezar la construcción
- El tiempo es muy alto, puede durar meses y hasta años, en algunos casos, al terminar la arquitectura, el problema ya ha cambiado o stakeholders se han hido

## Proceso adaptativo(usado en el curso)
- Propone ir diseñando la arquitectura de forma iterativa e incremental, se basa en el diseño en un corto periodo de tiempo(sprint)
- Identificamos 3 actividades principales:
  1. Especificación de requisitos de calidad
  2. Diseño minimo que satisfaga un conjunto de requisitos
  3. Validación del diseño mediante experimentación(hipótesis que deberá ser refutada o validada)
- La actividad del diseño queda documentada en modelos de arquitectura organizadas en vistas a diferentes niveles de detalle
- Toma como base un escenario de calidad

### Estructura de un escenario de calidad
- Fuente
- Estimulo
- Artefacto
- Respuesta
- Medida de la respuesta
- Ambiente

# La historia de arquitectura
- Tiene una narrativa similar a las historias de usuario
- Como <Fuente>, cuando <Estimulo> dado que <Ambiente>, quiero <Descripción Funcional> para <Respuesta>. Esto debe suceder <Medida de la respuesta>
