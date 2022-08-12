# Vistas y puntos de vista

## Puntos de vista
Plantillas o patrones que definen modelos y elementos de arquitectura que son útiles para expresar decisiones de diseño a un grupo de interesados

## Vista
Aplicación de un punto de vista en un proyecto y contexto específico(instancia de un punto de vista)

### Propuestas
- 4+1
- Views and beyond
- Views and perspective(usada en el curso)


### Punto de vista de contexto
Dejar clara la frontera entre el sistema y lo externo al sistema(tipos de usuarios y sistemas de información a interactuar).
Permite identificar el alcance del proyecto y los actores ivolucrados
- Orientado a todos los interesados en el sistema, párticularmente a los desarrolladores

### Punto de vista funcional
El más utilizado e importante, su propósito principal es describir como funciona el sistema. Esta descripción se hace normalmente a partir de los componentes
y conectores, que estructuran el sistema o alguno de los módulos a diseñar.

### Punto de vista de información
Describe la forma en la que el sistema amacena, manipula y distribuye la información. Se puede usar para mostrar el flujo de datos.
- Orientado a los arquitectos de información y encargados de bases de datos

### Punto de vista de concurrencia
- Describe la estategia de concurrencia del sistema, es decir, en cuales se usan procesos y en cuales hilos de ejecución.
- Busca asignar componentes a unidades de procesamiento como procesos e hilos de ejecución.
- Define los medios de comunicación para la interacción entre estos procesos
- Orientado a desarrolladores y administradores de infraestructura de cómputo

### Punto de vista de desarrollo
- Presenta el proceso sugerido de construcción de la arquitectura
- Su objetivo es presentar los paquetes, módulos y subsistemas asi como dependencias entre ellos y posibles estrategias de desarrollo
- Orientada a desarrolladores

### Punto de vista de despliegue
- Describe donde será desplegado el sistema y sus componentes.
- El objetivo es acordar con el cliente la tecnologia y la capacidad de procesamiento requerida para la operación
- Orientada a administradores de la plataforma, arquitectos de infraestructura

### Punto de vista de operación
- Describe el mecanismo de operación y mantenimiento del producto cuando esté en producción
- Entender implicaciones del diseño en facilidad de mantenimiento del sistema
- Orientado a administradores del sistema y encargados de operación
