# RESUMEN DE LOS 3 LIBROS - ARQUITECTURA IoT

## LIBRO 1: La Revolución del IoT e Industria 4.0

### Revoluciones Industriales
- **Primera Revolución Industrial (1784)**: Mecanización con agua y vapor
- **Segunda Revolución Industrial (1870)**: Producción en masa con electricidad
- **Tercera Revolución Industrial (1969)**: Automatización con electrónica y TI
- **Cuarta Revolución Industrial (Industria 4.0)**: Sistemas ciber-físicos, IoT, big data, cloud computing

### Conceptos Fundamentales de IoT
- **IoT (Internet of Things)**: Red de dispositivos físicos conectados que recopilan e intercambian datos
- **IIoT (IoT Industrial)**: Aplicación de IoT en entornos industriales
- **M2M (Machine to Machine)**: Comunicación directa entre máquinas sin intervención humana
- **Computación ubicua**: Tecnología omnipresente e invisible integrada en objetos cotidianos

### Tipos de Mantenimiento
- **Mantenimiento reactivo**: Reparar cuando falla (run-to-failure)
- **Mantenimiento preventivo**: Programado según calendario o uso
- **Mantenimiento predictivo**: Basado en condición real del equipo mediante monitoreo
- **Mantenimiento prescriptivo**: Usa IA/ML para recomendar acciones óptimas

### Métricas Clave
- **OEE (Overall Equipment Effectiveness)**: Mide eficiencia general del equipo
  - OEE = Disponibilidad × Rendimiento × Calidad
  - World-class OEE: 85% o superior
- **MTBF (Mean Time Between Failures)**: Tiempo promedio entre fallas
- **MTTR (Mean Time To Repair)**: Tiempo promedio de reparación

### IT vs OT
- **IT (Information Technology)**: Tecnología de la información, sistemas empresariales, datos
- **OT (Operational Technology)**: Tecnología operativa, control de procesos físicos, producción
- **Convergencia IT/OT**: Integración de ambos mundos para Industria 4.0

### Observabilidad
- **Los 3 pilares de observabilidad**:
  1. **Métricas**: Valores numéricos medidos en el tiempo
  2. **Logs**: Registros de eventos del sistema
  3. **Traces**: Seguimiento de solicitudes a través del sistema

### Tecnologías Clave
- **Sensores**: Dispositivos que detectan y miden variables físicas
- **Actuadores**: Dispositivos que ejecutan acciones físicas
- **Edge Computing**: Procesamiento de datos cerca de la fuente
- **Cloud Computing**: Procesamiento y almacenamiento en la nube
- **Big Data**: Análisis de grandes volúmenes de datos
- **Machine Learning**: Aprendizaje automático para predicciones

### Protocolos y Comunicación
- **MQTT**: Protocolo ligero de mensajería para IoT
- **SCADA**: Sistemas de Control y Adquisición de Datos
- **Modbus**: Protocolo de comunicación industrial
- **OPC UA**: Protocolo de interoperabilidad para automatización
- **AMQP**: Advanced Message Queuing Protocol

### Arquitecturas
- **Arquitectura de 3 capas**:
  1. Capa de percepción (sensores/dispositivos)
  2. Capa de red (comunicación)
  3. Capa de aplicación (servicios)

### Beneficios de Industria 4.0
- Mayor eficiencia operacional
- Reducción de costos de mantenimiento
- Mejor calidad del producto
- Toma de decisiones basada en datos
- Producción flexible y personalizada
- Optimización de recursos

---

## LIBRO 2: Modelo de Seguridad IoT - IoTSeMo

### IoTSeMo (IoT Security Model)
- **Definición**: Modelo de seguridad para aplicaciones IoT
- **Propósito**: Analizar y categorizar aspectos de seguridad según elementos usados en Edge, Fog y Cloud
- **Base**: Inspirado en arquitectura simplificada de Cisco

### Tipos de Comunicación IoT
- **M2H (Machine to Human)**: Comunicación de máquina a humano
- **M2M (Machine to Machine)**: Comunicación entre máquinas

### Tecnologías de Comunicación Inalámbrica
- **Bluetooth**: Comunicación de corto alcance
- **WiFi**: Red inalámbrica local de alta velocidad
- **GSM (Global System for Mobile Communications)**: Sistema global de comunicaciones móviles
- **NFC (Near Field Communication)**: Comunicación de campo cercano
- **LoRa (Long Range)**: Largo alcance con bajo consumo energético
- **ZigBee**: Protocolo de baja potencia para automatización
- **5G**: Quinta generación de comunicaciones móviles

### Características de 5G para IoT
- **eMBB (Enhanced Mobile Broadband)**: Banda ancha móvil mejorada
- **URLLC (Ultra-Reliable Low-Latency Communications)**: Comunicaciones ultraconfiables de baja latencia (<1ms)
- **mMTC (Massive Machine Type Communications)**: Comunicaciones masivas tipo máquina
- **Velocidad**: Más de 10 GBps
- **Latencia**: Inferior a 1 milisegundo

### Desafíos Técnicos de IoT con 5G
1. Escalabilidad y gestión de red
2. Interoperabilidad y heterogeneidad
3. Seguridad y privacidad

### Arquitectura IoT General
**Tres capas base**:
1. **Capa de detección/percepción/hardware**: Sensores, RFID, actuadores, gateways
2. **Capa de red/comunicación**: Enrutadores, repetidores, agregadores
3. **Capa de interfaces/servicios**: Aplicaciones y servicios

**Capas adicionales en arquitecturas extendidas**:
- **Capa de Servicio de Gestión**: Procesamiento y filtrado de datos
- **Capa de Procesamiento**: Almacenamiento, análisis y transformación
- **Capa de Negocio**: Reglas de negocio, privacidad, control de datos

### Componentes IoT
- **Sensor**: Dispositivo que detecta estímulo del entorno y lo convierte en impulso eléctrico
- **Actuador**: Dispositivo que recibe señal eléctrica y realiza una acción física
  - Tipos: Hidráulicos, neumáticos, eléctricos, térmicos/magnéticos, mecánicos
- **Gateway**: Intermediario que recibe, correlaciona y envía información entre nodos
  - Función adicional: Traducción bidireccional de protocolos
- **Lector RFID**: Envía comandos para interrogar y activar etiquetas

### Tecnologías de Red IoT
- **LR-WPAN (IEEE 802.15.4)**: Redes personales inalámbricas de baja velocidad
  - ZigBee, 6LoWPAN, WirelessHART operan sobre esta tecnología
- **WAVE (IEEE 1609)**: Tecnología sobre WiFi para vehículos

### Protocolos de Mensajería IoT
- **MQTT (Message Queuing Telemetry Transport)**: Protocolo ligero pub/sub
- **CoAP (Constrained Application Protocol)**: Protocolo para dispositivos restringidos
- **AMQP (Advanced Message Queuing Protocol)**: Protocolo avanzado de colas
- **XMPP (Extensible Messaging and Presence Protocol)**: Protocolo extensible de mensajería
- **DDS (Data Distribution Service)**: Servicio de distribución de datos
- **JMS (Java Message Service)**: Servicio de mensajería Java

### Modelos de Comunicación IoT
- **D2D (Device to Device)**: Dispositivo a dispositivo
- **D2C (Device to Cloud)**: Dispositivo a nube
- **D2G (Device to Gateway)**: Dispositivo a gateway
- **Modelo de datos compartidos**: Compartición de datos entre dispositivos

### Paradigmas de Computación
**Cloud Computing (Computación en la Nube)**:
- Modelo que permite acceso bajo demanda a recursos informáticos
- **Modelos de servicio**:
  - **SaaS (Software as a Service)**: Software como servicio
  - **PaaS (Platform as a Service)**: Plataforma como servicio
  - **IaaS (Infrastructure as a Service)**: Infraestructura como servicio

**Fog Computing (Computación en la Niebla)**:
- Capa intermedia entre edge y cloud
- Filtra datos y envía resultados concretos a la nube
- Reduce ancho de banda y almacenamiento en la nube

**Edge Computing (Computación en el Borde)**:
- Procesamiento cerca de la fuente de datos
- Reduce latencia significativamente
- Puede enviar resultados directamente a la nube (no requiere fog)

### Modelo IoTSeMo Detallado
**Estructura**:
- Dos pilas: Funcional principal y Gestión de datos/computación
- Tres paradigmas: Edge, Fog, Cloud
- Cada paradigma tiene 3 capas: Física, Comunicación, Aplicación

**Capas del Modelo**:
1. **Capa de Acceso a la Red**:
   - Tecnologías que operan en capas 1 y 2 del modelo OSI
   - Incluye dispositivos y protocolos de acceso
   - Tecnologías sin IP (LoRa, Bluetooth, ZigBee) necesitan gateway

2. **Capa de Comunicaciones** (2 subcapas):
   - **Subcapa de Redes**: Direccionamiento global y enrutamiento IP
   - **Subcapa de Comunicaciones extremo a extremo**: TCP, UDP, TLS

3. **Capa de Aplicación** (2 subcapas):
   - **Protocolos de aplicación TCP/IP**: MQTT, CoAP, ZMQ
   - **Servicios elementales**: Almacenamiento, procesamiento, autenticación, cola de mensajes

### Caso de Estudio: Sistema de Notificación de Proximidad
- **Tecnología**: Balizas (beacons) IoT Bluetooth de baja energía
- **Ubicación**: Perímetro de una universidad
- **Componentes**:
  - Apache Kafka: Cola de mensajes
  - Firebase Cloud Messaging (FCM): Notificaciones a móviles
  - LDAP: Autenticación
  - JDBC: Protocolo de base de datos
  - HTTP: Comunicación con API Gateway
- **Características**: Convergencia IP (no requiere gateway de traducción)

### Consideraciones de Seguridad
- Fabricantes priorizan funcionalidad sobre seguridad
- Dispositivos IoT tienen limitaciones de almacenamiento y procesamiento
- Necesidad de confidencialidad, privacidad y cumplimiento legal
- Falta de métodos claros para identificar qué proteger
- Riesgo de ataques (ej: notificaciones falsas en sistema de balizas)

---

## LIBRO 3: Anatomía de una Arquitectura IoT

### Pensamiento Arquitectónico

**Modelos de Referencia**:
- Guías basadas en mejores prácticas
- Muestran cómo las cosas encajan juntas
- Permiten comunicación entre organización
- Deben dividirse en niveles (0, 1, 2, 3) de complejidad
- **Nivel 0**: General, para stakeholders no técnicos
- **Niveles 1-3**: Mayor detalle técnico

**Enfoques de Arquitectura**:
- **Tradicional**: Diseñar para cada ocurrencia futura
- **Ágil**: Construir solo lo que necesitas, cuando lo necesitas (preferido con limitaciones de tiempo/presupuesto)

### Modelos Históricos

**Arquitectura de Referencia de Purdue**:
- Desarrollada a mediados de la década de 1990
- Define capas o niveles de separación para sistemas industriales
- Seis niveles divididos en varias zonas

**ISA-95**:
- Estándar para automatización de sistemas de control empresarial
- Basado en el modelo Purdue
- Enfocado en capas 3 y 4
- Define interconexión de sistemas de control de producción con sistemas de TI

**EA (Arquitectura Empresarial)**:
- Define arquitectura, estándares y visión para toda la organización
- Integra visión con dependencias, restricciones y objetivos operativos
- Instaurar disciplina arquitectónica

### Diseño por Capas de la Arquitectura IoT

**Ventajas de usar capas**:
- Agrupa funciones similares
- Separación de responsabilidades
- Facilita implementación de cambios
- Análisis en tiempo real cercano (near real-time)
- Contratos bien definidos entre capas permiten flexibilidad

#### Capa 1 y 2: Sensores y Controladores de Dispositivos

**Sensores**:
- Dispositivos de medición (transductores)
- Convierten energía de una forma a otra
- Miden temperatura, presión, luz, etc.
- Proporcionan voltaje analógico o digital

**Nodos**:
- También llamados RTU (Unidad de Telemetría Remota)
- Leen y transmiten valores de sensores
- Conectados a múltiples sensores
- Mantienen jerarquía de dispositivos

**Actuadores**:
- Dispositivos de control
- Regulan dispositivos finales
- Permiten gestión remota y autónoma
- Críticos para seguridad en tiempo real

**Patrones de Automatización**:

1. **Sistemas de Control Industrial**:
   - SCADA (Supervisory Control and Data Acquisition Systems)
   - PLC (Controladores Lógicos Programables)
   - RTU (Unidades de Telemetría Remota)
   - Protocolos de bus de campo: Modbus, BACnet, Probus
   - Generalmente sistemas de lazo cerrado
   - Pueden requerir conversión de protocolos

2. **Redes IP de Dispositivos**:
   - Usan protocolos compatibles con TI
   - MQTT sobre TCP
   - Mensajes pueden cifrarse o codificarse
   - Facilitan integración

3. **Redes IoT**:
   - LPWAN (Low Power Wide Area Network)
   - LoRa/LoRaWAN: Alcance de varios kilómetros
   - 4G/5G: Para redes públicas
   - Bajo consumo energético
   - Sensores sin acceso a redes cableadas

#### Capa 3: Servidores y Aplicaciones Perimetrales (Edge)

**Funciones**:
- Extracción de datos del entorno
- Preparación para reenvío o procesamiento
- Conversión de protocolos propietarios a estándares IT (ej: Modbus a MQTT)
- Reducción de latencia
- Análisis y control in situ

**Tipos de dispositivos**:
- PLCs (Programmable Logic Controllers)
- PACs (Programmable Automation Controllers)
- Servidores edge inteligentes
- Adaptadores de protocolo

**WAN/VPN a la nube**:
- División lógica y física entre fábrica y red corporativa
- Seguridad crítica para proteger ambas redes
- Control de flujo de datos

#### Capa 4: Gestión de Dispositivos

**Funciones**:
- Incorporación (onboarding)
- Administración
- Seguridad de dispositivos
- Gestión de certificados

**Gemelos Digitales (Digital Twins)**:
- Representación/réplica digital del dispositivo
- Mantiene estado y configuración actuales
- Permite interactuar sin acceso directo al dispositivo
- Guarda última configuración conocida (útil si dispositivo se desconecta)

#### Capa 5: Ingesta de Datos en la Nube

**Consideraciones**:
- Variedad de formatos, protocolos, volumen y velocidad
- Patrones específicos por organización
- Múltiples servicios de AWS disponibles
- No existe enfoque único para todos

**Decisión importante**: ¿Almacenar datos crudos antes de transformar?
- **Ventajas**: Coherencia, precisión, trazabilidad
- **Consideraciones**: 
  - Transformación en edge previa
  - Decodificación antes de almacenar
  - Costo y esfuerzo a largo plazo
  - Posibles requisitos legales

#### Capa 6: Almacenamiento y Transformación de Datos

**Opciones de almacenamiento**:
- **Lago de datos (Data Lake)**: Flexible, cualquier formato
- **Almacén de datos (Data Warehouse)**: Relacional, estructurado
- **Híbrido lago/almacén (Data Lakehouse)**: Combina ventajas de ambos

**Estructura del Lago de Datos (usando AWS S3)**:
- Archivos planos en estructura de carpetas jerárquica
- Múltiples áreas para diferentes etapas de procesamiento

**Tres Capas del Lago de Datos**:

1. **Capa de Datos Sin Procesar (Raw Data)**:
   - Datos en formato original
   - **Inmutables**: No se pueden cambiar una vez almacenados
   - Segura y bloqueada
   - Estructura sugerida: `Source → Component → Type → Year → Month → Day → Hour → <Minute>:<Second>`
   - Facilita ingesta rápida

2. **Capa de Datos Formateados (Formatted Data)**:
   - Transformación inicial
   - Cadenas binarias → valores reales (temperatura, humedad)
   - Formatos útiles: CSV, Parquet, Apache ORC, Avro
   - Estructura más granular
   - ETL específico por tipo de fuente
   - Acceso puede estar restringido

3. **Capa de Datos Curados (Curated Data)**:
   - Estructurados para análisis y negocio
   - Combina, agrega, transforma datos
   - Calcula valores adicionales (ej: ETO - Evapotranspiración)
   - Integra datos de otras fuentes (financieras, empresariales)
   - Datos desnormalizados
   - Mayor acceso dentro de organización (pero aún controlado)

**Nomenclatura alternativa**: Bronze, Silver, Gold

**Gestión de Metadatos**:
- Información sobre los datos: fuente, destino, refresh intervals
- Tipo, formato, ciclo de vida, transformación
- Información de sensores: tipos, ubicaciones
- Se almacena en base de datos (ej: AWS RDS)
- Puede requerir interfaz para facilitar gestión

#### Capa 7: Análisis y Aprendizaje Automático

**Dos áreas principales**:

1. **Aprendizaje Automático (Machine Learning)**:
   - **Análisis de datos de sensores**:
     - Establecer línea base
     - Buscar variaciones
     - Detectar problemas antes que se agraven
     - Múltiples flujos de datos relacionados
   
   - **Análisis de video o imagen**:
     - Detectar anomalías en productos
     - Problemas de color, ubicación, superficie
     - Evaluación de calidad temprana en manufactura
   
   - **Modelos avanzados**:
     - Ejemplo: Modelo de balance de demanda de agua
     - Considera clima, demanda histórica, suministro, costos
     - Optimiza estrategia y minimiza costos

2. **Análisis de Negocio (Business Analytics)**:
   - Enfocado en el futuro (vs inteligencia de negocio que mira al pasado)
   - Usa datos para generar insights
   - Responde: ¿Cómo funcionan las cosas? ¿Dónde pueden ocurrir problemas?
   - Combina con visualización
   - Ejemplo: ¿Cuántos widgets fabricamos? ¿Cuál es la predicción?
   - Preguntas avanzadas: ¿Equipos disminuyendo rendimiento? ¿Necesitan mantenimiento?

**Análisis de Borde (Edge Analytics)**:
- **Reacción en tiempo real**: Milisegundos cuentan en manufactura
- **Evita ralentizaciones por ancho de banda**: Sensores de alta frecuencia (cientos/segundo)
- Preprocesamiento o almacenamiento local
- Análisis esencial y rápido

**Caso de estudio - Club de Golf**:
- Monitoreo: Flujo de agua, bombas, niveles de lagos, clima, humedad del suelo
- Objetivo: Eficiencia, reducir desperdicios, costos, detectar anomalías
- Análisis: Flujo vs energía (eficiencia de bomba), dureza del green
- El aprendizaje automático comienza con análisis para entender datos

#### Capa 8: Visualización e Informes

**Propósitos**:
- Ver datos en formato de gráfico
- Comparar diferentes escalas de tiempo y mediciones
- Comprender qué es "normal"
- Detectar anomalías

**Dos opciones principales**:

1. **Informe (Report)**:
   - Vista de datos con herramientas para explorar
   - Diferentes granularidades (segundos, subsegundos)
   - Analistas responden preguntas
   - Detectar anomalías
   - Determinar mejoras

2. **Panel de Control (Dashboard)**:
   - Muestra estado en tiempo real
   - Configurado en operaciones
   - Detectar problemas potenciales
   - Determinar ubicaciones activas
   - Decisiones en tiempo real

**Aplicaciones Personalizadas vs Preconfiguradas**:
- Productos listos para usar: Buenos dentro de su dominio
- Desafío: Incorporar datos de otras fuentes puede ser complejo
- Combinar datos en tiempo real con costos, pedidos, historial de mantenimiento
- Considerar: Capacidad de integración vs costo de desarrollo personalizado

**Razones históricas para desarrollo personalizado**:
- IoT era nuevo, análisis de series temporales era novel
- Crear interfaz fácil de usar para usuarios no expertos
- Productos comerciales sin costos de licencia

**Realidad actual**:
- Muchos sistemas de control industrial ofrecen análisis
- Diferentes tipos de usuarios: analistas expertos vs usuarios operativos
- Herramientas complejas vs paneles simples

### Arquitectura Completa Propuesta

**Arquitectura en Capas (Bottom-Up)**:
1. Sensores y Actuadores
2. Controladores de Dispositivos (PLCs, RTUs)
3. Servidores y Aplicaciones Edge
4. WAN/VPN
5. Gestión de Dispositivos
6. Ingesta de Datos
7. Almacenamiento y Transformación (Lago de Datos)
8. Análisis y ML
9. Visualización e Informes

**Características**:
- Flexible, adaptable a circunstancias
- Puede mapearse a modelo Purdue
- Permite comunicación directa sensor-nube
- Considera protocolos y seguridad entre límites

### Definición de Estándares

**Objetivos del Arquitecto**:
- Servir al negocio
- Arquitectura funcional, robusta, escalable, segura y rentable
- Establecer estándares y convenciones

**Definiciones**:
- **Estándar**: Regla estricta sobre cómo hacer algo
- **Convención**: Sugerencia o guía, no obligatoria

**Importancia de Estándares**:
- Críticos para equipos grandes o proyectos largos
- Aseguran calidad del código
- Evitan problemas futuros
- Facilitan mantenimiento

**Recomendaciones Básicas (trimestrales o semestrales)**:

1. **Revisar sistema de gestión de código fuente**:
   - Nombres de proyectos/repositorios coherentes
   - Descripciones claras
   - Documentación actualizada
   - Facilita onboarding de nuevos miembros

2. **Revisar documentación de arquitectura**:
   - Diagramas actualizados y precisos
   - Cambios de flujo principales
   - Estructura y componentes principales
   - Actualizar 2 veces al año mínimo

3. **Reuniones periódicas del equipo**:
   - Analizar calidad del producto
   - Mesa redonda o sesiones de trabajo
   - Enfoque: ¿Qué podemos hacer mejor?
   - Feedback debe incorporarse en sprints

**Herramientas**:
- **Análisis estático de código**: Útil pero 100% adherencia no siempre posible
- Usar judiciosamente, balancear costo-beneficio

**Establecer Expectativas**:
- Construir relación y confianza con gerencia
- Balance entre supervisión (calidad) vs rapidez
- Comunicar valor para organización
- Gerencia quiere: Más rápido, barato y mejor calidad
- Realidad: No siempre es posible simultáneamente

**Sobre Metodologías Ágiles**:
- Hay forma correcta e incorrecta de adoptarlas
- No debe convertirse en herramienta para exigir más en menos tiempo
- Revisiones de código rigurosas no siempre viables en sprints cortos
- Balance necesario entre calidad y velocidad

### Consideraciones Importantes

**Desafíos en Organizaciones Grandes**:
- Poca estandarización entre fábricas
- Homogeneidad limitada
- Implementar estructura y EA requiere esfuerzo considerable

**Proceso como Motor de Cambio**:
- Mejor solución técnica puede fracasar si procesos no cambian
- Cambio debe surgir desde dentro
- Comunicar valor y beneficio real a stakeholders

**Sobre Arquitectura**:
- No existe "one-size-fits-all"
- Adaptar según ambiente y necesidades
- Evitar sobre-arquitectura
- Evitar sub-arquitectura
- Balance entre flexibilidad y estructura

**Progreso Incremental**:
- Empezar con algo es mejor que no empezar
- Arquitectura evolucionará con el tiempo
- Aprender de implementación
- Ajustar según necesidades reales

---

## Conceptos Transversales en los 3 Libros

### Protocolos Comunes Mencionados
- **MQTT**: Ligero, pub/sub, sobre TCP
- **CoAP**: Para dispositivos restringidos
- **Modbus**: Bus de campo industrial
- **HTTP/HTTPS**: Web estándar
- **TCP/UDP**: Transporte
- **TLS**: Seguridad en transporte

### Servicios de AWS Mencionados
- **S3**: Almacenamiento de objetos (lago de datos)
- **RDS**: Bases de datos relacionales
- **IoT Core**: Gestión de dispositivos IoT

### Principios Arquitectónicos Clave
1. **Separación de responsabilidades**: Cada capa tiene función específica
2. **Escalabilidad**: Diseñar para crecer
3. **Seguridad por capas**: Protección en cada nivel
4. **Flexibilidad**: Adaptable a cambios
5. **Interoperabilidad**: Sistemas deben comunicarse
6. **Observabilidad**: Métricas, logs, traces

### Tecnologías Emergentes
- **5G**: Revolucionará conectividad IoT
- **Edge AI**: Inteligencia artificial en el borde
- **Digital Twins**: Réplicas digitales de sistemas físicos
- **Blockchain**: Para seguridad y trazabilidad (mencionado implícitamente)

### Mejores Prácticas
- Empezar simple, crecer según necesidad
- Documentar arquitectura constantemente
- Establecer y seguir estándares
- Balance entre calidad y velocidad
- Involucrar stakeholders de negocio y técnicos
- Considerar seguridad desde el inicio
- Planear para mantenimiento y evolución
- Usar modelos de referencia como punto de partida
- Adaptar según contexto específico

---

## Glosario Rápido de Acrónimos

- **AWS**: Amazon Web Services
- **CoAP**: Constrained Application Protocol
- **D2C**: Device to Cloud
- **D2D**: Device to Device
- **D2G**: Device to Gateway
- **DDS**: Data Distribution Service
- **EA**: Enterprise Architecture (Arquitectura Empresarial)
- **eMBB**: Enhanced Mobile Broadband
- **ETO**: Evapotranspiration (Evapotranspiración)
- **GSM**: Global System for Mobile Communications
- **IaaS**: Infrastructure as a Service
- **IIoT**: Industrial Internet of Things
- **IoT**: Internet of Things
- **IT**: Information Technology
- **LoRa**: Long Range
- **LPWAN**: Low Power Wide Area Network
- **LR-WPAN**: Low Rate Wireless Personal Area Network
- **M2H**: Machine to Human
- **M2M**: Machine to Machine
- **mMTC**: Massive Machine Type Communications
- **MQTT**: Message Queuing Telemetry Transport
- **MTBF**: Mean Time Between Failures
- **MTTR**: Mean Time To Repair
- **NFC**: Near Field Communication
- **OEE**: Overall Equipment Effectiveness
- **OT**: Operational Technology
- **PaaS**: Platform as a Service
- **PAC**: Programmable Automation Controller
- **PLC**: Programmable Logic Controller
- **RFID**: Radio Frequency Identification
- **RTU**: Remote Telemetry Unit
- **SaaS**: Software as a Service
- **SCADA**: Supervisory Control and Data Acquisition
- **TLS**: Transport Layer Security
- **URLLC**: Ultra-Reliable Low-Latency Communications
- **XMPP**: Extensible Messaging and Presence Protocol

---

*Este resumen integra los conceptos clave de los tres libros sobre IoT, Industria 4.0 y arquitectura de sistemas industriales inteligentes.*
