# Capítulo 4: Microsoft Service Trust Portal, privacidad y soluciones de Microsoft Purview

# Microsoft Service Trust Portal y principios de privacidad de Microsoft

### Descripción de las ofertas del Service Trust Portal

El **Service Trust Portal (STP)** es el portal público de Microsoft que proporciona acceso directo a información de confianza, transparencia y cumplimiento normativo sobre los servicios en la nube de Microsoft (Azure, Microsoft 365, Dynamics 365).

*(Inserta aquí tu imagen o captura del Service Trust Portal)*

#### Principales recursos disponibles en el STP:

- **Informes de auditoría independientes:** Informes de auditoría de terceros que certifican que los servicios de Microsoft cumplen con estándares internacionales y marcos regulatorios reconocidos (como SOC 1, SOC 2, SOC 3, ISO/IEC 27001, ISO/IEC 27018, PCI DSS, FedRAMP, HIPAA, entre otros).
- **Guías de cumplimiento y evaluaciones de seguridad:** Documentos técnicos que explican cómo Microsoft implementa controles de seguridad, protección de datos y privacidad en sus centros de datos e infraestructura global.
- **Evaluaciones de la industria y el sector:** Documentación orientada a sectores altamente regulados (servicios financieros, salud, sector público) para facilitar la auditoría de riesgos de los proveedores cloud.
- **Acceso y requisitos:** La mayoría de los documentos públicos están disponibles para cualquier usuario, pero la descarga de ciertos informes de auditoría detallados requiere autenticarse con una cuenta profesional o educativa activa de Microsoft.

### Principios de privacidad de Microsoft

Microsoft fundamenta la gestión y protección de los datos de sus clientes bajo seis principios rectores de privacidad:

1. **Control:** El cliente mantiene el control sobre sus datos y su privacidad en todo momento, decidiendo cómo se utilizan y quién tiene acceso a ellos.
2. **Transparencia:** Microsoft es transparente sobre dónde se almacenan físicamente los datos, cómo se procesan, quién puede acceder a ellos y bajo qué condiciones.
3. **Seguridad:** Los datos del cliente se protegen mediante cifrado robusto en tránsito y en reposo, prácticas estrictas de seguridad física y lógica, y controles de acceso basados en privilegios mínimos.
4. **Fuertes protecciones legales:** Microsoft defiende la privacidad de los datos de sus clientes y rechaza solicitudes gubernamentales de acceso a la información que considere desproporcionadas o ilegales.
5. **Sin publicidad basada en datos del cliente:** Microsoft no utiliza el correo electrónico, archivos, conversaciones ni datos empresariales del cliente para orientar publicidad dirigida.
6. **Beneficio para el usuario:** El uso de los datos y la telemetría se orienta exclusivamente a proporcionar, mantener y mejorar los servicios contratados por el cliente.

> **Regla de oro:** En la nube de Microsoft, **el cliente es el dueño de sus datos**; Microsoft actúa como encargado del tratamiento (*data processor*).
> 

## Soluciones de seguridad de datos de Microsoft Purview

Microsoft Purview agrupa soluciones integradas para gobernar, proteger y gestionar el cumplimiento de los datos sensibles en entornos multinube, aplicaciones SaaS y sistemas locales.

```
                  ┌─────────────────────────────────────────┐
                  │          Microsoft Purview              │
                  │       (Seguridad de los datos)          │
                  └────────────────────┬────────────────────┘
         ┌───────────────────┬─────────┴─────────┬───────────────────┐
         ▼                   ▼                   ▼                   ▼
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│   Information   │ │    Data Loss    │ │  Insider Risk   │ │    Adaptive     │
│   Protection    │ │Prevention (DLP) │ │   Management    │ │   Protection    │
│  (Clasificación │ │  (Evitar fugas  │ │ (Riesgos desde  │ │ (DLP dinámico   │
│  y Etiquetas)   │ │  de datos)      │ │  el interior)   │ │  según riesgo)  │
└─────────────────┘ └─────────────────┘ └─────────────────┘ └─────────────────┘
```

### Funcionalidades de clasificación de datos de Microsoft Purview Information Protection

Para proteger la información, primero es necesario saber qué datos existen, dónde residen y qué nivel de sensibilidad tienen (**"Conoce tus datos"**).

#### Tipos de información confidencial (SIT - Sensitive Information Types)

Son definiciones basadas en patrones que identifican automáticamente datos sensibles:

- **SIT integrados:** Más de 300 tipos prediseñados por Microsoft para reconocer patrones globales y regionales (números de tarjetas de crédito, números de seguridad social, pasaportes, cuentas bancarias, credenciales API).
- **SIT personalizados:** Patrones creados por la organización utilizando expresiones regulares (Regex), palabras clave o diccionarios para detectar identificadores internos (como números de empleados o formatos de contratos propios).
- **Coincidencia exacta de datos (EDM - Exact Data Match):** Permite crear SITs basados en bases de datos exactas de la organización (por ejemplo, una lista exacta con los nombres y números de cuenta de los clientes), garantizando una detección de alta precisión sin falsos positivos.

#### Clasificadores entrenables (Trainable Classifiers)

Modelos de Machine Learning entrenados para reconocer tipos específicos de contenido basándose en el contexto del documento completo y no solo en cadenas o patrones de texto:

- **Preentrenados:** Reconocen categorías estándar como código fuente, acuerdos de confidencialidad (NDA), presupuestos, propiedad intelectual o quejas de clientes.
- **Personalizados:** La organización puede entrenar sus propios modelos proporcionando un conjunto de ejemplos positivos y negativos de documentos corporativos.

#### Exploradores de clasificación

- **Explorador de contenido (Content Explorer):** Permite a los administradores autorizados ver qué archivos específicos contienen información confidencial clasificada o etiquetas aplicadas, e inspeccionar su ubicación y contenido.
- **Explorador de actividad (Activity Explorer):** Proporciona un registro histórico de eventos sobre qué acciones se realizaron sobre los datos clasificados (quién aplicó una etiqueta, quién cambió la clasificación, quién intentó compartir un archivo protegido).

### Etiquetas y directivas de confidencialidad (Sensitivity Labels)

Las etiquetas de confidencialidad permiten clasificar y proteger los datos (documentos de Office, correos electrónicos, sitios de SharePoint, bases de datos SQL, reuniones de Teams) según su criticidad.

!image.png

#### Características de las etiquetas

- **Persistencia:** La etiqueta y su protección viajan incrustadas en los metadatos del archivo; si el documento se copia, se envía por correo o se sube a otra plataforma, la protección permanece activa.
- **Acciones de protección aplicables:**
    - **Cifrado:** Restringe quién puede abrir, leer, editar, imprimir o reenviar el archivo mediante Microsoft Rights Management.
    - **Marcas de contenido:** Aplica marcas de agua visuales, encabezados y pies de página en los documentos y correos.
    - **Control de acceso a nivel de contenedor:** Configura configuraciones de privacidad (público/privado) y directivas de acceso externo en sitios de SharePoint y equipos de Microsoft Teams.

#### Directivas de etiquetas de confidencialidad (Sensitivity Label Policies)

Determinan cómo y a quién se publican las etiquetas:

- Publican etiquetas específicas para usuarios o grupos seleccionados.
- Permiten exigir una **etiqueta predeterminada** a nuevos documentos y correos.
- Permiten exigir una **justificación obligatoria** cuando un usuario intenta rebajar la clasificación de un documento (por ejemplo, cambiar de *Altamente Confidencial* a *Público*).
- Permiten la **etiquetación automática (Auto-labeling):** Aplica etiquetas automáticamente cuando el sistema detecta que un documento coincide con determinados tipos de información confidencial (SIT).

### Prevención de pérdida de datos (DLP - Data Loss Prevention)

Microsoft Purview DLP ayuda a prevenir la divulgación o transferencia accidental o no autorizada de información confidencial fuera o dentro de la organización.

#### Cómo funciona una directiva DLP:

Una directiva DLP se compone de **Ubicaciones**, **Condiciones** y **Acciones**:

1. **Ubicaciones protegidas:** Exchange Online, SharePoint Online, OneDrive, chats y canales de Microsoft Teams, dispositivos finales (Endpoint DLP) y aplicaciones en la nube (mediante Defender for Cloud Apps).
2. **Condiciones:** Reglas que detectan cuándo se comparte información confidencial (ej. *«Si un correo enviado a un destinatario externo contiene más de 5 números de tarjeta de crédito»*).
3. **Acciones:**
    - Bloquear la transferencia o el envío del mensaje.
    - Mostrar sugerencias de directiva (*Policy Tips*) para educar al usuario en tiempo real sobre la política de seguridad.
    - Notificar al usuario y al equipo de seguridad.
    - Permitir la anulación por parte del usuario con justificación comercial.

#### DLP para dispositivos de punto de conexión (Endpoint DLP)

Extiende las reglas DLP a nivel de sistema operativo en dispositivos Windows y macOS:

- Bloquea o audita la copia de archivos sensibles a memorias USB.
- Bloquea la impresión de documentos confidenciales.
- Bloquea la copia de datos al portapapeles.
- Impide subir archivos sensibles a navegadores no autorizados o servicios en la nube personales.

### Administración de riesgos internos (Insider Risk Management)

Se enfoca en identificar, investigar y mitigar actividades maliciosas o riesgosas originadas dentro de la organización (empleados, contratistas o usuarios internos con acceso legítimo).

#### Señales analizadas:

Correlaciona eventos de múltiples fuentes para detectar indicadores de riesgo:

- Descargas masivas de archivos confidenciales antes de la fecha de renuncia de un empleado (integración con sistemas de RR. HH.).
- Copia inusual de propiedad intelectual o código fuente a repositorios externos.
- Intentos reiterados de eludir controles de seguridad y directivas DLP.
- Búsquedas o accesos a recursos confidenciales fuera de su rol habitual.

#### Enfoque de privacidad integrado:

- **Anonimización por defecto:** Los nombres de los usuarios se muestran seudonimizados (*User 1*, *User 2*) para los analistas, evitando sesgos durante las etapas iniciales de la investigación.
- **Controles de acceso basados en roles estrictos:** Solo personal autorizado de cumplimiento y legal puede levantar la anonimización bajo justificación justificada.

### Protección adaptable en Microsoft Purview (Adaptive Protection)

La Protección Adaptable integra **Insider Risk Management** con **Data Loss Prevention (DLP)** y **Conditional Access** mediante IA y Machine Learning:

```
[Análisis de comportamiento] ──> [Calcula nivel de riesgo del usuario] ──> [Aplica directivas DLP dinámicas]
```

1. **Evaluación continua:** Analiza las actividades diarias del usuario y le asigna dinámicamente un nivel de riesgo (*Elevado*, *Moderado*, *Menor*).
2. **Respuesta automatizada y proporcional:**
    - *Riesgo menor:* El usuario puede compartir archivos normalmente; solo recibe recordatorios de buenas prácticas (*Policy Tips*).
    - *Riesgo moderado:* Se auditan y restringen ciertas descargas o transferencias externas.
    - *Riesgo elevado:* Las directivas DLP bloquean automáticamente la copia a USB, la impresión y el uso compartido externo de archivos sensibles para ese usuario en tiempo real.

> **Beneficio clave:** Aplica controles estrictos únicamente a los usuarios con comportamientos de riesgo sin afectar la productividad del resto de los colaboradores.
> 

### Administración de la posición de seguridad de los datos (DSPM - Data Security Posture Management)

DSPM en Microsoft Purview proporciona una evaluación centralizada y continua sobre los riesgos que rodean a los datos sensibles de la organización:

- Identifica almacenes de datos huérfanos, no protegidos o expuestos públicamente.
- Evalúa la sobreasignación de permisos de acceso en repositorios de datos críticos.
- Analiza cómo interactúan los datos sensibles con aplicaciones de IA generativa (como Microsoft 365 Copilot) para prevenir fugas de información o respuestas basadas en contenido no autorizado.

### Investigaciones de seguridad de datos de Microsoft Purview

Herramientas forenses y paneles centralizados que permiten a los equipos de seguridad:

- Investigar incidentes combinados de fuga de datos, alertas DLP y actividades de riesgo interno.
- Visualizar la línea de tiempo completa de las acciones realizadas sobre los archivos afectados.
- Preservar evidencias de forma segura para procesos de auditoría, respuesta a incidentes o acciones legales.

## Soluciones de cumplimiento de datos de Microsoft Purview

Ayudan a las organizaciones a cumplir con marcos legales, regulaciones de la industria (GDPR, HIPAA, ISO) y estándares internos de gobernanza documental.

```
                  ┌─────────────────────────────────────────┐
                  │          Microsoft Purview              │
                  │       (Cumplimiento normativo)          │
                  └────────────────────┬────────────────────┘
         ┌───────────────────┬─────────┴─────────┬───────────────────┐
         ▼                   ▼                   ▼                   ▼
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│   Compliance    │ │  Communication  │ │   eDiscovery    │ │ Data Lifecycle &│
│     Manager     │ │   Compliance    │ │  (Investigación │ │     Records     │
│(Puntuación y    │ │(Mensajes inapro-│ │  legal/evidencia│ │  Management     │
│ evaluaciones)   │ │  piados y acoso)│ │   digital)      │ │(Retención/bajas)│
└─────────────────┘ └─────────────────┘ └─────────────────┘ └─────────────────┘
```

### Administrador de cumplimiento (Compliance Manager)

Herramienta de evaluación de riesgos de extremo a extremo que ayuda a las organizaciones a medir su postura de cumplimiento normativo y simplificar los procesos de auditoría.

!images.png

#### Puntuación de cumplimiento (Compliance Score)

Métrica basada en puntos que mide el progreso en la implementación de controles de cumplimiento:

- **Acciones de Microsoft:** Puntos asociados a los controles de seguridad física e infraestructura gestionados directamente por Microsoft en la nube.
- **Acciones administradas por el cliente:** Puntos asociados a las configuraciones, políticas y procedimientos que la propia organización debe implementar y verificar.

#### Evaluaciones y plantillas regulatorias

- Permite crear evaluaciones automáticas basadas en plantillas prediseñadas para normativas como ISO/IEC 27001, GDPR, HIPAA, NIST CSF y SOC 2.
- Proporciona instrucciones técnicas paso a paso y recomendaciones de mejora para elevar la puntuación y cerrar brechas de cumplimiento.

### Cumplimiento de comunicaciones (Communication Compliance)

Solución diseñada para supervisar canales de comunicación corporativa (Exchange Online, Microsoft Teams, Viva Engage y canales de mensajería compatibles) para detectar infracciones de políticas de conducta y cumplimiento regulatorio.

#### Casos de uso comunes:

- **Detección de lenguaje inapropiado y acoso:** Identifica conductas discriminatorias, insultos o acoso laboral (*bullying*).
- **Uso indebido de información confidencial:** Detecta el intercambio no autorizado de información financiera privilegiada o datos altamente confidenciales en chats y correos.
- **Infracciones normativas en el sector financiero:** Supervisa comunicaciones para evitar conflictos de interés y manipulación de mercado.

> **Mecanismo:** Utiliza clasificadores entrenables, aprendizaje automático y coincidencia de palabras clave para analizar el contexto de los mensajes respetando la privacidad de los usuarios.
> 

### eDiscovery (Descubrimiento electrónico)

Herramienta utilizada por los equipos legales y de cumplimiento para buscar, identificar, preservar, exportar y analizar evidencia digital (correos, documentos, mensajes de chat) requerida en litigios judiciales o investigaciones internas.

#### Niveles de eDiscovery en Microsoft Purview:

- **Búsqueda de contenido (Content Search):** Herramienta básica para realizar búsquedas rápidas de texto y palabras clave en buzones de Exchange, sitios de SharePoint, cuentas de OneDrive y Teams, permitiendo exportar los resultados.
- **eDiscovery Standard:** Permite crear casos legales, asociar búsquedas específicas a un caso, colocar **retenciones legales (*Core / Legal Holds*)** para evitar que los usuarios borren información relevante y exportar los datos para su revisión externa.
- **eDiscovery Premium:** Solución avanzada para litigios complejos que incluye:
    - Gestión de custodios (identificación y notificación formal a los usuarios involucrados).
    - Conjuntos de revisión (*Review Sets*) con indexación avanzada.
    - Análisis de datos mediante Machine Learning (detección de duplicados, agrupación de conversaciones por hilos de correo y análisis predictivo de relevancia).
    - Redacción de datos sensibles antes de la exportación legal.

### Auditoría en Microsoft Purview (Audit)

Registra y centraliza los eventos de actividad generados por usuarios y administradores en decenas de servicios de Microsoft 365 (inicios de sesión, accesos a buzones, descargas de archivos, cambios en directivas).

- **Audit (Estándar):**
    - Registra eventos de Exchange, SharePoint, OneDrive, Teams, Microsoft Entra y Power BI.
    - Conserva los registros de auditoría durante un período predeterminado de **180 días**.
- **Audit (Premium):**
    - Amplía la retención de registros de auditoría hasta **1 año por defecto** (y configurable hasta 10 años con licencias de extensión).
    - Incluye eventos forenses de alta fidelidad, como *MailItemsAccessed* (qué correos específicos fueron leídos o abiertos) y eventos de búsqueda en el buzón.
    - Mayor ancho de banda para consultas masivas a la API de auditoría de Office 365.

### Administración del ciclo de vida de los datos (Data Lifecycle Management)

Gestiona la retención y eliminación del contenido de la organización a escala para reducir el costo de almacenamiento y minimizar riesgos legales por retención excesiva de información (**"Gobierna tus datos"**).

#### Directivas de retención (Retention Policies)

Se aplican a nivel de contenedores completos (todos los buzones de Exchange, todos los sitios de SharePoint o todos los chats de Teams):

- **Conservar:** Mantiene el contenido accesible durante un tiempo específico (ej. conservar todo durante 5 años por motivos fiscales), impidiendo su borrado definitivo aunque el usuario lo elimine de su bandeja.
- **Eliminar:** Elimina automáticamente el contenido que ha superado un periodo determinado (ej. borrar chats de Teams después de 90 días).
- **Conservar y luego eliminar:** Mantiene el contenido durante el tiempo requerido y lo elimina definitivamente al finalizar el plazo.

#### Etiquetas de retención (Retention Labels)

Permiten aplicar reglas de retención de forma granular a nivel de un archivo o correo individual, basándose en la fecha de creación, fecha de modificación o en la fecha de un evento específico (como la fecha de renuncia de un empleado o el cierre de un contrato).

### Administración de registros de Microsoft Purview (Records Management)

Es una capacidad avanzada dentro del ciclo de vida de los datos orientada a gestionar el contenido que califica formalmente como un **registro corporativo o legal** (*Record*):

- **Declaración de registros:** Cuando se aplica una etiqueta de registro a un documento, este se bloquea para evitar su edición o eliminación por parte de los usuarios.
- **Registros normativos (*Regulatory Records*):** Nivel más estricto de bloqueo donde los metadatos y el contenido quedan sellados de forma permanente e inmutable, de modo que ni siquiera los administradores del sistema pueden modificarlo o borrarlo antes de que expire el período de retención.
- **Revisión de eliminación (*Disposition Review*):** Flujo de trabajo en el que revisores designados deben aprobar formalmente la destrucción o conservación de un registro antes de que el sistema lo elimine definitivamente.

## Soluciones de gobierno de datos de Microsoft Purview

Proporcionan un marco unificado para descubrir, mapear, catalogar y gobernar los activos de datos en entornos híbridos y multinube (Azure, AWS, Snowflake, bases de datos locales, SAP).

```
[Fuentes de datos multinube / locales] ──(Escaneo automatizado)──> [Microsoft Purview Data Map] ──> [Unified Catalog] ──(Consumo de negocio)
```

### Conceptos y ventajas del gobierno de datos

- **Democratización de datos:** Facilita que los analistas y científicos de datos encuentren datos confiables de forma rápida.
- **Calidad de datos:** Asegura que los datos sean precisos, completos y actualizados.
- **Trazabilidad y linaje (*Lineage*):** Muestra de dónde provienen los datos, cómo se transforman y hacia qué reportes (como Power BI) fluyen a lo largo de su ciclo de vida.
- **Cumplimiento y reducción de silos:** Unifica la visibilidad de datos dispersos en diferentes nubes y centros de datos bajo directivas de gobernanza uniformes.

### Mapa de datos de Microsoft Purview (Data Map)

Es el motor base de metadatos que escanea, clasifica e indexa los activos de datos de la organización:

- **Escaneo automatizado:** Conectores nativos que extraen metadatos de bases de datos relacionales, data lakes, servicios analíticos y sistemas ERP sin mover los datos de su ubicación original.
- **Clasificación y etiquetado automático:** Identifica tipos de datos sensibles (SITs) y aplica etiquetas de clasificación directamente sobre los metadatos de los esquemas de tablas y archivos.
- **Grafo de linaje de datos:** Mapea visualmente el flujo de los datos desde su origen en una base de datos transaccional, pasando por procesos ETL/ELT (como Azure Data Factory), hasta los paneles finales de visualización.

!power-bi-lineage-subartifacts.png

### Catálogo unificado de Microsoft Purview (Unified Catalog)

Es la interfaz de experiencia empresarial construida sobre el Data Map que permite a los usuarios técnicos y de negocio interactuar con el ecosistema de datos gobernados:

- **Búsqueda y descubrimiento de datos:** Buscador inteligente donde los usuarios pueden localizar activos de datos utilizando filtros por términos técnicos, esquemas, clasificaciones o términos de negocio.
- **Glosario empresarial (*Business Glossary*):** Diccionario centralizado que define términos de negocio estandarizados (como *«Cliente activo»*, *«Margen de beneficio»*, *«ID de transacción»*) y los vincula directamente con las tablas y columnas técnicas correspondientes.
- **Productos de datos y gobierno por dominios (*Data Domains*):** Permite organizar los activos en dominios de negocio funcionales (Finanzas, Recursos Humanos, Ventas) y empaquetar conjuntos de datos en "productos de datos" con propietarios claramente definidos y controles de acceso gobernados.