# **Capitulo 3: Introducción a la infraestructura en la nube: Descripción de la administración y la gobernanza de Azure**

# **Descripción de la administración de costos en Azure**

En este módulo, se le presentarán factores que afectan a los costos en Azure y las herramientas que le ayudarán a predecir los costos potenciales y supervisar y controlar los costos. También revisará las opciones de optimización de costos para diferentes patrones de carga de trabajo.

# **Describir factores que pueden afectar a los costos en Azure**

Con Azure, paga por los recursos de TI a medida que los usa en lugar de comprar y mantener su propia infraestructura. Tanto si es cómputo, almacenamiento o redes, alquila lo que necesite y lo libera cuando lo haya terminado. Este enfoque basado en el consumo significa que los costos se escalan con el uso real. 

Muchos factores afectan cuánto paga. Algunos de los factores que afectan al costo son:

- Tipo de recurso
- Consumo
- Mantenimiento
- Geografía
- Tipo de suscripción
- Azure Marketplace

!image.png

## **Tipo de recurso**

Varios factores influyen en el costo de los recursos de Azure. El tipo de recursos, la configuración del recurso y la región de Azure afectarán a cuánto cuesta un recurso. Al aprovisionar un recurso de Azure, Azure realiza un seguimiento de la cantidad de cada recurso que use y le cobra en función de ese uso.

Por ejemplo:

Con una cuenta de almacenamiento, puede elegir opciones que afecten al precio, como el tipo de datos almacenados (por ejemplo, Blob Storage para archivos e imágenes), la rapidez con la que necesita acceder a él, el número de copias de seguridad que se van a conservar y qué región se va a usar.

## **Consumo**

### 1. **Pago por uso (Pay-as-you-go)**

Es el modelo normal de Azure:

- Pagas solamente lo que consumes.
- Más recursos usados = más costo.
- Menos recursos usados = menos costo.

Ejemplo:

- Una VM encendida 24/7 → pagas más.
- Una VM usada pocas horas → pagas menos.

### 2. **Reservas (Reservations)**

Son descuentos por comprometerte a usar un recurso durante un tiempo.

Ejemplo:

"Voy a usar esta máquina virtual durante 1 o 3 años."

Azure te da un precio más bajo porque sabe que tendrá ese consumo asegurado.

### 3. **Plan de ahorro de Azure para cálculo (Savings Plan)**

Parecido a las reservas, pero más flexible.

En vez de comprometerte con una VM específica, te comprometes a gastar cierta cantidad por hora en servicios de computación.

Ejemplo:

"Voy a gastar mínimo $5 por hora en computación durante 1 año."

Azure aplica automáticamente el mejor descuento disponible.

### 4. **Azure Spot Virtual Machines**

Son máquinas virtuales más baratas que usan capacidad sobrante de Azure.

Pero tienen un riesgo:

- Azure puede apagar esa VM cuando necesite esa capacidad.

Sirven para tareas que pueden detenerse y continuar después:

- Procesamiento por lotes.
- Pruebas.
- Análisis de datos.

## **Mantenimiento**

Al eliminar un grupo de recursos en Azure se eliminan los recursos contenidos en él, mientras que al eliminar un recurso individual pueden permanecer recursos asociados que continúan generando costos. Entonces el mantenimiento es importante en esta situacion.

## **Geografía**

Al aprovisionar la mayoría de los recursos en Azure, debe definir una región donde se implementa el recurso. La infraestructura de Azure se distribuye globalmente, lo que le permite implementar los servicios de forma centralizada o más cercana a los clientes, o algo entre ellos. Esta implementación global tiene diferencias de precios globales. El costo del poder, la mano de obra, los impuestos y las tarifas varían en función de la ubicación.

Debido a estas variaciones, los recursos de Azure pueden diferir en los costos de la implementación en función de la región.

## **Tráfico de red**

El ancho de banda hace referencia a los datos que se mueven y salen de los centros de datos de Azure. Algunas transferencias de datos entrantes (datos que van a centros de datos de Azure) son gratuitos. En el caso de las transferencias de datos salientes (datos que salen de los centros de datos de Azure), los precios de transferencia de datos se basan en zonas.

## **Tipo de suscripción**

Algunos tipos de suscripción de Azure también incluyen asignaciones de uso, lo que afecta a los costos.

Por ejemplo, una suscripción de evaluación gratuita de Azure proporciona acceso a una serie de productos de Azure gratuitos durante 12 meses. También incluye crédito para gastar en los primeros 30 días del registro. Obtendrá acceso a más de 25 productos que siempre son gratuitos (en función de la disponibilidad de recursos y regiones).

## **Azure Marketplace**

Azure Marketplace le permite comprar soluciones y servicios basados en Azure de proveedores de terceros. Esto podría incluir un servidor web preconfigurado, una máquina virtual con software especializado ya instalado o una solución de copia de seguridad administrada. Todas las soluciones disponibles en Azure Marketplace están certificadas y compatibles con las directivas y estándares de Azure.

# **Exploración de la calculadora de precios**

La calculadora de precios le ayuda a calcular los posibles gastos de Azure. Puede acceder a ella en línea y crear una configuración. 

**Nota: Se ha retirado la calculadora del costo total de propiedad (TCO).** 

## **Calculadora de precios**

La calculadora de precios está diseñada para proporcionarle un costo estimado para el aprovisionamiento de recursos en Azure. Puede obtener una estimación de recursos individuales, crear una solución o usar un escenario de ejemplo para ver una estimación del gasto de Azure.

Nota: La calculadora de precios solo tiene fines informativos. Los precios son solo una estimación. No se aprovisiona nada al agregar recursos a la calculadora de precios y no se le cobrará por ningún servicio que seleccione.

# **Describir la herramienta Microsoft Cost Management**

Cost Management es un conjunto de herramientas que ayuda a las organizaciones a analizar, supervisar y administrar Azure costos para evitar esas situaciones.

## **¿Qué es Cost Management?**

Cost Management proporciona la capacidad de comprobar rápidamente los costos de recursos de Azure, crear alertas basadas en el gasto de recursos y crear presupuestos que se pueden usar para automatizar la administración de recursos. 

El análisis de costos es una característica de Cost Management que proporciona una representación visual rápida para los costos de Azure. Con el análisis de costos, puede ver rápidamente el costo total de varias maneras diferentes, incluido el ciclo de facturación, la región, el recurso, etc.

## **Alertas de costos**

Las alertas de costo proporcionan una única ubicación para comprobar rápidamente todos los distintos tipos de alertas que pueden aparecer en el servicio Cost Management. Los tres tipos de alertas que pueden aparecer son:

- **Alerta de crédito:** Hace referencia a organizaciones que cuentan con un **Enterprise Agreement (EA)** y un **crédito prepagado de Azure**. Azure envía automáticamente notificaciones cuando se ha consumido el **90%** y el **100%** del crédito disponible, para que la organización sepa que su saldo está por agotarse.
- **Alerta de presupuesto:** Permite que el administrador defina un **presupuesto o límite de gasto** para una suscripción, grupo de recursos o ámbito determinado. También puede configurar los porcentajes o montos en los que desea recibir notificaciones (por ejemplo, al 50%, 80% o 100% del presupuesto). **No requiere un prepago**, ya que es una herramienta de control de costos
- Alertas de cuota de gasto de departamento: Permite supervisar el gasto de un ámbito específico (como una suscripción, un grupo de recursos o un departamento) y generar notificaciones cuando el consumo alcanza las condiciones configuradas o cuando se detectan gastos que requieren atención. Su objetivo es ayudar a controlar y analizar el consumo de los recursos.

## **Presupuestos**

Un presupuesto es donde se establece un límite de gasto para Azure. Puede establecer presupuestos basados en una suscripción, un grupo de recursos, un tipo de servicio u otros criterios. Al establecer un presupuesto, también establecerá una alerta de presupuesto. Cuando el presupuesto alcance el nivel de alerta de presupuesto, desencadenará una alerta de presupuesto que se muestra en el área de alertas de costos.

# **Describir el propósito de las etiquetas**

A medida que aumenta el uso de la nube, es cada vez más importante mantenerse organizado. Una buena estrategia de etiquetado (Tag) le ayuda a comprender el uso de la nube y le ayuda a administrar los costos.

Una manera de organizar los recursos relacionados es colocarlos en sus propias suscripciones. También puede usar grupos de recursos para administrar recursos relacionados. Las etiquetas de recursos son otra manera de organizar los recursos.

Las etiquetas proporcionan información adicional o metadatos sobre los recursos. Estos metadatos son útiles para:

#### Administración de recursos

Las etiquetas (tags) permiten identificar y organizar recursos de Azure según información específica.

Ejemplo:

Una empresa tiene muchas máquinas virtuales:

VM-Servidor1 → etiqueta: Equipo=TI
VM-Servidor2 → etiqueta: Equipo=Seguridad
VM-Servidor3 → etiqueta: Entorno=Producción

Así puedes buscar, filtrar y administrar recursos más fácilmente.

#### Administración y optimización de costos

Las etiquetas ayudan a saber quién usa los recursos y cuánto cuesta cada área.

Ejemplo:

Una empresa etiqueta sus recursos:

Departamento: Marketing
Departamento: Finanzas
Departamento: Desarrollo

Después puede revisar:

Cuánto gastó Marketing.
Cuánto gastó Finanzas.
Qué equipo consume más recursos.

Esto ayuda a controlar presupuestos y estimar gastos futuros.

#### Administración de operaciones

Las etiquetas permiten clasificar recursos según su importancia para el funcionamiento del negocio.

Ejemplo:

Importancia: Crítica
Importancia: Alta
Importancia: Baja

Una base de datos principal puede tener una etiqueta:

SLA: 99.99%

Mientras que un servidor de pruebas puede tener una prioridad menor.

Esto ayuda a definir acuerdos de nivel de servicio (SLA) adecuados.

#### Seguridad

Las etiquetas ayudan a clasificar recursos según el nivel de protección que necesitan.

Ejemplo:

Clasificación: Público
Clasificación: Interno
Clasificación: Confidencial

Así una organización puede identificar rápidamente qué recursos contienen información sensible y aplicar controles adecuados.

#### Gobernanza y cumplimiento normativo

Las etiquetas ayudan a comprobar que los recursos cumplen reglas internas o estándares externos.

Ejemplo:

Una empresa exige que todos los recursos tengan:

Propietario: Juan
Departamento: Seguridad
Cumplimiento: ISO 27001

Esto facilita auditorías y permite verificar que los recursos siguen las políticas establecidas.

#### Optimización y automatización de cargas de trabajo

Las etiquetas ayudan a identificar recursos relacionados con una aplicación o proyecto para automatizar tareas.

Ejemplo:

Una aplicación tiene:

Aplicación: SistemaVentas

#### Todos los recursos relacionados:

Máquina virtual.
Base de datos.
Red.
Almacenamiento.

Tienen esa etiqueta.

Luego herramientas como Azure DevOps pueden encontrar esos recursos y ejecutar acciones automáticamente.

Un conjunto práctico de etiquetas de inicio para muchos equipos es `Environment`, `Owner`, `CostCenter`y `Workload`. Este conjunto admite tareas diarias comunes, como el filtrado de costos, la identificación de gestores de servicios y la definición del alcance de la automatización.

## **¿Cómo se administran las etiquetas de recursos?**

Puede agregar, modificar o eliminar etiquetas de recursos a través de Azure Portal, PowerShell, la CLI de Azure, las plantillas de Azure Resource Manager o la API REST.

Puede usar Azure Policy para aplicar reglas y convenciones de etiquetado. Por ejemplo, puede requerir que ciertas etiquetas se agreguen a los nuevos recursos a medida que se aprovisionan. También puede definir reglas que vuelvan a aplicar etiquetas que se hayan quitado.

## **Estructura de etiquetado de ejemplo**

Una etiqueta de recurso consta de un nombre y un valor. Puede asignar una o varias etiquetas a cada recurso de Azure.

| **Nombre** | **Valor** |
| --- | --- |
| AppName | Nombre de la aplicación de la que forma parte el recurso. |
| CostCenter | Código interno del centro de costos. |
| Dueño | Nombre del propietario técnico o del servicio responsable del recurso. |
| Medio ambiente | Un nombre de entorno, como "Prod", "Dev" o "Test". |
| Impacto | Lo importante que es el recurso para las operaciones, como "crítico para la misión", "impacto alto" o "bajo impacto". |

Tenga en cuenta que no es necesario aplicar que una etiqueta específica esté presente en todos los recursos. Por ejemplo, puede decidir que solo los recursos críticos tienen la etiqueta Impact. Después, todos los recursos no etiquetados no se considerarían como críticos.

En pocas palabras, poner etiqueta a lo mas importante y critico.

## **Descripción de las opciones de optimización de costos en Azure**

Después de calcular y supervisar los costos, el siguiente paso es elegir la opción de precios adecuada para cada perfil de carga de trabajo.

## **Reservas**

Las reservas son las mejores para cargas de trabajo estables y predecibles. Se compromete a una capacidad de recursos específica para un período de un año o tres años, y Azure aplica precios con descuento al uso coincidente. 

- Ejemplo: Cuando vas al barbero y reservas un turno, ahi te ahorras el tiempo si te comprometes a llegar a la hora adecuada.

## El plan de ahorro de Azure

El plan de ahorro de Azure para cómputo ofrece descuentos mediante un compromiso de gasto por hora durante 1 o 3 años, brindando más flexibilidad que las reservas al no depender de un tipo específico de recurso.

## Servicios Puntuales (Las Máquinas Virtuales de Spot)

Las Máquinas Virtuales de Spot utilizan capacidad no utilizada de Azure a precios reducidos, pero pueden ser interrumpidas cuando Azure necesita recuperar esos recursos. Son ideales para cargas de trabajo tolerantes a interrupciones.

## **Guía para la toma de decisiones**

Use este patrón de decisión rápido:

- Elija Reservas para cargas de trabajo predecibles y de larga duración con necesidades estables de recursos.
- Elija el plan de ahorro de Azure para el cómputo cuando el uso sea estable, pero necesite más flexibilidad en los servicios de cómputo.
- Elija Precios puntuales para cargas de trabajo con tolerancia a errores o interrumpibles, donde el costo más bajo es la prioridad más alta.

# **Descripción de las características y herramientas de Azure para la gobernanza y el cumplimiento**

En este módulo, se le presentará algunas de las características y herramientas que puede usar para ayudar con la gobernanza de su entorno de Azure. También obtendrá información sobre las herramientas que puede usar para ayudar a mantener los recursos conformes a los requisitos internos o normativos.

## **Descripción del propósito de Microsoft Purview**

Microsoft Purview es una familia de soluciones de gobernanza, riesgo y cumplimiento de datos que le ayudan a obtener una sola visión unificada de los datos. Microsoft Purview reúne información sobre los datos locales, multinube y software como servicio.

Con Microsoft Purview, puede mantenerse al día en su entorno de datos gracias a:

- Detección de datos automatizada
- Clasificación de datos confidenciales
- Linaje de datos de un extremo a otro

## **Soluciones de riesgo y cumplimiento de Microsoft Purview**

Características de Microsoft 365 como componente principal de las soluciones de cumplimiento y riesgos de Microsoft Purview. Microsoft Teams, OneDrive y Exchange son solo algunos de los servicios de Microsoft 365 que Microsoft Purview usa para ayudar a administrar y supervisar los datos. (SaaS)

Microsoft Purview, mediante la administración y supervisión de los datos, ayuda a su equipo a:

- Proteger datos confidenciales en nubes, aplicaciones y dispositivos.
- Identificar los riesgos de datos y administrar los requisitos de cumplimiento normativo.
- Comenzar con la normativa de cumplimiento.

## **Gobernanza unificada de datos**

Microsoft Purview proporciona una gobernanza unificada de datos, permitiendo administrar, organizar, clasificar y controlar los datos de una organización sin importar dónde estén almacenados (localmente, Azure, otras nubes o SaaS).

La gobernanza unificada de datos de Microsoft Purview ayuda a su equipo a:

- Crear un mapa actualizado de todo el patrimonio de datos que incluya la clasificación de datos y el linaje de un extremo a otro.
- Identificar dónde se almacenan los datos confidenciales en su patrimonio.
- Crear un entorno seguro para que los consumidores de datos encuentren datos valiosos.
- Generar información sobre cómo se almacenan y usan los datos.
- Administrar el acceso a los datos de su patrimonio de forma segura y a gran escala.

## **Descripción del propósito de Azure Policy**

¿Cómo se asegura de que los recursos se mantengan conformes? ¿Puede recibir un aviso cuando la configuración de un recurso cambie?

Azure Policy es un servicio que permite crear y aplicar reglas para controlar, auditar y mantener la configuración de los recursos de Azure, asegurando que cumplan con los estándares y requisitos definidos por la organización.

!image.png

### ¿Cómo se definen directivas en Azure Policy?

**Azure Policy** permite crear reglas que indican cómo deben configurarse los recursos de Azure.

Ejemplo:

> "Todas las máquinas virtuales deben estar en una región específica y deben tener una etiqueta de propietario."
> 

Azure Policy puede:

- **Auditar** recursos → detectar cuáles no cumplen la regla.
- **Denegar** recursos → impedir que se creen recursos que no cumplen.
- **Corregir automáticamente** → modificar o agregar configuraciones necesarias.

Las directivas se pueden aplicar en diferentes niveles:

```
Grupo de administración
        ↓
Suscripción
        ↓
Grupo de recursos
        ↓
Recurso individual
```

Las directivas se **heredan**, es decir, si aplicas una política a un nivel superior, los recursos dentro de ese nivel también la reciben.

### ¿Qué es una iniciativa de Azure Policy?

Una **iniciativa** es un conjunto de varias directivas relacionadas agrupadas bajo un mismo objetivo.

Ejemplo:

Una iniciativa de seguridad puede incluir:

- Comprobar que las bases de datos tengan cifrado.
- Verificar que los servidores tengan protección de endpoint.
- Revisar vulnerabilidades del sistema operativo.

En vez de administrar 100 políticas por separado, administras una iniciativa que contiene todas esas reglas.

### Ejemplo sencillo:

Una empresa quiere cumplir seguridad:

Sin iniciativa:

```
Política 1 → Cifrado obligatorio
Política 2 → Etiquetas obligatorias
Política 3 → Región permitida
Política 4 → Seguridad de VM
```

Con iniciativa:

```
Iniciativa "Seguridad empresarial"

     ├── Cifrado obligatorio
     ├── Etiquetas obligatorias
     ├── Región permitida
     └── Seguridad de VM
```

## **Descripción del propósito de bloqueos de recursos**

Los bloqueos de recursos impiden que se eliminen o modifiquen recursos por error.

Aun cuando haya directivas de control de acceso basado en roles de Azure (RBAC de Azure) en vigor, sigue existiendo el riesgo de que alguien con el nivel de acceso adecuado elimine recursos de nube críticos. Los bloqueos de recursos impiden que los recursos se eliminen o actualicen, según el tipo de bloqueo.  

Los bloqueos de recursos se heredan, lo que significa que si coloca un bloqueo de recursos en un grupo de recursos, también se aplicará el bloqueo a todos los recursos dentro del grupo.

!image.png

## **Tipos de bloqueos de recursos**

Hay dos tipos de bloqueos de recursos, uno que impide que los usuarios eliminen un recurso y otro que impide que los usuarios lo cambien o eliminen.

- **Eliminar** significa que los usuarios autorizados pueden leer y modificar un recurso, pero no eliminarlo.
- **ReadOnly** significa que los usuarios autorizados solo pueden leer recursos, pero no actualizarlos ni eliminarlos.

## **¿Cómo se administran los bloqueos de recursos?**

Los bloqueos de recursos se pueden administrar en Azure Portal, PowerShell, la CLI de Azure o con una plantilla de Azure Resource Manager. Para ver, agregar o eliminar bloqueos en Azure Portal, vaya a la sección Bloqueos del panel Configuración de cualquier recurso en Azure Portal.

## **¿Cómo se elimina o cambia un recurso bloqueado?**

Aunque los bloqueos impiden que se produzcan cambios por error, se pueden seguir realizando cambios realizando un proceso de dos pasos. Para modificar un recurso bloqueado, primero hay que quitar el bloqueo. Tras quitarlo, podemos aplicar cualquier acción que podamos realizar de acuerdo a nuestros permisos.

Nota: Los bloqueos de recursos se aplican con independencia de los permisos RBAC. Es decir, aun siendo el propietario del recurso, tendremos que quitar el bloqueo antes de poder realizar la actividad bloqueada.

## **Descripción de las ventajas del portal de confianza de servicios**

El Portal de confianza de servicios de Microsoft es un portal que proporciona contenido, herramientas y otros recursos sobre las prácticas de seguridad, privacidad y cumplimiento de Microsoft. El Portal de confianza de servicios contiene detalles sobre la implementación de controles y procesos de Microsoft que protegen nuestros servicios en la nube y los datos de los clientes.

Nota: Para acceder a algunos de los recursos en el Portal de confianza de servicios, debe iniciar sesión como usuario autenticado con su cuenta de servicios en la nube de Microsoft (Cuenta profesional o educativa de Microsoft Entra). Deberá revisar y aceptar el acuerdo de no divulgación de Microsoft para acceder a los materiales de cumplimiento.

!service-trust-portal.png

- **El Portal de confianza** de servicios proporciona un hipervínculo de acceso rápido para volver a la página principal del Portal de confianza de servicios.
- **Mi biblioteca** le permite guardar (o anclar) documentos para acceder rápidamente a ellos en la página Mi biblioteca. También puede establecer una configuración para recibir notificaciones cuando se actualicen los documentos en Mi biblioteca.
- **Todos los documentos** son un único lugar de aterrizaje para los documentos en el portal de confianza del servicio. En **Todos los documentos**, puede anclar documentos para que aparezcan en **mi biblioteca**.

# **Descripción de las características y herramientas para administrar e implementar recursos de Azure**

En este módulo se presentan las características y herramientas para administrar e implementar recursos de Azure. Obtenga información sobre Azure Portal (una interfaz gráfica para administrar recursos de Azure), la línea de comandos y las herramientas de scripting que ayudan a implementar o configurar recursos. 

## **Descripción de las herramientas para interactuar con Azure**

Para sacar el máximo partido de Azure, necesita una manera de interactuar con el entorno de Azure, los grupos de administración, las suscripciones, los grupos de recursos, los recursos, etc. Azure proporciona varias herramientas para administrar el entorno, entre las que se incluyen:

- Azure Portal
- Azure PowerShell
- Interfaz de la línea de comandos (CLI) de Azure

## **Operaciones asistidas por inteligencia artificial con Copilot en Azure**

Copilot en Azure es una experiencia de asistente de IA que puede ayudar a los administradores a trabajar más rápido al proporcionar instrucciones contextuales en lenguaje natural. En un nivel fundamental, trate a Copilot como asistente operativo. Debe seguir validando recomendaciones, confirmar permisos y revisar los cambios de implementación antes de aplicarlos en producción.

## **¿Qué es Azure Portal?**

Azure Portal es una consola unificada basada en web que proporciona una alternativa a las herramientas de línea de comandos. Con Azure Portal, puede administrar la suscripción de Azure mediante una interfaz gráfica de usuario. Puedes:

- Compilar, administrar y supervisar todo, desde aplicaciones web sencillas hasta implementaciones complejas en la nube
- Creación de paneles personalizados para una vista organizada de recursos
- Configuración de opciones de accesibilidad para una experiencia óptima

Azure Portal está diseñado para lograr resistencia y disponibilidad continua. Mantiene una presencia en cada centro de datos de Azure. Esta configuración hace que Azure Portal sea resistente a errores individuales del centro de datos y evita ralentizaciones de la red al estar cerca de los usuarios

## **Azure Cloud Shell**

Azure Cloud Shell es una herramienta de shell basada en explorador que permite crear, configurar y administrar recursos de Azure mediante un shell. Azure Cloud Shell admite Tanto Azure PowerShell como la interfaz de la línea de comandos (CLI) de Azure, que es un shell de Bash.

**Caracteristicas**:

Azure Cloud Shell tiene varias características que lo convierten en una oferta única para ayudarle a administrar Azure. Algunas de esas características son:

- Se trata de una experiencia de shell basada en explorador, sin que se requiera ninguna instalación o configuración local.
- Se autentica en las credenciales de Azure, por lo que cuando inicia sesión en él, sabe inherentemente quién es y qué permisos tiene.
- Elige el shell con el que está más familiarizado; Azure Cloud Shell admite Tanto Azure PowerShell como la CLI de Azure (que usa Bash).

## **¿Qué es Azure PowerShell?**

Azure PowerShell es una herramienta de administración que utiliza cmdlets para interactuar con Azure mediante la API REST, permitiendo crear, configurar y automatizar recursos mediante comandos y scripts repetibles.

Ejemplo:

En el portal:

> Crear una máquina virtual → seleccionar región → tamaño → disco → red → revisar → crear.
> 

Con Azure PowerShell:

```
New-AzVM
```

Un comando puede crear o modificar recursos siguiendo parámetros definidos.

## **¿Qué es la CLI de Azure?**

La CLI de Azure es funcionalmente equivalente a Azure PowerShell, y la diferencia principal es la sintaxis de los comandos. Aunque Azure PowerShell usa comandos de PowerShell, la CLI de Azure usa comandos de Bash.

La CLI de Azure proporciona las mismas ventajas de controlar tareas discretas o orquestar operaciones complejas mediante código. También se puede instalar en plataformas Windows, Linux y Mac, así como a través de Azure Cloud Shell.

## **Descripción del propósito de Azure Arc**

Azure Arc funciona con Azure Resource Manager para ampliar el cumplimiento y la supervisión de Azure a configuraciones híbridas y multinube. Azure Arc simplifica la gobernanza y la administración al ofrecer una plataforma coherente de administración multinube y local.

## **Escenario práctico**

Imagine que su organización ejecuta cargas de trabajo en Azure, un centro de datos local y otra nube pública. Con Azure Arc, los equipos de operaciones pueden aplicar un seguimiento coherente de la gobernanza, la directiva y el inventario en estos entornos desde Azure, en lugar de administrar cada entorno con herramientas desconectadas.

## **¿Qué puede hacer Azure Arc fuera de Azure?**

Actualmente, Azure Arc permite administrar los siguientes tipos de recursos hospedados fuera de Azure:

- Servidores
- Clústeres de Kubernetes
- Servicios de datos de Azure
- SQL Server
- Máquinas virtuales (versión preliminar)

## ¿Qué es Azure Resource Manager (ARM)?

**Azure Resource Manager es la capa de administración de Azure.**

Es decir, es el "intermediario" que recibe todas las solicitudes que haces en Azure y las procesa.

Ejemplo:

Tú quieres crear una máquina virtual.

Puedes hacerlo desde:

- Portal de Azure.
- Azure CLI.
- Azure PowerShell.
- SDK.

Pero todas pasan por:

```
Usuario
  ↓
Portal / CLI / PowerShell / API
  ↓
Azure Resource Manager
  ↓
Servicio de Azure
  ↓
Máquina Virtual creada
```

ARM se encarga de:

- Verificar tu identidad (autenticación).
- Revisar tus permisos (autorización).
- Crear, modificar o eliminar recursos.

## ¿Qué significa Infraestructura como Código (IaC)?

Normalmente una persona crea recursos manualmente:

```
Entrar al portal
↓
Crear VM
↓
Configurar red
↓
Configurar almacenamiento
↓
Crear recurso
```

Eso funciona, pero es lento y difícil de repetir.

**IaC cambia la idea:**

En lugar de configurar manualmente, escribes código que describe cómo quieres tu infraestructura.

Ejemplo:

"Quiero:

- Una VM.
- Una red.
- Un almacenamiento.
- Una base de datos."

Ese código lo ejecutas y Azure crea todo automáticamente.

## ¿Qué son las plantillas de Azure Resource Manager (ARM Templates)?

Son archivos **JSON** que describen el estado final que quieres tener en Azure.

No dicen:

> "Primero crea esto, luego haz esto, después configura aquello."
> 

Sino:

> "Este es el resultado final que quiero."
> 

Eso es lo que significa **declarativo**.

Ejemplo:

Tú declaras:

```
Necesito:
- 1 máquina virtual
- 1 red virtual
- 1 almacenamiento
```

Azure Resource Manager decide:

- En qué orden crearlos.
- Qué dependencias existen.
- Qué puede crear al mismo tiempo.

## ¿Por qué son importantes las plantillas ARM?

Porque permiten:

### Resultados repetibles

Puedes usar la misma plantilla para crear:

- Ambiente de desarrollo.
- Ambiente de pruebas.
- Ambiente de producción.

Y todos quedan iguales.

### Orquestación

ARM sabe las dependencias.

Ejemplo:

Una VM necesita:

- Una red.
- Un disco.

ARM sabe:

```
Crear red
    ↓
Crear disco
    ↓
Crear VM
```

### Modularidad

Puedes dividir una infraestructura grande en partes reutilizables.

Ejemplo:

```
Plantilla principal

 ├── Red
 ├── Máquinas virtuales
 └── Base de datos
```

## ¿Qué es Bicep?

**Bicep es un lenguaje creado por Microsoft para reemplazar las plantillas ARM JSON.**

Hace lo mismo, pero de una forma más sencilla.

Comparación:

ARM JSON:

```
{
 "type":"Microsoft.Compute/virtualMachines",
 "name":"Servidor01"
}
```

Bicep:

```
resource vm 'Microsoft.Compute/virtualMachines' = {
 name: 'Servidor01'
}
```

Bicep es:

- Más fácil de leer.
- Menos código.
- Más organizado.

Pero al final:

```
Bicep
  ↓
ARM
  ↓
Azure Resource Manager
  ↓
Recursos creados
```

En pocas palabras:

| Concepto | Qué es |
| --- | --- |
| **Azure Resource Manager** | Servicio que administra todas las solicitudes de Azure |
| **ARM Template** | Archivo JSON que define infraestructura como código |
| **IaC** | Administrar infraestructura usando código en vez de hacerlo manualmente |
| **Bicep** | Lenguaje más simple para crear implementaciones mediante ARM |

# **Descripción de las herramientas de supervisión de Azure**

En este módulo, se le presentarán herramientas que le ayudarán a supervisar el entorno y las aplicaciones, tanto en Azure como en entornos locales o multinube.

## **Describir el propósito de Azure Advisor**

Azure Advisor evalúa los recursos de Azure y realiza recomendaciones para ayudarle a mejorar la confiabilidad, la seguridad, el rendimiento y la eficacia de los costos. Piense en ella como una guía personalizada de procedimientos recomendados integrada en Azure Portal.

Nota: También puede configurar notificaciones para que Advisor le avise cuando aparezcan nuevas recomendaciones.

Las recomendaciones se dividen en cinco categorías:

- **La confiabilidad** ayuda a mantener las aplicaciones en ejecución marcando los riesgos de configuración.
- **La seguridad** detecta amenazas y vulnerabilidades que podrían provocar infracciones.
- **El rendimiento** identifica los cambios que pueden acelerar las aplicaciones.
- **La excelencia operativa** sugiere mejoras de flujo de trabajo e implementación.
- **Cost** encuentra formas de reducir el gasto en Azure.

!azure-advisor-dashboard.png

## **Descripción de Azure Service Health**

Azure Service Health le ayuda a mantenerse informado sobre el estado de Azure y los recursos específicos que se ejecutan. Combina tres vistas que limitan el ámbito de los recursos globales a los individuales.

## **Tres vistas de salud**

!image.png

- **Estado de Azure:**  proporciona una imagen **global** del estado de Azure en todos los servicios y regiones. Compruebe esta página cuando escuche una interrupción generalizada y quiera saber si afecta a Azure.
- **Service Health:** se centra en los servicios y regiones de Azure que realmente usas. Dado que ha iniciado sesión, Service Health conoce los servicios que son importantes para usted y muestra interrupciones, mantenimiento programado y avisos de estado relevantes para su entorno. Puede configurar alertas para que se le notifique automáticamente.
- **Resource Health:** se centra en los recursos individuales, como una máquina virtual específica. Indica si un recurso se está ejecutando normalmente o experimenta un problema y si el problema está en el lado de Azure o en el suyo.

## **Valor operativo**

Cuando un evento afecta a una de las cargas de trabajo, Azure Service Health proporciona vínculos a soporte técnico para que pueda responder rápidamente.

## **Descripción de Azure Monitor**

Azure Monitor es una plataforma para recopilar, analizar y actuar sobre los datos de los recursos y aplicaciones de Azure. Funciona con entornos de Azure, locales y multinube.

Azure Monitor recopila registros y métricas de las aplicaciones, los sistemas operativos y las capas de red, almacena esos datos de forma centralizada y hace que esté disponible a través de paneles, consultas y alertas.

## **Azure Log Analytics: Análisis de Registros de Azure**

Log Analytics es la herramienta en el portal de Azure donde se escriben y ejecutan consultas contra los datos recopilados por Azure Monitor. Puede realizar un filtrado sencillo, como buscar todos los errores en la última hora o ejecutar análisis avanzados para visualizar tendencias a lo largo del tiempo.

## **Alertas de Azure Monitor**

Las alertas le notifican cuando Azure Monitor detecta que se ha cumplido una condición definida. Se crea una regla de alerta que especifica la condición y un grupo de acciones que controla quién recibe una notificación y qué ocurre a continuación.

!azure-monitor-alerts.png

Las alertas pueden basarse en métricas o en registros. Por ejemplo, una alerta de métrica puede enviar un correo electrónico cuando la CPU de una máquina virtual permanece por encima de 80%.

## Application Insights

Application Insights es una característica de Azure Monitor que permite supervisar el rendimiento, disponibilidad y uso de aplicaciones web mediante métricas como errores, tiempos de respuesta, dependencias, usuarios y rendimiento del servidor.