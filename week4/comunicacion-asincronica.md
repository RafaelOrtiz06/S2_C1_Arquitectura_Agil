# Comunicación Asincrónica
El uso de comandos y consulta realizadas directamente entre los servicios mediante el uso de APIs sincrónicas generan acoplamiento entre ellos

La arquitectura hexagonal nos indica que los microservicios pueden conectarse también de manera asincronica mediante mensajes, mediante la
coreografía basada en mensajes.

Los eventos representan hechos ocurridos, historias de acciones ocurridas.
- Se requiere una intermediación al nivel de conector entre los microservicios, el conector o intermediario es por lo general una plataforma de mensajería que se encarga de la perstistencia, almacenamiento y entrega de los mensajes.
- Los microservicios no se conocen entre si, solo se comunican mediante mensajes, por lo que no genera un acoplamiento fuerte

## Comunicación orientada a mensajes
- Favorece la disponibilidad gracias al desacoplamiento anterior.
- Un microservicio puede recibir comandos (crear, actualizar)
- Una vez terminado el comando, puede generar eventos comunicando la ejecución correcta o incorrecta de ese comando.
- En este esquema el fallo de un microservicio no es visible para otros, como sucedería si la comunicación fuera sincronica