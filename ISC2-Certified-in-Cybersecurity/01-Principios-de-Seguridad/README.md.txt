# Dominio 1: Principios de seguridad

Esta documentación será parte de lo aprendido en la certificación **CC de ISC2**. Se tomarán apuntes de conceptos técnicos y algunos ejemplos de estos, tomando en cuenta que es una certificación donde la conceptualización y el pensamiento crítico como gestor de riesgos de IT son muy importantes.

Los módulos que estaremos viendo en el transcurso de la certificación son:

1. Principios de seguridad
2. Conceptos de respuesta a incidentes, continuidad del negocio y recuperación ante desastres
3. Conceptos de control de acceso
4. Seguridad de la red
5. Operaciones de seguridad

**Nota:** Debemos estar conscientes de que dominamos el tema actual antes de pasar al siguiente. Por eso es importante la documentación y evaluación por módulo.

# **Módulo 1: Principios de seguridad**

Este módulo se subdivide en 6 partes, que son las siguientes:

- **Módulo 1:** Comprender los conceptos de seguridad de la garantía de la información (D1.1)
- **Módulo 2:** Comprender el proceso de gestión de riesgos (D1.2)
- **Módulo 3:** Comprender los controles de seguridad (D1.3)
- **Módulo 4:** Comprender los elementos de gobernanza (D1.5)
- **Módulo 5:** Comprender el Código de Ética de (ISC)² (D1.4)
- **Módulo 6:** Resumen

### La Tríada de la CIA

- **Confidencialidad (Confidentiality):** Garantiza que la información solo sea accesible para usuarios autorizados, evitando accesos no permitidos o filtraciones de datos.
- **Integridad (Integrity):** Asegura que los datos se mantengan completos y precisos, sin modificaciones no autorizadas durante su almacenamiento o transmisión.
- **Disponibilidad (Availability):** Garantiza que la información esté disponible cuando se necesite, minimizando interrupciones o fallos.

PII: La **PII (Personally Identifiable Information)** o **Información de Identificación Personal** es cualquier dato que permite identificar directa o indirectamente a una persona. Por ejemplo, nombre completo de alguien, número de cédula, dirección física y más.

PHI: La **PHI (Protected Health Information)** es información médica protegida relacionada con la salud de una persona y que puede identificarla.

Sensibilidad: Hace referencia al nivel de impacto que puede tener una empresa en caso de una brecha de datos. Mientras más sensible sea la información, mayores controles de seguridad pueden ser necesarios.

La **integridad del sistema** garantiza que los datos y procesos se mantengan correctos, completos y sin modificaciones no autorizadas, asegurando la confiabilidad del sistema dentro de la tríada CIA.

### **Autenticación**

Concepto: La **autenticación** es el proceso para comprobar la identidad de un solicitante que intenta acceder a un sistema o recurso.

Existen 3 categorías de factores de autenticación para el solicitante, y son las siguientes:

- Algo que sabes: Frase para desbloquear algo, contraseña o información privada.
- Algo que tienes: Token, OTP, tarjetas inteligentes u otros dispositivos de autenticación.
- Algo que eres: Biometría, características físicas medibles y más.

Nota: **SFA (Single-Factor Authentication)** es la forma de validar al solicitante utilizando una sola categoría de autenticación, mientras que **MFA (Multi-Factor Authentication)** utiliza dos o más factores pertenecientes a categorías distintas.

Nota: El MFA requiere **dos o más categorías distintas** de factores de autenticación.

El **no repudio (non-repudiation)** es un principio de la ciberseguridad que ayuda a demostrar que una persona realizó una determinada acción dentro de un sistema, evitando que pueda negar posteriormente su participación. Esto puede apoyarse en mecanismos como firmas digitales, registros de auditoría y logs.

### Privacidad

**Concepto: Privacidad:** Es el derecho de una persona a controlar cómo se usa y comparte su información personal, protegiéndola del uso indebido.

**Seguridad de la información:** Es el conjunto de controles y prácticas que protegen los datos y sistemas, garantizando la confidencialidad, integridad y disponibilidad (CIA).

**GDPR (General Data Protection Regulation):** Es una regulación de la Unión Europea que establece requisitos para la protección de datos personales y la privacidad de las personas. También puede aplicarse al procesamiento de datos de personas en la UE realizado por organizaciones que se encuentran fuera de la Unión Europea, dependiendo de las circunstancias.

**HIPAA (Health Insurance Portability and Accountability Act):** Es una ley de EE. UU. que establece requisitos para proteger la información médica protegida (PHI) en determinadas entidades cubiertas y sus *business associates*. La HIPAA incluye normas relacionadas con la privacidad y seguridad de la información de salud. (HHS.gov)

# **Módulo 2: Comprender el proceso de gestión de riesgos**

Riesgo: Es la posibilidad de que algo pueda impactar de manera negativa a una organización.

**Nota: A veces, el riesgo se expresa de manera combinada entre el impacto y la probabilidad de que algo ocurra.**

El riesgo de seguridad de la información refleja los impactos adversos potenciales que resultan de la posibilidad de acceso, uso, divulgación, interrupción, modificación o destrucción no autorizados de la información y/o los sistemas de información.

### **Terminología de gestión de riesgos**

Un profesional del área utiliza sus conocimientos para evaluar la gestión de riesgos dentro de una empresa y así comenzar a priorizar los activos. Dentro de esto existen terminologías que van de la mano y son:

Un **Activo:** Esto es algo que tiene un valor dentro de la empresa y que necesita protección, por ejemplo, la data de un usuario.

Una **Vulnerabilidad:** Es una debilidad o brecha de seguridad, ya sea humana o tecnológica, que puede ser aprovechada por un actor de amenaza.

Una **Amenaza:** Es una persona, situación o evento con potencial de causar daño y que puede aprovechar una vulnerabilidad para comprometer información o sistemas.

**Nota: La cadena de un gestor de riesgos sería (Activo → Vulnerabilidad → Amenaza → Riesgo), por eso mismo los gestores de riesgos miran y observan su entorno.**

### Actores de amenaza

Los actores de amenazas son personas, grupos o tecnologías que pueden aprovechar una vulnerabilidad para afectar la confidencialidad, integridad o disponibilidad de los activos de una organización.

Los actores más comunes son:

- Insiders: empleados o usuarios internos que causan incidentes por mala intención, errores o negligencia.
- Atacantes externos: individuos o grupos que buscan explotar vulnerabilidades de forma oportunista o planificada.
- Ciberdelincuentes y competidores: organizaciones que buscan beneficios económicos, robo de información o ventaja comercial.
- Estados, terroristas y hacktivistas: actores con motivaciones políticas, ideológicas o estratégicas.
- Recolectores de información: actores enfocados en espionaje o inteligencia.
- Tecnología automatizada: bots, malware o inteligencia artificial utilizados para ejecutar ataques.

**Nota: Vector de amenaza es el medio o método utilizado para realizar el ataque, como phishing, malware, vulnerabilidades web o robo de credenciales.**

### Probabilidad

Concepto: La probabilidad es la posibilidad de que un actor de amenaza explote una vulnerabilidad y esto se convierta en un incidente de seguridad.

Impacto: Es la magnitud del daño que se puede esperar como resultado de las consecuencias de una amenaza.

**Riesgo = Probabilidad × Impacto**

### Riesgos

¿Cómo se identifica un riesgo?

Un riesgo se identifica analizando las amenazas, vulnerabilidades y posibles impactos que pueden afectar a una organización. Luego de identificarlo, el equipo de seguridad evalúa qué tan probable es que ocurra y qué tan grave sería el daño, para así aplicar medidas de mitigación o control.

La gestión de riesgos requiere:

- Pensamiento estratégico.
- Mejora continua.
- Trabajo en equipo.
- Concientización y capacitación constante.

¿Quién puede identificar un riesgo?

Todos dentro de la organización pueden identificar riesgos, ya que la seguridad es responsabilidad compartida.

Ruta básica:

1. Identificar el riesgo o actividad sospechosa.
2. Comunicarlo al área correspondiente.
3. Analizar el impacto y la probabilidad.
4. Aplicar controles para reducir o evitar el riesgo.
5. Mantener monitoreo y mejora continua.

#### Evaluación de riesgo

La evaluación de riesgos en una empresa consiste en identificar los activos, analizar cuáles están más expuestos a amenazas y determinar su nivel de riesgo. Este se calcula comúnmente como **Riesgo = Probabilidad × Impacto**, lo que permite priorizar los riesgos más críticos y definir medidas de mitigación adecuadas, documentadas para la toma de decisiones de la gerencia.

### Tratamiento de riesgos

Concepto: Hace referencia a la toma de decisiones cuando un riesgo se identifica. Este pasa por un proceso de priorización, tomando en cuenta factores como el impacto sobre el negocio, los costos y la CIA.

Opciones comunes para responder a estos riesgos son:

**Evitación:** Consiste en eliminar la actividad que genera el riesgo, evitando así la exposición a este. Se usa cuando el impacto o la probabilidad del riesgo es demasiado alta.

**Aceptación:** Es decidir no tomar medidas adicionales contra el riesgo porque el impacto es bajo o el beneficio de la actividad compensa el posible daño.

**Mitigar el riesgo:** Es aplicar controles y medidas de seguridad para reducir la probabilidad o el impacto del riesgo. Es una estrategia común en ciberseguridad y gestión IT.

**Transferencia del riesgo:** Es cuando una empresa transfiere parte del impacto o la responsabilidad económica de un riesgo a otra organización o tercero. Generalmente se hace mediante contratos, seguros u otros acuerdos.

### Prioridades de riesgos

La priorización de riesgos permite identificar cuáles riesgos necesitan mayor atención dentro de una organización.

Existen dos enfoques principales:

- **Cualitativo:** evalúa los riesgos de forma descriptiva, usando niveles como bajo, medio o alto.
- **Cuantitativo:** analiza los riesgos mediante valores numéricos, costos estimados, porcentajes y pérdidas económicas.

La prioridad del riesgo se determina combinando la probabilidad y el impacto:

- Probabilidad baja + impacto bajo = prioridad baja.
- Probabilidad alta + impacto alto = prioridad alta.

### Tolerancia al riesgo

La tolerancia al riesgo es el nivel y las condiciones de riesgo que una organización está dispuesta a aceptar al realizar una actividad. Esto depende del impacto que el riesgo pueda tener sobre el negocio, los costos y los objetivos de la empresa.

Por ejemplo, poner una empresa al lado de un volcán sabiendo que tarde o temprano ese volcán podría explotar y poner mi empresa en riesgo.

# **Módulo 3: Comprender los controles de seguridad**

### Controles de seguridad

Esto se define como el conjunto de políticas, reglas y acciones de una empresa, en el cual se encuentra involucrada la parte técnica, los controles administrativos y los controles físicos. Estos determinan quién puede y quién no puede realizar determinadas acciones, protegiendo la CIA.

### Tipos de controles

**Control Físico:** Los controles de acceso físico permiten limitar el acceso a áreas específicas únicamente a personas autorizadas. Estos controles pueden incluir medidas como biometría, tarjetas de acceso y sistemas electrónicos de autenticación.

**Control Técnico:** Los controles técnicos o controles lógicos son mecanismos de seguridad basados en tecnología que ayudan a proteger sistemas y datos frente a amenazas o accesos no autorizados. Estos controles pueden utilizar software y hardware, y trabajan junto con controles físicos y administrativos para fortalecer la seguridad de una organización. Algunos ejemplos son antivirus, VPN, MFA y firewalls.

**Control Administrativo:** Los controles administrativos o controles gerenciales son políticas y procedimientos utilizados para gestionar la seguridad dentro de una organización. Incluyen normas, capacitaciones, auditorías y controles de acceso basados en principios como Zero Trust y privilegio mínimo.

# **Módulo 4: Comprender los elementos y procesos de gobernanza**

La gobernanza en IT es la forma en que una empresa organiza reglas, decisiones y controles para cumplir sus objetivos de manera segura y ordenada.

### **La estructura va así:**

**Leyes/Reglamentos → Estándares → Políticas → Procedimientos**

### **Elementos de Gobernanza**

**1. Reglamentos y Leyes**

Son reglas obligatorias creadas por gobiernos.

Si no se cumplen, puede haber multas o sanciones.

Ejemplos:

- HIPAA → protege información médica.
- GDPR → protege datos personales.

Ejemplo IT:

Una empresa no puede filtrar datos de clientes porque podría violar leyes de privacidad.

**2. Estándares**

Son buenas prácticas o marcos de referencia que ayudan a cumplir las leyes.

No siempre son obligatorios, pero son muy usados.

Ejemplos:

- ISO → crea estándares de seguridad como ISO 27001.
- NIST → guías de ciberseguridad.
- IEEE → estándares de redes y telecomunicaciones.

Ejemplo IT:

Una empresa usa ISO 27001 para organizar su seguridad informática.

**3. Políticas**

Son reglas internas de la empresa.

Dicen **qué se debe hacer**, pero no explican paso a paso cómo hacerlo.

Las crea la gerencia o dirección.

**4. Procedimientos**

Son los pasos detallados para cumplir una política.

Explican exactamente **cómo hacerlo**.

**La jerarquía de estos y cómo se pueden aplicar.**

Ley → obliga

Estándar → guía

Política → define reglas

Procedimiento → explica pasos

# **Módulo 5: Entender ISC2 Código de Ética**

Todos los profesionales que están certificados por ISC2 deben comprometerse a cumplir con el **Código de Ética de ISC2**.

ISC2 Código de Ética - Preámbulo:

- La seguridad y el bienestar de la sociedad, el bien común, el deber hacia nuestros principales y entre nosotros requieren que nos adhiramos, y que se vea que nos adherimos, a los más altos estándares éticos de comportamiento.
- Por lo tanto, la estricta adherencia a este Código es una condición para la certificación.

ISC2 Cánones del Código de Ética:

- Proteger la sociedad, el bien común, la confianza necesaria, la confianza pública y la infraestructura.
- Actuar con honor, honestidad, justicia, responsabilidad y legalidad.
- Brindar un servicio diligente y competente a los directores.
- Promover y proteger la profesión.