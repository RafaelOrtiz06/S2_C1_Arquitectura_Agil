# Comunicación Sincrónica
Comunicación entre microservicios de manera sincrónica, tenemos 2 elementos que son: comandos y consultas
Justamente una estrategía para favorecer la disponibilidad es el uso de microservicios.

Si seleccionamos un estilo de comunicación sincrónica como el llamado de apis tipo rest, etc. Realizamos 2 tipos de operaciones:
- Los comandos: Afectan el estado de la aplicación, son intenciones(crear orden de compra)
- las consultas: No tienen efecto de borde, extrae información almacenada y no son una intención

Al ofrecer APIs como mecanismos de exposición de funcionalidades, sean comandos o consultas, generamos un acoplamiento con los consumidores de estos servicios

Este acoplamiento podemos verlo como el conocimiento de un microserviio que hace un llamado a otro para ejecutar un comando o cosulta.

Una táctica para desacoplar y ocultar las instancias activas de los microservicios en operación es la utilización de un API Gateway

## API Gateway
Oculta a los consumidores la localización y disponibilidad de los microservicios, ofreciendo un único punto de ingreso a las peticiones de los consumiedores
y redireccionando esas peticiones a los microservicios correspondientes en caso de encontrarlos disponibles.
Con el uso del api gateway, facilitamos el enmascaramiento de fallas en los microservicios, sin embargo, se siguen presentando situaciones que
van en contra de la disponibilidad:
- Los microservicios ofrecen funcionalidades mezcladas entre comandos y consultas, esto hace que algunas consultas tomen tiempo, afectando a algunos comandos
dando la sensación de indisponibilidad en el sistema
- Aún puede ser necesaria la orquestación entre servicios para resolver una operación, si uno de los microservicios falla, el otro puede verse afectado y 
generar una falla.

Una estrategía para solucionar este escenario es dividir y especializar los apis de los microservicios. Indica que podemos separar los comandos de las consultas.
Asi separamos operaciones que potencialmente pueden tomar un tiempo mayor como las consultas de otras operaciones más rápidas como los comandos.
Otro punto es que consultas que no afectan el estado pueden ser ejecutadas en paralelo para responder a las solicitudes de los usuarios.
De otro lado concentramos los comandos en un microservicio que no se verá afectado por las consultas y se ejecutan en ambientes de procesamiento diferentes

### Este patrón se conoce como CQRS por sus siglas en inglés y se refiere a la separación de responsabilidades entre comandos y consultas.
