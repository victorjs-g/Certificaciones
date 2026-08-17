# Capitulo 1: Introducción a la infraestructura en la nube Descripción de los conceptos de la nube

# Introducción a la infraestructura en la nube: Descripción de la informática en la nube

En este capítulo se abordarán los conceptos fundamentales de la informática en la nube dentro del contexto de la certificación **AZ-900 (Microsoft Azure Fundamentals)**.

Los contenidos principales de este capítulo son los siguientes:

1. Descripción de la informática en la nube
2. Descripción de las ventajas de usar servicios en la nube
3. Descripción de los tipos de servicio en la nube

---

# Descripción de la informática en la nube

En este módulo se presenta la informática en la nube. Se tratan aspectos como los conceptos de nube, los modelos de implementación y la comprensión del modelo de responsabilidad compartida en la nube.

## Introducción a los aspectos básicos de Microsoft Azure

Microsoft Azure es una plataforma en la nube que ofrece un conjunto de servicios para que las empresas puedan cumplir con sus objetivos técnicos. Azure ofrece servicios para diferentes necesidades, como computación, almacenamiento, redes, bases de datos, inteligencia artificial e IoT.

Y son los siguientes:

- Computación en la nube: Contenedores, funciones (sin servidor / serverless) y máquinas virtuales.
- Almacenamiento: Blob Storage, Files, Queues, Tables y más.
- Redes: VNet, Load Balancer, DNS, CDN, Front Door y más.
- Base de datos: SQL, Cosmos DB, MySQL, PostgreSQL.
- Inteligencia artificial y Machine Learning: Azure OpenAI, AI Services, Machine Learning.
- IoT: IoT Hub, IoT Central, servicios de Edge.

## **Introducción a la informática en la nube**

En este módulo se presentan los conceptos generales de la nube. Comienza con una introducción a la nube en general. A continuación, se profundiza en conceptos como el modelo de responsabilidad compartida y los diferentes modelos de nube, además de explorar el modelo de precios basado en el consumo.

### Objetivos de aprendizaje

- Definir la informática en la nube.
- Describir el modelo de responsabilidad compartida.
- Definir modelos de nube, incluidos los modelos públicos, privados e híbridos.
- Identificar los casos de uso adecuados para cada modelo de nube.
- Describir el modelo basado en el consumo.
- Comparar los modelos de precios en la nube.

## **¿Qué es la informática en la nube?**

La informática en la nube es la prestación de servicios informáticos a través de Internet. Los servicios informáticos incluyen recursos comunes de Tecnología de la Información (TI), como máquinas virtuales, almacenamiento, bases de datos, redes, Internet de las cosas (IoT), Machine Learning (ML) e inteligencia artificial (IA).

Al utilizar un modelo de computación en la nube basado en Internet, la infraestructura deja de estar restringida por las limitaciones físicas de un centro de datos tradicional. Esto permite aprovechar la escalabilidad y reducir los tiempos y costos asociados a la adquisición, gestión y despliegue físico de hardware.

#### **Ejemplo práctico:**

Una empresa lanza una nueva página web. En un día normal recibe alrededor de **40 usuarios** conectados al mismo tiempo, pero después de una campaña publicitaria comienza a recibir **4,000 usuarios simultáneos**. Si la empresa utiliza servidores físicos (on-premises), tendría que comprar e instalar más equipos para soportar ese aumento de tráfico, lo que requiere tiempo y una inversión considerable. En cambio, si utiliza **Cloud Computing**, puede aumentar la capacidad de sus servidores en cuestión de minutos para atender a todos los usuarios. Cuando el tráfico vuelve a la normalidad, reduce esos recursos y así disminuye sus costos. Esto permite responder rápidamente a la demanda y mantener el servicio disponible para los clientes.

## Describir el modelo de responsabilidad compartida en la nube

Es un modelo donde el proveedor de la nube y el cliente comparten responsabilidades de seguridad y administración. El proveedor protege la infraestructura y el cliente protege sus datos, además de controlar quién puede acceder a ellos.

### **Cómo cambian las responsabilidades en la nube**

#### Centro de datos local (On-Premises)

- **Responsabilidad:** Todo recae en la empresa.
- La empresa administra los servidores, la red, el almacenamiento, la seguridad física, las actualizaciones, el sistema operativo, las aplicaciones y los datos.

#### Infraestructura como Servicio (IaaS)

- **Responsabilidad:** La mayor parte sigue siendo del cliente.
- **Proveedor:** Se encarga de la infraestructura física (servidores, almacenamiento, red, energía y seguridad física).
- **Cliente:** Administra el sistema operativo, las aplicaciones, los datos, las actualizaciones y la **seguridad de acceso**, asegurando que solo las personas autorizadas puedan acceder a los recursos.

#### Plataforma como Servicio (PaaS)

- **Responsabilidad:** Se comparte de forma más equilibrada.
- **Proveedor:** Administra la infraestructura, el sistema operativo y la plataforma.
- **Cliente:** Se encarga de las aplicaciones, los datos y la **seguridad de acceso**, controlando quién puede utilizar la aplicación y acceder a la información.

#### Software como Servicio (SaaS)

- **Responsabilidad:** La mayor parte recae en el proveedor.
- **Proveedor:** Administra la aplicación, la plataforma y toda la infraestructura.
- **Cliente:** Administra sus datos, la configuración del servicio y la **seguridad de acceso**, es decir, decide qué usuarios pueden acceder y qué permisos tienen.

### Responsabilidad por modelo de servicio

En el siguiente diagrama se visualizará cómo el modelo de responsabilidad compartida en la nube indica quién es responsable de cada elemento, dependiendo del modelo de cloud.

!image.png

## Definición de modelos en la nube

#### ¿Qué son los modelos en la nube?

Los modelos en la nube definen cómo se implementan y administran los recursos en la nube. Los tres principales modelos en la nube son: **privado, público e híbrido**.

#### Nube Privada

Una nube privada es un modelo de computación en el que una organización tiene un entorno de nube dedicado exclusivamente a ella. Puede proporcionar un mayor nivel de control sobre la infraestructura, la seguridad y la privacidad de la información.

#### **Nube Pública**

Es un modelo de computación en el que un proveedor de servicios en la nube, como Microsoft o Google, es responsable de la infraestructura física (servidores, redes y centros de datos) y ofrece estos recursos a diferentes clientes a través de Internet.

#### **Nube Híbrida**

Una nube híbrida es un modelo de computación que combina una nube pública y un entorno privado, permitiendo utilizar ambos entornos según las necesidades de la organización. Por ejemplo, una organización puede mantener determinados sistemas en un entorno privado y utilizar la nube pública para aprovechar su escalabilidad y otros servicios.

#### Multinube

Consiste en utilizar dos o más proveedores de servicios en la nube, por ejemplo, Azure para infraestructura y AWS para alojar determinadas aplicaciones. La organización debe administrar los recursos y la seguridad de cada proveedor.

!679d9e10-991b-44ce-b597-d7cbf0aff518.png

#### **Azure Arc (Administrador de cloud)**

Es un servicio de Azure que permite administrar y gobernar recursos que se encuentran dentro y fuera de Azure desde Azure. Esto incluye servidores locales (on-premises), recursos en otras nubes como AWS o Google Cloud y entornos híbridos o multinube. Su objetivo es centralizar la administración, aplicar políticas, supervisar los recursos y facilitar su gestión desde un solo lugar.

#### Azure VMware Solution (AVS)

Permite ejecutar cargas de trabajo de VMware en Azure utilizando infraestructura de VMware administrada por Microsoft. De esta forma, las máquinas virtuales pueden seguir funcionando con pocos cambios, facilitando la migración de entornos VMware a Azure y permitiendo aprovechar los servicios de Azure.

## **Descripción del modelo basado en el consumo**

La informática en la nube funciona mediante un modelo basado en el consumo (OpEx): se paga por los recursos y servicios que se utilizan. Esto es diferente de comprar y mantener una infraestructura propia en un centro de datos (CapEx).

#### **CapEx (On-Premises)**

Es el gasto inicial en infraestructura física (servidores, equipos de red, almacenamiento y centro de datos) para operar un entorno local (On-Premises).

#### OpEx (Cloud Computing)

Hace referencia a los gastos operativos, es decir, los costos continuos por el uso de servicios, como los recursos consumidos en la nube. En Cloud Computing, normalmente se paga por lo que se utiliza.

#### **Precios de la nube**

Los proveedores de nube utilizan diferentes modelos de precios, incluido el pago por uso (OpEx). Normalmente, se paga por los servicios que se consumen, lo que ayuda a:

- Planear y administrar los costos operativos.
- Ejecutar la infraestructura de forma más eficaz.
- Escalar a medida que cambian las necesidades de la carga de trabajo.

El proveedor de nube mantiene la infraestructura subyacente, incluida la alimentación, la refrigeración, el hardware y las redes, por lo que la organización puede centrarse en resolver problemas empresariales y ofrecer nuevas funcionalidades a los usuarios.

# Descripción de las ventajas de usar servicios en la nube

En este módulo se presentan las ventajas que la informática en la nube puede ofrecer a una persona o a una organización.

## **Descripción de las ventajas de la alta disponibilidad y la escalabilidad en la nube**

Al implementar una aplicación web en la nube, dos consideraciones importantes son el tiempo de actividad (disponibilidad) y la capacidad de controlar la demanda (escalabilidad).

#### Alta Disponibilidad

La alta disponibilidad se centra en garantizar la máxima disponibilidad de un servicio, incluso cuando se producen interrupciones o eventos que puedan afectar al sistema.

Nota: Al diseñar la solución, se deben tener en cuenta las garantías de disponibilidad del servicio. Azure es un entorno de nube diseñado para ofrecer alta disponibilidad, con garantías de tiempo de actividad que dependen de cada servicio. Estas garantías forman parte de los contratos de nivel de servicio (SLA).

!image.png

#### SLA (Acuerdos de Nivel de Servicio)

Son acuerdos que contienen los términos específicos que definen los compromisos de servicio de Azure. Entre ellos se puede incluir la disponibilidad del servicio y las condiciones que se aplican cuando no se cumplen determinados niveles de servicio.

#### Escalabilidad

La escalabilidad hace referencia a la capacidad de ajustar los recursos para satisfacer la demanda. Si de pronto una aplicación web experimenta un tráfico elevado y los sistemas están sobrecargados, la capacidad de escalar permite agregar más recursos para controlar mejor la demanda.

Nota: Otra ventaja de la escalabilidad es que permite evitar pagar por recursos que no son necesarios. Dado que la nube utiliza modelos basados en el consumo, cuando la demanda baja se pueden reducir los recursos y, por tanto, los costos.

!bc89ecc0-9741-4d64-88f0-8d6fcbbff4b5.jpg

#### Escalado Vertical (Scale Up/Down)

Consiste en aumentar o reducir los recursos de una misma máquina, como la memoria RAM, la CPU, la cantidad de núcleos (cores) o el almacenamiento.

**Ejemplo:** Tienes una máquina virtual con 4 GB de RAM y 2 vCPU. Como necesita más capacidad, la aumentas a 16 GB de RAM y 8 vCPU.

#### Escalado Horizontal (Scale Out/In)

Consiste en agregar o quitar instancias o servidores para distribuir la carga de trabajo. En lugar de hacer una máquina más potente, se utilizan varias máquinas trabajando juntas.

Ejemplo: En lugar de mejorar esa única máquina, agregas **tres máquinas virtuales más** y un balanceador de carga distribuye las solicitudes entre ellas.

**Nota:** Vertical = hacer una máquina más potente / Horizontal = agregar más máquinas.

## Describir las ventajas de confiabilidad y previsibilidad en la nube

La confiabilidad y la previsibilidad son dos ventajas de la nube que ayudan a desarrollar soluciones con mayor confianza.

#### Confiabilidad

!image.png

La confiabilidad es la capacidad de un sistema para recuperarse de errores y seguir funcionando. También es uno de los pilares del **Microsoft Azure Well-Architected Framework**.

Imagina que una aplicación está desplegada en **dos regiones de Azure**. Todos los usuarios acceden normalmente a la **Región 1**. Si esa región sufre una falla, el servicio puede cambiar a la **Región 2**, por lo que los usuarios pueden seguir utilizando la aplicación, siempre que la solución haya sido diseñada para ello.

#### Previsibilidad

!8082c986-93a8-443f-8da3-721411df9906.jpg

La previsibilidad en Azure es la capacidad de anticipar cómo se comportarán los recursos de la nube, tanto en costo como en rendimiento. Esto permite a las organizaciones planificar mejor sus gastos y garantizar que sus aplicaciones tengan los recursos necesarios, sin excederlos ni quedarse cortas.

**Previsibilidad de costos:** Permite estimar cuánto se gastará según el consumo de recursos, ayudando a evitar gastos inesperados.

**Previsibilidad del rendimiento:** Permite conocer cómo pueden responder los recursos según la demanda y ajustar la capacidad cuando sea necesario.

## **Descripción de las ventajas de la seguridad y la gobernanza en la nube**

Independientemente del modelo de nube (IaaS, PaaS, SaaS u On-Premises), la gobernanza y el cumplimiento son partes esenciales de la administración de los recursos.

!image.png

#### Plantilla y estándares

Las plantillas permiten crear recursos de forma repetible siguiendo ciertas reglas. Si una empresa quiere crear 50 VM, en lugar de crearlas una por una, puede utilizar una plantilla con las configuraciones correctas, controles de seguridad, tamaños adecuados y demás parámetros. Esto se hace con el fin de evitar errores al momento de crear los recursos.

#### **Auditoría y cumplimiento**

La nube permite revisar si los recursos cumplen con los estándares establecidos. Si una empresa exige que todos los servidores tengan cifrado activo, por ejemplo, las herramientas de cumplimiento pueden detectar configuraciones que no cumplen con los estándares y políticas establecidos.

#### Actualizaciones automáticas

Dependiendo del modelo de servicio (IaaS, PaaS o SaaS), las actualizaciones pueden ser responsabilidad del cliente o del proveedor.

Ejemplo:

- **IaaS:** El cliente administra el sistema operativo y aplica parches.
- **PaaS:** El proveedor administra gran parte de las actualizaciones de la plataforma.
- **SaaS:** El proveedor se encarga de prácticamente todas las actualizaciones de la aplicación y la infraestructura subyacente.

#### Seguridad según el modelo de nube

La nube permite elegir cuánto control de seguridad quieres tener:

**IaaS**

- Más control para el cliente.
- Cliente administra:
    - Sistema operativo.
    - Aplicaciones.
    - Actualizaciones.
    - Seguridad interna.

**PaaS/SaaS**

- Menos administración para el cliente.
- El proveedor gestiona más elementos automáticamente.

#### Protección contra ataques DDoS

Los proveedores de nube tienen herramientas para proteger los servicios y la infraestructura contra ataques de denegación de servicio distribuido (DDoS).

## **Descripción de las ventajas de la capacidad de administración en la nube**

Una de las principales ventajas de la nube es la administración. Hay diferentes formas de administrar los recursos y el entorno de nube.

!image.png

La administración propia de la nube trata sobre administrar los recursos en la nube. En la nube, puede hacer lo siguiente:

- Escalar automáticamente la implementación de recursos en función de las necesidades.
- Implementar recursos basados en una plantilla preconfigurada, lo que elimina la necesidad de realizar la configuración manual.
- Supervisar la salud de los recursos y reemplazar automáticamente los recursos defectuosos.
- Recibir alertas automáticas basadas en métricas configuradas, por lo que conoce el rendimiento en tiempo real.

#### **Herramientas de administración en la nube**

!management-in-cloud.png

Las herramientas de administración en la nube permiten administrar el entorno de nube y los recursos. Puede administrarlos de las siguientes maneras:

- Mediante un portal web.
- Con una interfaz de línea de comandos.
- Mediante las API.
- Mediante PowerShell.

## **Descripción de las consideraciones de sostenibilidad en la nube**

!image.png

La sostenibilidad en Azure consiste, entre otras cosas, en utilizar los recursos de forma eficiente y evitar desperdiciar capacidad de cómputo. Esto puede beneficiar tanto al cliente, al reducir costos, como al medio ambiente, al reducir el consumo innecesario de energía en los centros de datos.

#### ¿Por qué la nube mejora la eficiencia?

Porque **puedes ajustar los recursos según las necesidades**. Si la demanda aumenta, agregas recursos; si disminuye, los reduces. Así puedes evitar mantener capacidad innecesaria durante largos periodos.

**Ejemplo:**

Una empresa recibe:

- 100 usuarios por la mañana.
- 20 usuarios por la noche.

En Azure puede aumentar los recursos durante el día y reducirlos por la noche, en lugar de mantener la misma capacidad las 24 horas.

### Prácticas que mejoran la eficiencia

#### 1. Reducir recursos cuando baja la demanda

Disminuir CPU, memoria o instancias cuando ya no son necesarias.

**Ejemplo:** Pasar de 10 máquinas virtuales a 3 porque terminó una promoción.

#### 2. Apagar recursos que no se utilizan

Si un recurso no está en uso, se puede apagar o desasignar para evitar costos innecesarios cuando el servicio lo permita.

**Ejemplo:** Un laboratorio de desarrollo se apaga automáticamente por las noches y los fines de semana.

#### 3. Elegir el tamaño adecuado (Right-sizing)

No aprovisionar recursos más grandes de lo necesario.

**Ejemplo:** Si una aplicación funciona bien con **2 vCPU y 8 GB de RAM**, no tiene sentido usar una VM con **16 vCPU y 64 GB de RAM**.

#### 4. Supervisar y optimizar continuamente

Revisar el uso de los recursos para identificar cuáles están infrautilizados o sobredimensionados y ajustarlos.

**Ejemplo:** Azure Monitor muestra que una máquina utiliza solo el 10 % de la CPU durante todo el mes, por lo que puede cambiarse por una más pequeña y económica.

# **Descripción de los tipos de servicio en la nube**

En este módulo se tratan los distintos tipos de servicios en la nube y se comparten algunos de los casos de uso y las ventajas asociadas con cada tipo de servicio.

## **Describir la infraestructura como servicio (IaaS)**

La infraestructura como servicio (IaaS) es la categoría más flexible de servicios en la nube. Proporciona una gran cantidad de control sobre los recursos en la nube. En un modelo IaaS, el proveedor de nube es responsable de mantener el hardware, la conectividad de red a Internet y la seguridad física. El cliente es responsable de otros elementos, incluyendo:

- Instalación, configuración y mantenimiento del sistema operativo.
- Configuración de red.
- Configuración de bases de datos y almacenamiento.

Los escenarios más comunes para usar IaaS son:

- Migración (Lift-and-shift): Consiste en mover una aplicación o servidor desde un centro de datos local a la nube sin realizar cambios importantes. (Ej. Una empresa traslada su servidor de Windows a una máquina virtual en la nube y sigue funcionando prácticamente igual).
- Pruebas y desarrollo: Permite crear y eliminar servidores rápidamente para desarrollar o probar aplicaciones. (Ej. Un desarrollador crea una máquina virtual para probar una aplicación y la elimina cuando termina).

## **Descripción de la plataforma como servicio (PaaS)**

La plataforma como servicio (PaaS) es un punto intermedio entre administrar la infraestructura y utilizar una solución completa de software como servicio. En un entorno PaaS, el proveedor de nube mantiene la infraestructura física, la seguridad física, la conexión a Internet, los sistemas operativos y otros componentes de la plataforma. El cliente se enfoca principalmente en desarrollar y administrar sus aplicaciones y datos.

Los escenarios más comunes para usar PaaS son:

- Marco de desarrollo: Los programadores crean y despliegan aplicaciones utilizando herramientas ya preparadas por el proveedor y se enfocan principalmente en escribir el código. (Ej. Un desarrollador crea una aplicación web usando Azure App Service, sin tener que configurar y administrar el servidor).
- Análisis o inteligencia empresarial: Se utilizan herramientas de la plataforma para analizar datos, encontrar patrones y generar información útil para tomar mejores decisiones. (Ej. Una empresa analiza sus ventas con Azure Synapse Analytics para identificar qué productos se venden más o menos).

## **Descripción del software como servicio (SaaS)**

Software como servicio (SaaS) es el modelo de servicio en la nube más completo desde el punto de vista del producto. Con SaaS, básicamente se utiliza una aplicación completamente desarrollada y administrada por el proveedor. El correo electrónico, el software financiero, las aplicaciones de mensajería y el software de productividad son ejemplos comunes de SaaS.

Los escenarios más comunes para usar SaaS son:

- Correo electrónico y mensajería: Usar aplicaciones en la nube para enviar correos (Ej. Outlook, Gmail).
- Aplicaciones de productividad: Crear y editar documentos, hojas de cálculo o presentaciones en línea (Ej. Microsoft 365, Google Docs).
- Seguimiento de finanzas y gastos: Gestionar ingresos, gastos y presupuestos desde una aplicación en la nube (Ej. QuickBooks).