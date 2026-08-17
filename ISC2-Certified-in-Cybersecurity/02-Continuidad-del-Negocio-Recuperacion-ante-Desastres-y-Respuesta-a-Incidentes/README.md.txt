# **Capítulo 2: Respuesta a incidentes, Continuidad del negocio y Recuperación ante desastres**

Esta documentación será parte de lo aprendido en la certificación **CC de ISC2**. Se tomarán apuntes de conceptos técnicos y algunos ejemplos de estos, tomando en cuenta que es una certificación donde la conceptualización y el pensamiento crítico como gestor de riesgos de IT son muy importantes.

Los módulos que estaremos viendo en el transcurso de la certificación son:

1. Principios de seguridad
2. Conceptos de respuesta a incidentes, continuidad del negocio y recuperación ante desastres
3. Conceptos de control de acceso
4. Seguridad de la red
5. Operaciones de seguridad

Nota: Debemos estar conscientes de que dominamos el tema actual antes de pasar al siguiente. Por eso es importante la documentación y evaluación por módulo.

El orden de este capítulo se basa en el siguiente:

# **Orden del día del capítulo**

- **Módulo 1:** Comprender la respuesta a incidentes (D2.3)
- **Módulo 2:** Comprender la continuidad del negocio (BC) (D2.1)
- **Módulo 3:** Comprender la recuperación ante desastres (DR) (D2.2)
- **Módulo 4:** Resumen

# **Módulo 1: Comprender la respuesta a incidentes**

**Terminología de incidentes**

Si bien sabemos que nosotros, como gestores de TI, estamos encargados de la parte de la seguridad de la empresa en muchos aspectos, entre ellos se encuentra la respuesta a incidentes, como un “socorrista”. No todo sale bien en las empresas, por más bien que lo tengamos planeado. Por eso debemos tener conocimiento de las terminologías utilizadas para describir varios eventos y ataques cibernéticos.

**Incumplimiento:** Básicamente, trata de la pérdida de control, el compromiso o la divulgación de datos a un usuario que no está autorizado. También puede darse el caso de que un usuario no autorizado acceda a información para un propósito distinto al permitido.

Nota: El **NIST Special Publication 800-53 Revision 5** habla principalmente de **controles de seguridad y privacidad** para proteger sistemas, redes, aplicaciones y datos.

**Evento:** Cualquier ocurrencia observable en una red o sistema. Un evento puede quedar registrado mediante un log.

**Explotar:** Es aprovechar una vulnerabilidad mediante un ataque o una técnica específica. Se llama así porque estos ataques aprovechan las debilidades de un sistema.

**Incidente:** Es un evento que realmente o potencialmente pone en riesgo la confidencialidad, integridad o disponibilidad de un sistema o de la información que este procesa. (NIST CSRC)

**Intrusión:** Una intrusión es cuando una persona no autorizada obtiene, o intenta obtener, acceso a un sistema o recurso sin autorización. RFC 4949 v2. (NIST CSRC)

Ejmplo:

Un equipo SOC recibe una alerta de varios intentos fallidos de acceso a una cuenta. Esto puede indicar un intento de intrusión, como un ataque de fuerza bruta.

Nota: RFC 4949 es un documento creado por la Internet Engineering Task Force (IETF), y uno de sus objetivos es servir como glosario de términos de seguridad informática y redes.

**Amenaza:** Es una persona, evento o circunstancia que puede poner en riesgo la seguridad, los activos o las operaciones de una empresa, causando daños económicos, operativos o de reputación.

**Vulnerabilidad:** Es una debilidad en una persona, proceso, sistema o tecnología dentro de la empresa que puede ser aprovechada por un actor de amenaza. NIST SP 800-30 Rev. 1. (NIST CSRC)

Nota: El NIST Special Publication 800-30 Revision 1 es una guía del National Institute of Standards and Technology enfocada en la **evaluación de riesgos** en ciberseguridad. (NIST CSRC)

**Día Cero:** Una vulnerabilidad previamente desconocida para el fabricante o para quienes deben corregirla, que puede ser explotada antes de que exista una solución o parche disponible. El hecho de que sea de día cero no significa necesariamente que no existan logs o que sea imposible detectarla.

### **El objetivo de la respuesta a incidentes**

El objetivo es poder responder a las incidencias que puedan llegar a ocurrir dentro de la empresa. Esto se hace mediante guías, políticas y procedimientos. La prioridad es proteger la **tríada CIA**, por eso, ante todo tipo de riesgo, es recomendable contar con un plan de respuesta a incidentes. El objetivo de este es reducir el impacto del incidente y ayudar a recuperar las operaciones de forma segura.

### **Componentes del Plan de Respuesta a Incidentes**

1. **Preparación**
    
    Tener herramientas, políticas, backups y personal listo antes del incidente.
    
2. **Detección y análisis**
    
    Detectar el incidente y confirmar qué ocurrió, cómo ocurrió y qué sistemas o información están afectados.
    
3. **Contención**
    
    Limitar o detener el ataque para evitar más daño.
    
4. **Erradicación**
    
    Eliminar la causa del incidente, como malware, accesos no autorizados o vulnerabilidades explotadas.
    
5. **Recuperación**
    
    Restaurar los sistemas y las operaciones normales de forma segura.
    
6. **Lecciones aprendidas y aprendizaje continuo**
    
    Documentar lo sucedido y mejorar los controles para futuros incidentes.
    

### **Equipo de respuesta a incidentes**

SOC (**Security Operations Center**) es un equipo encargado de monitorear y detectar eventos de seguridad y apoyar en la respuesta ante incidentes. Este se ayuda de herramientas que recopilan y analizan eventos, mejor conocidos como logs. Entre sus funciones se encuentran determinar qué pasó, por qué pasó, cuándo pasó, cómo pasó, qué sistemas fueron afectados y a quién se debe escalar el incidente.

Los miembros potenciales del equipo incluyen lo siguiente:

- Representante(s) de la alta gerencia
- Profesionales de la seguridad de la información
- Representantes legales
- Representantes de asuntos públicos/comunicaciones
- Representantes de ingeniería (sistema y red)

Estas personas que pertenecen al equipo de respuesta a incidentes deben estar en aprendizaje constante, documentar los hallazgos y mantener una participación activa.

Un **CSIRT (Computer Security Incident Response Team)** es un **equipo especializado en responder a incidentes de ciberseguridad** dentro de una organización o comunidad. Por ejemplo, el CNCS.

# **Módulo 2: Comprender la continuidad del negocio (BC) Business Continuity**

La intención de un plan de continuidad del negocio es que la empresa pueda mantener sus operaciones durante una interrupción y, si falla una parte de la empresa, otras áreas críticas puedan seguir trabajando mientras se soluciona el problema. Muchas veces las empresas tienen números de contacto de proveedores de electricidad, Internet u otros servicios para que, cuando ocurra un desastre de determinada magnitud, puedan recibir ayuda de manera más eficaz y rápida.

La continuidad del negocio incluye actividades de planificación, preparación, respuesta y recuperación.

### **Componentes de un Plan de Continuidad del Negocio**

La planificación de la continuidad del negocio (BCP) es el desarrollo proactivo de procedimientos para mantener o restaurar las operaciones comerciales después de un desastre u otra interrupción importante para la organización.

Estos son algunos componentes comunes de un plan integral de continuidad del negocio:

- **Equipo BCP:** Lista de las personas responsables del plan, con teléfonos, correos y contactos de respaldo.
- **Procedimientos inmediatos:** Pasos rápidos a seguir durante la emergencia, como evacuación, apagar sistemas o contactar a los servicios de emergencia.
- **Sistemas de notificación:** Métodos para avisar al personal, como llamadas, SMS o correos.
- **Guía de gestión:** Define quién tiene autoridad para tomar decisiones y activar el plan.
- **Activación del plan:** Explica cuándo y cómo se debe poner en marcha el BCP.
- **Contactos críticos:** Información de proveedores, clientes y terceros importantes para continuar las operaciones.

Nota: El famoso libro llamado “Libro Rojo” es un recurso físico que algunas empresas utilizan como respaldo de su plan de continuidad. Se asigna a una persona responsable para que lo tenga fuera de las instalaciones en caso de que ocurra algún desastre. Este libro contiene información y procedimientos necesarios para el BCP. Cada vez que este se actualice físicamente, también debe actualizarse su versión digital.

### Business Impact Analysis (BIA)

El BIA analiza el impacto que tendría una interrupción en los sistemas o procesos críticos de una empresa, ya sea por desastres naturales, fallas o ciberataques.

Ayuda a establecer prioridades de recuperación mediante análisis:

- **Cualitativos:** impacto alto, medio o bajo.
- **Cuantitativos:** pérdidas económicas, tiempo caído, clientes afectados, etc.

Va de la mano de:

- **RTO (Recovery Time Objective):** tiempo máximo objetivo para recuperar un sistema o proceso después de una interrupción.
- **RPO (Recovery Point Objective):** cantidad máxima de datos que la empresa está dispuesta a perder, medida en tiempo desde el último punto de recuperación disponible.

# **Módulo 3: Comprender la recuperación ante desastres (DR) Disaster Recovery**

Como ya vimos, la continuidad del negocio se trata de mantener las operaciones de la empresa durante una interrupción. La recuperación ante desastres se encarga de restaurar los sistemas, servicios e infraestructura necesarios para volver a las operaciones normales después de una interrupción.

PDR: Plan de Recuperación ante Desastres.

DR: Recuperación ante Desastres.

Nota: Cada equipo dentro de la empresa necesita un **backup** adecuado y, para los sistemas críticos, es recomendable contar con varias copias y medios de recuperación. Esto es importante porque existen incidentes que pueden tardar días o incluso meses en ser detectados.

#### **Plan de Recuperación ante Desastres**

Básicamente, no todos necesitan leer el mismo documento, por eso el plan se divide según el tipo de personal.

- **Resumen ejecutivo:**
    
    Documento corto para gerentes y directivos. Explica rápidamente qué pasó y cómo responde la empresa.
    
- **Planes por departamento:**
    
    Cada área tiene instrucciones específicas según sus funciones.
    
- **Guías técnicas:**
    
    Documentos para el personal de TI con pasos técnicos para restaurar servidores, redes, backups y sistemas críticos.
    
- **Copias completas del DRP:**
    
    Los miembros importantes del equipo de recuperación tienen acceso al plan completo.
    
- **Listas de verificación (checklists):**
    
    Ayudan a seguir pasos rápidos durante el desastre sin olvidar tareas importantes.