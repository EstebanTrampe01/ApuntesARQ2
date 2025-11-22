# **IoT Hub**
"Servicio en la nube que permite administrar  la comunicación bidereccional entre dispositivos IoT y Azure"

**Azure** 
plataforma de computación en la nube de Microsoft

**Tipos de mensajes**
por MQTT o HTTP
- D2C: Device to cloud
	- Dispositivo hacia la nube 
- C2D: cloud to device
	- nube hacia el dispositivo

----
## Stream Analytics
Análisis en tiempo real sin servidor desde la nube hasta el perímetro(edge).
ejecutando el análisis desde la nube (Azure) hasta el dispositivo o gatawey cercano (edge)

---
## Soluciones
1. Dispositivos generar eventos y lo envían a apps en la nube
2. las apps consiguen la información por la evaluación de datos de eventos de dispositivos entrantes
3. Dependiendo de los conocimientos las apps toman acciones por medio de la ejecución de procesos y flujos de trabajo. La apps pueden enviar comandos a dispositivos

**Acciones en Soluciones IoT**

![[Pasted image 20251120232740.png]]

---
## Arquitectura

En un sistema: 
1. Los sensores de dispositivos envían datos de telemetría (como la temperatura) a una app conectada por Azure Hub.
2. La app en la nube evalúa los datos y toma medidas si estos son críticos 
3.  los dispositivos reciben comandos para ajustar parámetros de sus procesos o iniciar y detener operaciones.
4.  existen sistemas de respaldo en caso de que un sistema principal funcione mal o se desconecte.

 ![[Pasted image 20251120233845.png]]

**Los procesos del sistema son:**

1. EL sistema envía datos de telemetría a IoT Hub, por medio de eventos del dispositivo en la nube, cada X cantidad de tiempo.
2. Las reglas de enrutamiento IoT Hub evalúan los eventos para obtener información 
3. Dependiendo de análisis el enrutamiento de eventos envía el evento a controladores específicos para que tomen acciones.
4. Un controlador hace una acción para enviar el mantenimiento al sitio por servicios de mantenimiento.
5. Un controlador envía un comando para comenzar el sistema de respaldo mientras el mantenimiento esta en camino.

### Consideraciones
- Considerar eventos, conocimientos y acciones puede ayudar a expandir los escenarios de IoT. 
	- Donde sistemas de monitorio pueden agregar información y acciones al usar eventos de dispositivos del sistema.
- Si bien aveces los datos no cambian, el tener recopilación de datos y aplicación de diferentes conocimientos permite estrategias para operar una gran cantidad de dispositivos en múltiples operaciones.

![[Pasted image 20251120235527.png]]

----
## Eventos
Estos representan la comunicación del dispositivo a la nube, siendo una solución de IoT, como notificaciones o telemetría

### Eventos de notificación
estas son
- Eventos no solicitados que el dispositivo envía para transmitir su estado 
- Solicitudes de un dispositivo a su app en la nube

Tipo son alertas, cambios de estado o solicitudes para que una app haga una acción.

- Alerta de falla de un dispositivo
- Actualización de un cambio o estado de dispositivo
- Solicitud de información

### Eventos de reconocimiento
Los dispositivos envían recontamiento para indicar el progreso o finalización de operaciones de segundo plano (asincronicas) solicitadas 

Apps que se basan en comunicación con estados del dispositivos requieren
1. Actualizaciones de progreso en solicitudes de larga duración.
2. Señal de éxito o fracaso de una operación en segundo plano
3. transacción de apps y dispositivos de varios pasos acoplados

### Eventos de telemetría
La telemetría (datos medidos a distancia y enviados a otro lugar) del dispositivo envía mediciones recurrentes, como el monitorio de sensores remotos usan eventos de telemetría como
- Datos continuos del sensor desde los dispositivos hasta las apps
- Datos de salud y diagnóstico monitoreados
- Datos de ubicación

---
## Perspectiva
Los insights son interpretaciones de eventos.
- Las que se derivan de eventos son **Perspectiva Conceptuales**
- Los conocimientos que provienen del procesamiento de apps de datos de eventos transformados o almacenados son **conocimientos agregados o en tiempo real.**

### Perspectiva contextual
interpretaciones sensibles al contexto de los eventos determinan dónde enrutar los eventos o acciones inmediatas a tomar
- donde enrutar (donde ira) un mensaje según datos contextuales como el contenido del encabezado del mensaje 
- Decisiones en tiempo de ejecución por código o manejo de eventos que decide si tomar una acción de forma inmediata
- Conciliación de que ambos recibieron el mensaje (ambas partes de acuerdo) 
  
### Perspectivas en tiempo real
se recompilan y observan en tiempo real con el objetivo de seguimiento y toma de decisión
- Recopilación y observación de estados
- Monitoreo de estados para alertas
- Combinación de eventos con otras fuentes de datos para transformar salidas en tiempo real
  
### Perspectivas Agregadas
Información y conclusiones al juntar y analizar muchos datos acumulados
- Creación de entrenamiento para Marchin Learning "Aprendizaje automático" y IA 
- Recopilación y observación de tendencias por largos periodos de tiempo para mejorar procesos.
- Consultas bajo demanda desde múltiples lugares

---
## Acciones
son actividades deliberadas que se llevan a cabo de forma programática o manual 

### Acciones del dispositivo
son instrucciones o información que una aplicación IoT envía a un dispositivo para actuar localmente 
- Comandos de una app a un dispostivo

### Acciones de servicio
son comunicaciones de servicio, es decir de sistema a sistema
- solicitud de datos servicios externos de uso de soluciones 
- llamar apis externas

### Acciones analógicas 
no se pueden automatizar completamente y dependen de un humano para realizar o confirmar 
IoT las registra pero no ejecuta
- operadores notifican cuando terminan de almacenar artículos de un flujo