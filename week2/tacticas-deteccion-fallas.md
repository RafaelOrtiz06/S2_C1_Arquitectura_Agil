# Tácticas para detección de fallas
Favorecen la disponibilidad, aunque pueden ser costosas, a nivel de tiempo, esfuerzo y económicamente:
- Omisión: El sistema no responde ante un estimulo
- Caída: El sistema repetidamente presenta fallas de omisión
- Tiempo: El sistema responde en un tiempo fuera de lo establecido
- Respuesta: El sistema responde pero la respuesta es incorrecta

## Detección de fallas
### Ping - Echo, Monitor, HeartBeat
La principal táctica para la detección es el uso de un componente de monitoreo, cuando el componente de monitoreo toma la iniciativa y pregunta,
se llama ping-echo, cuando el otro componente es el que notifica al monitor, se le denomina HeartBeat

### Voting
Esta táctica usa 3 o un número impar de componentes, ejecuta la misma operación y envía el resultado a un componente de monitoreo,
si este encuentra diferencias, identifica el componente que presenta la falla y la enmascara

## Recuperación de fallas
Una vez identificadas las fallas, se debe tomar decisiones para enmascararlas y asegurarnos que no sean visibles para los usuarios.

### Redundancia Activa
Una común es replicar el procesamiento, qui se tiene un componente principal y uno redundante, cuando se requiere la ejecución de una función,
ambos la ejecutan, de esta forma el estado del sistema está siempre sincronizado entre todos los componentes

### Redundancia Pasiva
El componente principal ejecuta las operaciones, periodicamente sincroniza su estado con los sistemas pasivos redundantes

### Degradación
Identificar las funcionalidades principales del sistema y darles prioridad, osea si hay degradación, los recursos irán a los componentes y servicios de mayor 
prioridad

### Reconfiguración
Identificar un componente defectuoso y retirarlo de la operación


## Prevención de fallas
