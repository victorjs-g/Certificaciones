# **Capítulo 3: Conceptos de control de acceso**

Esta documentación será parte de lo aprendido en la certificación **CC de ISC2**. Se tomarán apuntes de conceptos técnicos y algunos ejemplos de estos, tomando en cuenta que es una certificación donde la conceptualización y el pensamiento crítico como gestor de riesgos de IT son muy importantes.

Los módulos que estaremos viendo en el transcurso de la certificación son:

1. Principios de seguridad
2. Conceptos de respuesta a incidentes, continuidad del negocio y recuperación ante desastres
3. Conceptos de control de acceso
4. Seguridad de la red
5. Operaciones de seguridad

Nota: Debemos estar conscientes de que dominamos el tema actual antes de pasar al siguiente. Por eso es importante la documentación y evaluación por módulo.

El orden que veremos en este capítulo se divide de la siguiente manera:

# **Orden del día del capítulo**

- **Módulo 1:** Comprender los conceptos de control de acceso (D3.1, D3.2)
- **Módulo 2:** Comprender los controles de acceso físico (D3.1)
- **Módulo 3:** Comprender los controles de acceso lógico (D3.2)

# Módulo 1: Comprender los conceptos de control de acceso

### **¿Qué es Control de Seguridad?**

Esto hace referencia a las medidas o reglas que establecemos para algo o alguien dentro de una organización. Aquí tenemos el rol de la persona, qué debe hacer, los límites del individuo y demás. Esto se hace con el fin de proteger la seguridad de los datos y todo lo que tenga que ver con la tríada de la CIA.

### **Descripción general de los controles**

Como ya se había hablado, el acceso es el permiso que le damos a alguien para determinar dónde puede entrar y dónde no, y a qué recursos puede acceder una vez dentro.

El acceso se basa en 3 elementos importantes:

**Sujeto:** Un sujeto es una entidad que solicita acceso a un recurso o activo dentro de un sistema. Puede ser un usuario, programa, proceso o dispositivo. El sujeto es quien inicia la solicitud de acceso.

**Objeto:** Un objeto es un recurso o activo al que un sujeto intenta acceder. Es pasivo porque no inicia solicitudes, sino que recibe peticiones de acceso. Puede ser un archivo, impresora, base de datos, puerto o cualquier recurso que ofrezca información o servicios. Por eso se implementan controles de acceso, para limitar qué sujetos pueden acceder a los objetos.

**Reglas:** Las reglas o normas son instrucciones que definen qué sujetos pueden acceder a ciertos objetos o recursos dentro de un sistema. Estas permiten o deniegan el acceso según los permisos del sujeto.

Nota: Los controles físicos y los controles lógicos trabajan juntos para mitigar el riesgo dentro de una empresa.

### **Evaluaciones de controles**

La reducción del riesgo depende de la eficacia del control. Este debe aplicarse a la situación actual y adaptarse a un entorno cambiante. Primero se debe analizar cuál es el objetivo de la empresa y qué se hará en el lugar, y luego realizar la implementación de controles.

### **Defensa en profundidad**

La defensa en profundidad es una estrategia de seguridad que consiste en implementar múltiples capas de controles y protección para dificultar el acceso de un atacante a los sistemas o datos. Estos controles pueden ser físicos, técnicos y administrativos, y buscan proteger la tríada CIA.

### **Principio de privilegio mínimo**

El **Principio de Mínimo Privilegio** es un principio de seguridad que permite solo el acceso mínimo necesario para que los usuarios o programas cumplan su función. A los usuarios se les proporciona acceso únicamente a los sistemas y programas que necesitan para realizar su trabajo o tareas específicas.

Características:

- Acceso limitado a lo necesario.
- Evita el abuso de permisos.
- Aplica a usuarios, procesos y aplicaciones.
- Mejora el control de seguridad.

Ejemplos:

- Usuario solo puede ver archivos, no eliminarlos.

### Gestión de acceso privilegiado (PAM)

Es un conjunto de políticas, procesos y controles que regulan y protegen el acceso de usuarios con privilegios elevados, como administradores o cuentas críticas, definiendo quién puede acceder, a qué sistemas y en qué condiciones.

Nota: **Aprovisionamiento de usuarios** es el proceso de crear, modificar y eliminar cuentas de usuario dentro de una organización, asegurando que cada persona tenga los accesos correctos según su rol.

**Cuentas privilegiadas:** Las **cuentas privilegiadas** son aquellas con permisos superiores a los de los usuarios normales, como las cuentas de administradores.

Medidas de seguridad:

- **Registro y auditoría más detallados** que en cuentas normales, para detectar abusos y permitir revisiones.
- **Controles de acceso más estrictos**, incluyendo MFA y autenticación reforzada. También se puede aplicar acceso **just-in-time** para limitar los privilegios solo cuando se necesiten.
- **Verificación de confianza más profunda**, como antecedentes, acuerdos de confidencialidad y revisiones periódicas.
- **Auditorías frecuentes** para monitorear la actividad de estas cuentas.

### **Segregación de deberes**

La segregación de deberes (SoD) o separación de funciones es un principio de seguridad que establece que ninguna persona debe tener control completo de un proceso crítico de principio a fin. En su lugar, el proceso se divide en etapas y cada una es realizada o aprobada por personas diferentes.

### Control dual

Es una implementación de la segregación de funciones donde dos personas son necesarias para ejecutar una acción crítica. Para cumplir con esta regla, ambas deben estar presentes para que la acción sea ejecutada.

Ejemplo:

- En un banco, una bóveda tiene dos cerraduras.
- Cada persona conoce solo una combinación.
- Ninguna puede abrirla sola → se requiere cooperación obligatoria.

### **Personal autorizado versus personal no autorizado**

- **Usuario autorizado:** Su identidad fue verificada y **tiene permisos** para acceder a sistemas o áreas específicas según su rol.
- **Usuario no autorizado:** No tiene permisos (o no está verificado), por lo que **el sistema le niega el acceso**.

**Idea clave:** autenticación = quién eres; autorización = qué puedes hacer.

### Aprovisionamiento de cuentas (resumen breve)

Concepto: Es un proceso de gestión de identidad para crear y gestionar el acceso a recursos y sistemas de información.

- **Usuario nuevo (onboarding):** RR. HH. solicita la creación de la cuenta a TI o Seguridad. Se asignan accesos según el rol y las políticas, y se aprueban accesos privilegiados si aplica.
- **Cambio de rol (ascenso o traslado):** Se ajustan los permisos del usuario (más o menos privilegios) según su nueva función.
- **Salida del empleado (offboarding):** Se eliminan o desactivan los accesos antes o inmediatamente después de su salida para evitar accesos no autorizados o filtración de datos.
- **Licencia de largo tiempo:** Se puede desactivar temporalmente la cuenta del personal que se ausenta durante un largo período, evitando accesos no autorizados y manteniendo un mayor control.

Nota: El aprovisionamiento de usuarios asegura que cada persona tenga solo los accesos correctos durante todo su ciclo de vida en la empresa.

# **Módulo 2: Comprender los controles de acceso físico**

### **¿Qué son los controles de seguridad física?**

Los controles de seguridad física son medidas tangibles y ambientales diseñadas para **proteger instalaciones, personas, equipos y activos de información** mediante la **prevención, detección, retraso o restricción del acceso no autorizado** a áreas físicas o recursos críticos de una organización. Incluyen mecanismos como cámaras de vigilancia, guardias de seguridad, cerraduras, rejas, torniquetes, sensores de movimiento y sistemas de control de acceso.

### **¿Por qué tener controles de seguridad física?**

Las medidas de protección de controles físicos, como rejas, cámaras de seguridad, guardias y muchas otras, ayudan a evitar que intrusos accedan a lugares restringidos. Esto nos ayuda a proteger nuestra tríada CIA, la infraestructura y la seguridad de las personas.

### **Tipos de controles de acceso físico**

Sistemas de credencial y puerta de entrada: Esto es un sistema que autentica y autoriza al usuario y valida en su base de datos que el usuario esté autorizado para ingresar a un lugar. Por ejemplo, un torniquete puede permitir el acceso cuando el gerente presenta su tarjeta; sin embargo, un parqueador no puede acceder a la oficina de TI.

Una gama de tipos de tarjetas permite que el sistema se utilice en una variedad de entornos. Estas tarjetas incluyen:

- código de barras
- banda magnética
- proximidad
- inteligente
- híbrido

Crime Prevention Through Environmental Design (CPTED): CPTED es un enfoque de seguridad que busca prevenir el delito mediante el diseño del entorno físico, aumentando la visibilidad, el control natural y la sensación de vigilancia, de forma que el crimen sea más difícil, riesgoso o detectable.

- Aumenta la **visibilidad** (menos lugares ocultos).
- Mejora la **vigilancia natural** (que otros puedan ver lo que pasa).
- Refuerza el **control de accesos físicos**.
- Genera **territorialidad** (claridad de espacios públicos vs. privados).
- Reduce oportunidades para el crimen.

### **Biometría**

La biometría es un control de acceso que autentica a una persona utilizando características únicas de su cuerpo o comportamiento, comparándolas con una plantilla almacenada.

Tiene dos procesos principales: **inscripción**, donde se registran los datos biométricos y se crea una plantilla, y **verificación**, donde el sistema compara la muestra presentada con la información almacenada para permitir o negar el acceso.

Existen dos tipos: la **biometría fisiológica**, basada en características físicas como huella, iris o rostro, y la **biometría conductual**, que analiza patrones de comportamiento como la voz, la firma o la forma de teclear. Esto ayuda a reducir el riesgo de suplantación de identidad.

### **Vigilancia**

La vigilancia es un tipo de control físico de seguridad que se enfoca en observar, detectar y registrar actividades dentro de un entorno para identificar comportamientos sospechosos o incidentes de seguridad.

Cámaras de seguridad: Son sistemas de video utilizados para monitorear y grabar actividades en un área específica. Permiten la supervisión en tiempo real y sirven como evidencia posterior en caso de incidentes de seguridad.

Registro (logs / bitácoras): Es el registro sistemático de eventos y actividades dentro de un sistema o instalación, como accesos, salidas o incidentes. Se utiliza para auditoría, trazabilidad y análisis forense.

Alarmas: Son mecanismos que detectan condiciones anormales o intentos de intrusión y generan alertas sonoras, visuales o digitales para notificar al personal de seguridad o a los sistemas de monitoreo.

Guardia de seguridad: Es personal humano encargado de vigilar, controlar accesos y responder a incidentes de seguridad. También realiza rondas, verifica identidades y aplica protocolos de emergencia.

### **Módulo 3: Comprender los controles de acceso lógico**

Como sabemos, los controles físicos son implementaciones físicas para alertar, prevenir o proteger. Los controles lógicos son mecanismos electrónicos que limitan el acceso de alguien a un sistema y, en algunas ocasiones, a activos físicos.

Los tipos de controles lógicos incluyen:

- Contraseña.
- Biometría (implementada en celulares o laptops).
- Lectores de tarjetas/fichas conectados a un sistema.

Este tipo de herramientas lógicas nos ayuda a darle una capa de seguridad extra a los activos, en caso de que el control de acceso físico haya fallado.

### Tipos De Controles Lógicos

#### DAC: Control de acceso discrecional

Control de acceso discrecional (DAC): DAC es un modelo de control de acceso donde el propietario de un recurso tiene la capacidad de asignar y modificar permisos (leer, escribir, ejecutar o borrar) sobre ese recurso para otros usuarios.

Ejemplo:

- Víctor crea un archivo → Víctor es el propietario.
- Víctor decide:
    - María puede leerlo.
    - Pedro puede editarlo.
    - Ana no puede verlo.

Eso es DAC. Básicamente, la función que permite al propietario asignar permisos es DAC.

#### MAC: Control de acceso obligatorio

Control de acceso obligatorio (MAC): MAC es un modelo de acceso donde las políticas se configuran de manera central y luego se aplican de acuerdo con reglas y etiquetas de seguridad. Los usuarios no pueden modificar libremente estos permisos.

#### **Control de acceso basado en roles (RBAC)**

**El control de acceso basado en roles (RBAC)** configura los permisos de usuario basados en roles. Cada rol representa a usuarios con permisos similares o idénticos. En lugar de asignar permisos individualmente a cada usuario, los permisos se asignan a un rol y luego los usuarios reciben los permisos correspondientes a ese rol.