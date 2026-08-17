# **Capítulo 5: Operaciones de seguridad**

# **Orden del día del capítulo**

- **Módulo 1:** Comprender la seguridad de los datos (D5.1)
- **Módulo 2:** Comprender el endurecimiento del sistema (D5.2)
- **Módulo 3:** Comprender las mejores prácticas de políticas de seguridad (D5.3)
- **Módulo 4:** Comprender la capacitación de concientización sobre seguridad (D5.3, D5.4)

# **Módulo 1: Comprender la seguridad de los datos**

## **Manejo de datos**

Los datos son representaciones de información, hechos, valores o registros que pueden ser almacenados, procesados, transmitidos y protegidos.

### **Data Life Cycle**

Este hace referencia al ciclo de vida de un dato dentro de una organización o individuo.

- **Creación (Creation):** Proceso donde los datos son generados o recopilados por un usuario, sistema o dispositivo.
- **Almacenamiento (Storage):** Etapa donde los datos son guardados y protegidos en medios físicos o digitales.
- **Uso (Use):** Momento en el que los datos son accedidos, procesados o utilizados para operaciones y actividades.
- **Compartición (Sharing):** Proceso de transmitir o compartir datos entre usuarios, sistemas u organizaciones.
- **Archivado (Archiving):** Conservación de datos a largo plazo para referencia, cumplimiento o recuperación futura.
- **Destrucción (Destruction/Disposal):** Eliminación segura de los datos para evitar su recuperación no autorizada.

Nota: Algunos gobiernos exigen conservar determinados datos durante períodos específicos y llevar controles sobre su ciclo de vida.

Nota: Los períodos de retención de registros médicos dependen de la legislación y regulación aplicable. Por ejemplo, HIPAA establece requisitos de conservación para determinados registros y documentación, pero no establece una regla general de que todos los registros médicos deban conservarse exactamente durante 10 años. De igual forma, OSHA establece períodos de conservación específicos para determinados registros relacionados con lesiones y exposición laboral, algunos de los cuales pueden llegar a 30 años.

### **Prácticas de manejo de datos**

La clasificación es el proceso de reconocer o identificar los impactos organizacionales si la información sufre algún compromiso de seguridad relacionado con las características de la tríada CIA.

#### **Clasificación de datos**

La clasificación de datos es el proceso de categorizar la información según su sensibilidad, valor e impacto para la organización en caso de pérdida, modificación o divulgación. Su objetivo es determinar qué nivel de protección necesita cada dato para preservar la confidencialidad, integridad y disponibilidad. Las organizaciones pueden manejar niveles como altamente restringido, moderadamente restringido, sensibilidad baja y público.

#### **Etiquetado de datos**

El etiquetado de datos consiste en asignar marcas o etiquetas visibles a la información para indicar su nivel de sensibilidad y manejo requerido. El etiquetado representa visualmente la clasificación del dato y ayuda a controlar quién puede acceder, compartir o proteger determinada información.

#### **Retención de datos**

La retención de datos define cuánto tiempo una organización debe conservar la información antes de eliminarla. Esto depende de leyes, regulaciones, estándares y políticas internas. Retener datos más tiempo del necesario aumenta costos, consumo de almacenamiento y riesgos de seguridad.

#### **Destrucción de datos**

La destrucción de datos es el proceso de eliminar información de manera segura para evitar su recuperación. Dependiendo del medio de almacenamiento, pueden utilizarse métodos como borrado seguro, sobrescritura, desmagnetización o destrucción física mediante trituración. Esto ayuda a evitar la remanencia de datos y protege la información sensible.

### **Registro y monitoreo de eventos de seguridad**

#### **Eventos de seguridad**

Un evento es cualquier acción o cambio que ocurre dentro de un sistema, red o dispositivo. Estos eventos pueden incluir inicios de sesión, cambios de configuración, accesos a recursos, errores o actividades sospechosas.

#### **Registros (Logs)**

Los registros o logs son archivos que almacenan información sobre eventos ocurridos dentro de la infraestructura tecnológica. Su función es permitir el monitoreo, análisis y seguimiento de actividades realizadas por usuarios, sistemas o dispositivos.

#### **Información que contienen los logs**

Los registros pueden incluir identificaciones de usuarios, actividades del sistema, fechas y horas de eventos, identidad y ubicación de dispositivos, intentos exitosos o fallidos de acceso, cambios de configuración y activación o desactivación de mecanismos de seguridad.

#### **Importancia del monitoreo**

El monitoreo de eventos y registros permite detectar incidentes de seguridad, actividades sospechosas, fallos operativos y violaciones de políticas. También ayuda a correlacionar eventos de múltiples sistemas para comprender mejor un ataque o problema dentro de la organización.

#### **Auditoría y análisis forense**

Los logs son esenciales para auditorías e investigaciones forenses, ya que permiten mantener trazabilidad y responsabilidad sobre las acciones realizadas dentro de los sistemas. Por esta razón, los registros deben conservar su integridad y protegerse contra modificaciones o eliminaciones no autorizadas.

#### **Protección y retención de logs**

Los registros pueden contener información sensible, por lo que deben protegerse mediante controles de acceso, cifrado y políticas de retención. Además, las organizaciones deben preservar los logs necesarios para evitar la pérdida de evidencia ante incidentes de seguridad.

**Este es un ejemplo de evento de seguridad de datos.**
![Evento de Seguridad](./images/Evento%20De%20Seguridad.png)
### **Mejores prácticas de registro de eventos**

#### **Monitoreo de ingreso**

El monitoreo de ingreso consiste en supervisar el tráfico y los intentos de acceso que entran a la infraestructura para detectar amenazas o actividades sospechosas. Para ello se utilizan herramientas como Firewalls, gateways, servidores de autenticación remota, IDS/IPS, SIEM y soluciones antimalware.

#### **Monitoreo de salida**

El monitoreo de salida se enfoca en controlar y proteger los datos que salen de la organización mediante soluciones DLP (Data Loss Prevention), evitando fugas o pérdidas de información sensible. Estas soluciones pueden inspeccionar correos electrónicos, archivos adjuntos, copias a dispositivos portátiles, transferencias FTP, publicaciones web y APIs.

### **Criptografía**

La criptografía es el conjunto de técnicas utilizadas para proteger información mediante métodos matemáticos, incluyendo cifrado, hashing y firmas digitales. El cifrado transforma datos legibles (texto plano) en datos ilegibles (texto cifrado) para evitar accesos no autorizados.

#### **Cifrado**

El cifrado es el proceso de transformar información legible (texto plano) en información ilegible (texto cifrado) mediante algoritmos y claves criptográficas, con el objetivo de proteger los datos contra accesos no autorizados.

#### **Cifrado simétrico**

El cifrado simétrico utiliza una misma clave para cifrar y descifrar la información. Es rápido y eficiente, pero requiere que las partes involucradas puedan obtener y proteger la clave de manera segura.

#### **Cifrado asimétrico**

El cifrado asimétrico utiliza dos claves relacionadas: una clave pública y una clave privada. Dependiendo del uso, una clave puede utilizarse para cifrar y la otra para descifrar. También se utiliza en firmas digitales y mecanismos de autenticación.

#### **Hashing**

El hashing es un proceso criptográfico que transforma datos de cualquier tamaño en un valor de longitud determinada llamado hash. Su función principal es verificar la integridad de la información, ya que cualquier cambio en los datos debería producir un valor hash diferente.

#### **Firmas digitales**

Las firmas digitales permiten verificar la autenticidad e integridad de un mensaje o documento y proporcionan evidencia de que fue firmado utilizando la clave privada correspondiente. También ayudan a garantizar que el contenido no haya sido modificado después de la firma.

# **Módulo 2: Comprender el endurecimiento del sistema**

## **Descripción general de la gestión de la configuración**

La gestión de la configuración es un proceso y una disciplina que se utiliza para garantizar que los únicos cambios realizados en un sistema sean aquellos que han sido autorizados y validados. Esta incluye componentes esenciales que veremos a continuación.

### **Identificación**

Se basa en la identificación de la línea base de un sistema y todos sus componentes, interfaces y documentación.

### **Línea Base (Baseline)**

Es una configuración o estado de referencia aprobado de un sistema. Sirve como punto de comparación para determinar si el sistema cumple con los requisitos de seguridad y configuración establecidos.

### **Control de Cambios**

Es el proceso utilizado para gestionar, revisar y aprobar modificaciones realizadas en sistemas, configuraciones o líneas base. Su objetivo es garantizar que los cambios sean seguros y estables.

### **Verificación**

La verificación consiste en comprobar que los cambios, configuraciones o controles implementados funcionan correctamente y cumplen con los requisitos esperados. Su objetivo es validar que el sistema opere de manera adecuada, segura y conforme a la línea base o configuración aprobada.

### **Auditoría**

La auditoría es un proceso más formal de revisión y evaluación que busca determinar si los sistemas, controles y cambios cumplen con políticas, estándares, regulaciones y requisitos de seguridad establecidos por la organización o entidades externas.

Nota: Durante la gestión de configuración y control de cambios, es recomendable probar primero las actualizaciones o modificaciones en entornos limitados o segmentados antes de implementarlas a gran escala. Esto permite verificar estabilidad, compatibilidad y seguridad sin afectar toda la infraestructura. Si el cambio funciona correctamente, entonces puede desplegarse progresivamente al resto de los sistemas.

Nota: Todo cambio debe contar con un plan de reversión o recuperación en caso de fallos o interrupciones en producción. Para ello pueden utilizarse mecanismos como backups, snapshots, puntos de restauración, imágenes del sistema, rollback de configuraciones y más.

# **Módulo 3: Comprender las políticas de seguridad de mejores prácticas**

## **Políticas de seguridad comunes**

Aquí estaremos viendo las 6 políticas más implementadas a nivel mundial en las organizaciones.

### **Política de manejo de datos**

Una política de manejo de datos es un conjunto de reglas que define cómo la información debe ser clasificada, utilizada, almacenada, compartida y protegida dentro de una organización. Estas políticas establecen qué usuarios o roles pueden acceder a determinados datos y qué controles de seguridad deben aplicarse según su nivel de sensibilidad. También ayudan a cumplir estándares y regulaciones como PCI DSS (Payment Card Industry Data Security Standard), que establece requisitos para proteger los datos de tarjetas de pago mediante controles adecuados.

### **Política de contraseñas**

Una política de contraseñas es un conjunto de reglas que define cómo deben crearse y administrarse las contraseñas dentro de una organización para fortalecer la autenticación y reducir accesos no autorizados. Puede incluir medidas como longitud mínima, requisitos de complejidad, MFA, protección contra intentos de autenticación maliciosos y auditorías para verificar su cumplimiento.

### **La política de uso aceptable (AUP)**

Define cómo deben comportarse los usuarios y empleados al utilizar los sistemas, redes y recursos tecnológicos de una organización. Establece qué acciones están permitidas y cuáles están prohibidas para mantener la seguridad y el uso adecuado de la infraestructura. El incumplimiento de estas reglas puede generar sanciones o medidas disciplinarias.

### **BYOD (Bring Your Own Device)**

Es una política donde la organización permite que los empleados utilicen dispositivos personales, como laptops o teléfonos, para acceder a recursos, redes y datos corporativos. Aunque esto puede mejorar la comodidad y productividad, también genera riesgos de seguridad porque la empresa pierde parte del control sobre la configuración, privacidad y protección de esos dispositivos. Por esa razón, las organizaciones establecen políticas y controles de seguridad que los empleados deben aceptar y cumplir antes de conectarse a la infraestructura corporativa.

### **Política de Privacidad**

La política de privacidad establece cómo deben protegerse y utilizarse los datos personales o sensibles dentro de una organización, asegurando que solo sean usados para fines autorizados y cumpliendo las leyes y regulaciones de privacidad aplicables.

### **Política de gestión de cambios**

La gestión de cambios es el proceso utilizado para planificar, aprobar, implementar y verificar modificaciones dentro de sistemas, aplicaciones, infraestructura o procesos de una organización. Su objetivo es mover el sistema de un estado actual a uno nuevo sin afectar negativamente la seguridad ni las operaciones del negocio.

## **Políticas de seguridad comunes: Análisis más profundo**

Las políticas de seguridad comunes son reglas establecidas por la organización para proteger sistemas, datos y operaciones según sus necesidades y objetivos. Los empleados deben comprenderlas y cumplirlas, ya que su incumplimiento puede generar sanciones como advertencias, suspensiones o despidos, dependiendo de la gravedad de la infracción y de las políticas de la organización.

## **Componentes de gestión de cambios**

El proceso de gestión del cambio incluye los siguientes componentes.

### **Documentación / Request for Change (RFC)**

Esto aborda un conjunto común de actividades relacionadas con la solicitud para cambiar algo. Las solicitudes pueden pasar por varias etapas de evaluación, desarrollo y prueba antes de entregarse a los usuarios finales.

### **Aprobación**

Esto es básicamente el proceso de autorizar los cambios anteriormente mencionados. Se toman en cuenta las revisiones de las partes interesadas, la identificación de recursos y otros factores antes de aprobar o rechazar el cambio.

### **Retroceder / Rollback**

El rollback es el proceso de revertir un cambio o actualización para regresar el sistema a un estado anterior estable en caso de fallos, errores o interrupciones. Se utiliza dentro de la gestión y control de cambios para restaurar rápidamente la operación normal y evitar impactos en la productividad o en los servicios del negocio.

# **Módulo 4: Comprender la capacitación de concientización sobre seguridad**

## **¿Qué es la formación de conciencia de seguridad?**

Comencemos con una comprensión clara de los tres tipos diferentes de actividades de aprendizaje que utilizan las organizaciones, ya sea para la seguridad de la información o para cualquier otro propósito:

### **Educación**

El objetivo general de la educación es ayudar a los alumnos a mejorar su comprensión de estas ideas y su capacidad para relacionarlas con sus propias experiencias y aplicar ese aprendizaje de manera útil.

### **Capacitación**

La capacitación es el proceso de enseñar y desarrollar conocimientos, habilidades y buenas prácticas para que los empleados puedan realizar sus funciones de manera correcta, segura y eficiente.

### **Conciencia**

Estas son actividades que atraen y captan la atención del alumno al familiarizarlo con aspectos de un tema, preocupación, problema o necesidad.

Nota: El eslabón más débil dentro de una empresa puede ser un usuario sin capacitación o concientización adecuada.

## **Ejemplos de entrenamiento de concientización sobre seguridad**

### **Educación**

La educación ayuda a comprender conceptos y amenazas de seguridad.

Ejemplo: aprender cómo funciona un ataque de phishing.

### **Capacitación**

La capacitación enseña cómo actuar correctamente ante incidentes de seguridad mediante prácticas o simulaciones.

Ejemplo: identificar y reportar un correo de phishing falso.

### **Concientización**

La concientización mantiene a los usuarios alertas frente a amenazas mediante recordatorios y campañas.

Ejemplo: carteles o correos que advierten sobre enlaces sospechosos.

Nota: Debemos estar al tanto de las nuevas tecnologías y aplicarlas en nuestro entorno cuando sea necesario, además de capacitar a nuestro personal. También debemos ser comprensivos con los usuarios y fomentar la confianza mediante correcciones y orientación, en lugar de enfocarnos únicamente en sancionarlos cuando cometen errores.
