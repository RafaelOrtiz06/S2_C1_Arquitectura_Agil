# Microservicios
Es un estilo de arquitectura para favorecer la disponibilidad de un sistema, es importante recordar que es un sistema distribuido
(colección de computadores independientes que a la vista de los usuarios es uno solo)
- Es utilizado en el diseño y construcción de sistemas distribuidos
- Busca reducir la complejidad inherente al diseño y operación de sistemas distribuidos
- El sistema es descompuesto en partes autónomas que a los ojos de los usuarios, es una solución.
- Se despliegan de forma independiente y se enfocan en una funcionalidad de negocio específica
- Desde el punto de vista de la disponibilidad, estas características son esenciales, pues si uno falla, no falla el sistema entero

## Arquitectura Hexagonal
Notación para modelar microservicios.
Busca representar todos los puntos de contacto entre un componente y el mundo que lo rodea. Estos puntos de contacto le permiten a los microservicios,
interactuar con otros microservicios, con entidades y sistemas externos.

## Mecanismos de comunicación
Los conectores llamada-retorno, nos permiten comunicar de forma sincrona o asincrona los componentes de un sistema.
Uno - uno

También est'el esquema publicador - subscriptor, donde la comunicación es intermediada por plataformas de mensajeria que apoyan la entrega
de mensajes de manera asincrona.


### Comunicación
- Comando: Un microservicio puede enviar un comando a otro, este comando se ve como una solicitud o intención que tiene un efecto en el estado del sistema
- Consulta: Petición de información, estas no alteran el estado del sistema
