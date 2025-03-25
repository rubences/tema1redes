Ejercicios Resueltos - Introducción a las Redes de Ordenadores

# 1. Explica las diferencias entre el modelo OSI y el modelo TCP/IP.
Característica	Modelo OSI	Modelo TCP/IP
Número de capas	7 capas (Física, Enlace de datos, Red, Transporte, Sesión, Presentación y Aplicación)	4 capas (Acceso a red, Internet, Transporte y Aplicación)
Orientación	Modelo teórico con capas bien definidas	Modelo práctico basado en protocolos usados en redes reales
Capa de aplicación	Separa la presentación y sesión	Todo se maneja dentro de la capa de aplicación
Capa de transporte	Solo soporta comunicación orientada a conexión	Soporta tanto conexión (TCP) como sin conexión (UDP)
Ruteo de paquetes	Se realiza en la capa de red	Se realiza en la capa de internet
Flexibilidad	Mayor flexibilidad para definir protocolos en cada capa	Enfocado en la eficiencia y en protocolos ya estandarizados
Conclusión: El modelo OSI es más estructurado y teórico, mientras que el TCP/IP es un modelo más práctico y utilizado en la actualidad.

# 2. ¿Cuál es la función de la capa de transporte en ambos modelos?
La capa de transporte es responsable de proporcionar comunicación confiable entre dispositivos de red.

En OSI: La capa de transporte (capa 4) asegura la entrega de datos sin errores, en secuencia y sin duplicaciones. Ejemplo: TCP.
En TCP/IP: También se encarga de la transmisión de datos entre dispositivos, pero permite comunicación confiable (TCP) o no confiable (UDP).
# 3. Explica las principales diferencias entre TCP y UDP.
Característica	TCP (Transmission Control Protocol)	UDP (User Datagram Protocol)
Orientación	Orientado a conexión	No orientado a conexión
Fiabilidad	Confiable (usa acuses de recibo y retransmisiones)	No confiable (sin acuses de recibo)
Orden de datos	Garantiza que los datos lleguen en orden	No garantiza el orden de llegada
Velocidad	Más lento debido al control de errores	Más rápido, pero sin control de errores
Ejemplos de uso	Descarga de archivos, correo electrónico, navegación web	Streaming de video/audio, videollamadas, juegos en línea
# 4. ¿Qué protocolo de la capa de aplicación se utiliza para la transferencia de archivos?
El protocolo FTP (File Transfer Protocol) es el estándar para la transferencia de archivos en redes TCP/IP. Utiliza los puertos 20 y 21 para la conexión de datos y control respectivamente.

También existen alternativas como:

SFTP (Secure FTP): Transferencia segura a través de SSH.
TFTP (Trivial FTP): Versión simplificada sin autenticación.
# 5. Describe el proceso de resolución de nombres en DNS.
DNS (Domain Name System) traduce nombres de dominio en direcciones IP. El proceso de resolución de nombres sigue estos pasos:

El usuario ingresa una URL en el navegador.
El sistema operativo consulta la caché DNS local.
Si no hay coincidencia, la solicitud se envía al servidor DNS configurado en la red.
El servidor DNS busca en su caché. Si no encuentra la respuesta, reenvía la solicitud a servidores DNS raíz.
Los servidores raíz responden con el servidor de nombres del dominio.
El servidor DNS del dominio devuelve la dirección IP correspondiente.
El navegador establece una conexión con el servidor web usando la IP obtenida.
Ejemplo:

www.google.com → 142.250.185.4
# 6. Explica el proceso de comunicación entre dos dispositivos en una red usando el modelo TCP/IP.
Cuando dos dispositivos se comunican, siguen estas etapas:

Capa de Aplicación: La aplicación del usuario (ej., navegador) genera los datos y los pasa a la capa de transporte.
Capa de Transporte:
Si usa TCP, establece una conexión (handshake de 3 vías).
Si usa UDP, envía los datos sin establecer conexión.
Capa de Internet: Se asigna una dirección IP de origen y destino y se decide la mejor ruta.
Capa de Acceso a Red: Se encapsulan los datos en tramas Ethernet o WiFi y se transmiten a través del medio físico.
El dispositivo receptor procesa los datos y los envía a la aplicación destino.