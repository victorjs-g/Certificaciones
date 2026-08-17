# **Capítulo 4: Seguridad de la red**

Esta documentación será parte de lo aprendido en la certificación CC de ISC2. Se tomarán apuntes de conceptos técnicos y algunos ejemplos de estos, tomando en cuenta que es una certificación donde la conceptualización y el pensamiento crítico como gestor de riesgo IT son muy importantes.

Los módulos que estaremos viendo en el transcurso de la certificación serían:

1. Principios de seguridad
2. Conceptos de respuesta a incidentes, continuidad del negocio y recuperación ante desastres
3. Conceptos de control de acceso
4. Seguridad de la red
5. Operaciones de seguridad

> **Nota:** Debemos ser conscientes de que dominamos el tema actual para pasar al siguiente, por eso es importante la documentación y evaluación por módulo.
> 

## Orden del día del capítulo

- **Módulo 1:** Comprender las redes informáticas (D4.1)
- **Módulo 2:** Comprender las amenazas y ataques (cibernéticos) de red (D4.2)
- **Módulo 3:** Comprender la infraestructura de seguridad de la red (D4.3)
- **Módulo 4:** Resumen

# Módulo 1: Comprender las redes informáticas

## ¿Qué es la red?

Una red no es más que dos o varias computadoras conectadas entre sí, con el fin de enviar información, ya sean datos o recursos. Esto lleva un paso importante, donde se ven involucrados el Hardware, Software, cifrado, protocolos, puertos y más.

## Tipos de redes

Existen diversos tipos de redes donde cada uno cumple con un rol distinto. Existen tipos de redes para fines domésticos, empresariales o globales.

### LAN

**LAN (Local Area Network):** es una red que conecta dispositivos dentro de un área geográfica limitada, por ejemplo, casas, oficinas o campus pequeños.

### WAN

**WAN (Wide Area Network):** es una red que conecta múltiples redes LAN ubicadas en diferentes áreas geográficas o ubicaciones lejanas.

## Dispositivos de red

### Hub

**Hub, Centro o Concentrador:** Un hub es un dispositivo de red que conecta varios equipos dentro de una LAN, pero envía los datos a todos los dispositivos conectados, a diferencia de un switch, que los envía al destino correspondiente.

### Switch

**Switch o Conmutador:** Un switch es un dispositivo que conecta equipos en una LAN y envía la información al dispositivo destino correspondiente, permitiendo además el uso de VLANs y una mejor administración del tráfico.

### Router

**Enrutador o Router:** Un router o enrutador es un dispositivo de red que conecta diferentes redes entre sí y dirige los datos hacia las rutas correspondientes a su destino.

### Firewall

**Firewall o Cortafuegos:** Este es un dispositivo de seguridad que filtra el tráfico y permite decidir qué conexiones entran y cuáles salen de la red según reglas definidas. Estas reglas pueden utilizar ACLs, direcciones IP, puertos, protocolos y otros criterios.

### Servidor

**Servidor o Server:** Un servidor es un sistema o infraestructura que proporciona servicios, recursos o datos a otros dispositivos dentro de una red, conocidos como clientes.

### Host

**Puntos finales o Host:** Un punto final puede ser otro servidor, estación de trabajo de escritorio, computadora portátil, tableta, teléfono móvil o cualquier otro dispositivo conectado a una red.

## Otros términos de redes

### Ethernet

**Ethernet (IEEE 802.3):** Es un estándar que define cómo los dispositivos se conectan y funcionan dentro de una red cableada. Este estándar define aspectos como la velocidad, el cableado, el uso de direcciones MAC y cómo se transmiten los datos dentro de una LAN.

### Dirección MAC

**MAC o Dirección de control de acceso a medios:** Una MAC address es un identificador asociado a una interfaz de red (NIC). Se utiliza principalmente para identificar interfaces dentro de una red local. Los primeros 3 bytes de una dirección MAC tradicionalmente corresponden al identificador asignado al fabricante (OUI), aunque existen direcciones MAC especiales y mecanismos que permiten utilizar direcciones administradas localmente.

### Dirección IP

**Dirección de Protocolo de Internet (IP):** Una IP address es un identificador lógico asignado a una interfaz dentro de una red, que permite la comunicación entre dispositivos y ayuda a determinar el destino de los paquetes de datos.

## Diagrama de red empresarial vs. red doméstica

## Capas inferiores y superiores

### Capas inferiores

Las capas inferiores (1–4) se encargan de transmitir, transportar y enrutar los datos a través de la red. Aquí ocurre la comunicación física y lógica entre dispositivos, incluyendo bits, tramas, paquetes y transporte mediante TCP/UDP.

### Capas superiores

Las capas superiores (5–7) se encargan de la interacción con las aplicaciones y el usuario. Administran sesiones, presentan los datos de forma entendible y permiten la comunicación entre aplicaciones y servicios de red.

## Modelo OSI

### Secuencia del modelo OSI

1. Física
2. Enlace de Datos
3. Red
4. Transporte
5. Sesión
6. Presentación
7. Aplicación

### TCP/IP

- **TCP/IP:** modelo utilizado en Internet y en las redes modernas para implementar la comunicación de red.
- **OSI:** modelo de referencia utilizado principalmente para entender y enseñar cómo funcionan las redes.
- **Diferencia:** TCP/IP representa una arquitectura de protocolos utilizada en la práctica, mientras que OSI proporciona un modelo conceptual de siete capas.

## Protocolos de red

Al momento de enviar un paquete a través de la red se utilizan muchos protocolos, porque dependerá de lo que vayamos a hacer.

### FTP

**FTP (File Transfer Protocol):** Se utiliza para transferir archivos entre un cliente y un servidor. No está limitado únicamente a una LAN.

### SMTP

**SMTP (Simple Mail Transfer Protocol):** Se utiliza principalmente para el envío y la transferencia de correos electrónicos.

### DNS

**DNS (Domain Name System):** Traduce nombres de dominio a direcciones IP y también puede realizar otras consultas relacionadas con nombres y servicios.

### ICMP

**ICMP (Internet Control Message Protocol):** Se utiliza para enviar mensajes de control y diagnóstico en redes IP. Se utiliza en herramientas como Ping y Traceroute.

## Direccionamiento IPv4 e IPv6

### IPv4

IPv4 utiliza direcciones de **32 bits**.

### IPv6

IPv6 utiliza direcciones de **128 bits**.

> **Nota:** Ambos se utilizan hoy en día. IPv4 sigue teniendo una presencia muy amplia, mientras que IPv6 continúa expandiéndose para solucionar, entre otras cosas, la limitación de direcciones de IPv4.
> 

### Ventajas de IPv6

#### Mayor espacio de direccionamiento

Las direcciones IPv6 son de 128 bits, lo que permite aproximadamente 2^128 direcciones, una cantidad muchísimo mayor que la disponible en IPv4.

#### Seguridad

IPv6 fue diseñado teniendo en cuenta mecanismos como IPsec, pero es incorrecto decir que IPsec es obligatorio en IPv6. Actualmente, la seguridad de IPv6 depende de los protocolos y controles utilizados en cada implementación.

#### Calidad de servicio (QoS)

IPv6 incluye campos como Traffic Class y Flow Label que pueden ayudar al tratamiento y clasificación del tráfico, aunque la QoS depende también de la infraestructura y configuración de la red.

## Wi-Fi

Wi-Fi es una tecnología de red inalámbrica que permite conectar dispositivos a Internet o a una red local sin cables, facilitando la movilidad dentro de su alcance. Su seguridad depende de los protocolos y configuraciones utilizados, como WPA2 o WPA3.

Al ser una comunicación inalámbrica, el tráfico puede ser capturado desde el entorno físico si no está correctamente protegido.

## Seguridad en la red

TCP/IP tiene varias vulnerabilidades y muchos de sus protocolos originales no fueron diseñados teniendo en cuenta las amenazas de seguridad actuales, por lo que una red puede ser atacada tanto de forma activa como pasiva.

### DoS/DDoS

Intentan saturar un sistema o red con tráfico o solicitudes excesivas para que deje de funcionar o se vuelva inaccesible.

### Ataques de fragmentación

Consisten en utilizar la fragmentación de paquetes de forma maliciosa, por ejemplo, para evadir controles de seguridad o dificultar el análisis del tráfico.

### Paquetes de gran tamaño

Consiste en el envío de paquetes anormalmente grandes o malformados para intentar sobrecargar o desestabilizar sistemas que no los manejan correctamente.

### Suplantación de identidad (Spoofing)

El atacante falsifica una dirección IP, MAC u otra identidad para hacerse pasar por un usuario o sistema confiable.

### Ataques de intermediario (Man-in-the-Middle)

El atacante intercepta la comunicación entre dos partes para leer, alterar o robar información sin que ellas lo noten.

### Olfateo o monitoreo de red (Sniffing)

Ataque pasivo donde se captura y analiza el tráfico de red para obtener información sin modificar los datos.

## Puertos y protocolos

Existen puertos por donde entra y sale información; sin embargo, tenemos puertos físicos y puertos lógicos.

### Puertos físicos

Los puertos físicos son los puertos de los enrutadores, conmutadores, hubs, computadoras, USB y más, a los que normalmente les conectamos un cable para transmitir datos.

### Puerto lógico / Socket

Un puerto es un identificador lógico dentro de una computadora que permite distinguir qué servicio o aplicación está utilizando una conexión de red.

Diagrama De Red Empresarial vs Red Doméstica

Un socket combina elementos como una dirección IP, un puerto y un protocolo de transporte para identificar un extremo de una comunicación.

### Rangos de puertos

Los puertos se dividen en tres rangos principales:

- **System Ports:** 0–1023
- **User/Registered Ports:** 1024–49151
- **Dynamic/Private Ports:** 49152–65535

> **Nota:** Los puertos registrados pueden estar registrados ante IANA para determinados servicios y aplicaciones.
> 

> **Nota:** Los puertos privados o dinámicos se utilizan normalmente de forma temporal por aplicaciones y clientes para establecer conexiones.
> 

## Puertos y protocolos seguros

### FTP vs. SFTP

- **Puerto 21 — FTP:** protocolo tradicional de transferencia de archivos que no cifra las credenciales ni los datos por sí mismo.
- **Puerto 22 — SFTP:** protocolo de transferencia de archivos seguro que funciona sobre SSH.

### Telnet vs. SSH

- **Puerto 23 — Telnet:** conexión remota tradicional en texto plano.
- **Puerto 22 — SSH:** conexión remota protegida mediante cifrado y mecanismos de autenticación.

### SMTP vs. SMTP Submission

- **Puerto 25 — SMTP:** utilizado principalmente para transferencia de correo entre servidores y no proporciona cifrado por sí mismo.
- **Puerto 587 — SMTP Submission:** utilizado normalmente para el envío de correo por parte de clientes y puede utilizar TLS mediante STARTTLS.

### Time Protocol vs. NTP

- **Puerto 37 — Time Protocol:** protocolo antiguo utilizado para proporcionar la hora.
- **Puerto 123 — NTP:** utilizado para sincronizar la hora entre dispositivos de una red.

### DNS vs. DNS over TLS

- **Puerto 53 — DNS:** DNS tradicional no cifra las consultas.
- **Puerto 853 — DoT:** DNS over TLS permite realizar consultas DNS mediante una conexión protegida con TLS.

### HTTP vs. HTTPS

- **Puerto 80 — HTTP:** comunicación web sin cifrado.
- **Puerto 443 — HTTPS:** HTTP sobre TLS para proteger los datos en tránsito.

### IMAP vs. IMAPS

- **Puerto 143 — IMAP:** permite acceder y sincronizar correos; no cifra la comunicación por defecto.
- **Puerto 993 — IMAPS:** IMAP sobre TLS.

### SNMP

- **Puerto 161/162 — SNMP:** utilizado para administración y monitoreo de dispositivos de red.
- **SNMPv3:** incorpora mecanismos de autenticación, integridad y, según el nivel de seguridad utilizado, cifrado.

### SMB

- **Puerto 445 — SMB:** utilizado principalmente en sistemas Windows para compartir archivos, impresoras y otros recursos de red.

> **Nota:** SMB puede utilizar mecanismos de seguridad y cifrado dependiendo de la versión y configuración.
> 

### NFS

- **Puerto 2049 — NFS:** utilizado para compartir sistemas de archivos en red.

> **Nota:** NFS no debe considerarse automáticamente una versión "segura" de SMB. Su seguridad depende de la versión, configuración y mecanismos de autenticación.
> 

### LDAP vs. LDAPS

- **Puerto 389 — LDAP:** utilizado para consultar y administrar servicios de directorio.
- **Puerto 636 — LDAPS:** LDAP sobre SSL/TLS para cifrar la comunicación.

## TCP Three-Way Handshake

El protocolo TCP utiliza un método de establecimiento de conexión conocido como **Three-Way Handshake**.

### 1. SYN

El cliente envía un paquete **SYN** al puerto del servidor para solicitar el establecimiento de una conexión TCP.

### 2. SYN-ACK

El servidor responde al paquete SYN con un **SYN/ACK**, indicando que recibió la solicitud y está dispuesto a establecer la conexión.

### 3. ACK

Finalmente, el cliente responde con un **ACK**. En este punto, se establece la conexión TCP y las aplicaciones pueden comenzar a intercambiar datos.

# Módulo 2: Comprender las amenazas y ataques (cibernéticos) de red

## Tipos de amenazas

### Suplantación de identidad / Spoofing

Un ataque con el objetivo de obtener acceso o engañar a un sistema o usuario mediante el uso de una identidad falsificada.

### Phishing

Un ataque que intenta engañar a los usuarios legítimos para que revelen información, descarguen malware o accedan a sitios web maliciosos mediante correos electrónicos, mensajes, direcciones URL o hipervínculos fraudulentos.

### DoS/DDoS

Un ataque de denegación de servicio (DoS) busca consumir recursos de un sistema o red para impedir la actividad legítima.

Cuando el ataque utiliza numerosos sistemas comprometidos para generar el tráfico, se conoce como **DDoS**.

### Virus

El virus informático es un tipo de malware que puede propagarse al insertar su código en otros archivos o programas.

### Worm / Gusano

Los gusanos pueden propagarse automáticamente entre sistemas sin necesitar la intervención directa del usuario.

### Troyano

Es un programa que parece legítimo o benévolo, pero contiene una funcionalidad maliciosa detrás de escena.

### Ataque en ruta / On-Path Attack / MITM

Los atacantes se ubican entre dos dispositivos para interceptar o modificar información destinada a uno o ambos puntos finales.

### Canal lateral / Side-Channel Attack

Un canal lateral es un tipo de ataque donde el atacante no rompe directamente el cifrado ni el sistema lógico, sino que obtiene información observando efectos secundarios del sistema.

### Amenaza persistente avanzada / APT

Se refiere a amenazas que demuestran un nivel alto de sofisticación técnica y operativa y que pueden mantener una presencia prolongada dentro de un entorno.

### Insiders / Amenazas internas

Son amenazas que surgen de personas que tienen algún nivel de confianza o acceso dentro de una organización.

Estas amenazas pueden ser:

- **Intencionales:** empleados descontentos o involucrados en espionaje.
- **No intencionales:** usuarios legítimos que son víctimas de phishing, ingeniería social u otras estafas.

### Malware

Un programa o conjunto de código malicioso que se inserta en un sistema con la intención de comprometer la confidencialidad, integridad o disponibilidad de los datos, aplicaciones o sistema operativo.

### Ransomware

Malware utilizado para facilitar un ataque de rescate. Los ataques de ransomware suelen utilizar criptografía para bloquear o cifrar archivos y exigir un pago a cambio de una posible recuperación.

## Identificar amenazas y herramientas utilizadas para prevenirlas

### Reducción de la superficie de ataque

Si un sistema no necesita un servicio o puerto, es recomendable deshabilitarlo para reducir la superficie de ataque.

### Firewalls

Los Firewalls ayudan a prevenir distintos tipos de ataques. Existen cortafuegos basados en red y cortafuegos basados en host.

### HIDS

**HIDS (Host-Based Intrusion Detection System):** vigila y analiza actividades sospechosas dentro de un host específico.

### SIEM

**SIEM (Security Information and Event Management):** centraliza, correlaciona y analiza eventos de seguridad provenientes de múltiples fuentes.

## Sistema de detección de intrusos (IDS)

Un IDS es una herramienta de ciberseguridad que identifica actividades sospechosas o posibles ataques mediante el análisis de tráfico, logs y eventos.

### HIDS

**Host-Based IDS:** supervisa un host específico.

### NIDS

**Network-Based IDS:** supervisa el tráfico de una red o segmento de red.

## Prevención de amenazas

### Mantener aplicaciones actualizadas

Los proveedores de software lanzan actualizaciones que pueden incluir mejoras de seguridad y parches.

### Eliminar o deshabilitar servicios innecesarios

Si un sistema no necesita un servicio o protocolo, no debería estar funcionando.

### IDS e IPS

Los sistemas de detección y prevención de intrusiones observan la actividad e intentan detectar amenazas.

Un **IDS** genera alertas, mientras que un **IPS** también puede bloquear o detener determinadas actividades maliciosas.

### Software antimalware

Ayuda a prevenir y detectar diferentes tipos de malware en los hosts.

### Antivirus

Las soluciones modernas de seguridad para endpoints han evolucionado y suelen incorporar capacidades de detección y respuesta más amplias que las de un antivirus tradicional.

> **Nota:** Muchas soluciones de seguridad para host incluyen capacidades de IDS o IPS.
> 

## Escaneos de seguridad

Podemos hacer escaneos con herramientas como:

- **Nmap**
- **Zenmap**
- **Nessus**

Estas herramientas ayudan a identificar puertos, hosts, servicios expuestos, configuraciones y posibles vulnerabilidades.

> **Nota:** Los escaneos deben realizarse de forma autorizada y controlada.
> 

## Firewall

Un firewall o cortafuegos es un sistema de seguridad que filtra el tráfico de red y decide qué conexiones se permiten y cuáles se bloquean según reglas establecidas.

### Firewall tradicional

Trabaja principalmente con información de las capas 3 y 4 del modelo OSI, como:

- Direcciones IP
- Puertos
- Protocolos

### NGFW

Un **NGFW (Next-Generation Firewall)** puede analizar información de capas superiores, incluyendo:
- Aplicaciones
- Usuarios
- Contenido
- Amenazas
- Tráfico de red

Además, puede integrar capacidades de **IPS** y otras funciones de seguridad.

# Módulo 3: Comprender la infraestructura de seguridad de la red

## Centro de datos (Data Center)

Cuando hablamos de un centro de datos hay dos opciones: la organización puede contratar servicios de un centro de datos o puede poseer y administrar su propio centro de datos.

### Energía

La energía alimenta los dispositivos dentro de la red. Debe tenerse en cuenta el mantenimiento y la evaluación constante de la fuente de energía.

Una práctica importante es contar con **redundancia energética**.

### Supresión de incendios

En un Data Center es importante tener sistemas que ayuden a proteger el entorno en caso de una emergencia.

### Centros de datos y armarios

Los centros de datos y los armarios de cableado pueden incluir:

- Teléfonos
- Equipos de red
- Servidores
- Switches
- Componentes de cableado
- Equipos ISP
- Equipos de telecomunicaciones

### HVAC / Ambiental

Los equipos de alta densidad requieren refrigeración y flujo de aire adecuados.

El rango recomendado para la temperatura del entorno de equipos de TI suele situarse aproximadamente entre **18 °C y 27 °C**, dependiendo del estándar y las condiciones del centro de datos.

También deben controlarse contaminantes como:

- Polvo
- Humedad
- Humo
- Otros contaminantes ambientales

## Redundancia

El concepto de redundancia consiste en diseñar sistemas con componentes duplicados o alternativos para que, si ocurre una falla, exista otro componente capaz de continuar el servicio.

La redundancia puede contribuir a conseguir **alta disponibilidad**.

## Acuerdos y contratos

### Acuerdo de reciprocidad

Dos empresas acuerdan ayudarse mutuamente en caso de incidentes o desastres, compartiendo recursos o soporte temporal.

### JOA

**JOA (Joint Operating Agreement):** acuerdo operativo conjunto más formal y estructurado, donde se definen responsabilidades, recursos y cómo ambas organizaciones trabajarán juntas.

### MOU

**MOU (Memorandum of Understanding):** documento que expresa la intención de cooperación entre las partes.

### MOA

**MOA (Memorandum of Agreement):** parecido al MOU, pero suele ser más específico y formal, detallando responsabilidades y compromisos concretos.

### SLA

**SLA (Service Level Agreement):** documento que define qué servicio será brindado, cómo será entregado y cuáles niveles mínimos deben cumplirse.

## Cloud / Nube

Cloud Computing es el uso de servidores, almacenamiento, aplicaciones y otros recursos tecnológicos a través de Internet, sin necesidad de tener toda la infraestructura físicamente en la empresa o computadora.

### Redundancia en la nube

La redundancia en la nube permite que, si un componente, sistema o ubicación falla, los servicios puedan utilizar otros recursos disponibles para mantener la disponibilidad.

## Beneficios de Cloud Computing

- Uso medido y facturación según recursos consumidos.
- Reducción del costo de propiedad.
- Reducción de costos de energía y mantenimiento.
- Escalabilidad.
- Acceso a infraestructura sin necesidad de mantener todo el hardware localmente.

## Modelos de servicio Cloud

### SaaS

**Software as a Service:** el proveedor ofrece un software funcionando y el usuario simplemente accede y lo utiliza.

### IaaS

**Infrastructure as a Service:** el proveedor ofrece infraestructura como almacenamiento, red, CPU, memoria y máquinas virtuales.

### PaaS

**Platform as a Service:** el proveedor ofrece una plataforma y entorno preparados para desarrollar o ejecutar aplicaciones.

## Modelos de implementación Cloud

### Nube pública

Servicios cloud ofrecidos por un proveedor y utilizados por múltiples clientes.

### Nube privada

Infraestructura cloud exclusiva para una organización.

### Nube híbrida

Combinación de nube pública y privada.

### Nube comunitaria

Varias organizaciones comparten una infraestructura cloud porque tienen necesidades, normas u objetivos similares.

## Proveedores de servicios

### MSP

**MSP (Managed Service Provider):** empresa externa que administra servicios tecnológicos para otras organizaciones.

### MDR

**MDR (Managed Detection and Response):** servicio que monitorea continuamente la seguridad de una empresa y responde ante ataques o actividades sospechosas.

### SLA

**SLA (Service Level Agreement):** acuerdo entre un proveedor y un cliente donde se establecen servicios, responsabilidades y niveles de servicio.

## Diseño de red

El objetivo del diseño de red es satisfacer los requisitos de comunicación de datos y proporcionar un rendimiento general eficiente.

### Segmentación de redes

Implica separar áreas dentro de una empresa para limitar la comunicación innecesaria y proteger información sensible.

Puede realizarse mediante:

- Firewalls
- VLANs
- ACLs
- Otros controles de seguridad

### DMZ

Una **DMZ (Demilitarized Zone)** es una red intermedia entre Internet y la red interna de una organización.

### VLAN

Una **VLAN (Virtual Local Area Network)** permite segmentar lógicamente una red mediante switches.

### VPN

Una **VPN (Virtual Private Network)** crea un túnel de comunicación protegido para permitir comunicación entre dispositivos o redes a través de una red no confiable como Internet.

### NAC

**NAC (Network Access Control):** controla y valida qué dispositivos o usuarios pueden conectarse a la red.

## Defensa en profundidad

La defensa en profundidad es una estrategia de seguridad que utiliza múltiples capas de protección dentro de una organización.

La idea es que, si un control falla, existan otros mecanismos que continúen protegiendo los sistemas, redes y datos.

### Capas de defensa en profundidad

- **Datos:** cifrado, DLP y controles de acceso.
- **Aplicación:** WAF, monitoreo y controles de seguridad.
- **Host:** antivirus, firewalls y parches.
- **Red interna:** IDS, IPS, NAC y firewalls internos.
- **Perímetro:** firewalls, DMZ y análisis de malware.
- **Físico:** cerraduras, cámaras y controles de acceso físico.
- **Políticas y concientización:** reglas, procedimientos y capacitación.

## Zero Trust

Zero Trust es un modelo de seguridad basado en no confiar automáticamente en ningún usuario o dispositivo, incluso si ya está dentro de la red.

Cada acceso debe autenticarse y autorizarse según las políticas y permisos establecidos.

## Microsegmentación

La microsegmentación divide la red o el entorno en pequeñas áreas o segmentos para limitar el movimiento lateral de un atacante dentro de la organización.

## NAC

NAC controla el acceso a la red verificando la identidad del usuario y, dependiendo de la solución, el estado del dispositivo antes de permitir la conexión.

Si el dispositivo no cumple con las políticas de seguridad, puede ser:

- Bloqueado.
- Limitado.
- Enviado a una red de cuarentena.

## Segmentación de red

### DMZ

Una DMZ es una red intermedia entre Internet y la red interna de una organización.

### Sistemas embebidos e IoT

Los sistemas embebidos y dispositivos IoT son equipos conectados que controlan funciones físicas o servicios específicos.

Debido a sus riesgos de seguridad, deben ser aislados mediante segmentación de red, como VLANs y Firewalls.

### VLAN Hopping

Los ataques de **VLAN hopping** pueden permitir a un atacante acceder a tráfico o segmentos de VLAN que no debería poder alcanzar.

> **Nota:** Las VLAN ayudan a segmentar la red, pero no deben considerarse por sí solas como una medida de seguridad suficiente.
> 

## VPN

Una VPN crea un túnel protegido sobre Internet para permitir la comunicación segura entre un dispositivo y una red o entre dos redes.

### VPN de acceso remoto

Permite que un usuario se conecte desde una ubicación externa a los recursos de la red corporativa.

### VPN Site-to-Site

Permite conectar dos redes o ubicaciones diferentes mediante un túnel protegido