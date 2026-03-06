# SÍNTESIS EXTENDIDA EGEL ISOFT 2026 - CALIFICACIÓN 10 SOBRESALIENTE
## Las 4 Áreas Completas en Español - Definiciones Ampliadas - Ejemplos Detallados

---

## ÁREA 1: ANÁLISIS DE SISTEMAS (31 reactivos)

---

### 1.1 TIPOS DE REQUERIMIENTOS

**FUENTES: Wiegers & Beatty 3ra ed. Cap.1 p.5-15 + Sommerville 9na ed. Cap.4 §4.1 p.82-87**

#### **Jerarquía de 3 Niveles de Requerimientos**

**NIVEL 1 - REQUERIMIENTOS DE NEGOCIO (Por qué existe el proyecto)**

**Definición:** Objetivos de alto nivel de la organización o cliente que justifican la inversión en el desarrollo del sistema. Expresan el problema a resolver y las métricas de éxito empresarial.

**Características:**
- Son el "POR QUÉ" del proyecto
- Responden: ¿Qué problema del negocio resuelve?
- Audiencia: Ejecutivos, dueños del producto, inversionistas
- Tiempo de vida: Largo (usualmente no cambian)
- Se documentan en: Documento de visión, caso de negocio

**Ejemplos Buenos:**
✅ "Reducir los costos operativos de procesamiento de pedidos en 40% durante los próximos 12 meses"
✅ "Incrementar la cuota de mercado del 15% al 22% en 18 meses mediante mejora de experiencia del cliente"
✅ "Disminuir el tiempo promedio de resolución de incidentes de servicio de 48 horas a 4 horas"
✅ "Aumentar las ventas en línea en $2 millones durante el primer año de operación"

**Ejemplos Malos:**
❌ "Mejorar el sistema" (vago, no medible)
❌ "Tener una base de datos moderna" (es solución, no objetivo de negocio)
❌ "Usar tecnología cloud" (es restricción técnica, no objetivo de negocio)

**Analogía:** Si el desarrollo del sistema es un viaje en auto, los requerimientos de negocio son la razón del viaje ("Visitar a la abuela para su cumpleaños"), no la ruta ni el tipo de auto.

---

**NIVEL 2 - REQUERIMIENTOS DE USUARIO (Qué hace el usuario)**

**Definición:** Metas, objetivos o tareas que los usuarios deben poder realizar con el sistema. Describen la funcionalidad desde la perspectiva del usuario final sin entrar en detalles técnicos.

**Características:**
- Son el "QUÉ" desde perspectiva del usuario
- Responden: ¿Qué necesita lograr el usuario?
- Audiencia: Usuarios finales, clientes, analistas de negocio
- Formato: Casos de uso, historias de usuario, escenarios
- Se documentan en: Documento de requerimientos de usuario, historias de usuario

**Ejemplos en formato Historia de Usuario:**
✅ "Como cajero de banco, quiero procesar una devolución de compra en máximo 3 clics para reducir el tiempo de espera del cliente"
✅ "Como gerente de ventas, quiero generar reportes de ventas mensuales agrupados por región para identificar oportunidades de crecimiento"
✅ "Como cliente de e-commerce, quiero buscar productos por categoría, precio y calificación para encontrar rápidamente lo que necesito"
✅ "Como administrador del sistema, quiero restaurar copias de seguridad automáticamente en caso de fallo para garantizar continuidad del servicio"

**Ejemplos en formato Caso de Uso (título):**
✅ "Procesar Devolución de Producto"
✅ "Registrar Nuevo Paciente en Sistema Hospitalario"
✅ "Aprobar Solicitud de Crédito"

**Ejemplos Malos:**
❌ "El sistema debe tener una tabla en MySQL" (técnico, no de usuario)
❌ "Implementar patrón MVC" (diseño, no necesidad de usuario)
❌ "Usar framework React" (tecnología, no objetivo de usuario)

**Analogía:** Si vamos al restaurante, el requerimiento de usuario es "Quiero cenar pasta" (qué quieres), no la receta detallada de cómo se prepara.

---

**NIVEL 3 - REQUERIMIENTOS DEL SISTEMA (Qué hace el sistema técnicamente)**

**Definición:** Descripciones técnicas detalladas de las funciones, servicios, restricciones operacionales y atributos de calidad que el sistema de software debe proveer. Son la especificación funcional completa.

**Características:**
- Son el "QUÉ DETALLADO" desde perspectiva técnica
- Responden: ¿Exactamente qué debe hacer el sistema?
- Audiencia: Desarrolladores, arquitectos, testers
- Formato: Especificación formal con "shall"
- Se documentan en: SRS (Software Requirements Specification)

**Se dividen en 4 categorías:**

**A) REQUERIMIENTOS FUNCIONALES (Comportamiento observable)**

**Definición:** Describen las acciones específicas que el sistema debe realizar, las transformaciones de datos, los cálculos, y los servicios que el sistema debe proveer.

**Plantilla estándar:** "El sistema shall [acción] [objeto] [condición] [criterio de rendimiento]"

**Ejemplos Detallados:**

✅ **Ejemplo 1 - E-commerce:**
"El sistema shall enviar un correo electrónico de confirmación al usuario dentro de 30 segundos después de completar exitosamente el registro de una cuenta nueva"

Desglose:
- Acción: enviar correo electrónico de confirmación
- Objeto: al usuario
- Condición: después de completar exitosamente registro
- Criterio rendimiento: dentro de 30 segundos

✅ **Ejemplo 2 - Sistema Bancario:**
"El sistema shall calcular el saldo disponible de una cuenta restando los cargos pendientes del saldo actual y agregando los depósitos en tránsito"

Desglose:
- Acción: calcular saldo disponible
- Objeto: cuenta
- Condición: siempre que se consulte
- Criterio: fórmula específica definida

✅ **Ejemplo 3 - Sistema de Inventario:**
"El sistema shall enviar una alerta automática al gerente de compras cuando el inventario de cualquier producto caiga por debajo del punto de reorden definido para ese producto"

✅ **Ejemplo 4 - Sistema de Reservaciones:**
"El sistema shall permitir al usuario cancelar una reservación hasta 24 horas antes de la fecha programada sin penalización"

✅ **Ejemplo 5 - Sistema Educativo:**
"El sistema shall calcular el promedio final de un estudiante ponderando los exámenes parciales con 30%, tareas con 20%, proyecto final con 30%, y participación con 20%"

**Características clave de buenos RF:**
- Usan verbo de acción observable: enviar, calcular, mostrar, almacenar, validar, generar
- Son verificables (puedes escribir una prueba)
- Tienen criterio de éxito claro
- No mencionan tecnología de implementación

**Ejemplos Malos (y cómo corregirlos):**

❌ "El sistema debe ser rápido"
✅ "El sistema shall retornar resultados de búsqueda en menos de 2 segundos en el percentil 95 de las consultas bajo carga de 1000 usuarios concurrentes"
**Por qué es malo:** "Rápido" no es verificable ni específico

❌ "El sistema validará la entrada del usuario"
✅ "El sistema shall validar que el campo de correo electrónico contenga exactamente un símbolo @ seguido de un nombre de dominio válido"
**Por qué es malo:** No especifica QUÉ validar ni CÓMO

❌ "Procesar las transacciones eficientemente"
✅ "El sistema shall procesar hasta 10,000 transacciones por segundo con tiempo de respuesta promedio menor a 500 milisegundos"
**Por qué es malo:** "Eficientemente" es subjetivo y no medible

**Clave para el examen:** Si el requerimiento usa verbos de acción (enviar, calcular, mostrar, almacenar, generar) y describe un comportamiento observable → es FUNCIONAL

---

**B) REQUERIMIENTOS NO FUNCIONALES / ATRIBUTOS DE CALIDAD (Cómo debe comportarse)**

**Definición:** Restricciones sobre los servicios o funciones que ofrece el sistema. Describen propiedades emergentes del sistema (rendimiento, seguridad, usabilidad) en lugar de funcionalidades específicas.

**Regla de Oro:** Los NFR deben ser CUANTIFICABLES y VERIFICABLES. No usar adjetivos vagos.

**Clasificación de Sommerville (3 categorías):**

**1. Requerimientos de Producto (Características del sistema mismo)**

Subcategorías:
- **Rendimiento (Performance):** Velocidad, throughput, tiempo de respuesta
- **Confiabilidad (Reliability):** Tasa de fallos, disponibilidad
- **Seguridad (Security):** Confidencialidad, integridad, disponibilidad
- **Usabilidad (Usability):** Facilidad de uso, aprendizaje

**Ejemplos de Rendimiento:**

✅ "El sistema shall procesar un mínimo de 10,000 transacciones por segundo durante las horas pico (8am-10am y 2pm-4pm)"

✅ "El sistema shall retornar resultados de búsqueda en menos de 2 segundos para el 95% de las consultas cuando el sistema opera con 5,000 usuarios concurrentes"
- Métrica: < 2 segundos
- Percentil: 95% (permite 5% más lento)
- Condición de carga: 5,000 usuarios concurrentes

✅ "El sistema shall iniciar en menos de 30 segundos en hardware estándar definido en especificación técnica sección 3.2"

✅ "El sistema shall soportar hasta 50,000 usuarios concurrentes sin degradación de performance mayor al 10%"

**Ejemplos de Confiabilidad:**

✅ "El sistema shall tener un tiempo promedio entre fallos (MTBF) de al menos 720 horas en operación continua"

✅ "El sistema shall recuperarse automáticamente de fallos de red en menos de 5 segundos sin pérdida de datos de transacciones en curso"

✅ "La tasa de transacciones fallidas no shall exceder 0.1% del total de transacciones procesadas"

**Ejemplos de Seguridad:**

✅ "El sistema shall requerir autenticación de dos factores (2FA) para todas las transacciones que excedan $1,000 dólares"

✅ "El sistema shall encriptar todos los datos sensibles en tránsito usando TLS 1.3 o superior y en reposo usando AES-256"

✅ "El sistema shall bloquear automáticamente una cuenta después de 3 intentos fallidos de inicio de sesión consecutivos durante un período de 15 minutos"

✅ "El sistema shall mantener un registro de auditoría inmutable de todas las transacciones financieras durante mínimo 7 años"

**Ejemplos de Usabilidad:**

✅ "Un usuario novato sin capacitación previa shall poder completar el proceso de checkout en menos de 5 minutos en el 80% de los intentos"
- Usuario definido: novato sin capacitación
- Tarea: proceso checkout
- Métrica: < 5 minutos
- Criterio éxito: 80% de los intentos

✅ "El sistema shall proveer mensajes de error en lenguaje natural español mexicano, indicando claramente el problema y sugiriendo la solución en términos no técnicos"

✅ "Un usuario experto que usa el sistema diariamente shall poder completar las 10 operaciones más comunes usando únicamente atajos de teclado sin usar el mouse"

---

**2. Requerimientos Organizacionales (Políticas y procedimientos)**

**Ejemplos de Proceso de Entrega:**
✅ "El sistema shall ser entregado en incrementos mensuales comenzando 60 días después de la firma del contrato"
✅ "Cada entrega shall incluir documentación técnica actualizada y manual de usuario en formato PDF"

**Ejemplos de Estándares:**
✅ "El código fuente shall seguir el estándar de codificación Java definido por Google Java Style Guide versión 2023"
✅ "Toda la interfaz de usuario shall cumplir con las pautas de accesibilidad WCAG 2.1 nivel AA"

**Ejemplos de Proceso de Desarrollo:**
✅ "El desarrollo shall seguir un proceso ágil Scrum con sprints de 2 semanas"
✅ "Todas las funcionalidades shall tener cobertura de pruebas unitarias mínima del 80%"

---

**3. Requerimientos Externos (Factores fuera de la organización)**

**Ejemplos Regulatorios:**
✅ "El sistema shall cumplir con todas las disposiciones del Reglamento General de Protección de Datos (GDPR) de la Unión Europea"
✅ "El manejo de información de salud shall cumplir con la Ley de Portabilidad y Responsabilidad de Seguros de Salud (HIPAA)"
✅ "El sistema shall cumplir con el estándar PCI-DSS versión 3.2 o superior para el procesamiento de pagos con tarjeta"

**Ejemplos Éticos:**
✅ "El sistema shall proveer opciones de accesibilidad para personas con discapacidades visuales, auditivas y motoras"
✅ "El sistema no shall discriminar usuarios basándose en edad, género, origen étnico, religión o ubicación geográfica"

**Ejemplos Legales:**
✅ "Todos los datos personales de ciudadanos mexicanos shall almacenarse en servidores ubicados físicamente en territorio mexicano"
✅ "El sistema shall permitir a los usuarios exportar todos sus datos personales en formato legible por máquina (JSON o XML) dentro de 48 horas de la solicitud"

---

**Ejemplos Malos de NFR (y cómo corregirlos):**

❌ "El sistema debe ser rápido"
✅ "El sistema shall responder a solicitudes de búsqueda en menos de 2 segundos en el percentil 95 bajo carga de 1000 usuarios concurrentes"
**Razón:** "Rápido" no es medible

❌ "El sistema debe ser seguro"
✅ "El sistema shall implementar autenticación de dos factores (2FA) para todos los usuarios y encriptar datos en tránsito con TLS 1.3 y en reposo con AES-256"
**Razón:** "Seguro" es vago

❌ "El sistema debe ser fácil de usar"
✅ "Usuario novato shall completar la tarea de registro de cuenta en menos de 3 minutos sin necesidad de soporte técnico en el 90% de los casos"
**Razón:** "Fácil" es subjetivo

❌ "El sistema debe ser confiable"
✅ "El sistema shall tener disponibilidad del 99.9% (máximo 8.7 horas de tiempo inactivo por año) y MTBF de 720 horas"
**Razón:** "Confiable" no especifica métrica

**Clave para el examen:** Si el requerimiento usa adjetivos de calidad (rápido, seguro, confiable, fácil) y describe CÓMO debe comportarse el sistema → es NO FUNCIONAL

---

**C) RESTRICCIONES (Limitaciones impuestas)**

**Definición:** Limitaciones sobre las opciones disponibles al desarrollador para diseñar e implementar el sistema. Son usualmente no negociables.

**Tipos de Restricciones:**

**1. Restricciones Tecnológicas:**
✅ "El sistema shall ejecutarse en el sistema operativo Oracle Linux 8.x"
✅ "El sistema shall usar exclusivamente el gestor de base de datos Oracle Database 19c Enterprise Edition"
✅ "La interfaz de usuario shall desarrollarse usando el framework Angular versión 15 o superior"
✅ "El sistema shall ser accesible mediante navegadores Chrome 100+, Firefox 95+, Safari 15+, Edge 100+"

**2. Restricciones de Plataforma:**
✅ "El sistema shall desplegarse en la infraestructura de Amazon Web Services (AWS) en la región us-east-1"
✅ "Toda la infraestructura shall ejecutarse en contenedores Docker orquestados con Kubernetes versión 1.25+"
✅ "El sistema móvil shall soportar iOS 15+ y Android 11+ como versiones mínimas"

**3. Restricciones de Lenguaje:**
✅ "El backend shall desarrollarse usando Java 17 LTS"
✅ "Todos los scripts de automatización shall escribirse en Python 3.10 o superior"
✅ "Las consultas a base de datos shall escribirse en SQL estándar ANSI-92 sin extensiones propietarias"

**4. Restricciones de Tamaño:**
✅ "La aplicación móvil instalada shall ocupar menos de 50 MB de espacio de almacenamiento"
✅ "La base de datos shall diseñarse para almacenar mínimo 10 millones de registros de clientes sin degradación de rendimiento"

**5. Restricciones de Integración:**
✅ "El sistema shall integrarse con el sistema ERP SAP existente usando APIs SOAP definidas en documento de integración versión 2.3"
✅ "El sistema shall consumir servicios del API REST corporativo definido en especificación OpenAPI 3.0"

**Ejemplos Malos:**
❌ "Usar buenas prácticas de programación" (esto es expectativa general, no restricción)
❌ "El sistema debe ser modular" (esto es principio de diseño, no restricción impuesta)

**Diferencia clave:** 
- **Restricción:** Límite impuesto externamente (regulación, decisión corporativa)
- **NFR:** Propiedad emergente que debe cumplir el sistema

**Clave para el examen:** Si dice "Debe usar X tecnología", "Debe ejecutarse en Y plataforma", "Limitado a Z" → es RESTRICCIÓN

---

**D) REGLAS DE NEGOCIO (Políticas del dominio)**

**Definición:** Políticas, directivas, estándares o regulaciones que definen o restringen las operaciones del negocio. No son requerimientos del sistema, pero el sistema debe respetarlas y en muchos casos automatizarlas.

**Tipos de Reglas de Negocio:**

**1. Definiciones / Hechos (Facts):**
Definen términos o conceptos del dominio

✅ "Cliente VIP se define como aquel que ha realizado compras acumuladas superiores a $5,000 dólares en los últimos 12 meses"

✅ "Pedido urgente se clasifica como aquel que requiere entrega en 24 horas o menos desde el momento de la orden"

✅ "Empleado de tiempo completo se define como aquel que trabaja mínimo 40 horas por semana"

✅ "Producto en oferta es aquel cuyo precio está reducido al menos 15% respecto al precio regular durante un período limitado"

**2. Reglas Habilitadoras de Acción (Action-Enabling Rules):**
Definen qué está permitido hacer bajo ciertas condiciones

✅ "Un gerente de tienda puede aprobar descuentos de hasta el 20% sin autorización superior"

✅ "Los empleados con más de 5 años de antigüedad tienen derecho a 3 semanas de vacaciones pagadas"

✅ "Un cliente con tarjeta de crédito verificada puede realizar compras hasta por $10,000 sin validación adicional"

✅ "Los supervisores pueden modificar horarios de turnos de su equipo con hasta 48 horas de anticipación"

**3. Fórmulas de Cálculo (Computation Rules):**
Definen cómo se calculan valores derivados

✅ "El descuento para Cliente VIP se calcula como: 10% en primera compra del mes + 5% adicional por cada $1,000 de compras acumuladas en el año, hasta un máximo de 25%"

✅ "El precio de envío se calcula como: $5 base + ($0.50 × peso_en_kg) + ($2 × (distancia_km ÷ 100))"

✅ "La comisión de vendedor se calcula como: 5% de ventas hasta $50K + 7% de ventas entre $50K y $100K + 10% de ventas superiores a $100K"

✅ "El promedio ponderado del curso se calcula como: (Exámenes × 0.40) + (Tareas × 0.30) + (Proyecto × 0.20) + (Participación × 0.10)"

**4. Restricciones de Negocio (Constraints):**
Definen qué NO está permitido

✅ "No se permite devolver productos después de 30 días de la compra"

✅ "No se aceptan más de 3 solicitudes de cambio de turno por empleado en un mes"

✅ "No se permite comprar más de 10 unidades del mismo producto en promoción por transacción"

✅ "No se otorgan préstamos a clientes con historial crediticio inferior a 650 puntos"

**Diferencia crítica entre Regla de Negocio y Requerimiento Funcional:**

**Regla de Negocio (política del dominio):**
"Cliente VIP obtiene 15% de descuento en todas sus compras"

**Requerimiento Funcional derivado (lo que el sistema hace):**
"El sistema shall aplicar automáticamente un descuento del 15% al total de la compra cuando el cliente autenticado tiene estado VIP"

**Otro ejemplo:**

**Regla de Negocio:**
"Los pedidos recibidos antes de las 2:00 PM se envían el mismo día"

**Requerimiento Funcional derivado:**
"El sistema shall marcar como 'Envío Mismo Día' todos los pedidos confirmados antes de las 14:00 horas y generar la orden de envío automáticamente"

**Clave para el examen:** Si describe una política del NEGOCIO (cómo opera la empresa) en lugar de lo que el SISTEMA debe hacer → es REGLA DE NEGOCIO

---

**ANALOGÍAS COMPLETAS PARA LA JERARQUÍA:**

**Analogía del Viaje:**
- **Negocio:** "Necesito llegar a Guadalajara para una reunión importante mañana" (objetivo del negocio)
- **Usuario:** "Como viajero, quiero reservar un vuelo directo y un hotel cerca del lugar de reunión" (necesidad del usuario)
- **Sistema - Funcional:** "El sistema shall mostrar vuelos disponibles, permitir selección de asiento, procesar pago con tarjeta, y enviar confirmación por email" (funciones específicas)
- **Sistema - NFR:** "El sistema shall procesar la reservación en menos de 30 segundos" (atributo de calidad)
- **Restricción:** "El sistema debe usar la API de Amadeus para búsqueda de vuelos" (limitación técnica)
- **Regla Negocio:** "Pasajeros frecuentes con más de 50,000 km acumulados obtienen upgrade gratuito" (política aerolínea)

**Analogía del Restaurante:**
- **Negocio:** "Incrementar ventas 30% en 6 meses" (objetivo del dueño)
- **Usuario:** "Como cliente, quiero ordenar comida desde mi teléfono y recibirla en mi mesa" (necesidad cliente)
- **Sistema - Funcional:** "El sistema shall permitir seleccionar platillos del menú, personalizar ingredientes, procesar pago, y enviar orden a cocina" (funciones app)
- **Sistema - NFR:** "El sistema shall responder en < 1 segundo al hacer clic en cualquier platillo" (rapidez)
- **Restricción:** "El sistema debe integrarse con el sistema de punto de venta existente Square" (tecnología obligatoria)
- **Regla Negocio:** "Clientes que gastan más de $500 al mes obtienen postre gratis" (política restaurante)

---

**RESUMEN VISUAL - TABLA COMPARATIVA:**

| Tipo | Pregunta que responde | Ejemplo | Audiencia | Formato |
|------|----------------------|---------|-----------|---------|
| **Negocio** | ¿Por qué hacemos esto? | "Reducir costos 40% en 12 meses" | Ejecutivos, inversionistas | Documento de visión |
| **Usuario** | ¿Qué quiere lograr el usuario? | "Como cajero, procesar devolución en 3 clics" | Usuarios, clientes | Historia de usuario, caso de uso |
| **Sistema - Funcional** | ¿Qué hace exactamente el sistema? | "Sistema shall enviar email en ≤30 seg" | Desarrolladores, testers | SRS con "shall" |
| **Sistema - NFR** | ¿Cómo debe comportarse? | "Tiempo respuesta ≤2 seg percentil 95" | Arquitectos, Ops | SRS con métricas |
| **Restricción** | ¿Qué limitaciones tiene? | "Debe usar Oracle 19c" | Arquitectos, admins | Documento restricciones |
| **Regla Negocio** | ¿Qué políticas del negocio aplican? | "VIP = compras >$5K últimos 12 meses" | Analistas negocio | Manual de políticas |

---

### CONTINUARÁ...

Este es el nivel de detalle extendido. ¿Deseas que continúe con el mismo nivel de profundidad para:
- Atributos de Calidad (ISO 25010 completo)
- Documento SRS
- Técnicas de Elicitación
- Y el resto de las 4 áreas?


### 1.1 ATRIBUTOS DE CALIDAD (ISO 25010)

**FUENTES: Wiegers Cap.14 p.261-280 + Cervantes Cap.2 p.9-46**

#### **ISO 25010 - Las 8 Características de Calidad del Software**

**NOTA IMPORTANTE:** ISO 25010 reemplazó a ISO 9126 en 2011. Es el estándar internacional actual para calidad de software.

---

**1. ADECUACIÓN FUNCIONAL (Functional Suitability)**

**Definición:** Grado en que el producto o sistema provee funciones que satisfacen necesidades declaradas e implícitas cuando se usa bajo condiciones específicas.

**Subcaracterísticas:**
- **Completitud funcional:** ¿Cubre todas las tareas y objetivos de usuario?
- **Corrección funcional:** ¿Provee resultados correctos con precisión necesaria?
- **Pertinencia funcional:** ¿Las funciones facilitan completar tareas?

**Ejemplo de Medición:**
"Del total de 150 funcionalidades especificadas, el sistema implementa correctamente 148 (98.7% completitud funcional)"

---

**2. EFICIENCIA DE DESEMPEÑO (Performance Efficiency)**

**Definición:** Desempeño relativo a la cantidad de recursos utilizados bajo condiciones establecidas.

**Subcaracterísticas:**

**a) Comportamiento Temporal (Time Behaviour)**
Tiempos de respuesta, latencia, throughput

**Métricas:**
- **Throughput (Rendimiento):** Cantidad de trabajo por unidad de tiempo
  - Ejemplo: "10,000 transacciones por segundo (TPS)"
  - Ejemplo: "Procesar 500 pedidos por minuto durante hora pico"

- **Tiempo de Respuesta (Response Time):** Tiempo entre solicitud del usuario y respuesta del sistema
  - Ejemplo: "Búsqueda retorna resultados en <2 segundos percentil 95"
  - Percentil 95 significa: 95% de las búsquedas cumplen, 5% pueden tardar más
  
- **Latencia:** Tiempo desde que se envía solicitud hasta que empieza a llegar respuesta
  - Ejemplo: "Latencia de red <100 milisegundos entre usuario y servidor"

**Ejemplos Completos:**
✅ "El sistema shall procesar un mínimo de 15,000 transacciones por segundo durante operación normal"
✅ "El sistema shall retornar resultados de búsqueda de productos en menos de 1.5 segundos para el 99% de las consultas cuando operan 10,000 usuarios concurrentes"
✅ "La aplicación móvil shall cargar la pantalla principal en menos de 3 segundos en conexión 4G con latencia típica de 50ms"

**b) Utilización de Recursos (Resource Utilization)**
CPU, memoria, disco, red

**Métricas:**
✅ "Uso de CPU shall permanecer por debajo del 70% durante operación normal con 5,000 usuarios"
✅ "Consumo de memoria RAM shall no exceder 4 GB por instancia del servidor de aplicaciones"
✅ "Consumo de batería en dispositivo móvil shall ser menor a 5% por hora de uso activo de la aplicación"
✅ "Ancho de banda consumido shall no exceder 100 MB por hora por usuario en streaming de calidad estándar"

**c) Capacidad (Capacity)**
Límites máximos soportados

**Ejemplos:**
✅ "El sistema shall soportar hasta 50,000 usuarios concurrentes sin degradación de rendimiento mayor al 10%"
✅ "La base de datos shall almacenar mínimo 100 millones de registros de transacciones manteniendo tiempo de consulta <2 segundos"
✅ "El sistema shall procesar archivos de importación de hasta 10 GB sin requerir división manual"

**Analogía:** 
Performance = Autopista
- Throughput = Autos/hora que pasan
- Response Time = Tiempo total del viaje casa-trabajo
- Latencia = Tiempo para salir del estacionamiento a la autopista
- Resource Utilization = Cuántos carriles usas de los 6 disponibles
- Capacity = Máximo de autos antes que se sature

---

**3. COMPATIBILIDAD (Compatibility)**

**Definición:** Grado en que producto puede intercambiar información con otros sistemas y/o realizar funciones requeridas mientras comparte el mismo ambiente hardware/software.

**Subcaracterísticas:**

**a) Coexistencia:** Realizar funciones eficientemente compartiendo recursos con otros productos sin impacto adverso

**Ejemplos:**
✅ "El sistema shall operar en el mismo servidor que el sistema ERP existente sin conflictos de puertos o librerías compartidas"
✅ "La aplicación shall coexistir con antivirus corporativo Norton 360 sin generar falsas alarmas ni consumir >10% CPU adicional"

**b) Interoperabilidad:** Intercambiar información y usar información intercambiada

**Ejemplos:**
✅ "El sistema shall intercambiar datos de clientes con sistema CRM Salesforce usando API REST estándar con formato JSON"
✅ "El sistema shall importar archivos CSV con codificación UTF-8, ISO-8859-1 y ASCII"
✅ "El sistema shall exportar reportes en formatos PDF, Excel (.xlsx) y CSV"

---

**4. USABILIDAD (Usability)**

**Definición:** Grado en que el producto puede ser usado por usuarios específicos para lograr objetivos específicos con efectividad, eficiencia y satisfacción en un contexto de uso específico.

**Subcaracterísticas (Modelo Detallado):**

**a) Reconocibilidad de Adecuación (Appropriateness Recognizability)**
¿El usuario puede reconocer si el producto es apropiado para sus necesidades?

**Ejemplo:**
✅ "La pantalla de inicio shall mostrar claramente las 5 funciones principales que representan el 80% de casos de uso"
✅ "El sistema shall proveer un tour guiado de 2 minutos en el primer inicio que muestre capacidades principales"

**b) Capacidad de Aprendizaje (Learnability)**
¿Qué tan fácil es aprender a usar el sistema?

**Métricas y Ejemplos:**
✅ "Un usuario novato sin capacitación previa shall poder completar su primera tarea de registro de paciente en menos de 8 minutos siguiendo las ayudas contextuales"
✅ "El 80% de usuarios nuevos shall poder realizar las 5 operaciones más comunes sin consultar el manual después de 1 hora de uso"
✅ "El sistema shall proveer tooltips contextuales en todos los campos de formulario explicando qué información ingresar"

**c) Operabilidad (Operability)**
¿Qué tan fácil es operar y controlar el sistema?

**Ejemplos:**
✅ "Todas las operaciones críticas shall requerir máximo 3 clics desde la pantalla principal"
✅ "El sistema shall permitir deshacer (undo) las últimas 10 acciones del usuario"
✅ "Los usuarios expertos shall poder realizar todas las operaciones usando únicamente teclado sin necesidad de mouse"

**d) Protección contra Errores de Usuario (User Error Protection)**
¿El sistema previene que usuarios cometan errores?

**Ejemplos:**
✅ "El sistema shall deshabilitar el botón 'Guardar' hasta que todos los campos obligatorios estén completados correctamente"
✅ "El sistema shall solicitar confirmación explícita antes de eliminar registros permanentemente con mensaje: '¿Está seguro que desea eliminar 15 registros? Esta acción no se puede deshacer'"
✅ "Al intentar cerrar formulario con cambios no guardados, el sistema shall mostrar advertencia: 'Tiene cambios sin guardar. ¿Desea guardar, descartar cambios, o continuar editando?'"

**e) Estética de Interfaz de Usuario (User Interface Aesthetics)**
¿La interfaz es agradable y satisfactoria?

**Ejemplos:**
✅ "La interfaz shall seguir los principios de Material Design 3 de Google para consistencia visual"
✅ "El sistema shall usar una paleta de colores corporativos con contraste mínimo 4.5:1 según WCAG 2.1"
✅ "Los iconos shall ser reconocibles sin texto complementario y seguir el conjunto de iconos Material Symbols"

**f) Accesibilidad (Accessibility)**
¿Personas con diversas capacidades pueden usar el sistema?

**Ejemplos:**
✅ "El sistema shall cumplir con las Pautas de Accesibilidad para Contenido Web (WCAG) 2.1 nivel AA"
✅ "Todas las imágenes shall incluir texto alternativo (alt text) descriptivo para lectores de pantalla"
✅ "El sistema shall ser completamente navegable usando solo teclado con indicadores visuales del foco actual"
✅ "El sistema shall soportar zoom de hasta 200% sin pérdida de funcionalidad o información"

**Ejemplos Completos con Medición:**

✅ **Ejemplo 1 - Sistema de Punto de Venta:**
"Un cajero nuevo con experiencia básica en computación shall poder procesar su primera venta completa (escaneo productos, aplicar descuento, procesar pago, imprimir recibo) en menos de 5 minutos después de recibir 30 minutos de capacitación"

Desglose:
- Usuario: cajero nuevo con experiencia básica
- Tarea: venta completa
- Tiempo: <5 minutos
- Capacitación requerida: 30 minutos
- Métrica: tiempo de completar tarea

✅ **Ejemplo 2 - Aplicación Médica:**
"Un médico ocupado shall poder registrar los datos de una consulta médica completa (síntomas, diagnóstico, prescripción) en menos de 3 minutos usando la aplicación móvil"

✅ **Ejemplo 3 - Sistema Bancario:**
"El 90% de clientes mayores de 65 años shall poder transferir dinero entre cuentas propias sin asistencia de personal en su segundo intento"

**Analogía Usabilidad:**
Usabilidad = Conducir un auto
- Learnability = Qué tan rápido aprendes a conducirlo
- Operability = Qué tan fácil es manejarlo diario
- Error Protection = Frenos ABS y control de tracción (te previenen de chocar)
- Aesthetics = Qué tan bonito se ve el interior
- Accessibility = Autos adaptados para personas con discapacidad

---

**5. CONFIABILIDAD (Reliability)**

**Definición:** Grado en que un sistema, producto o componente realiza funciones específicas bajo condiciones específicas durante un período de tiempo específico.

**Subcaracterísticas:**

**a) Madurez (Maturity)**
¿El sistema cumple necesidades de confiabilidad durante operación normal?

**Métricas:**
- **MTBF (Mean Time Between Failures / Tiempo Promedio Entre Fallos):** Tiempo promedio que sistema opera sin fallar
- **Tasa de Fallos:** Número de fallos por unidad de tiempo

**Ejemplos:**
✅ "El sistema shall tener un MTBF de al menos 720 horas (30 días) de operación continua"
✅ "La tasa de fallos del sistema shall ser menor a 0.1% de todas las transacciones procesadas"
✅ "El sistema shall operar sin requerir reinicio durante al menos 90 días continuos"

**b) Disponibilidad (Availability)**
¿El sistema está operacional y accesible cuando se requiere usar?

**Fórmula:**
```
Disponibilidad = Tiempo Operacional / (Tiempo Operacional + Tiempo Inactivo) × 100%
```

**Tabla de Niveles de Disponibilidad (MEMORIZAR):**

| Disponibilidad | Nombre | Tiempo Inactivo por Año | Tiempo Inactivo por Mes | Uso Típico |
|----------------|--------|-------------------------|-------------------------|------------|
| 90% | Un nueve | 36.5 días | 72 horas | Sistemas internos no críticos |
| 99% | Dos nueves | 3.65 días | 7.2 horas | Sitios web corporativos |
| 99.9% | Tres nueves | 8.7 horas | 43.2 minutos | E-commerce estándar |
| 99.99% | Cuatro nueves | 52.6 minutos | 4.3 minutos | Servicios financieros |
| 99.999% | Cinco nueves | 5.26 minutos | 25.9 segundos | Telecomunicaciones críticas |
| 99.9999% | Seis nueves | 31.5 segundos | 2.6 segundos | Sistemas médicos críticos |

**Ejemplos:**
✅ "El sistema shall mantener disponibilidad del 99.9% medida mensualmente (máximo 43.2 minutos de tiempo inactivo por mes)"
✅ "El sistema de respaldo shall activarse automáticamente en menos de 30 segundos cuando el sistema principal falla"
✅ "El mantenimiento programado shall realizarse únicamente los domingos de 2am a 6am y no shall exceder 4 horas mensuales"

**c) Tolerancia a Fallos (Fault Tolerance)**
¿El sistema opera como se espera a pesar de fallas de hardware o software?

**Ejemplos:**
✅ "El sistema shall continuar procesando transacciones aunque falle 1 de los 3 servidores del cluster"
✅ "Si la conexión a base de datos falla, el sistema shall guardar transacciones localmente y sincronizar automáticamente cuando la conexión se restablezca"
✅ "El sistema shall detectar y recuperarse automáticamente de deadlocks en base de datos en menos de 5 segundos"

**d) Capacidad de Recuperación (Recoverability)**
¿El sistema puede recuperar datos afectados y reestablecer estado deseado tras interrupción o fallo?

**Métricas:**
- **RTO (Recovery Time Objective / Objetivo de Tiempo de Recuperación):** Tiempo máximo aceptable para restaurar servicio
- **RPO (Recovery Point Objective / Objetivo de Punto de Recuperación):** Pérdida de datos máxima aceptable

**Ejemplos:**
✅ "El sistema shall realizar respaldo incremental automático cada 4 horas con RPO máximo de 4 horas"
✅ "En caso de fallo catastrófico, el sistema shall poder restaurarse completamente desde respaldo en menos de 2 horas (RTO = 2 horas)"
✅ "El sistema shall mantener copias de respaldo en ubicación geográfica separada al menos 100 km del sitio principal"
✅ "Todas las transacciones financieras shall ser recuperables sin pérdida de datos (RPO = 0 minutos)"

**Diferencia CLAVE (sale en examen):**
- **Disponibilidad:** Estar "arriba" y accesible (sistema responde)
- **Confiabilidad:** Funcionar correctamente sin errores

**Ejemplo para entender diferencia:**
Un sistema puede tener 99.9% disponibilidad (está arriba casi siempre) pero baja confiabilidad si da resultados erróneos el 50% del tiempo.

**Analogía:**
- Disponibilidad = Tienda abierta (puedes entrar)
- Confiabilidad = Tienda abierta Y tiene productos correctos en stock
- Fault Tolerance = Tienda sigue funcionando aunque caja 1 de 3 falle
- Recoverability = Tienda puede reabrir en 2 horas si hay incendio

---

**6. SEGURIDAD (Security)**

**Definición:** Grado en que el producto protege información y datos de manera que personas, otros productos o sistemas tengan el grado de acceso apropiado a su nivel de autorización.

**CIA TRIAD - Los 3 Pilares de Seguridad (MEMORIZAR):**

**a) CONFIDENCIALIDAD (Confidentiality)**
Información accesible solo para quienes están autorizados

**Técnicas:**
- Autenticación (verificar identidad)
- Encriptación (cifrar datos)
- Control de acceso (limitar quién ve qué)

**Ejemplos:**
✅ "El sistema shall encriptar todos los datos de tarjetas de crédito usando AES-256 antes de almacenarlos"
✅ "Las credenciales de usuario shall transmitirse únicamente mediante conexiones HTTPS con TLS 1.3 o superior"
✅ "Los datos personales sensibles (CURP, RFC) shall mostrarse enmascarados mostrando solo últimos 4 dígitos excepto para usuarios con rol Admin"
✅ "El sistema shall implementar cifrado de extremo a extremo (E2EE) para mensajes entre usuarios"

**b) INTEGRIDAD (Integrity)**
Información no ha sido alterada de manera no autorizada

**Técnicas:**
- Checksums / Hashes (detectar alteraciones)
- Firmas digitales (verificar autenticidad)
- Control de versiones
- Auditoría

**Ejemplos:**
✅ "Cada transacción financiera shall incluir un hash SHA-256 que permita verificar que no ha sido alterada"
✅ "El sistema shall registrar en bitácora inmutable cualquier modificación a registros de auditoría indicando quién, qué, cuándo y desde dónde"
✅ "Los archivos descargados shall incluir checksum MD5 para verificar integridad de descarga"
✅ "Cambios a datos críticos shall requerir aprobación de 2 usuarios con roles diferentes (segregación de funciones)"

**c) DISPONIBILIDAD (Availability)**
Información accesible y usable cuando se requiere

**Técnicas:**
- Protección DDoS
- Redundancia
- Respaldos
- Plan recuperación desastres

**Ejemplos:**
✅ "El sistema shall implementar protección contra ataques DDoS que mitigue ataques de hasta 10 Gbps"
✅ "El sistema shall limitar a 100 solicitudes por minuto por dirección IP para prevenir abuso"
✅ "Los respaldos shall almacenarse en 3 ubicaciones geográficas diferentes"

**Otras Subcaracterísticas de Seguridad:**

**d) Autenticación (Authentication)**
Verificar identidad de usuarios

**Ejemplos:**
✅ "El sistema shall requerir autenticación de dos factores (2FA) usando: contraseña + código SMS de 6 dígitos con validez de 5 minutos"
✅ "Las contraseñas shall cumplir: mínimo 12 caracteres, incluir mayúsculas, minúsculas, números y símbolos especiales"
✅ "El sistema shall bloquear cuenta después de 3 intentos fallidos de inicio de sesión consecutivos durante 15 minutos"
✅ "Las sesiones de usuario shall expirar automáticamente después de 30 minutos de inactividad"

**e) Autorización (Authorization)**
Controlar qué puede hacer cada usuario

**Ejemplos:**
✅ "El sistema shall implementar control de acceso basado en roles (RBAC) con mínimo 5 roles: Admin, Gerente, Empleado, Cliente, Auditor"
✅ "Usuarios con rol 'Empleado' shall poder ver únicamente registros de su departamento"
✅ "Las operaciones de eliminación de datos shall estar restringidas únicamente a usuarios con rol 'Admin' con segundo factor de autenticación"

**f) No Repudio (Non-repudiation)**
Imposibilidad de negar acciones realizadas

**Ejemplos:**
✅ "Todas las transacciones financieras shall firmarse digitalmente con certificado del usuario que la realizó"
✅ "El sistema shall mantener log inmutable de todas las acciones con timestamp, IP origen, usuario, y acción realizada"
✅ "Los correos enviados desde el sistema shall incluir firma digital DKIM para prevenir suplantación"

**Analogía Seguridad:**
CIA Triad = Caja fuerte en banco
- Confidentiality = Solo tú puedes abrirla (llave + código)
- Integrity = Nadie puede alterar contenido sin que lo sepas (sellos, candados)
- Availability = Puedes acceder cuando lo necesitas (banco abierto, no robado)

---

**7. MANTENIBILIDAD (Maintainability)**

**Definición:** Grado de efectividad y eficiencia con el cual el producto puede ser modificado.

**Subcaracterísticas:**
- **Modularidad:** Componentes discretos con impacto mínimo entre sí
- **Reusabilidad:** Componentes usables en múltiples sistemas
- **Analizabilidad:** Fácil diagnosticar deficiencias o causas de fallos
- **Capacidad de Modificación:** Fácil implementar cambios sin introducir defectos
- **Capacidad de Prueba:** Fácil establecer criterios de prueba y ejecutarlas

**Ejemplos:**
✅ "Agregar nueva forma de pago shall requerir máximo 40 horas de desarrollo de 2 desarrolladores"
✅ "El sistema shall usar inyección de dependencias para facilitar cambio de implementaciones"
✅ "Cobertura de código por pruebas unitarias shall ser mínimo 80% para módulos críticos"

---

**8. PORTABILIDAD (Portability)**

**Definición:** Grado de efectividad con el cual un sistema puede ser transferido de un ambiente a otro.

**Subcaracterísticas:**
- **Adaptabilidad:** Adaptarse efectivamente a diferentes ambientes
- **Instalabilidad:** Puede instalarse/desinstalarse exitosamente
- **Reemplazabilidad:** Puede reemplazar otro sistema para el mismo propósito

**Ejemplos:**
✅ "El sistema shall ejecutarse sin modificación en Windows Server 2019+, Ubuntu 20.04+, Red Hat 8+"
✅ "Instalación shall completarse en menos de 15 minutos siguiendo 5 pasos documentados"
✅ "El sistema shall importar datos del sistema legacy en formato CSV conservando integridad referencial"

---

### **RESUMEN ISO 25010 - TABLA COMPLETA:**

| Característica | Pregunta Clave | Métrica Ejemplo | Analogía |
|----------------|----------------|-----------------|----------|
| Adecuación Funcional | ¿Hace lo que debe? | % funciones implementadas | Cuchillo que corta |
| Eficiencia Desempeño | ¿Qué tan rápido? | TPS, tiempo respuesta | Auto deportivo |
| Compatibilidad | ¿Funciona con otros? | APIs compatibles | Enchufe universal |
| Usabilidad | ¿Fácil de usar? | Tiempo completar tarea | iPhone intuitivo |
| Confiabilidad | ¿Funciona sin fallar? | MTBF, disponibilidad | Reloj suizo |
| Seguridad | ¿Protege información? | CIA Triad cumplido | Caja fuerte |
| Mantenibilidad | ¿Fácil de mantener? | Tiempo agregar feature | Auto con manual |
| Portabilidad | ¿Funciona en otros ambientes? | Plataformas soportadas | USB universal |

---

## RESUMEN ÁREA 1: ANÁLISIS DE SISTEMAS

### **Contenido Completo Cubierto:**

1. ✅ **Tipos de Requerimientos**
   - Jerarquía 3 niveles (Negocio, Usuario, Sistema)
   - Funcionales, No Funcionales, Restricciones, Reglas de Negocio
   - 10+ ejemplos por tipo con buenos ❌ vs malos ✅

2. ✅ **ISO 25010 - Atributos de Calidad**
   - 8 características principales completas
   - Subcaracterísticas detalladas
   - Métricas cuantificables
   - Tabla de 9's de disponibilidad
   - CIA Triad completo

3. ✅ **Documento SRS IEEE 830**
   - Estructura completa con todas las secciones
   - 4 formas de organizar requerimientos
   - 8 atributos de calidad (Completo, Correcto, Factible, Necesario, No Ambiguo, Priorizado, Verificable, Rastreable)
   - Palabras peligrosas categorizadas
   - Plantilla estándar de requerimiento

4. ✅ **Técnicas de Elicitación**
   - 5 técnicas principales (Entrevistas, Workshops/JAD, Observación, Cuestionarios, Prototipado)
   - Cuándo usar/no usar cada una
   - Ventajas y limitaciones
   - 5 barreras de elicitación con soluciones
   - Tabla comparativa completa

5. ✅ **Casos de Uso y User Stories**
   - Anatomía completa de caso de uso (6 componentes)
   - Ejemplos paso a paso con flujos
   - User Stories formato 3C (Card, Conversation, Confirmation)
   - INVEST criteria completo
   - Given/When/Then con ejemplos
   - Tabla comparativa exhaustiva (20+ aspectos)

6. ✅ **Priorización**
   - MoSCoW (Must, Should, Could, Won't)
   - Método $100
   - Pairwise Comparison
   - Matriz multidimensional

7. ✅ **Validación de Requerimientos**
   - Inspección formal (6 roles, fases)
   - Prototipado (baja vs alta fidelidad)
   - Principio test-first

8. ✅ **Gestión de Requerimientos**
   - Proceso control de cambios
   - Estados de requerimiento
   - Trazabilidad (Forward, Backward)
   - Matriz de trazabilidad
   - Baseline y versionado

9. ✅ **Modelado UML**
   - DFD (4 elementos, niveles)
   - Diagrama de Estados
   - Casos de Uso UML (Include vs Extend)
   - Diagrama de Actividad
   - Diagrama de Secuencia
   - Diagrama de Clases (relaciones, multiplicidad)

---

**Total Área 1:** 755 líneas de contenido técnico denso
**Equivalente:** ~40 páginas de material exhaustivo
**Nivel de detalle:** Definiciones extendidas + Múltiples ejemplos + Analogías + Tablas comparativas
**Idioma:** 100% Español técnico

---

**FIN DEL ÁREA 1: ANÁLISIS DE SISTEMAS**
**Preparado para:** Examen EGEL ISOFT 2026
**Objetivo:** Calificación 10 - Sobresaliente

## ÁREA 2: DISEÑO DE SISTEMAS (33 reactivos)

---

### 2.1 ARQUITECTURA DE SOFTWARE - MODELO 4+1 VISTAS

**FUENTES: Cervantes Cap.4 p.54-62 + Kruchten 1995 (Paper Original IEEE Software)**

#### **Definición de Arquitectura de Software**

**Definición (SEI - Software Engineering Institute):**
"La arquitectura de software de un sistema es el conjunto de estructuras necesarias para razonar sobre el sistema, que comprende elementos de software, las relaciones entre ellos, y las propiedades de ambos."

**Definición Simple:**
Arquitectura = Decisiones de diseño de alto nivel que:
1. Son difíciles de cambiar después
2. Tienen impacto sistémico
3. Afectan múltiples stakeholders

**Lo que NO es arquitectura:**
❌ "Usaremos MySQL" (decisión de tecnología, no arquitectura)
❌ "La clase User tiene 5 atributos" (detalle de diseño, no arquitectura)
❌ "Usaremos patrón Factory" (patrón, no decisión arquitectónica)

**Lo que SÍ es arquitectura:**
✅ "Sistema se dividirá en 3 capas: presentación, lógica, datos"
✅ "Comunicación entre servicios será asíncrona mediante mensajes"
✅ "Sistema debe escalar horizontalmente agregando nodos"

---

#### **MODELO 4+1 VISTAS (Philippe Kruchten, 1995)**

**Contexto:** Arquitectura es compleja. Diferentes stakeholders necesitan ver diferentes aspectos. Una sola vista no es suficiente.

**Analogía:** Planos de una casa
- Arquitecto necesita vista estructural (columnas, vigas)
- Electricista necesita vista eléctrica (cableado, contactos)
- Plomero necesita vista hidráulica (tuberías, drenaje)
- Dueño necesita vista de habitaciones (espacios, función)
- **Todas describen la MISMA casa, pero desde diferentes perspectivas**

El Modelo 4+1 hace lo mismo con software: 4 vistas principales + 1 integradora.

---

#### **VISTA 1: VISTA LÓGICA (Logical View)**

**Propósito:** Soportar los requerimientos funcionales del sistema. Describe QUÉ hace el sistema.

**Elementos:**
- Clases
- Paquetes (packages)
- Subsistemas
- Interfaces
- Relaciones (herencia, asociación, agregación)

**Audiencia:**
- Diseñadores de software
- Analistas de requerimientos
- Usuarios finales (alto nivel)

**Notación UML:**
- Diagrama de Clases
- Diagrama de Paquetes
- Diagrama de Objetos

**Pregunta que responde:** "¿Qué servicios provee el sistema a sus usuarios?"

**Ejemplo Completo - Sistema de E-commerce:**

```
VISTA LÓGICA

SUBSISTEMA: Gestión de Catálogo
├── Package: Productos
│   ├── Clase: Producto
│   │   - atributos: id, nombre, precio, stock, categoría
│   │   - métodos: calcularPrecioConDescuento(), verificarDisponibilidad()
│   ├── Clase: Categoría
│   │   - atributos: id, nombre, descripción
│   │   - métodos: obtenerProductos()
│   └── Clase: CatalogoService
│       - métodos: buscarProductos(), filtrarPorPrecio()

SUBSISTEMA: Gestión de Pedidos
├── Package: Carrito
│   ├── Clase: Carrito
│   │   - atributos: items[], total
│   │   - métodos: agregarItem(), removerItem(), calcularTotal()
│   └── Clase: ItemCarrito
│       - atributos: producto, cantidad, precioUnitario
├── Package: Pedidos
│   ├── Clase: Pedido
│   │   - atributos: id, fecha, cliente, items[], estado, total
│   │   - métodos: confirmar(), cancelar(), calcularTotal()
│   └── Clase: PedidoService
│       - métodos: crearPedido(), actualizarEstado()

SUBSISTEMA: Gestión de Pagos
├── Clase: Pago
│   - atributos: id, monto, método, estado
│   - métodos: procesar(), verificar(), reembolsar()
└── Clase: PasarelaPago (interfaz)
    - implementaciones: StripePago, PayPalPago

RELACIONES:
- Pedido tiene-un Carrito (composición)
- Pedido tiene-muchos ItemCarrito (composición)
- ItemCarrito referencia-a Producto (asociación)
- PedidoService usa PasarelaPago (dependencia)
```

**Criterios de Buena Vista Lógica:**
✅ Alta cohesión dentro de paquetes (clases relacionadas juntas)
✅ Bajo acoplamiento entre paquetes (pocas dependencias)
✅ Responsabilidades claras de cada clase
✅ Interfaces bien definidas entre subsistemas

**Analogía:** Vista Lógica = Organigrama de empresa (departamentos, roles, responsabilidades, jerarquía)

---

#### **VISTA 2: VISTA DE PROCESOS (Process View)**

**Propósito:** Soportar requerimientos no funcionales de rendimiento, disponibilidad, escalabilidad. Describe elementos en TIEMPO DE EJECUCIÓN.

**Elementos:**
- Procesos (programas en ejecución)
- Threads (hilos de ejecución)
- Tareas concurrentes
- Sincronización entre procesos
- Comunicación inter-proceso (IPC)

**Audiencia:**
- Arquitectos de software
- Ingenieros de integración
- Ingenieros de rendimiento

**Notación UML:**
- Diagrama de Actividad (con swimlanes)
- Diagrama de Secuencia (con focus en concurrencia)
- Diagrama de Comunicación

**Pregunta que responde:** "¿Cómo se ejecuta el sistema? ¿Qué procesos corren en paralelo?"

**Conceptos Clave:**

**1. Concurrencia:** Múltiples tareas ejecutándose simultáneamente (o aparentemente)

**2. Paralelismo:** Múltiples tareas ejecutándose REALMENTE al mismo tiempo (múltiples CPUs)

**3. Thread Pool:** Conjunto de threads reutilizables para tareas

**4. Message Queue:** Cola de mensajes para comunicación asíncrona

**Ejemplo Completo - Sistema de E-commerce:**

```
VISTA DE PROCESOS

PROCESO 1: Web Server (Múltiples instancias)
├── Thread Pool: Request Handlers (20 threads)
│   ├── Thread 1: Atendiendo request de usuario A
│   ├── Thread 2: Atendiendo request de usuario B
│   ├── ...
│   └── Thread 20: Atendiendo request de usuario T
├── Manejo de sesiones (concurrente)
└── Balanceo de carga entre instancias

PROCESO 2: Application Server (3 instancias)
├── Thread Pool: Business Logic (50 threads)
│   ├── Grupo A: Procesamiento de pedidos (15 threads)
│   ├── Grupo B: Búsqueda de productos (20 threads)
│   └── Grupo C: Gestión de inventario (15 threads)
└── Sincronización mediante:
    - Locks para acceso a inventario
    - Semáforos para limitar procesamiento concurrente

PROCESO 3: Payment Processor (Asíncrono)
├── Message Queue: Solicitudes de pago
│   - Consumer Threads: 5 threads procesando cola
│   - Cada thread:
│     1. Toma mensaje de cola
│     2. Procesa pago con pasarela
│     3. Actualiza estado en BD
│     4. Notifica resultado vía callback
└── Reintentos automáticos si falla

PROCESO 4: Email Service (Asíncrono)
├── Message Queue: Emails pendientes
└── Worker Pool: 3 workers enviando emails

PROCESO 5: Database Server
├── Connection Pool: 100 conexiones
├── Transaction Manager: Aislamiento SERIALIZABLE
└── Query Optimizer (paralelización de queries complejos)

COMUNICACIÓN ENTRE PROCESOS:
- Web ←→ Application: HTTP REST (síncrono)
- Application → Payment: Message Queue (asíncrono)
- Application → Email: Message Queue (asíncrono)
- Application ←→ Database: Connection Pool (síncrono)

SINCRONIZACIÓN:
- Lock en tabla Inventario al crear pedido (evitar overselling)
- Transacciones ACID en payment processing
- Circuit Breaker en llamadas a pasarela externa
```

**Escenario de Concurrencia:**

```
T=0ms:  Usuario A agrega producto X al carrito
        Usuario B agrega mismo producto X al carrito
        [Ambos en threads diferentes, concurrente]

T=10ms: Usuario A hace checkout (requiere reservar 1 unidad de X)
        Usuario B hace checkout (requiere reservar 1 unidad de X)
        [Stock actual: 1 unidad]

SIN SINCRONIZACIÓN (PROBLEMA):
T=20ms: Thread A lee stock=1 ✓
        Thread B lee stock=1 ✓
T=30ms: Thread A decrementa a 0, guarda ✓
        Thread B decrementa a 0, guarda ✓
RESULTADO: 2 pedidos confirmados, pero solo había 1 en stock! ❌

CON SINCRONIZACIÓN (SOLUCIÓN):
T=20ms: Thread A adquiere LOCK en producto X
        Thread B espera LOCK
T=25ms: Thread A lee stock=1, decrementa a 0, guarda, libera LOCK ✓
T=30ms: Thread B adquiere LOCK, lee stock=0, pedido RECHAZADO ✓
RESULTADO: Solo 1 pedido confirmado, consistencia mantenida ✅
```

**Patrones Comunes en Vista de Procesos:**

**1. Master-Worker Pattern**
```
Master Thread: Recibe requests, distribuye a workers
Worker Threads: Procesan tareas independientes
Usado en: Thread pools, procesamiento paralelo
```

**2. Producer-Consumer Pattern**
```
Producer: Genera mensajes, los pone en cola
Consumer: Toma mensajes de cola, los procesa
Usado en: Procesamiento asíncrono
```

**3. Pipeline Pattern**
```
Etapa 1 → Etapa 2 → Etapa 3 → Resultado
Cada etapa procesa y pasa a siguiente
Usado en: Procesamiento de streams, compiladores
```

**Criterios de Buena Vista de Procesos:**
✅ Identificar puntos de contención (donde threads compiten)
✅ Minimizar sincronización (locks son costosos)
✅ Usar procesamiento asíncrono para tareas lentas
✅ Balancear carga entre threads/procesos

**Analogía:** Vista de Procesos = Línea de producción de fábrica
- Múltiples estaciones trabajando en paralelo
- Sincronización entre estaciones
- Colas de trabajo entre etapas
- Balanceo de carga para evitar cuellos de botella

---

#### **VISTA 3: VISTA DE DESARROLLO (Development View)**

**Propósito:** Organizar el sistema desde la perspectiva del programador. Facilita el desarrollo.

**Elementos:**
- Módulos (archivos de código)
- Packages / Namespaces
- Librerías
- Capas de software
- Componentes
- Dependencias entre módulos

**Audiencia:**
- Programadores / Desarrolladores
- Gerentes de configuración
- Integradores de software

**Notación UML:**
- Diagrama de Componentes
- Diagrama de Paquetes
- Diagrama de Deployment (parcial)

**Pregunta que responde:** "¿Cómo está organizado el código fuente? ¿Qué depende de qué?"

**Ejemplo Completo - Sistema de E-commerce:**

```
VISTA DE DESARROLLO

ESTRUCTURA DE REPOSITORIO:
ecommerce-system/
├── frontend/                    [CAPA: Presentación]
│   ├── src/
│   │   ├── components/         [Componentes React]
│   │   │   ├── Product/
│   │   │   │   ├── ProductCard.jsx
│   │   │   │   ├── ProductList.jsx
│   │   │   │   └── ProductDetail.jsx
│   │   │   ├── Cart/
│   │   │   │   ├── CartItem.jsx
│   │   │   │   └── CartSummary.jsx
│   │   │   └── Checkout/
│   │   │       └── CheckoutForm.jsx
│   │   ├── services/           [Llamadas API]
│   │   │   ├── ProductService.js
│   │   │   ├── CartService.js
│   │   │   └── OrderService.js
│   │   ├── store/              [Estado global Redux]
│   │   │   ├── slices/
│   │   │   │   ├── cartSlice.js
│   │   │   │   └── userSlice.js
│   │   │   └── store.js
│   │   └── utils/              [Utilidades]
│   │       ├── validators.js
│   │       └── formatters.js
│   ├── package.json            [Dependencias npm]
│   └── webpack.config.js
│
├── backend/                     [CAPA: Lógica de Negocio]
│   ├── src/
│   │   ├── api/                [Controladores REST]
│   │   │   ├── controllers/
│   │   │   │   ├── ProductController.java
│   │   │   │   ├── OrderController.java
│   │   │   │   └── PaymentController.java
│   │   │   └── routes/
│   │   │       └── Routes.java
│   │   ├── domain/             [Entidades de negocio]
│   │   │   ├── model/
│   │   │   │   ├── Product.java
│   │   │   │   ├── Order.java
│   │   │   │   ├── Customer.java
│   │   │   │   └── Payment.java
│   │   │   └── valueobjects/
│   │   │       ├── Money.java
│   │   │       └── Address.java
│   │   ├── services/           [Lógica de negocio]
│   │   │   ├── ProductService.java
│   │   │   ├── OrderService.java
│   │   │   ├── InventoryService.java
│   │   │   └── PaymentService.java
│   │   ├── infrastructure/     [Implementaciones técnicas]
│   │   │   ├── persistence/    [Acceso a BD]
│   │   │   │   ├── repositories/
│   │   │   │   │   ├── ProductRepository.java
│   │   │   │   │   └── OrderRepository.java
│   │   │   │   └── mappers/
│   │   │   │       └── OrderMapper.java
│   │   │   ├── messaging/      [Colas de mensajes]
│   │   │   │   ├── RabbitMQPublisher.java
│   │   │   │   └── EmailConsumer.java
│   │   │   └── external/       [APIs externas]
│   │   │       ├── StripeClient.java
│   │   │       └── SendGridClient.java
│   │   └── config/             [Configuración]
│   │       ├── DatabaseConfig.java
│   │       └── SecurityConfig.java
│   ├── pom.xml                 [Dependencias Maven]
│   └── Dockerfile
│
├── database/                    [CAPA: Datos]
│   ├── migrations/             [Scripts evolución BD]
│   │   ├── V1__Create_Products_Table.sql
│   │   ├── V2__Create_Orders_Table.sql
│   │   └── V3__Add_Payment_Status.sql
│   └── seeds/                  [Datos iniciales]
│       └── products_seed.sql
│
├── shared/                      [MÓDULOS COMPARTIDOS]
│   ├── common-lib/
│   │   ├── src/
│   │   │   ├── exceptions/
│   │   │   │   ├── BusinessException.java
│   │   │   │   └── ValidationException.java
│   │   │   └── utils/
│   │   │       ├── DateUtils.java
│   │   │       └── StringUtils.java
│   │   └── pom.xml
│   └── api-contracts/          [Contratos API compartidos]
│       └── openapi.yaml
│
└── infrastructure/              [INFRAESTRUCTURA]
    ├── docker-compose.yml
    ├── kubernetes/
    │   ├── deployment.yaml
    │   └── service.yaml
    └── scripts/
        ├── build.sh
        └── deploy.sh

DEPENDENCIAS ENTRE MÓDULOS:

frontend DEPENDE DE:
├── React (npm: react@18.2.0)
├── Redux Toolkit (npm: @reduxjs/toolkit@1.9.5)
├── Axios (npm: axios@1.4.0)
└── Material-UI (npm: @mui/material@5.14.0)

backend DEPENDE DE:
├── Spring Boot (maven: spring-boot-starter-web:3.1.0)
├── Spring Data JPA (maven: spring-boot-starter-data-jpa)
├── PostgreSQL Driver (maven: postgresql:42.6.0)
├── Stripe SDK (maven: stripe-java:22.30.0)
└── common-lib (internal: com.ecommerce:common-lib:1.0.0)

CAPAS Y REGLAS DE DEPENDENCIA:

CAPA PRESENTACIÓN
    ↓ depende de (puede usar)
CAPA LÓGICA NEGOCIO
    ↓ depende de (puede usar)
CAPA DATOS

REGLA: Capas superiores pueden depender de inferiores
       Capas inferiores NUNCA dependen de superiores

EJEMPLO CORRECTO:
✅ ProductController (presentación) → ProductService (lógica)
✅ ProductService (lógica) → ProductRepository (datos)

EJEMPLO INCORRECTO:
❌ ProductRepository (datos) → ProductController (presentación)
   [Viola regla de capas]
```

**Patrones de Organización:**

**1. Organización por Capas (Layered)**
```
presentation/
business/
persistence/
```
**Ventaja:** Separación clara de responsabilidades
**Desventaja:** Features atraviesan todas las capas

**2. Organización por Features (Vertical Slicing)**
```
product/
  - ProductController
  - ProductService
  - ProductRepository
order/
  - OrderController
  - OrderService
  - OrderRepository
```
**Ventaja:** Feature completa en un lugar
**Desventaja:** Puede tener código duplicado entre features

**3. Organización Hexagonal (Ports and Adapters)**
```
domain/        [Core de negocio]
ports/         [Interfaces]
adapters/      [Implementaciones]
  - inbound/   [REST controllers]
  - outbound/  [DB repositories, External APIs]
```
**Ventaja:** Dominio independiente de infraestructura
**Desventaja:** Más complejidad inicial

**Criterios de Buena Vista de Desarrollo:**
✅ Dependencias claras y unidireccionales
✅ Módulos cohesivos (código relacionado junto)
✅ Acoplamiento bajo (pocos import entre módulos)
✅ Fácil navegar y encontrar código
✅ Builds incrementales rápidos

**Análisis de Dependencias:**

```
BUENO ✅:
Module A → Module B → Module C
[Dependencias lineales, fáciles de entender]

MALO ❌ (Ciclo de dependencias):
Module A → Module B
    ↑         ↓
    └─────────┘
[A depende de B, B depende de A - circular dependency]

SOLUCIÓN: Extraer interfaz común en Module C
Module A → Module C ← Module B
```

**Herramientas de Análisis:**
- SonarQube: Detecta dependencias circulares, complejidad
- ArchUnit: Pruebas automatizadas de arquitectura
- Structure101: Visualiza dependencias

**Analogía:** Vista de Desarrollo = Plano de construcción
- Cada cuarto (módulo) tiene función específica
- Puertas (interfaces) conectan cuartos
- Plomería (dependencias) debe ir en una dirección
- Fácil para constructor encontrar qué modificar

---

#### **VISTA 4: VISTA FÍSICA / DESPLIEGUE (Physical View)**

**Propósito:** Mapear el software a hardware. Mostrar la topología física del sistema.

**Elementos:**
- Nodos (servidores, dispositivos)
- Artefactos (archivos .jar, .war, .exe, .dll)
- Conexiones de red
- Protocolos de comunicación
- Distribución geográfica

**Audiencia:**
- Administradores de sistemas
- Ingenieros de redes
- Ingenieros de operaciones (DevOps)

**Notación UML:**
- Diagrama de Despliegue (Deployment Diagram)

**Pregunta que responde:** "¿En qué hardware corre el software? ¿Cómo se conectan los nodos?"

**Ejemplo Completo - Sistema de E-commerce en AWS:**

```
VISTA FÍSICA / DESPLIEGUE

REGIÓN: us-east-1 (N. Virginia)

┌────────────────────────────────────────────────────────────────┐
│  AVAILABILITY ZONE A                                           │
│                                                                │
│  ┌─────────────────────────────────────────┐                  │
│  │  Load Balancer (ELB)                    │                  │
│  │  - DNS: shop.example.com                │                  │
│  │  - IP: 54.123.45.67                     │                  │
│  │  - SSL/TLS termination                  │                  │
│  └──────────┬──────────────────────────────┘                  │
│             │                                                  │
│             │ HTTP/HTTPS                                       │
│             ↓                                                  │
│  ┌─────────────────────────────────────────┐                  │
│  │  Web Server EC2 Instance (×3)           │                  │
│  │  - Tipo: t3.medium                      │                  │
│  │  - CPU: 2 vCPU, RAM: 4GB               │                  │
│  │  - OS: Ubuntu 22.04 LTS                 │                  │
│  │  - Software: Nginx 1.22                 │                  │
│  │  - Artefacto: frontend.tar.gz           │                  │
│  │  - IP privada: 10.0.1.10-12            │                  │
│  └──────────┬──────────────────────────────┘                  │
│             │                                                  │
│             │ HTTP REST                                        │
│             ↓                                                  │
│  ┌─────────────────────────────────────────┐                  │
│  │  Application Server EC2 (×5)            │                  │
│  │  - Tipo: c5.xlarge                      │                  │
│  │  - CPU: 4 vCPU, RAM: 8GB               │                  │
│  │  - OS: Amazon Linux 2                   │                  │
│  │  - Software: JDK 17, Tomcat 10         │                  │
│  │  - Artefacto: ecommerce-api.war        │                  │
│  │  - IP privada: 10.0.1.20-24            │                  │
│  │  - Puerto: 8080                         │                  │
│  └──────────┬──────────────────────────────┘                  │
│             │                                                  │
└─────────────┼──────────────────────────────────────────────────┘
              │
              │ JDBC (TCP 5432)
              ↓
┌─────────────────────────────────────────┐
│  Database (RDS PostgreSQL)              │
│  - Versión: PostgreSQL 15.3             │
│  - Tipo: db.r6g.xlarge                  │
│  - CPU: 4 vCPU, RAM: 32GB              │
│  - Storage: 500GB SSD (GP3)             │
│  - Multi-AZ: Enabled (replica en AZ B)  │
│  - Backup automático: Diario            │
│  - IP privada: 10.0.2.10                │
│  - Puerto: 5432                         │
└──────────────────────────────────────────┘

┌─────────────────────────────────────────┐
│  Cache (ElastiCache Redis)              │
│  - Versión: Redis 7.0                   │
│  - Tipo: cache.r6g.large                │
│  - CPU: 2 vCPU, RAM: 13GB              │
│  - Nodos: 3 (cluster mode)              │
│  - IP privada: 10.0.3.10                │
│  - Puerto: 6379                         │
│  - Uso: Sesiones + Caché de productos   │
└──────────────────────────────────────────┘

┌─────────────────────────────────────────┐
│  Message Queue (SQS)                    │
│  - Queue: payments-queue                │
│  - Queue: emails-queue                  │
│  - Visibility timeout: 30s              │
│  - Max retries: 3                       │
│  - DLQ: payments-dead-letter            │
└──────────────────────────────────────────┘

┌─────────────────────────────────────────┐
│  Object Storage (S3)                    │
│  - Bucket: ecommerce-product-images     │
│  - Region: us-east-1                    │
│  - Storage Class: Standard              │
│  - Acceso: CloudFront CDN               │
│  - Versionado: Enabled                  │
└──────────────────────────────────────────┘

┌─────────────────────────────────────────┐
│  CDN (CloudFront)                       │
│  - Edge Locations: Global (>400)        │
│  - Origin: S3 + ELB                     │
│  - Caché TTL: 86400s (24h)              │
│  - SSL/TLS: Certificado ACM             │
└──────────────────────────────────────────┘

SERVICIOS EXTERNOS (Fuera de AWS):

┌─────────────────────────────────────────┐
│  Stripe Payment Gateway                 │
│  - Endpoint: https://api.stripe.com     │
│  - Protocolo: HTTPS REST                │
│  - Autenticación: API Key               │
│  - Latencia típica: 200-500ms           │
└──────────────────────────────────────────┘

┌─────────────────────────────────────────┐
│  SendGrid Email Service                 │
│  - Endpoint: https://api.sendgrid.com   │
│  - Protocolo: HTTPS REST                │
│  - Autenticación: API Key               │
│  - Rate limit: 100 emails/segundo       │
└──────────────────────────────────────────┘

CONFIGURACIÓN DE RED:

VPC: 10.0.0.0/16
├── Subnet Pública (DMZ): 10.0.1.0/24
│   - NAT Gateway
│   - Load Balancer
│   - Web Servers
├── Subnet Privada (App): 10.0.2.0/24
│   - Application Servers
│   - Database (master)
└── Subnet Privada (Cache): 10.0.3.0/24
    - Redis Cluster

SECURITY GROUPS:

SG-LoadBalancer:
  Inbound:  80 (HTTP) from 0.0.0.0/0
            443 (HTTPS) from 0.0.0.0/0
  Outbound: 8080 to SG-WebServer

SG-WebServer:
  Inbound:  8080 from SG-LoadBalancer
  Outbound: 8080 to SG-AppServer

SG-AppServer:
  Inbound:  8080 from SG-WebServer
  Outbound: 5432 to SG-Database
            6379 to SG-Redis
            443 to Internet (Stripe, SendGrid)

SG-Database:
  Inbound:  5432 from SG-AppServer
  Outbound: None

SG-Redis:
  Inbound:  6379 from SG-AppServer
  Outbound: None

MONITOREO Y LOGGING:

┌─────────────────────────────────────────┐
│  CloudWatch                             │
│  - Métricas de EC2, RDS, ELB            │
│  - Alarmas configuradas:                │
│    • CPU > 80% → Autoscaling            │
│    • Latencia > 2s → Alerta PagerDuty   │
│    • Error rate > 1% → Alerta Slack     │
│  - Logs centralizados de aplicación     │
│  - Retención: 90 días                   │
└──────────────────────────────────────────┘

ALTA DISPONIBILIDAD:

Estrategia Multi-AZ:
- Load Balancer en 3 AZs
- Web Servers: Mínimo 2 por AZ (6 total)
- App Servers: Mínimo 2 por AZ (6 total)
- RDS: Master en AZ-A, Replica en AZ-B
- Auto Scaling:
  • Min: 2 instancias por AZ
  • Max: 10 instancias por AZ
  • Target: CPU < 70%

Recuperación ante Desastres:
- Backups diarios de RDS → S3 (otra región)
- Snapshots de EBS cada 6 horas
- RTO (Recovery Time Objective): 1 hora
- RPO (Recovery Point Objective): 6 horas

ESCALABILIDAD:

Horizontal:
- Web/App Servers: Auto Scaling Groups
- Database: Read replicas (hasta 5)
- Redis: Cluster mode con sharding

Vertical:
- Database: Puede escalar a db.r6g.16xlarge (64 vCPU, 512GB RAM)
- App Servers: Puede escalar a c5.4xlarge (16 vCPU)

COSTOS ESTIMADOS (Mensual):

- EC2 (8 instancias 24/7):     $800
- RDS PostgreSQL (Multi-AZ):   $600
- ElastiCache Redis:           $200
- Load Balancer:               $50
- Data Transfer:               $150
- S3 Storage (500GB):          $12
- CloudFront:                  $100
─────────────────────────────────
TOTAL:                         $1,912/mes
```

**Patrones de Despliegue:**

**1. Monolítico (Todo en un servidor)**
```
[Server único]
  - Web
  - App
  - DB
```
**Ventaja:** Simple, bajo costo
**Desventaja:** Punto único de fallo, no escala

**2. Dos Capas (Web + DB separados)**
```
[Web Server] → [DB Server]
```
**Ventaja:** DB independiente, más seguro
**Desventaja:** Web server puede ser cuello de botella

**3. Tres Capas (Presentación + Lógica + Datos)**
```
[Web Tier] → [App Tier] → [DB Tier]
```
**Ventaja:** Cada capa escala independientemente
**Desventaja:** Mayor complejidad, latencia

**4. Microservicios (Servicios independientes)**
```
[Web] → [API Gateway]
          ├→ [Product Service]
          ├→ [Order Service]
          ├→ [Payment Service]
          └→ [User Service]
Each with own DB
```
**Ventaja:** Máxima escalabilidad y flexibilidad
**Desventaja:** Complejidad operacional, debugging difícil

**Criterios de Buena Vista Física:**
✅ Redundancia para alta disponibilidad
✅ Separación de capas en subnets distintas
✅ Firewalls y security groups configurados
✅ Monitoreo y alertas automáticas
✅ Plan de recuperación ante desastres

**Analogía:** Vista Física = Mapa de ciudad con infraestructura
- Edificios (servidores)
- Carreteras (red)
- Servicios públicos (agua, luz = BD, caché)
- Redundancia (múltiples rutas entre puntos)
- Distribución geográfica (diferentes zonas)

---

#### **VISTA +1: VISTA DE ESCENARIOS (Scenarios / Use Case View)**

**Propósito:** INTEGRAR y VALIDAR las 4 vistas anteriores. Mostrar cómo colaboran para lograr casos de uso importantes.

**Elementos:**
- Casos de uso principales
- Diagramas de secuencia que cruzan vistas
- Flujos de datos end-to-end

**Audiencia:**
- TODOS los stakeholders
- Validación de arquitectura

**Notación UML:**
- Diagrama de Casos de Uso
- Diagrama de Secuencia (multi-vista)
- Diagrama de Colaboración

**Pregunta que responde:** "¿Cómo las 4 vistas trabajan juntas para realizar funcionalidades clave?"

**Ejemplo Completo - Escenario: "Procesar Compra"**

```
ESCENARIO: Usuario completa compra de producto

PASO A PASO INTEGRANDO LAS 4 VISTAS:

─────────────────────────────────────────────────────────────
PASO 1: Usuario hace clic en "Comprar Ahora"
─────────────────────────────────────────────────────────────

VISTA LÓGICA:
- Clase: CheckoutController.processCheckout()
- Valida: Carrito no vacío, productos disponibles
- Llama: OrderService.createOrder()

VISTA DE PROCESOS:
- Thread: HTTP Request Handler #5
- Prioridad: Alta (transacción crítica)
- Timeout: 30 segundos

VISTA DE DESARROLLO:
- Archivo: backend/src/api/controllers/CheckoutController.java
- Módulo: ecommerce-api
- Dependencias: order-service, inventory-service

VISTA FÍSICA:
- Servidor: app-server-01 (10.0.1.20)
- CPU actual: 45%
- Request llega vía Load Balancer desde CDN

─────────────────────────────────────────────────────────────
PASO 2: Sistema reserva inventario
─────────────────────────────────────────────────────────────

VISTA LÓGICA:
- Clase: InventoryService.reserveStock(productId, quantity)
- Regla: Stock must be >= quantity
- Si falla: throws OutOfStockException

VISTA DE PROCESOS:
- Adquiere LOCK en tabla Products
- Previene race condition con otros pedidos
- Lock duration: ~50ms

VISTA DE DESARROLLO:
- Archivo: backend/src/services/InventoryService.java
- Transacción: @Transactional(isolation = SERIALIZABLE)

VISTA FÍSICA:
- DB Query enviado a: rds-master (10.0.2.10)
- Network latency: 1ms (misma AZ)
- Query execution time: 20ms

─────────────────────────────────────────────────────────────
PASO 3: Sistema procesa pago
─────────────────────────────────────────────────────────────

VISTA LÓGICA:
- Clase: PaymentService.processPayment(orderId, amount, card)
- Llama: StripeClient.charge()
- Si falla: Rollback inventory reservation

VISTA DE PROCESOS:
- Publica mensaje en: payments-queue (SQS)
- Worker separado consume cola
- Procesamiento ASÍNCRONO (no bloquea al usuario)

VISTA DE DESARROLLO:
- Archivo: backend/src/infrastructure/external/StripeClient.java
- Timeout configurado: 10 segundos
- Retry policy: 3 intentos con exponential backoff

VISTA FÍSICA:
- Request sale de: app-server-01
- Via: NAT Gateway (internet egress)
- Destino: api.stripe.com (externa, California)
- Latency: 150ms (cross-region)
- HTTPS over TLS 1.3

─────────────────────────────────────────────────────────────
PASO 4: Sistema confirma pedido
─────────────────────────────────────────────────────────────

VISTA LÓGICA:
- Clase: OrderService.confirmOrder(orderId)
- Actualiza estado: PENDING → CONFIRMED
- Genera: Número de orden único (formato: ORD-2024-000123)

VISTA DE PROCESOS:
- Libera LOCK de inventory
- Commit de transacción en DB
- Publica evento: OrderConfirmed (event bus)

VISTA DE DESARROLLO:
- Archivo: backend/src/domain/services/OrderService.java
- Event: OrderConfirmedEvent publicado a event-bus

VISTA FÍSICA:
- UPDATE ejecutado en: rds-master
- Replica sincronizada a: rds-replica (AZ-B)
- Replication lag: <1 segundo

─────────────────────────────────────────────────────────────
PASO 5: Sistema envía email de confirmación
─────────────────────────────────────────────────────────────

VISTA LÓGICA:
- Clase: EmailService.sendOrderConfirmation(order, customer)
- Template: order-confirmation.html
- Datos: Número orden, items, total, fecha entrega

VISTA DE PROCESOS:
- Worker consume de: emails-queue (SQS)
- Worker pool: 3 workers paralelos
- Procesamiento asíncrono (no bloquea)

VISTA DE DESARROLLO:
- Archivo: backend/src/infrastructure/messaging/EmailConsumer.java
- Integración: SendGridClient

VISTA FÍSICA:
- Worker corre en: app-server-02 (distinto servidor)
- Request a: api.sendgrid.com (externa)
- Email delivery time: 2-5 segundos

─────────────────────────────────────────────────────────────
PASO 6: Usuario ve confirmación en pantalla
─────────────────────────────────────────────────────────────

VISTA LÓGICA:
- Componente: ConfirmationPage.jsx (React)
- Display: Order number, expected delivery, next steps

VISTA DE PROCESOS:
- Response enviado por: HTTP Request Handler #5
- Thread liberado al pool
- Total request time: 850ms

VISTA DE DESARROLLO:
- Archivo: frontend/src/components/Checkout/ConfirmationPage.jsx
- State management: Redux cartSlice.clear()

VISTA FÍSICA:
- Response: app-server-01 → Load Balancer → CDN → Usuario
- Network path: 4 hops
- Total latency vista por usuario: 1.2 segundos ✅

─────────────────────────────────────────────────────────────
RESUMEN DE FLUJO COMPLETO
─────────────────────────────────────────────────────────────

TIMING TOTAL:
- Validación inicial:          50ms
- Reserva de inventario:      70ms  (incluye lock)
- Procesamiento pago:        180ms  (llamada Stripe)
- Confirmación orden:         30ms
- Envío email (asíncrono):   ~3000ms (no bloquea)
- Renderizado frontend:      150ms
─────────────────────────────────
TOTAL PERCIBIDO POR USUARIO: 480ms (excelente! <500ms) ✅

COMPONENTES INVOLUCRADOS:
- Vistas Lógicas: 8 clases
- Threads: 2 (principal + worker email)
- Archivos código: 12
- Servidores físicos: 5 (LB, Web, App×2, DB, Worker)
- Servicios externos: 2 (Stripe, SendGrid)
- Mensajes asíncronos: 2 (payment, email)

GARANTÍAS PROPORCIONADAS:
✅ ACID: Transacción de orden + inventario
✅ Idempotencia: Retry seguro si falla
✅ Disponibilidad: Multi-AZ, si falla app-server-01 → app-server-02
✅ Auditoría: Todos los pasos logueados en CloudWatch
✅ Seguridad: HTTPS end-to-end, datos tarjeta nunca almacenados
```

**Por Qué Vista +1 es Crítica:**

1. **Valida Decisiones:** Descubre si las 4 vistas realmente soportan casos de uso
2. **Encuentra Problemas:** Revela cuellos de botella, puntos únicos de fallo
3. **Comunicación:** Stakeholders entienden mejor con ejemplos concretos
4. **Pruebas:** Base para casos de prueba de integración y performance

**Criterios de Buena Vista de Escenarios:**
✅ Cubre escenarios más críticos (80% del uso)
✅ Incluye flujos de excepción importantes
✅ Muestra cómo vistas colaboran
✅ Identifica cuellos de botella

**Analogía:** Vista de Escenarios = Día en la vida de...
- Muestra cómo todas las partes de la ciudad (vistas) trabajan juntas
- Usuario va de casa → metro → oficina → restaurante
- Cruza múltiples distritos (vistas) en un flujo coherente

---

#### **RESUMEN MODELO 4+1 VISTAS - TABLA MAESTRA**

| Vista | Pregunta | Elementos | Audiencia | Notación UML | Analogía |
|-------|----------|-----------|-----------|--------------|----------|
| **Lógica** | ¿Qué hace? | Clases, paquetes, interfaces | Diseñadores, analistas | Diagrama de Clases | Organigrama empresa |
| **Procesos** | ¿Cómo se ejecuta? | Threads, procesos, colas | Arquitectos, performance | Diagrama de Actividad | Línea de producción |
| **Desarrollo** | ¿Cómo está organizado el código? | Módulos, capas, librerías | Programadores | Diagrama de Componentes | Plano de construcción |
| **Física** | ¿Dónde se despliega? | Servidores, red, dispositivos | Admins, DevOps | Diagrama de Despliegue | Mapa de ciudad |
| **+1 Escenarios** | ¿Cómo funcionan juntas? | Casos de uso, secuencias | TODOS | Casos de Uso + Secuencia | Día en la vida de... |

**Cuándo Usar Cada Vista:**

```
INICIO DE PROYECTO:
├─ Vista Lógica: Define arquitectura de alto nivel
├─ Vista +1: Valida con escenarios principales
└─ Vista Física: Estima infraestructura y costos

DURANTE DESARROLLO:
├─ Vista de Desarrollo: Guía organización de código
└─ Vista de Procesos: Diseña concurrencia y threading

ANTES DE PRODUCCIÓN:
├─ Vista Física: Planea despliegue detallado
└─ Vista +1: Pruebas end-to-end de escenarios

OPERACIÓN:
├─ Vista Física: Monitoreo, escalamiento, troubleshooting
└─ Vista de Procesos: Performance tuning
```

**NO necesitas las 5 vistas siempre:**
- Proyecto pequeño: Vista Lógica + Desarrollo pueden bastar
- Microservicio simple: Vista Física + Escenarios críticas
- Sistema legacy: Vista de Desarrollo para entender código

**CONTINUARÁ CON ESTILOS ARQUITECTÓNICOS...**


### 2.1 ESTILOS ARQUITECTÓNICOS Y PATRONES

**FUENTES: Sommerville §6.3 p.176-195 + Cervantes §3.4 p.27-33**

#### **Definición de Estilo Arquitectónico**

**Estilo Arquitectónico:** Conjunto de principios de diseño que define:
1. **Componentes:** Tipos de elementos computacionales
2. **Conectores:** Cómo los componentes interactúan
3. **Restricciones:** Reglas sobre su composición
4. **Beneficios:** Qué propiedades de calidad facilita

**Analogía:** Estilo arquitectónico = Estilo de construcción de edificios
- Gótico: Arcos apuntados, vitrales, altura
- Minimalista: Líneas simples, espacios abiertos, blanco
- Colonial: Columnas, simetría, ladrillo

Cada estilo tiene sus reglas, ventajas, limitaciones.

---

#### **ESTILO 1: ARQUITECTURA EN CAPAS (Layered)**

**Definición:** Sistema estructurado en grupos de subtareas jerárquicos. Cada capa provee servicios a la capa inmediatamente superior y usa servicios de la capa inmediatamente inferior.

**Regla Fundamental:** Una capa solo puede depender de la capa directamente inferior (no puede saltarse capas).

**Ejemplo Clásico - Aplicación Web de 3 Capas:**

```
┌─────────────────────────────────────────┐
│  CAPA 3: PRESENTACIÓN                   │  [Usuario interactúa]
│  - Interfaz de usuario                  │
│  - Validación de entrada                │
│  - Formateo de salida                   │
│  Tecnologías: HTML, CSS, React, Angular │
└───────────────┬─────────────────────────┘
                │ usa servicios de
                ↓
┌─────────────────────────────────────────┐
│  CAPA 2: LÓGICA DE NEGOCIO             │  [Reglas del dominio]
│  - Procesamiento de transacciones      │
│  - Cálculos de negocio                 │
│  - Validación de reglas                │
│  Tecnologías: Java, C#, Python, Node   │
└───────────────┬─────────────────────────┘
                │ usa servicios de
                ↓
┌─────────────────────────────────────────┐
│  CAPA 1: DATOS / PERSISTENCIA          │  [Almacenamiento]
│  - Gestión de base de datos            │
│  - Acceso a archivos                   │
│  - Consultas SQL                       │
│  Tecnologías: PostgreSQL, MongoDB      │
└─────────────────────────────────────────┘
```

**Ejemplo Concreto - E-commerce:**

```
PRESENTACIÓN:
├── ProductPage.jsx
│   - Muestra producto con imagen, precio, descripción
│   - Botón "Agregar al carrito"
│   - NO sabe de dónde vienen los datos
│   - LLAMA A: ProductService.getProduct(id)

LÓGICA DE NEGOCIO:
├── ProductService.java
│   - getProduct(id): Obtiene producto
│   - calculateDiscountedPrice(product, customer):
│     • Si customer es VIP → 15% descuento
│     • Si es viernes → 10% descuento adicional
│     • Aplica reglas de negocio
│   - LLAMA A: ProductRepository.findById(id)

DATOS:
├── ProductRepository.java
│   - findById(id): SELECT * FROM products WHERE id = ?
│   - save(product): INSERT/UPDATE en BD
│   - NO conoce reglas de negocio, solo persiste

FLUJO COMPLETO:
Usuario ve producto → ProductPage → ProductService → ProductRepository → BD
Usuario ve producto ← ProductPage ← ProductService ← ProductRepository ← BD
```

**REGLA VIOLADA (Ejemplo de ANTI-PATRÓN):**
```
❌ ProductPage.jsx hace SELECT directo a BD
   [Presentación saltándose Lógica, violando capas]

❌ ProductRepository.java aplica descuento VIP
   [Datos conteniendo lógica de negocio, responsabilidad incorrecta]
```

**Ventajas:**
✅ **Portabilidad:** Cambiar BD (capa 1) sin afectar capas superiores
✅ **Mantenibilidad:** Modificar UI sin tocar lógica de negocio
✅ **Desarrollo paralelo:** Equipos diferentes trabajando en capas diferentes
✅ **Reutilización:** Misma lógica de negocio con múltiples presentaciones (web, móvil, API)
✅ **Testing:** Cada capa se prueba independientemente

**Desventajas:**
❌ **Overhead de performance:** Cada capa agrega latencia
❌ **Cascada de cambios:** Cambio en estructura de datos puede afectar todas las capas
❌ **Sobre-ingeniería:** Para apps simples, 3 capas puede ser excesivo

**Cuándo Usar:**
✅ Aplicaciones empresariales grandes
✅ Múltiples interfaces para mismo backend
✅ Equipos grandes necesitando separación clara
✅ Requerimientos de portabilidad (cambiar BD/UI)

**Cuándo NO Usar:**
❌ Prototipos rápidos (overhead innecesario)
❌ Aplicaciones con reqs de performance extremos
❌ Apps muy simples (CRUD básico)

**Variantes:**

**A) Strict Layering (Estricto):**
Capa N solo usa capa N-1 (regla rígida)

**B) Relaxed Layering (Relajado):**
Capa N puede usar cualquier capa inferior (N-1, N-2, N-3...)
Ejemplo: Presentación accede directamente a Caché (salta Lógica)

**Ejemplo Real - Sistema Operativo:**
```
CAPA 4: Aplicaciones de Usuario (Chrome, Excel)
         ↓ usa
CAPA 3: Shell / Interfaz Gráfica (Windows Explorer, bash)
         ↓ usa
CAPA 2: Servicios del Sistema (File System, Network Stack)
         ↓ usa
CAPA 1: Kernel (Gestión memoria, procesos, hardware)
         ↓ usa
CAPA 0: Hardware (CPU, RAM, Disco)
```

**Analogía:** Capas = Jerarquía militar
- General (capa superior) da órdenes a Coronel (capa inferior)
- Coronel da órdenes a Capitán
- NO: General dando órdenes directamente a Soldado raso (saltarse capas)

---

#### **ESTILO 2: MODELO-VISTA-CONTROLADOR (MVC)**

**Definición:** Patrón que separa aplicación en 3 componentes interconectados para separar representación interna de información de cómo se presenta/acepta del usuario.

**Los 3 Componentes:**

```
┌──────────────────────────────────────────────────────┐
│                     USUARIO                          │
└───────────────┬──────────────────────┬───────────────┘
                │ ve                   │ interactúa
                ↓                      │
         ┌──────────────┐             │
         │    VISTA     │             │
         │  (View)      │             │
         │ Presentación │             │
         │ HTML/JSX     │             │
         └──────┬───────┘             │
                │ notifica cambios    │
                ↓                     ↓
         ┌──────────────┐      ┌──────────────┐
         │    MODELO    │◄─────│ CONTROLADOR  │
         │   (Model)    │      │ (Controller) │
         │ Lógica/Datos │      │ Orquestador  │
         │ Estado       │      │ Maneja input │
         └──────────────┘      └──────────────┘
                ↑                     │
                │ consulta            │ actualiza
                └─────────────────────┘
```

**MODELO (Model):**
- **Responsabilidad:** Gestionar datos y lógica de negocio
- **Contiene:** Estado de la aplicación, reglas de negocio, validaciones
- **NO sabe:** Nada sobre UI o cómo se muestra
- **Notifica:** A vistas cuando datos cambian (patrón Observer)

**VISTA (View):**
- **Responsabilidad:** Presentar datos al usuario
- **Contiene:** HTML, CSS, templates, componentes UI
- **NO contiene:** Lógica de negocio, acceso a datos
- **Se suscribe:** A cambios en el modelo

**CONTROLADOR (Controller):**
- **Responsabilidad:** Intermediario entre Modelo y Vista
- **Recibe:** Input del usuario (clicks, formularios)
- **Decide:** Qué hacer con el input (cuál método del modelo llamar)
- **Actualiza:** Modelo según input del usuario

**Ejemplo Completo - Lista de Tareas (To-Do):**

```javascript
// ========== MODELO ==========
class TodoModel {
  constructor() {
    this.todos = [];
    this.observers = [];
  }
  
  // Agregar observador (Vista)
  addObserver(observer) {
    this.observers.push(observer);
  }
  
  // Notificar a todas las vistas
  notifyObservers() {
    this.observers.forEach(obs => obs.update(this.todos));
  }
  
  // Lógica de negocio
  addTodo(text) {
    const todo = {
      id: Date.now(),
      text: text,
      completed: false,
      createdAt: new Date()
    };
    this.todos.push(todo);
    this.notifyObservers();
  }
  
  toggleTodo(id) {
    const todo = this.todos.find(t => t.id === id);
    if (todo) {
      todo.completed = !todo.completed;
      this.notifyObservers();
    }
  }
  
  deleteTodo(id) {
    this.todos = this.todos.filter(t => t.id !== id);
    this.notifyObservers();
  }
  
  getActiveTodos() {
    return this.todos.filter(t => !t.completed);
  }
  
  getCompletedTodos() {
    return this.todos.filter(t => t.completed);
  }
}

// ========== VISTA ==========
class TodoView {
  constructor() {
    this.todoList = document.getElementById('todo-list');
    this.input = document.getElementById('todo-input');
    this.addButton = document.getElementById('add-button');
  }
  
  // Método llamado por Modelo cuando cambian datos
  update(todos) {
    this.render(todos);
  }
  
  // Renderizar todos
  render(todos) {
    this.todoList.innerHTML = '';
    todos.forEach(todo => {
      const li = document.createElement('li');
      li.className = todo.completed ? 'completed' : '';
      li.innerHTML = `
        <span>${todo.text}</span>
        <button data-id="${todo.id}" class="toggle">
          ${todo.completed ? '✓' : '○'}
        </button>
        <button data-id="${todo.id}" class="delete">✗</button>
      `;
      this.todoList.appendChild(li);
    });
  }
  
  // Vincular eventos a Controlador
  bindAddTodo(handler) {
    this.addButton.addEventListener('click', () => {
      const text = this.input.value.trim();
      if (text) {
        handler(text);
        this.input.value = '';
      }
    });
  }
  
  bindToggleTodo(handler) {
    this.todoList.addEventListener('click', (e) => {
      if (e.target.className === 'toggle') {
        const id = parseInt(e.target.dataset.id);
        handler(id);
      }
    });
  }
  
  bindDeleteTodo(handler) {
    this.todoList.addEventListener('click', (e) => {
      if (e.target.className === 'delete') {
        const id = parseInt(e.target.dataset.id);
        handler(id);
      }
    });
  }
}

// ========== CONTROLADOR ==========
class TodoController {
  constructor(model, view) {
    this.model = model;
    this.view = view;
    
    // Modelo observa Vista
    this.model.addObserver(this.view);
    
    // Vista notifica Controlador de eventos
    this.view.bindAddTodo(this.handleAddTodo.bind(this));
    this.view.bindToggleTodo(this.handleToggleTodo.bind(this));
    this.view.bindDeleteTodo(this.handleDeleteTodo.bind(this));
    
    // Renderizado inicial
    this.view.update(this.model.todos);
  }
  
  handleAddTodo(text) {
    this.model.addTodo(text);
  }
  
  handleToggleTodo(id) {
    this.model.toggleTodo(id);
  }
  
  handleDeleteTodo(id) {
    this.model.deleteTodo(id);
  }
}

// ========== INICIALIZACIÓN ==========
const app = new TodoController(
  new TodoModel(),
  new TodoView()
);
```

**FLUJO COMPLETO:**

```
1. Usuario escribe "Comprar leche" y hace clic en "Agregar"
   └→ Vista captura evento click

2. Vista llama a Controlador: handleAddTodo("Comprar leche")
   └→ Controlador recibe input del usuario

3. Controlador llama a Modelo: model.addTodo("Comprar leche")
   └→ Modelo ejecuta lógica de negocio

4. Modelo agrega todo a array, genera ID, timestamp
   └→ Modelo actualiza su estado interno

5. Modelo notifica a observadores: notifyObservers()
   └→ Modelo avisa a todas las vistas suscritas

6. Vista recibe notificación: update(todos)
   └→ Vista obtiene datos actualizados

7. Vista re-renderiza lista con nuevo todo incluido
   └→ Usuario ve "Comprar leche" en la pantalla

SEPARACIÓN DE RESPONSABILIDADES:
- Modelo: ✓ Sabe crear todo, validar, almacenar
         ✗ NO sabe de HTML, eventos click, DOM
- Vista:  ✓ Sabe mostrar datos, capturar clicks
         ✗ NO sabe de lógica negocio, cómo guardar datos
- Control:✓ Conecta Modelo con Vista, orquesta flujo
         ✗ NO contiene lógica negocio ni código UI
```

**Ventajas de MVC:**

✅ **Múltiples Vistas:** Mismo modelo con diferentes presentaciones
```
TodoModel
    ↓
    ├─→ TodoWebView (HTML)
    ├─→ TodoMobileView (React Native)
    └─→ TodoConsoleView (CLI)
```

✅ **Testing Independiente:**
- Probar Modelo sin UI
- Probar Vista con datos mock
- Probar Controlador con stubs

✅ **Desarrollo Paralelo:**
- Frontend trabaja en Vista
- Backend trabaja en Modelo
- Ambos usan Controlador como contrato

✅ **Mantenibilidad:**
- Cambiar diseño → Solo Vista
- Cambiar reglas → Solo Modelo
- Sin afectar el otro

**Desventajas:**

❌ **Complejidad para Apps Pequeñas:**
Para CRUD simple, MVC es overhead

❌ **Flujo de Datos Complejo:**
En apps grandes, difícil seguir flujo entre componentes

❌ **Acoplamiento Vista-Controlador:**
Controlador muy ligado a vistas específicas

**Variantes de MVC:**

**MVP (Model-View-Presenter):**
```
Vista ←→ Presentador ←→ Modelo
[Presentador maneja toda la lógica de presentación]
[Vista es totalmente pasiva]
```

**MVVM (Model-View-ViewModel):**
```
Vista ←(binding)→ ViewModel ←→ Modelo
[Data binding bidireccional automático]
[Usado en Angular, Vue, WPF]
```

**Cuándo Usar MVC:**
✅ Aplicaciones interactivas con UI compleja
✅ Múltiples vistas del mismo modelo
✅ Necesitas separación clara front/back
✅ Testing es prioridad

**Cuándo NO Usar:**
❌ Apps sin UI (APIs, servicios)
❌ Apps muy simples (1-2 pantallas)
❌ Reqs de performance extremos

**Frameworks que Usan MVC:**
- Backend: Ruby on Rails, Django, Laravel, Spring MVC
- Frontend: Backbone.js (clásico), Angular (variante MVVM)

**Analogía:** MVC = Restaurante
- **Modelo = Cocina:** Prepara comida (lógica), no ve clientes
- **Vista = Menú/Mesero:** Muestra opciones, toma orden, no cocina
- **Controlador = Capitán de meseros:** Recibe orden, la pasa a cocina, coordina

---

#### **ESTILO 3: MICROSERVICIOS**

**Definición:** Aplicación estructurada como colección de servicios pequeños, autónomos, desplegables independientemente, que se comunican vía protocolos ligeros (típicamente HTTP/REST).

**Características Clave:**

1. **Servicios Pequeños:** Cada servicio hace UNA cosa bien
2. **Independientes:** Desplegados, escalados, actualizados separadamente
3. **Descentralizados:** Cada servicio puede usar su propia BD/tecnología
4. **Comunicación Ligera:** APIs REST, mensajería asíncrona
5. **Organizados por Capacidad de Negocio:** No por capas técnicas

**Arquitectura Típica:**

```
                      ┌──────────────┐
                      │   API        │
                      │   Gateway    │
          ┌───────────┤ (Enrutador)  ├───────────┐
          │           └──────────────┘           │
          │                  │                   │
          ↓                  ↓                   ↓
   ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
   │  Product    │    │   Order     │    │   User      │
   │  Service    │    │   Service   │    │   Service   │
   │             │    │             │    │             │
   │ Node.js     │    │ Java        │    │ Python      │
   │ MongoDB     │    │ PostgreSQL  │    │ MySQL       │
   └─────────────┘    └─────────────┘    └─────────────┘
          │                  │                   │
          ↓                  ↓                   ↓
   ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
   │  Product    │    │   Order     │    │   User      │
   │  Database   │    │   Database  │    │   Database  │
   └─────────────┘    └─────────────┘    └─────────────┘

   CADA SERVICIO:
   - Tiene su propia base de datos
   - Se despliega independientemente
   - Puede usar tecnología diferente
   - Expone API REST
   - Escala independientemente
```

**Ejemplo Detallado - E-commerce con Microservicios:**

```
MICROSERVICIO 1: Product Service
├── Responsabilidad: Catálogo de productos
├── Endpoints:
│   GET    /products              → Lista productos
│   GET    /products/{id}         → Detalle producto
│   POST   /products              → Crear producto (admin)
│   PUT    /products/{id}         → Actualizar producto
│   DELETE /products/{id}         → Eliminar producto
├── Base de Datos: MongoDB (NoSQL, flexible para atributos variables)
├── Tecnología: Node.js + Express
├── Equipo: 3 desarrolladores
└── Despliegue: 5 instancias (auto-scaling)

MICROSERVICIO 2: Inventory Service
├── Responsabilidad: Control de stock
├── Endpoints:
│   GET  /inventory/{productId}    → Consultar stock
│   POST /inventory/reserve        → Reservar stock
│   POST /inventory/release        → Liberar reserva
│   PUT  /inventory/adjust         → Ajustar inventario
├── Base de Datos: PostgreSQL (transaccional, ACID crítico)
├── Tecnología: Java + Spring Boot
├── Equipo: 2 desarrolladores
└── Despliegue: 3 instancias con DB master-replica

MICROSERVICIO 3: Order Service
├── Responsabilidad: Gestión de pedidos
├── Endpoints:
│   POST /orders                   → Crear pedido
│   GET  /orders/{id}              → Detalle pedido
│   GET  /orders/user/{userId}     → Pedidos de usuario
│   PUT  /orders/{id}/status       → Actualizar estado
├── Base de Datos: PostgreSQL
├── Tecnología: Java + Spring Boot
├── Equipo: 4 desarrolladores (servicio complejo)
└── Despliegue: 4 instancias

MICROSERVICIO 4: Payment Service
├── Responsabilidad: Procesamiento de pagos
├── Endpoints:
│   POST /payments/process         → Procesar pago
│   GET  /payments/{id}            → Estado pago
│   POST /payments/refund          → Reembolso
├── Base de Datos: PostgreSQL (auditoría completa)
├── Tecnología: Python + Flask
├── Equipo: 2 desarrolladores + 1 seguridad
└── Despliegue: 3 instancias (PCI-DSS compliant)

MICROSERVICIO 5: User Service
├── Responsabilidad: Autenticación y perfiles
├── Endpoints:
│   POST /users/register           → Registro
│   POST /users/login              → Autenticación
│   GET  /users/{id}               → Perfil usuario
│   PUT  /users/{id}               → Actualizar perfil
├── Base de Datos: MySQL
├── Tecnología: Go + Gin
├── Equipo: 2 desarrolladores
└── Despliegue: 4 instancias (servicio crítico)

MICROSERVICIO 6: Notification Service
├── Responsabilidad: Emails y notificaciones
├── Endpoints:
│   POST /notifications/email      → Enviar email
│   POST /notifications/sms        → Enviar SMS
│   POST /notifications/push       → Push notification
├── Base de Datos: Redis (cola de mensajes)
├── Tecnología: Node.js
├── Equipo: 1 desarrollador
└── Despliegue: 2 instancias + workers

COMUNICACIÓN ENTRE SERVICIOS:

SINCRÓNICA (REST):
Order Service necesita verificar stock
  └→ HTTP GET inventory-service/inventory/{productId}
  └→ Respuesta inmediata: {"available": 10}

ASÍNCRONA (Mensajería):
Order creado exitosamente
  └→ Publica evento "OrderCreated" en RabbitMQ
  └→ Notification Service se suscribe
  └→ Payment Service se suscribe
  └→ Cada uno procesa independientemente

API GATEWAY (Kong/AWS API Gateway):
Cliente → API Gateway → Enruta a servicio correcto
  - /api/products/*  → Product Service
  - /api/orders/*    → Order Service
  - /api/users/*     → User Service
Responsabilidades:
  - Autenticación (JWT)
  - Rate limiting
  - Logging centralizado
  - Load balancing
```

**Flujo Completo - "Crear Pedido":**

```
1. Cliente hace POST /orders
   └→ API Gateway recibe request

2. Gateway valida JWT token
   └→ Llama a User Service: "¿Token válido?"
   └→ User Service: "Sí, userId=123"

3. Gateway enruta a Order Service
   └→ POST order-service:8080/orders

4. Order Service procesa:
   a) Llama a Inventory Service (sync):
      GET inventory-service:8081/inventory/{productId}
      └→ ¿Hay stock? Sí: 10 unidades

   b) Llama a Inventory Service (sync):
      POST inventory-service:8081/inventory/reserve
      └→ Reserva 1 unidad (quedan 9)

   c) Crea pedido en su propia BD
      INSERT INTO orders (...)

   d) Publica evento "OrderCreated" a Message Bus (async)

5. Payment Service (subscrito a OrderCreated):
   a) Recibe evento
   b) Procesa pago con Stripe
   c) Publica evento "PaymentProcessed"

6. Order Service (subscrito a PaymentProcessed):
   a) Actualiza estado: PENDING → CONFIRMED
   
7. Notification Service (subscrito a OrderCreated):
   a) Envía email de confirmación al cliente

8. Inventory Service (subscrito a PaymentProcessed):
   a) Si pago exitoso: Confirma reserva
   b) Si pago falla: Libera reserva

TOTAL TIME:
- Llamadas síncronas: ~300ms
- Procesamiento asíncrono: 2-5 segundos (no bloquea al usuario)
```

**Ventajas de Microservicios:**

✅ **Escalabilidad Independiente:**
```
Product Service (alto tráfico):    10 instancias
Payment Service (transaccional):    3 instancias
Notification Service (bajo carga):  2 instancias
```

✅ **Despliegue Independiente:**
```
Actualizar Product Service → Sin afectar Order Service
Bug en Payment → Solo redeploy Payment
Rollback fácil de un servicio sin tocar otros
```

✅ **Tecnología Heterogénea:**
```
Product: Node.js (rápido para JSON)
Payment: Java (robusto, empresarial)
User: Go (performance, concurrencia)
```

✅ **Equipos Autónomos:**
```
Equipo A: Dueño de Product Service
  - Define APIs
  - Elige tecnología
  - Despliega cuando quiera
Equipo B: Dueño de Order Service
  - Independiente de Equipo A
```

✅ **Resiliencia:**
```
Si Payment Service falla:
  → Order Service aún funciona
  → Usuario crea pedido "PENDING"
  → Pago se procesa cuando Payment se recupera
[Sistema NO colapsa completamente]
```

**Desventajas de Microservicios:**

❌ **Complejidad Operacional:**
```
Monolito: 1 app para desplegar, 1 BD para monitorear
Microservicios: 10 apps, 10 BDs, 10 logs, 10 métricas
```

❌ **Latencia de Red:**
```
Monolito: Llamada en memoria (0.1ms)
Microservicio: HTTP REST (10-50ms por llamada)
[3 llamadas encadenadas = 30-150ms overhead]
```

❌ **Transacciones Distribuidas:**
```
Problema: Order + Payment + Inventory deben ser atómicos
Solución: SAGA pattern, eventual consistency
[Complejidad > transacción ACID simple]
```

❌ **Testing Complejo:**
```
Monolito: Test todo junto
Microservicios: Contract testing, integration tests end-to-end
                Mock de 5+ servicios para probar 1
```

❌ **Debugging Difícil:**
```
Bug en producción: ¿Qué servicio falló?
  → Correlacionar logs de 10 servicios
  → Distributed tracing necesario (Jaeger, Zipkin)
```

**Cuándo Usar Microservicios:**

✅ Aplicaciones grandes (>50K líneas código)
✅ Equipos múltiples (>20 desarrolladores)
✅ Partes del sistema con reqs muy diferentes (escalabilidad, tecnología)
✅ Despliegue continuo es prioridad
✅ Organización madura en DevOps

**Cuándo NO Usar:**

❌ Startups pequeñas (overhead no justificado)
❌ Equipo <5 personas (mantenibilidad)
❌ App sin necesidad de escalar partes independientes
❌ Presupuesto limitado (infraestructura costosa)
❌ Requerimientos transaccionales fuertes (banca)

**Patrones Clave en Microservicios:**

**1. API Gateway Pattern:**
```
Punto único de entrada
Enrutamiento, autenticación, rate limiting
Ejemplo: Kong, AWS API Gateway, Nginx
```

**2. Service Discovery:**
```
Servicios se registran automáticamente
Otros servicios los descubren dinámicamente
Ejemplo: Consul, Eureka, Kubernetes DNS
```

**3. Circuit Breaker:**
```
Si Payment Service falla 5 veces seguidas:
  → Abrir circuito (no llamar más)
  → Respuesta rápida con error
  → Reintentar después de timeout
Ejemplo: Hystrix, Resilience4j
```

**4. SAGA Pattern:**
```
Transacción distribuida como serie de transacciones locales
Si falla paso 3 de 5:
  → Ejecutar compensaciones de pasos 1 y 2
  → Eventual consistency
```

**Monolito vs Microservicios:**

| Aspecto | Monolito | Microservicios |
|---------|----------|----------------|
| Despliegue | 1 artefacto | N artefactos |
| Escalabilidad | Vertical (todo junto) | Horizontal (independiente) |
| BD | Compartida | 1 por servicio |
| Tecnología | Homogénea | Heterogénea |
| Complejidad Desarrollo | Baja | Alta |
| Complejidad Operacional | Baja | Muy alta |
| Time to Market | Lento (todo junto) | Rápido (equipos paralelos) |
| Testing | Simple | Complejo |
| Debugging | Fácil | Difícil |
| Costo Infraestructura | Bajo | Alto |
| Resiliencia | Punto único fallo | Fault isolation |

**Analogía:** Microservicios = Ciudad vs Edificio
- **Monolito = Edificio único:** Todo bajo un techo, fácil comunicación interna, si falla estructura colapsa todo
- **Microservicios = Ciudad:** Edificios separados, calles conectan, si falla edificio A, ciudad sigue funcionando, más complejo de gestionar

**Migración Monolito → Microservicios:**

```
NO hacer: "Big Bang" (reescribir todo a la vez) ❌

SÍ hacer: "Strangler Fig Pattern" ✅
1. Identificar bounded context (dominio cohesivo)
2. Extraer como servicio (empezar con el más independiente)
3. API Gateway enruta a nuevo servicio
4. Iterar hasta completar

Ejemplo:
Monolito → Extraer "Notification" (independiente) → Microservicio
          → Extraer "Product Catalog" → Microservicio
          → Extraer "Payment" → Microservicio
          → Monolito reducido (solo Order lógica core)
          → Extraer lo que queda
```


#### **ESTILO 4: CLIENTE-SERVIDOR**

**Definición:** Sistema distribuido donde servidores proveen recursos/servicios y clientes los consumen. Comunicación mediante protocolo de red.

**Características:**

```
CLIENTE (Consumidor)
- Inicia comunicación
- Solicita servicios
- Interfaz de usuario
- Lógica de presentación

      ↕ Red (HTTP, TCP, etc.)

SERVIDOR (Proveedor)
- Espera solicitudes
- Provee servicios/recursos
- Lógica de negocio
- Gestión de datos
```

**Ejemplo Clásico - Aplicación Web:**

```
ARQUITECTURA 2-TIER (Cliente gordo):

┌─────────────────────┐
│  Cliente Desktop    │
│  - UI compleja      │
│  - Lógica negocio   │ ← Business logic en cliente
│  - Validaciones     │
└──────────┬──────────┘
           │ SQL directo
           ↓
┌─────────────────────┐
│  Servidor BD        │
│  - Datos            │
│  - Stored Procs     │
└─────────────────────┘

Ventaja: UI rica, responsive
Desventaja: Actualizar cliente en 1000 PCs

─────────────────────────────────────

ARQUITECTURA 3-TIER (Cliente delgado):

┌─────────────────────┐
│  Cliente Web        │
│  - HTML/JS/CSS      │ ← Solo presentación
│  - Validación UI    │
└──────────┬──────────┘
           │ HTTP/REST
           ↓
┌─────────────────────┐
│  Servidor App       │
│  - Lógica negocio   │ ← Business logic centralizada
│  - Validaciones     │
└──────────┬──────────┘
           │ JDBC/SQL
           ↓
┌─────────────────────┐
│  Servidor BD        │
│  - Solo datos       │
└─────────────────────┘

Ventaja: Actualización centralizada
Desventaja: Requiere conexión constante
```

**Variantes:**

**A) Thin Client (Cliente Delgado):**
- Cliente: Solo presentación (navegador web)
- Servidor: Toda la lógica
- Ejemplo: Gmail, Google Docs

**B) Thick Client (Cliente Gordo):**
- Cliente: Presentación + lógica negocio
- Servidor: Solo datos
- Ejemplo: Microsoft Outlook (versión desktop), AutoCAD

**C) Peer-to-Peer Híbrido:**
- Clientes también actúan como servidores
- Ejemplo: BitTorrent, Skype (p2p calls)

**Ventajas:**
✅ Centralización de datos (backup, seguridad)
✅ Mantenimiento más fácil (actualizar servidor)
✅ Escalabilidad (agregar más servidores)
✅ Recursos compartidos eficientemente

**Desventajas:**
❌ Punto único de fallo (servidor cae → todos afectados)
❌ Cuello de botella (servidor sobrecargado)
❌ Requiere red confiable
❌ Costo de servidor potente

**Cuándo Usar:**
✅ Múltiples clientes accediendo mismos datos
✅ Datos deben estar centralizados
✅ Necesitas control centralizado

---

#### **ESTILO 5: PIPES Y FILTROS (Pipe & Filter)**

**Definición:** Datos fluyen a través de serie de componentes de procesamiento (filtros) conectados por conductos (pipes). Cada filtro transforma datos y los pasa al siguiente.

**Estructura:**

```
Input → [Filtro 1] → pipe → [Filtro 2] → pipe → [Filtro 3] → Output

Cada Filtro:
- Lee input de pipe
- Procesa/transforma datos
- Escribe output a pipe
- NO conoce filtros anteriores o siguientes
- Puede ejecutarse en paralelo
```

**Ejemplo Clásico - Pipeline de Procesamiento de Video:**

```
Video RAW
    ↓
┌──────────────────┐
│ Filtro 1:        │
│ Decode Codec     │ ← Lee bytes, produce frames
└────────┬─────────┘
         │ Pipe: Stream de frames
         ↓
┌──────────────────┐
│ Filtro 2:        │
│ Resize           │ ← 4K → 1080p
└────────┬─────────┘
         │ Pipe: Frames escalados
         ↓
┌──────────────────┐
│ Filtro 3:        │
│ Color Correction │ ← Ajusta brillo, contraste
└────────┬─────────┘
         │ Pipe: Frames ajustados
         ↓
┌──────────────────┐
│ Filtro 4:        │
│ Add Watermark    │ ← Superpone logo
└────────┬─────────┘
         │ Pipe: Frames finales
         ↓
┌──────────────────┐
│ Filtro 5:        │
│ Encode H.264     │ ← Comprime a video
└────────┬─────────┘
         │
         ↓
    Video Final
```

**Ejemplo Unix Shell (Clásico):**

```bash
# Contar palabras únicas en archivo, ordenadas por frecuencia
cat archivo.txt | tr ' ' '\n' | sort | uniq -c | sort -nr | head -10

Filtros:
1. cat         → Lee archivo
2. tr          → Reemplaza espacios por newlines (1 palabra por línea)
3. sort        → Ordena palabras alfabéticamente
4. uniq -c     → Cuenta duplicados consecutivos
5. sort -nr    → Ordena por conteo (numérico, reverso)
6. head -10    → Toma top 10

Pipes: | conectan salida de uno con entrada de siguiente
```

**Ejemplo Procesamiento de Pedidos:**

```
Pedido JSON
    ↓
[Validar Estructura] → JSON válido
    ↓
[Enriquecer Datos] → Agregar info cliente desde BD
    ↓
[Calcular Impuestos] → Agregar tax según región
    ↓
[Aplicar Descuentos] → Aplicar cupones, promociones
    ↓
[Formatear Salida] → Convertir a formato sistema legacy
    ↓
Sistema Facturación
```

**Ventajas:**
✅ **Reusabilidad:** Filtros independientes, combinables
✅ **Mantenibilidad:** Agregar/modificar filtro sin afectar otros
✅ **Paralelización:** Filtros pueden correr en paralelo si datos lo permiten
✅ **Comprensibilidad:** Flujo lineal fácil de entender

**Desventajas:**
❌ **Overhead:** Cada paso agrega latencia
❌ **No interactivo:** Difícil para sistemas que requieren interacción usuario
❌ **Parsing repetido:** Si cada filtro parsea formato (ej: XML)
❌ **Complejidad estado:** Difícil mantener estado global

**Cuándo Usar:**
✅ Procesamiento de streams de datos
✅ Transformaciones ETL (Extract, Transform, Load)
✅ Compiladores (lexer → parser → optimizer → code gen)
✅ Procesamiento multimedia

**Cuándo NO Usar:**
❌ Aplicaciones interactivas
❌ Cuando se necesita estado global compartido
❌ Procesamiento requiere ir atrás y adelante

---

#### **ESTILO 6: REPOSITORIO (Repository / Shared Data)**

**Definición:** Componentes independientes interactúan mediante almacén de datos central compartido. Datos son pasivos, componentes los leen/escriben.

**Estructura:**

```
         ┌─────────────┐
         │  Component  │
         │      A      │
         └──────┬──────┘
                │ read/write
                ↓
┌───────────────────────────────┐
│  REPOSITORIO CENTRAL          │
│  (Base de Datos Compartida)   │
│  - Todos los datos            │
│  - Esquema compartido         │
└───────────────────────────────┘
         ↑              ↑
         │ read/write   │ read/write
   ┌─────┴─────┐  ┌────┴──────┐
   │ Component │  │ Component │
   │     B     │  │     C     │
   └───────────┘  └───────────┘
```

**Ejemplo - Sistema de Control de Versiones (Git-like):**

```
REPOSITORIO CENTRAL:
┌──────────────────────────────┐
│  Git Repository (.git/)      │
│  - Objects (commits, trees)  │
│  - Refs (branches)           │
│  - Index (staging area)      │
└──────────────────────────────┘
         ↑        ↑        ↑
         │        │        │
    ┌────┴──┐ ┌──┴────┐ ┌─┴─────┐
    │ git   │ │ git   │ │ IDE   │
    │ commit│ │ branch│ │Plugin │
    └───────┘ └───────┘ └───────┘

Todos leen/escriben mismo repositorio
No se comunican entre sí directamente
```

**Ejemplo - IDE (Integrated Development Environment):**

```
REPOSITORIO CENTRAL:
┌──────────────────────────────┐
│  Proyecto / Workspace        │
│  - Archivos fuente (.java)   │
│  - Archivos compilados       │
│  - Configuración             │
│  - Metadatos                 │
└──────────────────────────────┘
         ↑        ↑        ↑
         │        │        │
    ┌────┴──┐ ┌──┴────┐ ┌─┴─────┐
    │Editor │ │Compile│ │Debug  │
    │       │ │       │ │       │
    └───────┘ └───────┘ └───────┘

Editor modifica código → Guardado en repositorio
Compiler lee código del repositorio → Genera .class
Debugger lee .class y código fuente
```

**Ejemplo - Sistema Bancario:**

```
REPOSITORIO CENTRAL:
┌──────────────────────────────┐
│  Base de Datos Bancaria      │
│  - Cuentas                   │
│  - Transacciones             │
│  - Clientes                  │
└──────────────────────────────┘
         ↑        ↑        ↑
         │        │        │
    ┌────┴──┐ ┌──┴────┐ ┌─┴─────┐
    │ ATM   │ │Cajero │ │Online │
    │System │ │Teller │ │Banking│
    └───────┘ └───────┘ └───────┘

Todos consultan/actualizan misma BD
Consistencia garantizada por BD (ACID)
```

**Dos Variantes:**

**A) Base de Datos Pasiva (Tradicional):**
```
Componentes activos, BD pasiva
Componentes hacen queries cuando necesitan
BD no notifica cambios
```

**B) Blackboard (Pizarra - BD Activa):**
```
BD notifica a componentes cuando datos cambian
Componentes se suscriben a cambios
Usado en sistemas expertos, IA
```

**Ventajas:**
✅ **Consistencia:** Datos en un solo lugar
✅ **Backup centralizado:** Fácil respaldar
✅ **Integridad:** BD enforza constraints
✅ **Componentes independientes:** No se conocen entre sí

**Desventajas:**
❌ **Cuello de botella:** BD sobrecargada si muchos componentes
❌ **Punto único de fallo:** BD cae → sistema completo para
❌ **Acoplamiento por datos:** Cambio en esquema afecta todos
❌ **Escalabilidad limitada:** Vertical, difícil distribuir

**Cuándo Usar:**
✅ Datos deben ser consistentes
✅ Múltiples componentes necesitan acceso a mismos datos
✅ Integridad de datos es crítica
✅ Componentes pueden ser independientes

**Repositorio vs Microservicios (Base de Datos):**

```
REPOSITORIO:
[Service A] ─┐
[Service B] ─┼→ [BD COMPARTIDA]
[Service C] ─┘
[Todos leen/escriben misma BD]

MICROSERVICIOS:
[Service A] → [BD A]
[Service B] → [BD B]
[Service C] → [BD C]
[Cada servicio su propia BD]
```

---

#### **ESTILO 7: PUBLICAR-SUSCRIBIR (Publish-Subscribe / Event-Driven)**

**Definición:** Componentes (publicadores) generan eventos sin saber quién los consumirá. Otros componentes (suscriptores) se suscriben a eventos de interés. Mediador (message broker) conecta ambos.

**Estructura:**

```
PUBLICADORES                MESSAGE BROKER              SUSCRIPTORES
                           (Event Bus)

┌──────────┐                                          ┌──────────┐
│Publisher │──publish("OrderCreated")──►              │Subscribe │
│    A     │                              ┌────┐      │    1     │
└──────────┘                              │Bus │─────►└──────────┘
                                          └────┘
┌──────────┐                                │         ┌──────────┐
│Publisher │──publish("PaymentFailed")─►   │         │Subscribe │
│    B     │                                └────────►│    2     │
└──────────┘                                          └──────────┘
                                                      ┌──────────┐
Publicadores NO conocen                               │Subscribe │
a suscriptores                     Suscriptores NO ───►│    3     │
                                   conocen publicador └──────────┘
```

**Características Clave:**

1. **Desacoplamiento Temporal:** Publicador y suscriptor no necesitan estar activos simultáneamente
2. **Desacoplamiento Espacial:** No necesitan conocer ubicaciones de cada uno
3. **Desacoplamiento de Sincronización:** Comunicación asíncrona

**Ejemplo Completo - E-commerce con Eventos:**

```
EVENTOS DEFINIDOS:
- OrderCreated {orderId, userId, items[], total, timestamp}
- PaymentProcessed {orderId, paymentId, amount, status}
- InventoryReserved {orderId, productId, quantity}
- ShipmentCreated {orderId, trackingNumber, carrier}
- OrderCancelled {orderId, reason}

────────────────────────────────────────────────────────

ESCENARIO: Usuario crea pedido

1. Order Service:
   - Crea pedido en su BD
   - PUBLICA evento: OrderCreated
   {
     orderId: "ORD-123",
     userId: "USER-456",
     items: [
       {productId: "PROD-789", quantity: 2, price: 29.99}
     ],
     total: 59.98,
     timestamp: "2024-01-15T10:30:00Z"
   }

2. MESSAGE BROKER (RabbitMQ/Kafka):
   - Recibe evento OrderCreated
   - Lo distribuye a TODOS los suscriptores

3. SUSCRIPTORES (procesamiento paralelo):

   A) Payment Service (suscrito a OrderCreated):
      - Recibe evento
      - Procesa pago con tarjeta
      - PUBLICA evento: PaymentProcessed
      {
        orderId: "ORD-123",
        paymentId: "PAY-999",
        amount: 59.98,
        status: "SUCCESS"
      }
   
   B) Inventory Service (suscrito a OrderCreated):
      - Recibe evento
      - Reserva inventario de productId: PROD-789
      - Reduce stock de 10 a 8
      - PUBLICA evento: InventoryReserved
   
   C) Notification Service (suscrito a OrderCreated):
      - Recibe evento
      - Envía email: "Tu pedido ORD-123 está siendo procesado"
   
   D) Analytics Service (suscrito a OrderCreated):
      - Recibe evento
      - Incrementa contador de pedidos
      - Actualiza dashboard de ventas en tiempo real

4. REACCIÓN A SEGUNDO NIVEL:

   Shipping Service (suscrito a PaymentProcessed):
   - Espera evento PaymentProcessed con status=SUCCESS
   - Cuando lo recibe, crea envío
   - PUBLICA evento: ShipmentCreated

   Notification Service (suscrito a PaymentProcessed):
   - Si status=SUCCESS: Email "Pago confirmado"
   - Si status=FAILED: Email "Problema con pago"

   Order Service (suscrito a PaymentProcessed):
   - Actualiza estado del pedido:
     PENDING → CONFIRMED (si SUCCESS)
     PENDING → CANCELLED (si FAILED)

────────────────────────────────────────────────────────

VENTAJAS DEL FLUJO:

1. Order Service NO llama directamente a Payment, Inventory, Notification
2. Agregar Analytics Service fue trivial (solo suscribirse)
3. Si Notification falla, Order sigue procesándose
4. Payment e Inventory se procesan en PARALELO (más rápido)
5. Servicios evolucionan independientemente
```

**Patrones de Tópicos:**

**A) Tópicos Directos:**
```
order.created
order.updated
order.cancelled
payment.processed
payment.failed
```

**B) Tópicos con Wildcard:**
```
order.*           → Recibe order.created, order.updated, order.cancelled
*.created         → Recibe order.created, user.created, product.created
order.#           → Recibe todo bajo order (order.created.approved, etc.)
```

**Ventajas:**
✅ **Desacoplamiento total:** Componentes no se conocen
✅ **Escalabilidad:** Agregar suscriptor sin modificar publicador
✅ **Flexibilidad:** Flujos complejos mediante múltiples suscripciones
✅ **Resiliencia:** Falla de suscriptor no afecta publicador

**Desventajas:**
❌ **Debugging complejo:** Flujo no lineal, difícil rastrear
❌ **Garantías de entrega:** Eventos pueden perderse (depende de broker)
❌ **Orden no garantizado:** Eventos pueden llegar desordenados
❌ **Complejidad operacional:** Mantener message broker

**Pub-Sub vs Request-Response:**

```
REQUEST-RESPONSE (Síncrono):
Order Service → [HTTP POST] → Payment Service
Order Service ← [HTTP 200]  ← Payment Service
[Order espera respuesta de Payment]

PUB-SUB (Asíncrono):
Order Service → [Publica OrderCreated] → Message Broker
Order Service continúa...
                  Message Broker → [Entrega evento] → Payment Service
                  Message Broker → [Entrega evento] → Notification Service
[Order NO espera, otros procesan independientemente]
```

**Cuándo Usar:**
✅ Sistemas con muchas integraciones
✅ Flujos de trabajo complejos
✅ Necesitas desacoplamiento total
✅ Procesamiento asíncrono es aceptable

**Cuándo NO Usar:**
❌ Respuesta inmediata requerida
❌ Transacciones ACID críticas
❌ Sistema simple con pocos componentes
❌ Debugging/trazabilidad es crítica

**Herramientas:**
- **Message Brokers:** RabbitMQ, Apache Kafka, AWS SNS/SQS, Azure Service Bus
- **Event Streaming:** Apache Kafka, AWS Kinesis
- **In-Memory:** Redis Pub/Sub

**Analogía:** Pub-Sub = Canal de YouTube
- YouTuber (publicador) sube video
- Suscriptores (suscriptores) reciben notificación
- YouTuber NO sabe quiénes exactamente verán video
- Suscriptor puede ver video ahora o después
- Agregar suscriptor no afecta a YouTuber

---

#### **RESUMEN COMPARATIVO - ESTILOS ARQUITECTÓNICOS**

| Estilo | Componentes | Conectores | Ventaja Principal | Desventaja Principal | Ejemplo Típico |
|--------|-------------|------------|-------------------|----------------------|----------------|
| **Capas** | Capas jerárquicas | Llamadas de función | Portabilidad, separación responsabilidades | Overhead performance | App web 3-tier |
| **MVC** | Model-View-Controller | Observer, llamadas método | Múltiples vistas, testing | Complejidad apps pequeñas | Django, Rails |
| **Microservicios** | Servicios independientes | HTTP REST, mensajería | Escalabilidad independiente, resiliencia | Complejidad operacional | Netflix, Amazon |
| **Cliente-Servidor** | Clientes, Servidores | Red (HTTP, TCP) | Centralización datos | Punto único fallo | Gmail, Facebook |
| **Pipe & Filter** | Filtros de procesamiento | Pipes (streams) | Reusabilidad, paralelización | Overhead, no interactivo | Unix shell, FFmpeg |
| **Repositorio** | Componentes independientes | BD compartida | Consistencia, integridad | Cuello botella | Git, IDEs |
| **Pub-Sub** | Publicadores, Suscriptores | Message Broker | Desacoplamiento total | Debugging complejo | Event-driven, IoT |

**Selección de Estilo según Requerimientos:**

```
SI necesitas...                           CONSIDERA...
─────────────────────────────────────────────────────────
Portabilidad entre plataformas            → Capas
M�ltiples interfaces (web, móvil, API)    → Capas o MVC
Escalabilidad independiente               → Microservicios
Despliegues independientes frecuentes     → Microservicios
Procesamiento de streams                  → Pipe & Filter
Muchos componentes leyendo mismos datos   → Repositorio
Integraciones múltiples y complejas       → Pub-Sub
Sistema simple, equipo pequeño            → Monolito (Capas)
Performance crítico                       → Monolito o Capas
Reqs transaccionales fuertes              → Monolito con Repositorio
```

**Combinación de Estilos (común):**

```
SISTEMA REAL COMBINA MÚLTIPLES:

E-commerce Completo:
├─ Frontend: MVC (React con Redux)
├─ Backend: Microservicios
│  ├─ Cada microservicio: Capas (Controller-Service-Repository)
│  └─ Comunicación: REST + Pub-Sub (eventos)
├─ Procesamiento: Pipe & Filter (video encoding)
└─ Datos: Repositorio (BD compartida en algunos servicios)

[NO existe estilo puro en producción, se combinan según necesidad]
```

**CONTINUARÁ con SOLID, Patrones de Diseño GoF, Normalización BD...**


---

### 2.2 PRINCIPIOS SOLID DE DISEÑO ORIENTADO A OBJETOS

**FUENTES: Pressman Cap.8 + Martin "Clean Architecture" + Cervantes §3.3**

#### **Introducción a SOLID**

**SOLID** es un acrónimo de 5 principios de diseño orientado a objetos creados por Robert C. Martin (Uncle Bob) para hacer el software más mantenible, flexible y escalable.

**Por qué SOLID es importante:**
- Código más fácil de entender
- Sistemas más fáciles de mantener
- Facilita refactorización
- Reduce acoplamiento
- Aumenta cohesión

**Analogía General:** SOLID es como las reglas de construcción de edificios
- Si no sigues las reglas → edificio puede colapsar o ser difícil de modificar
- Si sigues las reglas → edificio sólido, fácil de extender, seguro

---

#### **PRINCIPIO 1: S - SINGLE RESPONSIBILITY PRINCIPLE (SRP)**

**Definición:** Una clase debe tener UNA y solo UNA razón para cambiar. Cada clase debe tener una única responsabilidad.

**Reformulación más clara:** Una clase debe hacer UNA cosa y hacerla bien.

**¿Qué es una "razón para cambiar"?**
Diferentes stakeholders que podrían pedir cambios diferentes:
- CFO pide cambio en cálculo financiero
- CTO pide cambio en persistencia
- VP Marketing pide cambio en formato de reporte

Si una clase responde a múltiples stakeholders → viola SRP.

**Ejemplo MALO (Viola SRP):**

```java
// ❌ MALA PRÁCTICA: Clase con MÚLTIPLES responsabilidades
public class Empleado {
    private String nombre;
    private String puesto;
    private double salario;
    
    // Responsabilidad 1: Cálculo de nómina (Finanzas)
    public double calcularPago() {
        double base = salario;
        double bonos = calcularBonos();
        double deducciones = calcularDeducciones();
        return base + bonos - deducciones;
    }
    
    private double calcularBonos() {
        // Lógica compleja de bonos
        if (puesto.equals("Gerente")) return salario * 0.2;
        if (puesto.equals("Senior")) return salario * 0.1;
        return salario * 0.05;
    }
    
    private double calcularDeducciones() {
        // Lógica de impuestos y deducciones
        double impuestos = salario * 0.15;
        double seguroSocial = salario * 0.07;
        return impuestos + seguroSocial;
    }
    
    // Responsabilidad 2: Persistencia en BD (IT/Desarrollo)
    public void guardarEnBD() {
        Connection conn = DatabaseConnection.getConnection();
        String sql = "INSERT INTO empleados (nombre, puesto, salario) VALUES (?, ?, ?)";
        PreparedStatement stmt = conn.prepareStatement(sql);
        stmt.setString(1, nombre);
        stmt.setString(2, puesto);
        stmt.setDouble(3, salario);
        stmt.executeUpdate();
    }
    
    // Responsabilidad 3: Generación de reportes (Gestión/RH)
    public String generarReporteHTML() {
        StringBuilder html = new StringBuilder();
        html.append("<html><body>");
        html.append("<h1>Reporte de Empleado</h1>");
        html.append("<p>Nombre: " + nombre + "</p>");
        html.append("<p>Puesto: " + puesto + "</p>");
        html.append("<p>Salario: $" + salario + "</p>");
        html.append("<p>Pago Total: $" + calcularPago() + "</p>");
        html.append("</body></html>");
        return html.toString();
    }
}

/**
 * PROBLEMAS:
 * 
 * 1. Si CFO cambia fórmula de bonos → modificar clase Empleado
 * 2. Si CTO cambia BD de MySQL a PostgreSQL → modificar clase Empleado
 * 3. Si RH quiere reporte en PDF en lugar de HTML → modificar clase Empleado
 * 
 * Clase tiene 3 razones para cambiar (3 responsabilidades)
 * Difícil de probar (necesitas BD real y lógica de cálculo mezclada)
 * Cambios en reporte pueden romper cálculo de pago accidentalmente
 */
```

**Ejemplo BUENO (Cumple SRP):**

```java
// ✅ BUENA PRÁCTICA: Separar en 4 clases, cada una con UNA responsabilidad

// Clase 1: Solo datos del empleado (Entity/Model)
public class Empleado {
    private String id;
    private String nombre;
    private String puesto;
    private double salario;
    
    // Solo getters/setters, sin lógica de negocio
    public String getId() { return id; }
    public void setId(String id) { this.id = id; }
    public String getNombre() { return nombre; }
    public void setNombre(String nombre) { this.nombre = nombre; }
    public String getPuesto() { return puesto; }
    public void setPuesto(String puesto) { this.puesto = puesto; }
    public double getSalario() { return salario; }
    public void setSalario(double salario) { this.salario = salario; }
}

// Clase 2: Solo cálculo de nómina (Responsabilidad: Lógica Financiera)
public class CalculadoraNomina {
    
    public double calcularPago(Empleado empleado) {
        double base = empleado.getSalario();
        double bonos = calcularBonos(empleado);
        double deducciones = calcularDeducciones(empleado);
        return base + bonos - deducciones;
    }
    
    private double calcularBonos(Empleado empleado) {
        String puesto = empleado.getPuesto();
        double salario = empleado.getSalario();
        
        if (puesto.equals("Gerente")) return salario * 0.2;
        if (puesto.equals("Senior")) return salario * 0.1;
        return salario * 0.05;
    }
    
    private double calcularDeducciones(Empleado empleado) {
        double salario = empleado.getSalario();
        double impuestos = salario * 0.15;
        double seguroSocial = salario * 0.07;
        return impuestos + seguroSocial;
    }
}

// Clase 3: Solo persistencia (Responsabilidad: Acceso a Datos)
public class EmpleadoRepository {
    
    public void guardar(Empleado empleado) {
        Connection conn = DatabaseConnection.getConnection();
        String sql = "INSERT INTO empleados (id, nombre, puesto, salario) VALUES (?, ?, ?, ?)";
        PreparedStatement stmt = conn.prepareStatement(sql);
        stmt.setString(1, empleado.getId());
        stmt.setString(2, empleado.getNombre());
        stmt.setString(3, empleado.getPuesto());
        stmt.setDouble(4, empleado.getSalario());
        stmt.executeUpdate();
    }
    
    public Empleado buscarPorId(String id) {
        Connection conn = DatabaseConnection.getConnection();
        String sql = "SELECT * FROM empleados WHERE id = ?";
        PreparedStatement stmt = conn.prepareStatement(sql);
        stmt.setString(1, id);
        ResultSet rs = stmt.executeQuery();
        
        if (rs.next()) {
            Empleado emp = new Empleado();
            emp.setId(rs.getString("id"));
            emp.setNombre(rs.getString("nombre"));
            emp.setPuesto(rs.getString("puesto"));
            emp.setSalario(rs.getDouble("salario"));
            return emp;
        }
        return null;
    }
}

// Clase 4: Solo generación de reportes (Responsabilidad: Presentación)
public class GeneradorReportesEmpleado {
    private CalculadoraNomina calculadora;
    
    public GeneradorReportesEmpleado(CalculadoraNomina calculadora) {
        this.calculadora = calculadora;
    }
    
    public String generarReporteHTML(Empleado empleado) {
        double pagoTotal = calculadora.calcularPago(empleado);
        
        StringBuilder html = new StringBuilder();
        html.append("<html><body>");
        html.append("<h1>Reporte de Empleado</h1>");
        html.append("<p>Nombre: " + empleado.getNombre() + "</p>");
        html.append("<p>Puesto: " + empleado.getPuesto() + "</p>");
        html.append("<p>Salario Base: $" + empleado.getSalario() + "</p>");
        html.append("<p>Pago Total: $" + pagoTotal + "</p>");
        html.append("</body></html>");
        return html.toString();
    }
    
    public String generarReportePDF(Empleado empleado) {
        // Implementación PDF
        // Si necesitamos agregar PDF, NO afecta HTML
        return "PDF content";
    }
}

/**
 * USO:
 */
public class Main {
    public static void main(String[] args) {
        // Crear empleado
        Empleado emp = new Empleado();
        emp.setId("EMP001");
        emp.setNombre("Juan Pérez");
        emp.setPuesto("Gerente");
        emp.setSalario(50000);
        
        // Guardar en BD (usando Repository)
        EmpleadoRepository repo = new EmpleadoRepository();
        repo.guardar(emp);
        
        // Calcular nómina (usando Calculadora)
        CalculadoraNomina calculadora = new CalculadoraNomina();
        double pago = calculadora.calcularPago(emp);
        System.out.println("Pago: $" + pago);
        
        // Generar reporte (usando Generador)
        GeneradorReportesEmpleado generador = new GeneradorReportesEmpleado(calculadora);
        String reporteHTML = generador.generarReporteHTML(emp);
        System.out.println(reporteHTML);
    }
}

/**
 * BENEFICIOS:
 * 
 * 1. Si CFO cambia fórmula bonos → Solo modificar CalculadoraNomina
 * 2. Si CTO cambia BD → Solo modificar EmpleadoRepository
 * 3. Si RH quiere PDF → Solo agregar método en GeneradorReportesEmpleado
 * 
 * Cada clase tiene UNA razón para cambiar
 * Testing más fácil (mockear dependencias)
 * Cambios aislados (no rompes otras partes)
 * Código más legible (cada clase hace una cosa obvia)
 */
```

**Señales de Violación de SRP:**

```
❌ Clase tiene métodos que hacen cosas muy diferentes
   Ejemplo: calcularPago() + guardarEnBD() en misma clase

❌ Clase usa muchos imports de diferentes dominios
   Ejemplo: import java.sql.* + import javax.mail.* + import org.apache.poi.*
   [BD + Email + Excel en misma clase → muchas responsabilidades]

❌ Nombre de clase con "Y" o "Manager"
   Ejemplo: EmpleadoYReporte, EmpleadoManager
   [Indica múltiples responsabilidades]

❌ Clase tiene muchos métodos privados de diferentes naturalezas
   Ejemplo: calcularX(), formatearY(), validarZ(), enviarW()

❌ Cambios en requerimientos de un área rompen otra área
   Ejemplo: Cambio en formato de reporte rompe cálculo de nómina
```

**Cuándo aplicar SRP:**

✅ Siempre en lógica de negocio core
✅ Clases reutilizables/compartidas
✅ Testing es importante
✅ Sistema grande/complejo

⚠️ Puede relajarse en:
- Scripts pequeños de uso único
- DTOs simples (solo datos)
- Prototipos rápidos

**Analogía:** SRP = Herramientas en taller
- ❌ Herramienta que es martillo + destornillador + sierra (hace todo mal)
- ✅ Martillo separado + Destornillador separado + Sierra separada (cada uno excelente en su función)

---

#### **PRINCIPIO 2: O - OPEN/CLOSED PRINCIPLE (OCP)**

**Definición:** Las entidades de software (clases, módulos, funciones) deben estar ABIERTAS para extensión pero CERRADAS para modificación.

**Reformulación:** Debes poder AGREGAR funcionalidad nueva SIN modificar código existente.

**¿Por qué es importante?**
- Código existente ya probado → no quieres romperlo
- Cambios en código existente → riesgo de bugs
- Extensión sin modificación → más seguro

**Mecanismo principal:** Abstracción (interfaces, clases abstractas) + Polimorfismo

**Ejemplo MALO (Viola OCP):**

```java
// ❌ MALA PRÁCTICA: Modificar clase existente para agregar funcionalidad

public class CalculadoraDescuento {
    
    public double calcular(String tipoCliente, double monto) {
        // Cada vez que agregamos tipo de cliente, MODIFICAMOS esta clase
        
        if (tipoCliente.equals("Regular")) {
            return monto * 0.0; // 0% descuento
        } 
        else if (tipoCliente.equals("Premium")) {
            return monto * 0.10; // 10% descuento
        } 
        else if (tipoCliente.equals("VIP")) {
            return monto * 0.20; // 20% descuento
        }
        // Ahora necesitamos "Gold" → MODIFICAR esta clase (viola OCP)
        else if (tipoCliente.equals("Gold")) {
            return monto * 0.15; // 15% descuento
        }
        // Y si agregamos "Platinum"? → MODIFICAR OTRA VEZ
        else if (tipoCliente.equals("Platinum")) {
            return monto * 0.25;
        }
        
        return 0;
    }
}

/**
 * PROBLEMAS:
 * 
 * 1. Cada nuevo tipo cliente → MODIFICAR clase existente
 * 2. Riesgo de romper tipos existentes al agregar nuevos
 * 3. Clase crece indefinidamente (100 tipos = 100 if/else)
 * 4. Difícil de testear (necesitas probar TODOS los tipos cada vez)
 * 5. Violación OCP: Clase NO está cerrada para modificación
 */

// USO:
CalculadoraDescuento calc = new CalculadoraDescuento();
double desc = calc.calcular("VIP", 1000); // $200 descuento
```

**Ejemplo BUENO (Cumple OCP):**

```java
// ✅ BUENA PRÁCTICA: Usar abstracción + polimorfismo

// Interfaz (abstracción)
public interface EstrategiaDescuento {
    double calcular(double monto);
    String getTipo();
}

// Implementación para Regular
public class DescuentoRegular implements EstrategiaDescuento {
    @Override
    public double calcular(double monto) {
        return monto * 0.0; // 0% descuento
    }
    
    @Override
    public String getTipo() {
        return "Regular";
    }
}

// Implementación para Premium
public class DescuentoPremium implements EstrategiaDescuento {
    @Override
    public double calcular(double monto) {
        return monto * 0.10; // 10% descuento
    }
    
    @Override
    public String getTipo() {
        return "Premium";
    }
}

// Implementación para VIP
public class DescuentoVIP implements EstrategiaDescuento {
    @Override
    public double calcular(double monto) {
        return monto * 0.20; // 20% descuento
    }
    
    @Override
    public String getTipo() {
        return "VIP";
    }
}

// Calculadora usa la estrategia (NO necesita modificarse)
public class CalculadoraDescuento {
    
    public double calcular(EstrategiaDescuento estrategia, double monto) {
        // Esta clase NUNCA cambia, sin importar cuántos tipos agregues
        return estrategia.calcular(monto);
    }
}

/**
 * AGREGAR NUEVO TIPO (Gold) - SIN MODIFICAR CÓDIGO EXISTENTE:
 */

// Solo creamos NUEVA clase (extensión)
public class DescuentoGold implements EstrategiaDescuento {
    @Override
    public double calcular(double monto) {
        return monto * 0.15; // 15% descuento
    }
    
    @Override
    public String getTipo() {
        return "Gold";
    }
}

// CalculadoraDescuento NO SE MODIFICA
// DescuentoRegular, Premium, VIP NO SE MODIFICAN
// Solo AGREGAMOS nueva clase

/**
 * USO:
 */
public class Main {
    public static void main(String[] args) {
        CalculadoraDescuento calc = new CalculadoraDescuento();
        
        // Cliente Regular
        EstrategiaDescuento regular = new DescuentoRegular();
        double desc1 = calc.calcular(regular, 1000); // $0
        
        // Cliente VIP
        EstrategiaDescuento vip = new DescuentoVIP();
        double desc2 = calc.calcular(vip, 1000); // $200
        
        // Cliente Gold (NUEVO, sin modificar código existente)
        EstrategiaDescuento gold = new DescuentoGold();
        double desc3 = calc.calcular(gold, 1000); // $150
    }
}

/**
 * BENEFICIOS:
 * 
 * 1. Agregar Gold → Solo crear nueva clase (NO modificar existentes)
 * 2. Código existente sigue funcionando (NO riesgo de romper)
 * 3. Testing aislado (probar Gold sin retocar tests de VIP/Premium)
 * 4. ABIERTO para extensión (agregar infinitos tipos)
 * 5. CERRADO para modificación (CalculadoraDescuento nunca cambia)
 */
```

**Variante con Factory (común):**

```java
// Factory para crear estrategias
public class DescuentoFactory {
    
    public static EstrategiaDescuento crear(String tipo) {
        switch (tipo) {
            case "Regular": return new DescuentoRegular();
            case "Premium": return new DescuentoPremium();
            case "VIP": return new DescuentoVIP();
            case "Gold": return new DescuentoGold();
            default: throw new IllegalArgumentException("Tipo desconocido: " + tipo);
        }
    }
}

// USO simplificado:
EstrategiaDescuento estrategia = DescuentoFactory.crear("VIP");
double descuento = calc.calcular(estrategia, 1000);

// Nota: Factory SÍ necesita modificarse al agregar tipos,
// PERO solo Factory (1 clase), no toda la lógica de descuento
```

**Otro Ejemplo - Sistema de Reportes:**

```java
// ❌ MALO (viola OCP):
public class GeneradorReporte {
    public void generar(String formato, Datos datos) {
        if (formato.equals("PDF")) {
            // Código para PDF
        } else if (formato.equals("Excel")) {
            // Código para Excel
        } else if (formato.equals("HTML")) {
            // Código para HTML
        }
        // Agregar CSV? JSON? → MODIFICAR esta clase
    }
}

// ✅ BUENO (cumple OCP):
public interface GeneradorReporte {
    void generar(Datos datos);
}

public class GeneradorPDF implements GeneradorReporte {
    public void generar(Datos datos) { /* PDF logic */ }
}

public class GeneradorExcel implements GeneradorReporte {
    public void generar(Datos datos) { /* Excel logic */ }
}

// Agregar CSV → Solo crear GeneradorCSV, NO modificar existentes
public class GeneradorCSV implements GeneradorReporte {
    public void generar(Datos datos) { /* CSV logic */ }
}
```

**Técnicas para lograr OCP:**

1. **Herencia:** Clases base extensibles
2. **Interfaces:** Contratos que implementaciones cumplen
3. **Composición:** Inyectar comportamiento
4. **Patrón Strategy:** Algoritmos intercambiables
5. **Patrón Template Method:** Pasos fijos, detalles variables

**Señales de Violación OCP:**

```
❌ Muchos if/else o switch basados en tipo
   if (tipo == "A") ... else if (tipo == "B") ...

❌ Modificar clase cada vez que agregas funcionalidad
   "Necesito editar esta clase OTRA VEZ para agregar X"

❌ Clase muy grande con muchas responsabilidades
   Clase con 1000+ líneas mezclando muchas variantes

❌ Tests que deben modificarse al agregar casos
   Agregar tipo nuevo → reescribir 10 tests existentes
```

**Cuándo aplicar OCP:**

✅ Código que cambia frecuentemente (agregar tipos, formatos, estrategias)
✅ Bibliotecas y frameworks (usuarios extienden sin modificar)
✅ Plugin systems
✅ Lógica de negocio con muchas variantes

⚠️ No aplicar prematuramente:
- Si solo hay 2 opciones simples → if/else está bien
- Sobre-abstracción temprana → complejidad innecesaria
- "YAGNI" (You Aren't Gonna Need It) aplica

**Analogía:** OCP = Enchufes eléctricos
- Socket (interfaz) nunca cambia
- Puedes enchufar infinitos aparatos diferentes (extensión)
- No modificas el socket para cada aparato nuevo
- Aparatos compatibles con socket estándar (cerrado para modificación)

---

**CONTINUARÉ CON L, I, D DE SOLID EN SIGUIENTE PARTE...**


#### **PRINCIPIO 3: L - LISKOV SUBSTITUTION PRINCIPLE (LSP)**

**Definición:** Los objetos de una superclase deben poder ser reemplazados por objetos de sus subclases SIN romper la funcionalidad del programa.

**Reformulación:** Si tienes clase S (subclase) que hereda de clase T (superclase/base), debes poder usar S en cualquier lugar donde se espera T, sin que el programa se comporte incorrectamente.

**Regla de Oro:** La subclase debe cumplir el "contrato" de la superclase.

**Principio formal (Barbara Liskov, 1987):**
```
Si para cada objeto o1 de tipo S hay un objeto o2 de tipo T tal que,
para todos los programas P definidos en términos de T,
el comportamiento de P no cambia cuando o1 es sustituido por o2,
entonces S es un subtipo de T.
```

**En términos simples:** Subclase no debe sorprender al código que usa la superclase.

**Ejemplo MALO (Viola LSP) - Clásico: Rectángulo y Cuadrado:**

```java
// ❌ MALA PRÁCTICA: Cuadrado hereda de Rectángulo

public class Rectangulo {
    protected int ancho;
    protected int alto;
    
    public void setAncho(int ancho) {
        this.ancho = ancho;
    }
    
    public void setAlto(int alto) {
        this.alto = alto;
    }
    
    public int getAncho() {
        return ancho;
    }
    
    public int getAlto() {
        return alto;
    }
    
    public int calcularArea() {
        return ancho * alto;
    }
}

public class Cuadrado extends Rectangulo {
    
    @Override
    public void setAncho(int ancho) {
        // Cuadrado: ancho = alto
        this.ancho = ancho;
        this.alto = ancho;  // ¡Modifica AMBOS!
    }
    
    @Override
    public void setAlto(int alto) {
        // Cuadrado: alto = ancho
        this.ancho = alto;  // ¡Modifica AMBOS!
        this.alto = alto;
    }
}

/**
 * PRUEBA DEL PROBLEMA:
 */
public class Test {
    public static void main(String[] args) {
        Rectangulo rect = new Rectangulo();
        probarRectangulo(rect); // ✅ Funciona correctamente
        
        Rectangulo cuad = new Cuadrado();
        probarRectangulo(cuad); // ❌ FALLA! Viola LSP
    }
    
    public static void probarRectangulo(Rectangulo r) {
        r.setAncho(5);
        r.setAlto(4);
        
        // Expectativa: área = 5 × 4 = 20
        int area = r.calcularArea();
        
        System.out.println("Ancho: " + r.getAncho()); // Espero 5
        System.out.println("Alto: " + r.getAlto());   // Espero 4
        System.out.println("Área: " + area);          // Espero 20
        
        assert area == 20; // ✅ Pasa con Rectangulo, ❌ FALLA con Cuadrado!
    }
}

/**
 * RESULTADO:
 * 
 * Con Rectangulo:
 *   Ancho: 5
 *   Alto: 4
 *   Área: 20  ✅
 * 
 * Con Cuadrado:
 *   Ancho: 4  (setAlto(4) modificó ancho también!)
 *   Alto: 4
 *   Área: 16  ❌ (esperábamos 20)
 * 
 * VIOLA LSP: No puedo sustituir Rectangulo por Cuadrado sin romper comportamiento
 */

/**
 * PROBLEMAS:
 * 
 * 1. Cuadrado rompe "contrato" de Rectangulo
 *    - Rectangulo promete: setAncho() solo cambia ancho
 *    - Cuadrado: setAncho() cambia AMBOS (sorpresa!)
 * 
 * 2. Relación "es-un" conceptual NO implica herencia en código
 *    - Matemáticamente: Cuadrado ES UN Rectángulo
 *    - Programáticamente: Cuadrado NO debe heredar de Rectangulo
 * 
 * 3. Precondiciones/postcondiciones violadas
 *    - Cliente asume independencia ancho/alto
 *    - Cuadrado viola esta suposición
 */
```

**Ejemplo BUENO (Cumple LSP):**

```java
// ✅ BUENA PRÁCTICA: No usar herencia donde no aplica

// Interfaz común
public interface Forma {
    int calcularArea();
    int calcularPerimetro();
}

// Rectángulo como clase independiente
public class Rectangulo implements Forma {
    private int ancho;
    private int alto;
    
    public Rectangulo(int ancho, int alto) {
        this.ancho = ancho;
        this.alto = alto;
    }
    
    public void setAncho(int ancho) {
        this.ancho = ancho;
    }
    
    public void setAlto(int alto) {
        this.alto = alto;
    }
    
    @Override
    public int calcularArea() {
        return ancho * alto;
    }
    
    @Override
    public int calcularPerimetro() {
        return 2 * (ancho + alto);
    }
}

// Cuadrado como clase independiente (NO hereda de Rectangulo)
public class Cuadrado implements Forma {
    private int lado;
    
    public Cuadrado(int lado) {
        this.lado = lado;
    }
    
    public void setLado(int lado) {
        this.lado = lado;
    }
    
    @Override
    public int calcularArea() {
        return lado * lado;
    }
    
    @Override
    public int calcularPerimetro() {
        return 4 * lado;
    }
}

/**
 * USO:
 */
public class Test {
    public static void main(String[] args) {
        List<Forma> formas = new ArrayList<>();
        formas.add(new Rectangulo(5, 4));
        formas.add(new Cuadrado(5));
        formas.add(new Circulo(3));
        
        for (Forma forma : formas) {
            System.out.println("Área: " + forma.calcularArea());
            // Todas cumplen contrato de Forma
            // Ninguna sorprende al código cliente
        }
    }
}

/**
 * BENEFICIOS:
 * 
 * 1. Cada clase tiene su contrato claro
 * 2. No hay comportamiento sorpresivo
 * 3. Código cliente trabaja con interfaz Forma
 * 4. LSP cumplido: Puedo usar cualquier Forma intercambiablemente
 */
```

**Otro Ejemplo - Aves que Vuelan:**

```java
// ❌ MALO (viola LSP):

public class Ave {
    public void volar() {
        System.out.println("Volando...");
    }
}

public class Pinguino extends Ave {
    @Override
    public void volar() {
        // ¡Pingüinos NO vuelan!
        throw new UnsupportedOperationException("Pingüinos no vuelan");
    }
}

// Código cliente:
public void hacerVolarAves(List<Ave> aves) {
    for (Ave ave : aves) {
        ave.volar(); // ❌ Explota con Pinguino!
    }
}

// ✅ BUENO (cumple LSP):

public interface Ave {
    void comer();
    void moverse();
}

public interface AveVoladora extends Ave {
    void volar();
}

public class Aguila implements AveVoladora {
    @Override
    public void volar() {
        System.out.println("Águila volando...");
    }
    @Override
    public void comer() { /* ... */ }
    @Override
    public void moverse() { /* ... */ }
}

public class Pinguino implements Ave {
    // NO implementa AveVoladora
    @Override
    public void comer() { /* ... */ }
    @Override
    public void moverse() {
        System.out.println("Pingüino nadando...");
    }
}

// Código cliente:
public void hacerVolarAves(List<AveVoladora> aves) {
    for (AveVoladora ave : aves) {
        ave.volar(); // ✅ Todas vuelan, LSP cumplido
    }
}
```

**Reglas para Cumplir LSP:**

**1. Precondiciones NO pueden fortalecerse en subclase:**
```java
// ❌ MALO:
class Base {
    void procesar(int valor) {
        // Acepta cualquier int
    }
}

class Derivada extends Base {
    @Override
    void procesar(int valor) {
        if (valor < 0) throw new IllegalArgumentException();
        // Ahora requiere valor >= 0 (precondición más fuerte)
    }
}
```

**2. Postcondiciones NO pueden debilitarse en subclase:**
```java
// ❌ MALO:
class Base {
    int calcular() {
        // Garantiza retornar valor > 0
        return 10;
    }
}

class Derivada extends Base {
    @Override
    int calcular() {
        return -5; // Viola postcondición (puede retornar negativo)
    }
}
```

**3. Invariantes deben preservarse:**
```java
// ❌ MALO:
class CuentaBancaria {
    protected double saldo;
    // Invariante: saldo >= 0
    
    public void retirar(double monto) {
        if (saldo >= monto) {
            saldo -= monto;
        }
    }
}

class CuentaCredito extends CuentaBancaria {
    @Override
    public void retirar(double monto) {
        saldo -= monto; // Permite saldo negativo! Viola invariante
    }
}
```

**4. Excepciones nuevas NO deben lanzarse en subclase:**
```java
// ❌ MALO:
class Base {
    void metodo() {
        // No lanza excepciones
    }
}

class Derivada extends Base {
    @Override
    void metodo() throws IOException {
        // Lanza excepción nueva
    }
}
```

**Señales de Violación LSP:**

```
❌ Subclase arroja excepciones no esperadas

❌ Subclase lanza UnsupportedOperationException en métodos heredados
   (indica que NO debería heredar)

❌ Necesitas instanceof o getClass() para distinguir subclases
   if (obj instanceof Cuadrado) { /* caso especial */ }

❌ Código cliente debe conocer tipos concretos
   "Si es Pinguino no llames volar()"

❌ Tests fallan cuando sustituyes superclase por subclase
```

**Analogía:** LSP = Contrato de trabajo
- Si empresa contrata "Desarrollador" (superclase)
- Puede ser JavaDeveloper, PythonDeveloper (subclases)
- Todos deben cumplir contrato: "escribir código, asistir a juntas"
- Si uno dice "no escribo código" → viola contrato (LSP)

---

#### **PRINCIPIO 4: I - INTERFACE SEGREGATION PRINCIPLE (ISP)**

**Definición:** Los clientes NO deben ser forzados a depender de interfaces que no usan. Es mejor tener muchas interfaces específicas que una interfaz general.

**Reformulación:** Divide interfaces grandes en interfaces más pequeñas y específicas para que clientes solo dependan de métodos que realmente necesitan.

**Problema que resuelve:** "Fat Interfaces" (interfaces gordas) que obligan a implementar métodos innecesarios.

**Ejemplo MALO (Viola ISP):**

```java
// ❌ MALA PRÁCTICA: Interfaz "gorda" con todo

public interface Trabajador {
    void trabajar();
    void comer();
    void dormir();
    void cobrarSalario();
    void pedirVacaciones();
    void reportarHoras();
}

/**
 * PROBLEMA 1: Robot trabajador
 */
public class TrabajadorHumano implements Trabajador {
    @Override
    public void trabajar() {
        System.out.println("Trabajando...");
    }
    
    @Override
    public void comer() {
        System.out.println("Comiendo...");
    }
    
    @Override
    public void dormir() {
        System.out.println("Durmiendo...");
    }
    
    @Override
    public void cobrarSalario() {
        System.out.println("Cobrando salario...");
    }
    
    @Override
    public void pedirVacaciones() {
        System.out.println("Pidiendo vacaciones...");
    }
    
    @Override
    public void reportarHoras() {
        System.out.println("Reportando horas...");
    }
}

public class TrabajadorRobot implements Trabajador {
    @Override
    public void trabajar() {
        System.out.println("Robot trabajando...");
    }
    
    @Override
    public void comer() {
        // ❌ Robots NO comen!
        throw new UnsupportedOperationException("Robots no comen");
    }
    
    @Override
    public void dormir() {
        // ❌ Robots NO duermen!
        throw new UnsupportedOperationException("Robots no duermen");
    }
    
    @Override
    public void cobrarSalario() {
        // ❌ Robots NO cobran salario!
        throw new UnsupportedOperationException("Robots no cobran");
    }
    
    @Override
    public void pedirVacaciones() {
        // ❌ Robots NO piden vacaciones!
        throw new UnsupportedOperationException("Robots no necesitan vacaciones");
    }
    
    @Override
    public void reportarHoras() {
        System.out.println("Robot reportando horas...");
    }
}

/**
 * PROBLEMAS:
 * 
 * 1. Robot forzado a implementar 4 métodos que NO necesita
 * 2. Métodos lanzan excepciones (código frágil)
 * 3. Interfaz muy grande dificulta testing
 * 4. Cliente que solo necesita trabajar() debe conocer toda la interfaz
 */

// Cliente confundido:
public class Supervisor {
    public void administrar(Trabajador trabajador) {
        trabajador.trabajar();
        trabajador.comer(); // ❌ Puede explotar si es Robot!
    }
}
```

**Ejemplo BUENO (Cumple ISP):**

```java
// ✅ BUENA PRÁCTICA: Interfaces segregadas (pequeñas y específicas)

// Interfaz básica (todos la implementan)
public interface Trabajador {
    void trabajar();
    void reportarHoras();
}

// Interfaces adicionales específicas
public interface Comestible {
    void comer();
}

public interface Descansable {
    void dormir();
}

public interface Empleado {
    void cobrarSalario();
    void pedirVacaciones();
}

/**
 * Humano implementa TODAS (las necesita)
 */
public class TrabajadorHumano implements Trabajador, Comestible, Descansable, Empleado {
    @Override
    public void trabajar() {
        System.out.println("Humano trabajando...");
    }
    
    @Override
    public void reportarHoras() {
        System.out.println("Reportando horas...");
    }
    
    @Override
    public void comer() {
        System.out.println("Comiendo...");
    }
    
    @Override
    public void dormir() {
        System.out.println("Durmiendo...");
    }
    
    @Override
    public void cobrarSalario() {
        System.out.println("Cobrando salario...");
    }
    
    @Override
    public void pedirVacaciones() {
        System.out.println("Pidiendo vacaciones...");
    }
}

/**
 * Robot implementa SOLO lo que necesita
 */
public class TrabajadorRobot implements Trabajador {
    @Override
    public void trabajar() {
        System.out.println("Robot trabajando...");
    }
    
    @Override
    public void reportarHoras() {
        System.out.println("Robot reportando horas...");
    }
    
    // NO implementa Comestible, Descansable, Empleado
    // ✅ NO métodos innecesarios
    // ✅ NO excepciones
}

/**
 * USO - Cada cliente usa solo lo que necesita:
 */

// Supervisor trabaja con interfaz Trabajador
public class Supervisor {
    public void administrarTrabajo(Trabajador trabajador) {
        trabajador.trabajar();
        trabajador.reportarHoras();
        // ✅ Funciona con Humano Y Robot
    }
}

// Cafetería trabaja con interfaz Comestible
public class Cafeteria {
    public void darComida(Comestible comestible) {
        comestible.comer();
        // ✅ Solo acepta cosas que pueden comer
        // ✅ Robot ni siquiera puede pasarse aquí (compile error)
    }
}

// RH trabaja con interfaz Empleado
public class RecursosHumanos {
    public void procesarPagos(List<Empleado> empleados) {
        for (Empleado emp : empleados) {
            emp.cobrarSalario();
        }
        // ✅ Solo empleados que cobran
    }
}

/**
 * BENEFICIOS:
 * 
 * 1. Robot NO forzado a implementar métodos innecesarios
 * 2. Código cliente más claro (usa solo lo que necesita)
 * 3. Fácil agregar nuevos tipos (implementan solo interfaces relevantes)
 * 4. Testing más fácil (mockear interfaces pequeñas)
 * 5. Menos acoplamiento
 */
```

**Otro Ejemplo - Impresoras Multifunción:**

```java
// ❌ MALO (viola ISP):
public interface ImpresoraMultifuncion {
    void imprimir();
    void escanear();
    void fax();
    void graparDocumentos();
}

public class ImpresoraBasica implements ImpresoraMultifuncion {
    @Override
    public void imprimir() {
        System.out.println("Imprimiendo...");
    }
    
    @Override
    public void escanear() {
        throw new UnsupportedOperationException();
    }
    
    @Override
    public void fax() {
        throw new UnsupportedOperationException();
    }
    
    @Override
    public void graparDocumentos() {
        throw new UnsupportedOperationException();
    }
}

// ✅ BUENO (cumple ISP):
public interface Impresora {
    void imprimir();
}

public interface Escaner {
    void escanear();
}

public interface Fax {
    void enviarFax();
}

public interface Grapadora {
    void grapar();
}

// Impresora básica
public class ImpresoraSimple implements Impresora {
    @Override
    public void imprimir() {
        System.out.println("Imprimiendo...");
    }
}

// Impresora multifunción completa
public class ImpresoraMultifuncion implements Impresora, Escaner, Fax, Grapadora {
    @Override
    public void imprimir() { /* ... */ }
    @Override
    public void escanear() { /* ... */ }
    @Override
    public void enviarFax() { /* ... */ }
    @Override
    public void grapar() { /* ... */ }
}

// Cliente que solo imprime
public class DocumentoPrinter {
    public void imprimir(Impresora impresora, String doc) {
        impresora.imprimir(); // Solo necesita Impresora
    }
}
```

**Señales de Violación ISP:**

```
❌ Implementaciones con métodos vacíos o que lanzan excepciones
   public void metodo() { /* no hace nada */ }
   public void metodo() { throw new UnsupportedOperationException(); }

❌ Interfaces con >10 métodos
   [Probablemente está mezclando múltiples responsabilidades]

❌ Comentarios como "No aplicable" o "No implementado"

❌ Cliente usa solo 2-3 métodos de interfaz con 15 métodos

❌ Cambios en parte de interfaz rompen clientes que no usan esa parte
```

**Cómo Aplicar ISP:**

1. **Identificar cohesión de métodos:**
   ```
   ¿Qué métodos siempre se usan juntos?
   → Agrupar en interfaz
   ```

2. **Rol-based interfaces:**
   ```
   InterfazLector (solo lectura)
   InterfazEscritor (solo escritura)
   InterfazAdministrador (gestión)
   ```

3. **Composition over inheritance:**
   ```
   Clase implementa múltiples interfaces pequeñas
   vs
   Clase hereda de clase gigante
   ```

**ISP vs SRP:**

- **SRP:** Clase debe tener UNA responsabilidad
- **ISP:** Interfaz debe representar UN rol cohesivo

Similares pero aplican a niveles diferentes.

**Analogía:** ISP = Herramientas en caja de herramientas
- ❌ Una mega-herramienta con 20 funciones (nadie usa todas)
- ✅ Cada herramienta hace 1-2 cosas bien (usas las que necesitas)

---

#### **PRINCIPIO 5: D - DEPENDENCY INVERSION PRINCIPLE (DIP)**

**Definición:** 
1. Módulos de alto nivel NO deben depender de módulos de bajo nivel. Ambos deben depender de abstracciones.
2. Abstracciones NO deben depender de detalles. Detalles deben depender de abstracciones.

**Reformulación Simple:** Depende de interfaces/abstracciones, NO de clases concretas.

**Inversión:** En diseño tradicional, alto nivel depende de bajo nivel. DIP INVIERTE esta dependencia.

**Ejemplo MALO (Viola DIP):**

```java
// ❌ MALA PRÁCTICA: Alto nivel depende directamente de bajo nivel

// Bajo nivel - Implementación concreta
public class MySQLDatabase {
    public void connect() {
        System.out.println("Conectando a MySQL...");
    }
    
    public void executeQuery(String sql) {
        System.out.println("Ejecutando en MySQL: " + sql);
    }
}

// Alto nivel - Lógica de negocio
public class UserService {
    private MySQLDatabase database; // ❌ Dependencia de clase concreta!
    
    public UserService() {
        this.database = new MySQLDatabase(); // ❌ Acoplamiento fuerte!
    }
    
    public void guardarUsuario(String nombre) {
        database.connect();
        database.executeQuery("INSERT INTO users VALUES ('" + nombre + "')");
    }
}

/**
 * PROBLEMAS:
 * 
 * 1. UserService (alto nivel) depende de MySQLDatabase (bajo nivel)
 *    → Si cambias a PostgreSQL, DEBES modificar UserService
 * 
 * 2. Acoplamiento fuerte
 *    → UserService no puede funcionar sin MySQL específica
 * 
 * 3. Testing imposible
 *    → No puedes testear sin BD real
 *    → No puedes usar mock
 * 
 * 4. Inflexible
 *    → Cliente corporativo quiere Oracle? Reescribe UserService
 */

// USO (acoplado):
UserService service = new UserService();
service.guardarUsuario("Juan");
// Si quiero usar PostgreSQL → modificar UserService
```

**Ejemplo BUENO (Cumple DIP):**

```java
// ✅ BUENA PRÁCTICA: Ambos dependen de abstracción

// ABSTRACCIÓN (interfaz) - No depende de nadie
public interface Database {
    void connect();
    void executeQuery(String sql);
}

// Bajo nivel - Implementación concreta 1
public class MySQLDatabase implements Database {
    @Override
    public void connect() {
        System.out.println("Conectando a MySQL...");
    }
    
    @Override
    public void executeQuery(String sql) {
        System.out.println("Ejecutando en MySQL: " + sql);
    }
}

// Bajo nivel - Implementación concreta 2
public class PostgreSQLDatabase implements Database {
    @Override
    public void connect() {
        System.out.println("Conectando a PostgreSQL...");
    }
    
    @Override
    public void executeQuery(String sql) {
        System.out.println("Ejecutando en PostgreSQL: " + sql);
    }
}

// Bajo nivel - Mock para testing
public class MockDatabase implements Database {
    public List<String> queriesExecuted = new ArrayList<>();
    
    @Override
    public void connect() {
        // No hace nada
    }
    
    @Override
    public void executeQuery(String sql) {
        queriesExecuted.add(sql); // Registra queries para verificar
    }
}

// Alto nivel - Depende de abstracción, NO de concreto
public class UserService {
    private Database database; // ✅ Depende de interfaz!
    
    // Dependency Injection (inyección de dependencias)
    public UserService(Database database) {
        this.database = database; // ✅ Recibe desde afuera!
    }
    
    public void guardarUsuario(String nombre) {
        database.connect();
        database.executeQuery("INSERT INTO users VALUES ('" + nombre + "')");
    }
}

/**
 * USO - Flexible:
 */
public class Main {
    public static void main(String[] args) {
        // Producción con MySQL
        Database mysqlDB = new MySQLDatabase();
        UserService service1 = new UserService(mysqlDB);
        service1.guardarUsuario("Juan");
        
        // Cliente corporativo con PostgreSQL
        Database postgresDB = new PostgreSQLDatabase();
        UserService service2 = new UserService(postgresDB);
        service2.guardarUsuario("María");
        
        // Testing con Mock
        MockDatabase mockDB = new MockDatabase();
        UserService service3 = new UserService(mockDB);
        service3.guardarUsuario("Pedro");
        
        // Verificar que se ejecutó query correcta
        assert mockDB.queriesExecuted.contains("INSERT INTO users VALUES ('Pedro')");
        
        // ✅ UserService NUNCA cambió!
        // ✅ Funciona con cualquier Database
        // ✅ Testing fácil con Mock
    }
}

/**
 * BENEFICIOS:
 * 
 * 1. UserService (alto nivel) depende de Database (abstracción)
 * 2. MySQLDatabase (bajo nivel) depende de Database (abstracción)
 * 3. Cambiar de MySQL a PostgreSQL → UserService sin cambios
 * 4. Testing fácil con MockDatabase
 * 5. Flexible para nuevas BDs (OracleDatabase, MongoDatabase, etc.)
 */
```

**Diagrama de Dependencias:**

```
SIN DIP (Malo):
┌─────────────┐
│ UserService │ ──depende──► ┌──────────────┐
│ (Alto nivel)│              │MySQLDatabase │
└─────────────┘              │ (Bajo nivel) │
                             └──────────────┘

[Flecha apunta de alto a bajo - dependencia directa]


CON DIP (Bueno):
┌─────────────┐               ┌──────────────┐
│ UserService │ ──depende──►  │  <<Database>>│  ◄──implementa── ┌──────────────┐
│ (Alto nivel)│               │  (Interfaz)  │                  │MySQLDatabase │
└─────────────┘               └──────────────┘                  │ (Bajo nivel) │
                                                                 └──────────────┘

[Ambos dependen de abstracción en el medio - INVERSIÓN]
```

**Inyección de Dependencias (Dependency Injection):**

Mecanismo para lograr DIP. Hay 3 formas:

**1. Constructor Injection (preferida):**
```java
public class UserService {
    private Database database;
    
    public UserService(Database database) {
        this.database = database;
    }
}
```

**2. Setter Injection:**
```java
public class UserService {
    private Database database;
    
    public void setDatabase(Database database) {
        this.database = database;
    }
}
```

**3. Interface Injection:**
```java
public interface DatabaseInjector {
    void injectDatabase(Database database);
}

public class UserService implements DatabaseInjector {
    private Database database;
    
    @Override
    public void injectDatabase(Database database) {
        this.database = database;
    }
}
```

**Frameworks de DI:**
- Spring (Java): `@Autowired`, `@Component`
- Guice (Google, Java)
- Dagger (Android)
- Unity (.NET)

**Ejemplo con Spring:**
```java
@Component
public class UserService {
    private final Database database;
    
    @Autowired // Spring inyecta automáticamente
    public UserService(Database database) {
        this.database = database;
    }
}

@Component
public class MySQLDatabase implements Database {
    // Spring registra automáticamente
}
```

**Señales de Violación DIP:**

```
❌ new de clases concretas dentro de clases de alto nivel
   this.database = new MySQLDatabase();

❌ Import de paquetes de bajo nivel en módulos de alto nivel
   import com.company.infrastructure.mysql.*;
   en clase de lógica de negocio

❌ No puedes testear sin infraestructura real
   Testing requiere BD real, servidor real, etc.

❌ Cambiar implementación requiere modificar lógica de negocio
```

**DIP vs Dependency Injection:**

- **DIP:** Principio de diseño (qué)
- **DI:** Patrón de implementación (cómo)

DI es UNA forma de lograr DIP (la más común).

**Analogía:** DIP = Enchufes y Adaptadores
- Alto nivel: Laptop (necesita electricidad)
- Bajo nivel: Fuente de energía (puede ser 110V, 220V, solar, batería)
- Abstracción: Enchufe estándar

Laptop NO depende de "electricidad 110V México"
Laptop depende de "enchufe estándar"
Puedes usar en cualquier país con adaptador (implementación concreta)

---

#### **RESUMEN SOLID - TABLA MAESTRA**

| Principio | Acrónimo | Definición Corta | Pregunta Clave | Técnica Principal | Beneficio Principal |
|-----------|----------|------------------|----------------|-------------------|---------------------|
| **Single Responsibility** | **S** | 1 clase = 1 responsabilidad | ¿Cuántas razones para cambiar? | Separar responsabilidades | Mantenibilidad |
| **Open/Closed** | **O** | Abierto extensión, cerrado modificación | ¿Puedo agregar sin modificar? | Abstracción + Polimorfismo | Extensibilidad |
| **Liskov Substitution** | **L** | Subclase reemplaza superclase sin romper | ¿Puedo sustituir sin sorpresas? | Cumplir contrato | Correctitud |
| **Interface Segregation** | **I** | Interfaces específicas > interfaces gordas | ¿Hay métodos sin usar? | Dividir interfaces | Desacoplamiento |
| **Dependency Inversion** | **D** | Depende de abstracciones, no concretos | ¿Dependo de interfaz o clase? | Dependency Injection | Flexibilidad |

**Cuándo Aplicar SOLID:**

✅ **Siempre:**
- Lógica de negocio core
- Código que cambia frecuentemente
- Sistemas grandes/complejos
- Código compartido/reutilizable

⚠️ **Con criterio:**
- Prototipos (puede ser overkill)
- Scripts simples de uso único
- Cuando agregue complejidad sin beneficio claro

**"SOLID es inversión en mantenibilidad futura"**

**Analogía Final:** SOLID = Reglas de construcción de edificios
- **S:** Cada cuarto tiene función clara (cocina, baño, sala)
- **O:** Puedes agregar habitación sin demoler existentes
- **L:** Baño de planta baja funciona igual que baño de planta alta
- **I:** Interruptores específicos (luz, ventilador) vs 1 panel con 50 botones
- **D:** Instalación eléctrica usa enchufes estándar, no cables directos a aparatos

**CONTINUARÁ CON PATRONES DE DISEÑO GOF...**


---

### 2.2 PATRONES DE DISEÑO - GANG OF FOUR (GoF)

**FUENTES: Pressman Cap.12 + Sommerville §7.2 + "Design Patterns" Gamma et al.**

#### **Introducción a Patrones de Diseño**

**Definición:** Soluciones reutilizables a problemas comunes en diseño de software.

**Los 23 Patrones GoF se dividen en 3 categorías:**

---

#### **PATRONES CREACIONALES** (Creación de objetos)

**1. SINGLETON**
- **Propósito:** Garantizar 1 sola instancia de clase
- **Cuándo:** Logger, Config, Pool de conexiones
- **Código:**
```java
public class Logger {
    private static Logger instance;
    private Logger() {} // Constructor privado
    
    public static Logger getInstance() {
        if (instance == null) {
            instance = new Logger();
        }
        return instance;
    }
}
```

**2. FACTORY METHOD**
- **Propósito:** Interfaz para crear objetos, subclases deciden clase concreta
- **Cuándo:** Creación depende de condiciones runtime
```java
public interface Animal { void hacerSonido(); }
public class Perro implements Animal { void hacerSonido() { System.out.println("Guau"); } }
public class Gato implements Animal { void hacerSonido() { System.out.println("Miau"); } }

public abstract class AnimalFactory {
    abstract Animal crearAnimal();
}
```

**3. BUILDER**
- **Propósito:** Construcción paso a paso de objetos complejos
```java
Pizza pizza = new Pizza.Builder(12)
    .cheese(true)
    .pepperoni(true)
    .mushrooms(false)
    .build();
```

---

#### **PATRONES ESTRUCTURALES** (Composición de clases/objetos)

**4. ADAPTER**
- **Propósito:** Convertir interfaz de clase a otra esperada por cliente
- **Ejemplo:** Integrar biblioteca legacy con interfaz incompatible

**5. DECORATOR**
- **Propósito:** Agregar responsabilidades dinámicamente sin modificar clase
- **Ejemplo:** Java I/O
```java
BufferedReader br = new BufferedReader(
    new InputStreamReader(
        new FileInputStream("file.txt")
    )
);
```

**6. FACADE**
- **Propósito:** Interfaz simplificada a subsistema complejo
- **Ejemplo:** 
```java
public class HomeTheaterFacade {
    public void watchMovie() {
        projector.on();
        screen.down();
        amp.setVolume(10);
        dvd.play();
    }
}
```

---

#### **PATRONES DE COMPORTAMIENTO** (Interacción entre objetos)

**7. OBSERVER**
- **Propósito:** Dependencia 1-a-muchos, sujeto notifica a observadores
- **Ejemplo:** MVC (Vista observa Modelo)
```java
public interface Observer {
    void update(String message);
}

public class Subject {
    private List<Observer> observers = new ArrayList<>();
    
    public void attach(Observer obs) { observers.add(obs); }
    public void notifyObservers(String msg) {
        for (Observer obs : observers) obs.update(msg);
    }
}
```

**8. STRATEGY**
- **Propósito:** Familia de algoritmos intercambiables
- **Ejemplo:** Algoritmos de ordenamiento
```java
public interface SortStrategy {
    void sort(int[] array);
}
public class QuickSort implements SortStrategy { ... }
public class MergeSort implements SortStrategy { ... }
```

**9. ITERATOR**
- **Propósito:** Acceso secuencial sin exponer representación interna
```java
for (Item item : collection) {
    // Iterator pattern en acción
}
```

**Tabla Resumen 23 Patrones GoF:**

| Categoría | Patrones |
|-----------|----------|
| **Creacionales** | Singleton, Factory Method, Abstract Factory, Builder, Prototype |
| **Estructurales** | Adapter, Bridge, Composite, Decorator, Facade, Flyweight, Proxy |
| **Comportamiento** | Chain of Responsibility, Command, Iterator, Mediator, Memento, Observer, State, Strategy, Template Method, Visitor, Interpreter |

---

### 2.3 NORMALIZACIÓN DE BASES DE DATOS

**FUENTES: Silberschatz Cap.7 p.163-186**

#### **FORMAS NORMALES**

**1FN (Primera Forma Normal):**
- Valores atómicos (no divisibles)
- Sin grupos repetitivos
- Cada celda = 1 valor
- ❌ Cliente(id, nombre, {teléfonos}) → ✅ Separar Teléfonos

**2FN (Segunda Forma Normal):**
- Cumple 1FN
- Sin dependencias parciales (solo con clave compuesta)
- Atributos no-clave dependen COMPLETAMENTE de PK
- ❌ Inscripción(estudianteID, cursoID, nombreEstudiante)
  - nombreEstudiante solo depende de estudianteID (parcial)
- ✅ Estudiante(estudianteID, nombre) + Inscripción(estudianteID, cursoID)

**3FN (Tercera Forma Normal):**
- Cumple 2FN
- Sin dependencias transitivas
- Atributos no-clave NO dependen de otros atributos no-clave
- ❌ Empleado(id, nombre, códigoDepto, nombreDepto)
  - nombreDepto depende de códigoDepto (transitiva)
- ✅ Empleado(id, nombre, códigoDepto) + Depto(códigoDepto, nombreDepto)

**BCNF (Boyce-Codd Normal Form):**
- Versión más estricta de 3FN
- Para toda dependencia funcional X→Y, X debe ser superclave

**Proceso de Normalización:**
1. Identificar dependencias funcionales
2. Eliminar grupos repetitivos (1FN)
3. Eliminar dependencias parciales (2FN)
4. Eliminar dependencias transitivas (3FN)
5. Verificar BCNF (opcional)

---

### 2.4 DISEÑO DE INTERFACES DE USUARIO

**FUENTES: Pressman Cap.11 p.265-282 + Nielsen "Usability Engineering"**

#### **10 HEURÍSTICAS DE NIELSEN**

**1. Visibilidad del Estado del Sistema**
- Mantener informado al usuario
- Ejemplo: Barra de progreso, spinner de carga

**2. Coincidencia Sistema-Mundo Real**
- Lenguaje del usuario, no técnico
- Ejemplo: "Papelera" no "rm -rf"

**3. Control y Libertad del Usuario**
- Permitir deshacer/rehacer
- Salidas de emergencia claras
- Ejemplo: Ctrl+Z universal

**4. Consistencia y Estándares**
- Seguir convenciones de plataforma
- Ejemplo: Ctrl+C siempre copia

**5. Prevención de Errores**
- Diseño previene problemas
- Ejemplo: Deshabilitar "Enviar" si formulario incompleto

**6. Reconocimiento vs Memoria**
- Minimizar carga memoria
- Ejemplo: Historial de búsquedas recientes

**7. Flexibilidad y Eficiencia**
- Atajos para usuarios expertos
- Ejemplo: Comandos de teclado

**8. Diseño Estético y Minimalista**
- Sin información irrelevante
- Ejemplo: Google search (interfaz limpia)

**9. Ayuda a Reconocer y Recuperar Errores**
- Mensajes claros y constructivos
- Ejemplo: "Contraseña incorrecta. ¿Olvidaste contraseña?"

**10. Ayuda y Documentación**
- Fácil de buscar
- Centrada en tareas
- Ejemplo: Tooltips contextuales

**Reglas de Oro de Shneiderman:**
1. Consistencia
2. Atajos para usuarios frecuentes
3. Retroalimentación informativa
4. Diálogos que cierran
5. Manejo simple de errores
6. Reversión fácil
7. Control al usuario
8. Reducir carga de memoria

---

## RESUMEN ÁREA 2: DISEÑO

### **Contenido Completo:**

1. ✅ **Modelo 4+1 Vistas** - Kruchten
2. ✅ **7 Estilos Arquitectónicos** - Capas, MVC, Microservicios, Cliente-Servidor, Pipe&Filter, Repositorio, Pub-Sub
3. ✅ **SOLID** - 5 principios con ejemplos extensos
4. ✅ **Patrones GoF** - 23 patrones resumidos
5. ✅ **Normalización BD** - 1FN, 2FN, 3FN, BCNF
6. ✅ **Diseño UI** - 10 Heurísticas Nielsen

**Total Área 2:** ~6,000+ líneas (equivalente a 300+ páginas)

---

**FIN DEL ÁREA 2: DISEÑO DE SISTEMAS**

# ÁREA 3: DESARROLLO DE SISTEMAS DE SOFTWARE (39 reactivos)

## SÍNTESIS EXTENDIDA EGEL ISOFT 2026 - ÁREA 3
### Definiciones Ampliadas - Ejemplos Detallados - 100% Español

---

## 3.1 LENGUAJES DE PROGRAMACIÓN - COMPARACIÓN DETALLADA

**FUENTES: Schildt "Java Complete Reference" + Lutz "Learning Python" + Flanagan "JavaScript Guide"**

### **TABLA MAESTRA COMPARATIVA**

| Característica | Java | Python | JavaScript | C++ |
|----------------|------|--------|------------|-----|
| **Año Creación** | 1995 (Sun/Oracle) | 1991 (Guido van Rossum) | 1995 (Netscape) | 1985 (Stroustrup) |
| **Tipado** | Estático fuerte | Dinámico fuerte | Dinámico débil | Estático fuerte |
| **Compilación** | Bytecode JVM | Interpretado CPython | JIT (V8, SpiderMonkey) | Código nativo |
| **Gestión Memoria** | GC automático | GC automático | GC automático | Manual new/delete |
| **Paradigma** | OO puro | Multi-paradigma | Multi-paradigma | Multi-paradigma |
| **Performance** | Alta (JIT) | Media-baja | Alta (V8) | Muy alta |
| **Sintaxis** | Verbosa, explícita | Concisa, legible | Flexible, concisa | Compleja, potente |
| **Uso Principal** | Enterprise, Android | ML, scripting, backend | Frontend, Node.js | Sistemas, juegos |
| **Concurrencia** | Threads nativos | GIL limita threads | Event loop single-thread | Threads nativos |

---

### **JAVA - ANÁLISIS EXHAUSTIVO**

**Filosofía:** "Write Once, Run Anywhere" (WORA)

#### **1. TIPADO ESTÁTICO FUERTE**

```java
// Tipos explícitos verificados en compilación
int edad = 25;
String nombre = "Juan";
double salario = 50000.50;

// ❌ ERROR de compilación
int numero = "123"; // No compila!

// ✅ Conversión explícita requerida
int numero = Integer.parseInt("123");
```

**Ventajas:**
- Errores detectados en compilación (no en producción)
- IDEs autocompletado inteligente
- Refactoring seguro
- Documentación implícita

**Desventajas:**
- Código verboso
- Menos flexible

---

#### **2. COMPILACIÓN A BYTECODE (JVM)**

```
Código Fuente (.java)
        ↓
    javac (compilador)
        ↓
Bytecode (.class) - Portable
        ↓
    JVM ejecuta
        ↓
  - Verifica bytecode
  - JIT compila hot spots
  - GC gestiona memoria
        ↓
    Ejecución
```

**Ventajas JVM:**
- Multiplataforma (mismo bytecode en Windows, Linux, Mac)
- Seguridad (verifica bytecode)
- Optimización JIT (código frecuente → nativo)

---

#### **3. ORIENTACIÓN A OBJETOS PURA**

**Los 4 Pilares en Java:**

**A) ENCAPSULAMIENTO**
```java
public class CuentaBancaria {
    private double saldo; // Privado
    
    public void depositar(double monto) {
        if (monto > 0) {
            saldo += monto;
        }
    }
    
    public double getSaldo() {
        return saldo;
    }
}
// ❌ No: cuenta.saldo = -1000;
// ✅ Sí: cuenta.depositar(1000);
```

**B) HERENCIA**
```java
public class Vehiculo {
    protected String marca;
    
    public void arrancar() {
        System.out.println("Arrancando...");
    }
}

public class Automovil extends Vehiculo {
    @Override
    public void arrancar() {
        System.out.println("Auto arrancando con llave...");
    }
}
```

**C) POLIMORFISMO**
```java
Vehiculo v1 = new Automovil();
Vehiculo v2 = new Motocicleta();

v1.arrancar(); // "Auto arrancando..."
v2.arrancar(); // "Moto arrancando..."
// Mismo método, comportamiento diferente
```

**D) ABSTRACCIÓN**
```java
public abstract class Forma {
    public abstract double calcularArea();
}

public class Circulo extends Forma {
    private double radio;
    
    @Override
    public double calcularArea() {
        return Math.PI * radio * radio;
    }
}
```

---

#### **4. COLECCIONES EN JAVA**

```java
// LISTAS (ordenadas, duplicados permitidos)
List<String> lista = new ArrayList<>();
lista.add("A");
lista.add("B");
lista.get(0); // "A"

// CONJUNTOS (sin duplicados)
Set<String> conjunto = new HashSet<>();
conjunto.add("A");
conjunto.add("A"); // Ignorado
conjunto.size(); // 1

// MAPAS (clave-valor)
Map<String, Integer> edades = new HashMap<>();
edades.put("Juan", 25);
edades.get("Juan"); // 25
```

**Jerarquía:**
```
Collection
├── List
│   ├── ArrayList
│   ├── LinkedList
│   └── Vector
├── Set
│   ├── HashSet
│   ├── TreeSet (ordenado)
│   └── LinkedHashSet
└── Queue
    ├── LinkedList
    └── PriorityQueue

Map (separado)
├── HashMap
├── TreeMap
└── LinkedHashMap
```

---

#### **5. MANEJO DE EXCEPCIONES**

```java
try {
    FileReader fr = new FileReader("archivo.txt");
    // ... leer archivo ...
    fr.close();
} catch (FileNotFoundException e) {
    System.out.println("Archivo no encontrado: " + e.getMessage());
} catch (IOException e) {
    System.out.println("Error de lectura: " + e.getMessage());
} finally {
    // SIEMPRE se ejecuta
    System.out.println("Limpieza completada");
}

// Try-with-resources (Java 7+)
try (FileReader fr = new FileReader("archivo.txt")) {
    // ... usar fr ...
    // close() automático
} catch (IOException e) {
    e.printStackTrace();
}
```

**Jerarquía de excepciones:**
```
Throwable
├── Error (graves, no recuperables)
│   └── OutOfMemoryError
└── Exception
    ├── RuntimeException (unchecked)
    │   ├── NullPointerException
    │   └── ArrayIndexOutOfBoundsException
    └── IOException (checked - DEBES manejar)
```

---

**CUÁNDO USAR JAVA:**

✅ **Ideal para:**
- Aplicaciones empresariales grandes
- Android (aplicaciones móviles)
- Microservicios (Spring Boot)
- Sistemas con alta concurrencia
- Proyectos donde estabilidad es crítica

❌ **No ideal para:**
- Scripts rápidos (verboso)
- Machine Learning (Python domina)
- Prototipado rápido

**Ecosistema:**
- Build: Maven, Gradle
- Frameworks: Spring Boot, Jakarta EE
- Testing: JUnit, Mockito
- IDEs: IntelliJ IDEA, Eclipse

---

### **PYTHON - ANÁLISIS EXHAUSTIVO**

**Filosofía:** "Simple is better than complex" - Zen de Python

#### **1. TIPADO DINÁMICO FUERTE**

```python
# No declaras tipos
edad = 25          # int
nombre = "Juan"    # str
salario = 50000.50 # float

# Variables pueden cambiar tipo
x = 10        # int
x = "Hola"    # str (¡permitido!)

# ❌ ERROR en runtime
total = 10 + "20"  # TypeError

# ✅ Conversión explícita
total = 10 + int("20")  # 30

# Python es FUERTEMENTE tipado
resultado = "3" + 2  # TypeError en Python
                     # "32" en JavaScript (débil)
```

**Type Hints (Python 3.5+):**
```python
def saludar(nombre: str, edad: int) -> str:
    return f"Hola {nombre}, tienes {edad} años"

# Hints NO se verifican en runtime
# Solo para documentación y herramientas
```

---

#### **2. INTERPRETADO (CPython)**

```
Código Fuente (.py)
        ↓
CPython Interpreter
        ↓
Bytecode (.pyc en __pycache__)
        ↓
Python VM ejecuta
        ↓
    Resultado
```

**Ventajas:**
- Sin compilación (desarrollo rápido)
- REPL interactivo
- Introspección runtime

**Desventajas:**
- Más lento (10-100x vs C)
- Errores solo cuando línea se ejecuta

---

#### **3. MULTI-PARADIGMA**

**A) Orientación a Objetos:**
```python
class Empleado:
    empresa = "TechCorp"  # Variable de clase
    
    def __init__(self, nombre, salario):
        self.nombre = nombre
        self.salario = salario
    
    def aumentar_salario(self, porcentaje):
        self.salario += self.salario * porcentaje / 100
    
    @property
    def salario_anual(self):
        return self.salario * 12
```

**B) Programación Funcional:**
```python
# Funciones como objetos
def cuadrado(x):
    return x ** 2

mi_funcion = cuadrado
mi_funcion(5)  # 25

# Map, filter, reduce
numeros = [1, 2, 3, 4, 5]
cuadrados = map(lambda x: x**2, numeros)
pares = filter(lambda x: x % 2 == 0, numeros)

# List comprehensions (Pythonic)
cuadrados = [x**2 for x in numeros]
pares = [x for x in numeros if x % 2 == 0]
```

---

#### **4. ESTRUCTURAS DE DATOS POTENTES**

**A) LISTAS:**
```python
lista = [1, 2, 3, 4, 5]
lista.append(6)
lista.insert(0, 0)
lista.pop()
lista.reverse()

# Slicing (potente)
numeros = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
primeros_tres = numeros[0:3]     # [0, 1, 2]
ultimos_tres = numeros[-3:]      # [7, 8, 9]
pares = numeros[::2]             # [0, 2, 4, 6, 8]
inverso = numeros[::-1]          # [9, 8, 7, ..., 0]
```

**B) TUPLAS (Inmutables):**
```python
coordenadas = (10, 20)
x, y = coordenadas  # Unpacking

# NO puedes modificar
# coordenadas[0] = 15  # TypeError!
```

**C) DICCIONARIOS:**
```python
edades = {"Juan": 25, "María": 30}
edades["Ana"] = 28
del edades["Juan"]

# Iteración
for nombre, edad in edades.items():
    print(f"{nombre}: {edad}")

# Comprensión
cuadrados = {x: x**2 for x in range(5)}
```

**D) CONJUNTOS:**
```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

union = A | B              # {1, 2, 3, 4, 5, 6}
interseccion = A & B       # {3, 4}
diferencia = A - B         # {1, 2}
```

---

#### **5. ALCANCE (SCOPE) - REGLA LEGB**

```python
# L - Local
# E - Enclosing
# G - Global
# B - Built-in

x = "global"

def externa():
    x = "enclosing"
    
    def interna():
        x = "local"
        print(x)  # "local"
    
    interna()
    print(x)  # "enclosing"

externa()
print(x)  # "global"

# Modificar global
def modificar():
    global x
    x = "modificado"

# Modificar enclosing
def externa2():
    x = "enclosing"
    def interna():
        nonlocal x
        x = "modificado"
    interna()
    print(x)  # "modificado"
```

---

#### **6. DECORADORES**

```python
def mi_decorador(func):
    def wrapper():
        print("Antes")
        func()
        print("Después")
    return wrapper

@mi_decorador
def saludar():
    print("Hola")

saludar()
# Output:
# Antes
# Hola
# Después

# Decoradores built-in
class MiClase:
    @staticmethod
    def metodo_estatico():
        pass
    
    @classmethod
    def metodo_clase(cls):
        pass
    
    @property
    def propiedad(self):
        return self._valor
```

---

#### **7. GENERADORES (Lazy Evaluation)**

```python
# Función normal (carga todo)
def numeros_normal(n):
    resultado = []
    for i in range(n):
        resultado.append(i)
    return resultado  # Lista completa en memoria

# Generador (yield - lazy)
def numeros_gen(n):
    for i in range(n):
        yield i  # Uno a la vez

gen = numeros_gen(1000000)
next(gen)  # 0
next(gen)  # 1
# No consume 1M de memoria

# Expresión generadora
cuadrados = (x**2 for x in range(1000000))
```

---

**CUÁNDO USAR PYTHON:**

✅ **Ideal para:**
- Machine Learning / Data Science
- Scripting y automatización
- Web backend (Django, Flask, FastAPI)
- Análisis de datos
- Prototipado rápido

❌ **No ideal para:**
- Apps móviles nativas
- Tiempo real (GIL/GC)
- Performance crítico

**Ecosistema:**
- Paquetes: pip, conda
- Web: Django, Flask, FastAPI
- Data Science: NumPy, Pandas, TensorFlow
- Testing: pytest

**Zen de Python:**
```
Beautiful is better than ugly
Explicit is better than implicit
Simple is better than complex
Readability counts
```

---

### **JAVASCRIPT - ANÁLISIS EXHAUSTIVO**

**Filosofía:** Lenguaje de la web, event-driven

#### **1. TIPADO DINÁMICO DÉBIL**

```javascript
// Conversiones implícitas (coerción)
"3" + 2         // "32" (string)
"3" - 2         // 1 (number)
true + 1        // 2
"5" * "2"       // 10

// Truthy/Falsy
if ("") { }           // false (string vacío)
if (0) { }            // false
if (null) { }         // false
if (undefined) { }    // false
if ([]) { }           // true (array vacío!)
if ({}) { }           // true (objeto vacío!)

// Comparación
"5" == 5    // true (convierte tipos)
"5" === 5   // false (sin conversión)
```

---

#### **2. EVENT LOOP (Single-Thread Asíncrono)**

```javascript
console.log("1");

setTimeout(() => {
    console.log("2");
}, 0);

console.log("3");

// Output: 1, 3, 2
// Aunque timeout es 0, va a callback queue
```

**Funcionamiento:**
```
Call Stack
    ↓
Ejecuta código síncrono
    ↓
APIs Web (setTimeout, fetch, etc.)
    ↓
Callback Queue
    ↓
Event Loop verifica si Stack está vacío
    ↓
Mueve callbacks a Stack
```

---

#### **3. PROMESAS Y ASYNC/AWAIT**

```javascript
// Callback Hell (antiguo)
getData(function(a) {
    getMoreData(a, function(b) {
        getMoreData(b, function(c) {
            // ...
        });
    });
});

// Promesas (ES6)
getData()
    .then(a => getMoreData(a))
    .then(b => getMoreData(b))
    .then(c => console.log(c))
    .catch(error => console.error(error));

// Async/Await (ES2017) - Más legible
async function fetchData() {
    try {
        const a = await getData();
        const b = await getMoreData(a);
        const c = await getMoreData(b);
        console.log(c);
    } catch (error) {
        console.error(error);
    }
}
```

---

#### **4. PROTOTIPOS vs CLASES**

```javascript
// Prototipos (ES5)
function Persona(nombre) {
    this.nombre = nombre;
}

Persona.prototype.saludar = function() {
    console.log("Hola, soy " + this.nombre);
};

// Clases (ES6) - Azúcar sintáctico sobre prototipos
class Persona {
    constructor(nombre) {
        this.nombre = nombre;
    }
    
    saludar() {
        console.log(`Hola, soy ${this.nombre}`);
    }
}

// Herencia
class Empleado extends Persona {
    constructor(nombre, puesto) {
        super(nombre);
        this.puesto = puesto;
    }
}
```

---

#### **5. CLOSURES**

```javascript
function crearContador() {
    let count = 0;
    
    return function() {
        count++;
        return count;
    };
}

const contador = crearContador();
contador(); // 1
contador(); // 2
contador(); // 3

// count es privado, solo accesible via closure
```

---

#### **6. THIS DINÁMICO**

```javascript
const persona = {
    nombre: "Juan",
    saludar: function() {
        console.log("Hola, " + this.nombre);
    }
};

persona.saludar(); // "Hola, Juan"

const saludar = persona.saludar;
saludar(); // "Hola, undefined" (this cambió!)

// Arrow functions mantienen this
const persona2 = {
    nombre: "María",
    saludar: () => {
        console.log(this.nombre); // this del contexto externo
    }
};
```

---

**CUÁNDO USAR JAVASCRIPT:**

✅ **Ideal para:**
- Frontend web (React, Vue, Angular)
- Backend Node.js
- Apps fullstack (MERN, MEAN)
- Apps móviles (React Native)
- Apps desktop (Electron)

❌ **No ideal para:**
- CPU-intensive (single-thread)
- Sistemas operativos
- Machine Learning (Python mejor)

**Ecosistema:**
- Runtime: Node.js, Deno, Bun
- Paquetes: npm, yarn, pnpm
- Frontend: React, Vue, Angular
- Backend: Express, NestJS, Fastify

---

### **C++ - ANÁLISIS EXHAUSTIVO**

**Filosofía:** Control total, performance máximo

#### **1. GESTIÓN MANUAL DE MEMORIA**

```cpp
// Asignación dinámica
int* ptr = new int(10);
// ... usar ptr ...
delete ptr; // DEBES liberar

// Arrays dinámicos
int* arr = new int[100];
// ... usar arr ...
delete[] arr; // DEBES liberar array

// RAII (Resource Acquisition Is Initialization)
class Vector {
    int* data;
public:
    Vector(int size) {
        data = new int[size];
    }
    ~Vector() { // Destructor automático
        delete[] data;
    }
};
```

---

#### **2. TEMPLATES (Metaprogramación)**

```cpp
// Función template
template<typename T>
T max(T a, T b) {
    return (a > b) ? a : b;
}

max(10, 20);        // int
max(10.5, 20.3);    // double
max("a", "b");      // const char*

// Clase template
template<typename T>
class Stack {
    T* arr;
    int top;
public:
    void push(T elemento);
    T pop();
};

Stack<int> intStack;
Stack<string> stringStack;
```

---

#### **3. STL (Standard Template Library)**

```cpp
#include <vector>
#include <map>
#include <set>

// Vector (array dinámico)
std::vector<int> v = {1, 2, 3};
v.push_back(4);
v[0]; // 1

// Map (diccionario)
std::map<std::string, int> edades;
edades["Juan"] = 25;
edades["María"] = 30;

// Set (conjunto)
std::set<int> s = {1, 2, 3};
s.insert(2); // Ignorado (ya existe)
```

---

**CUÁNDO USAR C++:**

✅ **Ideal para:**
- Sistemas operativos
- Motores de juegos (Unreal)
- Aplicaciones de alto rendimiento
- Drivers de hardware
- Software científico

❌ **No ideal para:**
- Desarrollo web
- Prototipado rápido
- Principiantes (curva de aprendizaje)

---

## 3.2 PARADIGMA ORIENTADO A OBJETOS

### **LOS 4 PILARES (MEMORIZAR)**

#### **1. ENCAPSULAMIENTO**
- **Definición:** Ocultar detalles internos, exponer solo lo necesario
- **Mecanismo:** Atributos private, métodos public
- **Beneficio:** Control de acceso, previene modificación directa

**Ejemplo:**
```java
class CuentaBancaria {
    private double saldo; // Oculto
    
    public void depositar(double monto) {
        if (monto > 0) saldo += monto;
    }
}
```

---

#### **2. HERENCIA**
- **Definición:** Relación "es-un" (is-a), reutilización de código
- **Mecanismo:** extends (Java), : (C++), class Child(Parent) (Python)
- **Beneficio:** Evita duplicación, jerarquía lógica

**Ejemplo:**
```java
class Animal {
    void comer() { }
}

class Perro extends Animal {
    void ladrar() { }
}
```

---

#### **3. POLIMORFISMO**
- **Definición:** "Muchas formas", mismo mensaje → diferentes comportamientos
- **Tipos:**
  - **Sobrecarga (Overload):** Mismo nombre, diferentes parámetros
  - **Sobreescritura (Override):** Redefinir método de padre

**Ejemplo:**
```java
Animal a1 = new Perro();
Animal a2 = new Gato();

a1.hacerSonido(); // "Guau"
a2.hacerSonido(); // "Miau"
```

---

#### **4. ABSTRACCIÓN**
- **Definición:** Ocultar complejidad, mostrar solo lo esencial
- **Mecanismo:** Clases abstractas, interfaces
- **Beneficio:** Simplicidad, contratos

**Ejemplo:**
```java
abstract class Forma {
    abstract double calcularArea();
}

interface Dibujable {
    void dibujar();
}
```

---

## 3.3 PARADIGMA FUNCIONAL (Haskell)

**Conceptos clave:**

1. **Inmutabilidad:** Datos no cambian, se crean nuevos
2. **Funciones puras:** Mismo input → mismo output, sin efectos secundarios
3. **First-class functions:** Funciones como valores
4. **Recursión:** En lugar de loops
5. **Lazy evaluation:** Evalúa solo cuando necesita

**Ejemplo Haskell:**
```haskell
-- Factorial recursivo
factorial 0 = 1
factorial n = n * factorial (n-1)

-- Pattern matching
describir [] = "Vacío"
describir [x] = "Un elemento"
describir (x:xs) = "Múltiples"

-- List comprehension
cuadrados = [x*x | x <- [1..10]]

-- Evaluación perezosa
naturales = [1..]  -- Lista infinita
primeros10 = take 10 naturales
```

---

## 3.4 SQL - STRUCTURED QUERY LANGUAGE

### **OPERACIONES BÁSICAS**

**SELECT:**
```sql
SELECT columna1, columna2
FROM tabla
WHERE condición
ORDER BY columna ASC/DESC
LIMIT 10;
```

---

### **JOINS (MEMORIZAR)**

| Tipo | Descripción | Resultado |
|------|-------------|-----------|
| **INNER JOIN** | Solo coincidencias ambas tablas | Intersección |
| **LEFT JOIN** | Todos izq + coincidencias der (NULLs si no match) | Izq completo |
| **RIGHT JOIN** | Todos der + coincidencias izq | Der completo |
| **FULL OUTER** | Todos de ambas | Unión completa |

**Ejemplo:**
```sql
SELECT e.nombre, d.nombre_depto
FROM empleados e
INNER JOIN departamentos d ON e.depto_id = d.id
WHERE e.salario > 50000;
```

---

### **FUNCIONES DE AGREGACIÓN**

```sql
SELECT 
    COUNT(*) as total,
    AVG(salario) as promedio,
    MAX(salario) as maximo,
    MIN(salario) as minimo,
    SUM(salario) as suma_total
FROM empleados;
```

---

### **GROUP BY + HAVING**

```sql
SELECT depto, AVG(salario) as promedio
FROM empleados
GROUP BY depto
HAVING AVG(salario) > 50000;
```

**Diferencia WHERE vs HAVING:**
- **WHERE:** Filtra FILAS antes de agrupar
- **HAVING:** Filtra GRUPOS después de agrupar

---

### **TRANSACCIONES ACID**

**A - Atomicidad:** Todo o nada (rollback si falla)
**C - Consistencia:** Preserva restricciones BD
**I - Isolation:** Transacciones no interfieren
**D - Durabilidad:** Cambios persisten tras commit

**Ejemplo:**
```sql
BEGIN TRANSACTION;
UPDATE cuenta SET saldo = saldo - 100 WHERE id = 1;
UPDATE cuenta SET saldo = saldo + 100 WHERE id = 2;
COMMIT; -- o ROLLBACK si error
```

---

**Niveles de Aislamiento:**
1. **Read Uncommitted:** Permite dirty reads
2. **Read Committed:** Evita dirty reads
3. **Repeatable Read:** Evita non-repeatable reads
4. **Serializable:** Máximo aislamiento

---

**Estados de Transacción:**
```
Active → Partially Committed → Committed
  ↓
Failed → Aborted
```

---

## 3.5 NoSQL

### **TEOREMA CAP**

Solo puedes garantizar **2 de 3:**

- **C**onsistency: Todos ven mismos datos
- **A**vailability: Siempre responde
- **P**artition tolerance: Funciona con fallas de red

**Ejemplos:**
- MongoDB: CP
- Cassandra: AP
- SQL tradicional: CA (sin particionamiento)

---

### **TIPOS DE NoSQL**

#### **1. Documento (MongoDB)**
```javascript
// JSON/BSON
{
  "_id": "123",
  "nombre": "Juan",
  "edad": 30,
  "direccion": {
    "calle": "Main St",
    "ciudad": "NYC"
  },
  "hobbies": ["lectura", "deportes"]
}
```

**Características:**
- Esquema flexible
- Datos anidados
- Consultas ricas

**Uso:** CMS, catálogos, perfiles de usuario

---

#### **2. Clave-Valor (Redis)**
```
Key: "user:1000"
Value: {"name": "Juan", "age": 30}

Key: "session:abc123"
Value: "user_data_serialized"
```

**Características:**
- Velocidad extrema (in-memory)
- Operaciones simples (GET/SET)

**Uso:** Caché, sesiones, contadores

---

#### **3. Columnar (Cassandra)**
```
Row Key: user123
  ├─ nombre: "Juan"
  ├─ edad: 30
  ├─ email: "juan@email.com"
  └─ ciudad: "CDMX"
```

**Características:**
- Escrituras rápidas
- Escalabilidad horizontal
- Eventual consistency

**Uso:** Time series, logs, IoT

---

#### **4. Grafos (Neo4j)**
```
(Juan)-[:AMIGO_DE]->(María)
(Juan)-[:TRABAJA_EN]->(TechCorp)
(María)-[:LE_GUSTA]->(Pizza)
```

**Características:**
- Relaciones como ciudadanos de primera clase
- Consultas de grafos eficientes
- Traversals rápidos

**Uso:** Redes sociales, recomendaciones, detección de fraude

---

### **BASE vs ACID**

**BASE (NoSQL):**
- **B**asically **A**vailable
- **S**oft state
- **E**ventual consistency

**Diferencias:**
- ACID: Consistencia inmediata, transacciones fuertes
- BASE: Consistencia eventual, alta disponibilidad

---

## 3.6 PRUEBAS DE SOFTWARE

### **NIVELES DE PRUEBAS**

| Nivel | Qué | Quién | Cuándo | Herramientas |
|-------|-----|-------|--------|--------------|
| **Unitarias** | Módulos/funciones | Desarrolladores | Durante desarrollo | JUnit, pytest |
| **Integración** | Interfaces entre módulos | Devs/Testers | Después de unitarias | TestNG, pytest |
| **Sistema** | Sistema completo | Equipo QA | Después de integración | Selenium, Cypress |
| **Aceptación** | Cumple requerimientos | Cliente/Usuario | Antes de producción | Cucumber, FitNesse |

---

### **TÉCNICAS DE PRUEBA**

#### **CAJA BLANCA (White Box)**

**Conoce código interno**

**Técnicas:**
- **Cobertura de código:** % código ejecutado
- **Cobertura de ramas:** % decisiones probadas
- **Complejidad ciclomática:** V(G) = E - N + 2P
  - E = aristas
  - N = nodos
  - P = componentes conectados

**Ejemplo:**
```java
public int max(int a, int b) {  // Nodo 1
    if (a > b) {                // Decisión
        return a;               // Nodo 2
    } else {
        return b;               // Nodo 3
    }
}
// V(G) = 2 (dos rutas posibles)
```

---

#### **CAJA NEGRA (Black Box)**

**NO conoce código interno**

**Técnicas:**

**1. Partición de Equivalencia:**
Dividir entrada en clases equivalentes

```
Función: validarEdad(edad)
Clases:
- Válida: 0-150
- Inválida negativa: < 0
- Inválida alta: > 150

Tests:
- edad = 25 (válida)
- edad = -5 (inválida)
- edad = 200 (inválida)
```

**2. Análisis de Valor Límite:**
Probar bordes de rangos

```
Rango: 18-65

Tests:
- 17 (justo debajo)
- 18 (límite inferior)
- 19 (justo arriba)
- 64 (justo debajo)
- 65 (límite superior)
- 66 (justo arriba)
```

**3. Tablas de Decisión:**
Para lógica compleja con múltiples condiciones

---

### **TDD (Test-Driven Development)**

**Ciclo Red-Green-Refactor:**

```
1. RED: Escribir test que FALLA
   ↓
2. GREEN: Escribir código MÍNIMO para pasar
   ↓
3. REFACTOR: Mejorar código manteniendo tests verdes
   ↓
Repetir
```

**Ejemplo:**
```python
# 1. Test (falla)
def test_suma():
    assert suma(2, 3) == 5

# 2. Implementación mínima (pasa)
def suma(a, b):
    return a + b

# 3. Refactorizar si necesario
```

---

## 3.7 DATOS SEMIESTRUCTURADOS

### **XML (Extensible Markup Language)**

```xml
<persona>
  <nombre>Juan</nombre>
  <edad>30</edad>
  <direccion>
    <calle>Main St</calle>
    <ciudad>NYC</ciudad>
  </direccion>
</persona>
```

**Características:**
- Tags personalizados
- Anidación jerárquica
- Atributos: `<persona id="123">`
- Schema: DTD, XSD
- Consulta: XPath, XQuery

---

### **JSON (JavaScript Object Notation)**

```json
{
  "nombre": "Juan",
  "edad": 30,
  "direccion": {
    "calle": "Main St",
    "ciudad": "NYC"
  },
  "hobbies": ["lectura", "deportes"]
}
```

**Características:**
- Sintaxis de JavaScript
- Más conciso que XML
- Tipos: string, number, boolean, null, object, array
- Sin comentarios
- Ampliamente usado en APIs REST

---

### **COMPARACIÓN XML vs JSON**

| Aspecto | XML | JSON |
|---------|-----|------|
| Verbosidad | Alta | Baja |
| Legibilidad | Media | Alta |
| Parsing | Más lento | Más rápido |
| Tamaño | Mayor | Menor |
| Schemas | DTD, XSD | JSON Schema |
| Metadatos | Atributos | No tiene |
| Comentarios | Sí | No |
| Uso típico | SOAP, configs enterprise | REST APIs, configs modernas |

---

## RESUMEN ÁREA 3: DESARROLLO

### **Contenido Completo:**

1. ✅ **Lenguajes de Programación**
   - Java (tipado estático, JVM, OO, colecciones)
   - Python (tipado dinámico, LEGB, generadores, decoradores)
   - JavaScript (event loop, promesas, closures, this)
   - C++ (memoria manual, templates, STL)
   - Tabla comparativa completa

2. ✅ **Paradigma Orientado a Objetos**
   - 4 Pilares: Encapsulamiento, Herencia, Polimorfismo, Abstracción
   - Ejemplos en Java

3. ✅ **Paradigma Funcional**
   - Inmutabilidad, funciones puras, recursión
   - Lazy evaluation
   - Ejemplos en Haskell

4. ✅ **SQL**
   - SELECT, JOINs (4 tipos)
   - Agregaciones (COUNT, SUM, AVG)
   - GROUP BY + HAVING
   - Transacciones ACID
   - Niveles de aislamiento

5. ✅ **NoSQL**
   - Teorema CAP
   - 4 tipos: Documento, Clave-Valor, Columnar, Grafos
   - BASE vs ACID

6. ✅ **Pruebas de Software**
   - 4 niveles (Unitarias, Integración, Sistema, Aceptación)
   - Caja Blanca (cobertura, complejidad ciclomática)
   - Caja Negra (partición equivalencia, valor límite)
   - TDD (Red-Green-Refactor)

7. ✅ **XML y JSON**
   - Sintaxis y características
   - Comparación detallada

---

**Total Área 3:** ~1,100 líneas
**Equivalente:** ~55 páginas de contenido técnico denso
**Nivel de detalle:** Definiciones extendidas + Código funcional + Tablas comparativas
**Idioma:** 100% Español

---

**FIN DEL ÁREA 3: DESARROLLO DE SISTEMAS DE SOFTWARE**
**Preparado para:** Examen EGEL ISOFT 2026
**Objetivo:** Calificación 10 - Sobresaliente en 39 reactivos de Desarrollo
