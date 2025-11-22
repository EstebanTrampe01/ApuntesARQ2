



# Modelo de seguridad para aplicaciones IoT - IoTSeMo

```
Rafael V. Páez-Méndez1[0000−^0003 −^1721 −0883)], Edgar E. Ruiz
García1[0000−^0002 −^6657 −3608], and Jordi Forné2[0000−^0002 −^8401 −3292]
```

(^1) Pontificia Universidad Javeriana, Bogotá 110231, Colombia⋆⋆  
{paez-r,eruiz}@javeriana.edu.co  
(^2) Universidad Politécnica de Cataluña, Barcelona 08034, España  
jordi.forne@upc.edu  
Resumen. El Internet de las Cosas (IoT) es una tecnología que se ha  
popularizado por su facilidad de uso, accesibilidad y los servicios que ofrece  
para mejorar la calidad de vida de los usuarios. Sin embargo, la mayoría de los fabricantes  
y desarrolladores de IoT no consideran los riesgos inherentes a esta  
nueva tecnología debido, entre otros factores, a su afán por comercializar  
sus productos y/o aplicaciones y a la falta de métodos claros  
para identificar dónde y qué proteger en este amplio entorno, con el fin de preservar  
los datos según su sensibilidad. A pesar de lo anterior, los ecosistemas de IoT  
ya se utilizan en múltiples contextos, como la sanidad,  
la industria automotriz y la domótica, entre otros; por lo tanto, es necesario contar con  
una metodología estructurada para desarrollar aplicaciones de IoT seguras. Por lo tanto,  
se propone un nuevo Modelo de Seguridad IoT (IoTSeMo) para identificar fácilmente qué  
mecanismos de seguridad deben implementarse, según el manejo  
de la información.  
Palabras clave: seguridad IoT, modelo IoT, requisitos de seguridad,  
metodología de seguridad

## 1 Introducción

```
The term IoT is associated with any node connected to Internet, that facilitates
machine-to-human (M2H) and machine-to-machine (M2M) communication with
the physical world. This interaction involves different communication technolo-
gies, in addition to RFID, such as Bluetooth, WiFi, Global System for Mo-
bile Communications (GSM), Near Field Communicaction (NFC) and satellite
communication, but for IoT ecosystems it is required to have a broadband, so
```

⋆⋆Rafael V. Páez-Méndez es beneficiario de un postdoctorado “Fundación Carolina”

```
fellowship. This work was also supported by the Spanish Government under the
project “Enhancing Communication Protocols with Machine Learning while Pro-
tecting Sensitive Data (COMPROMISE)” PID2020-113795RB-C31, funded by MI-
CIU/AEI/10.13039/501100011033; the project “Anonymization technology for AI-
based analytics of mo- bility data (MOBILYTICS)” (TED2021-129782B-I00), funded
byMICIU/AEI/10.13039/501100011033 and by the European Union NextGenera-
tionEU/PRTR; and funded by the Generalitat de Catalunya, under AGAUR grant
“2021 SGR 01413”
```

Actualmente se utilizan las tecnologías 3G y 4G, si bien no son del todo óptimas  
para aplicaciones de IoT. Sin embargo, se espera que con el despliegue global de  
la tecnología 5G, que ya opera comercialmente en muchos países  
, sea posible lograr la computación ubicua a través de dispositivos IoT,  
permitiéndoles comunicarse entre sí y conectarse a  
internet.  
Gracias a las mejores características que ofrece 5G en cuanto a velocidad de transmisión,  
baja latencia, escalabilidad, movilidad, etc., y dado que muchos países ya han  
implementado esta tecnología y otros están en proceso de hacerlo, es necesario estar  
preparados para aprovechar sus beneficios en diferentes sectores industriales (conocidos  
como IoT Industrial o IIoT), así como en escenarios de la vida cotidiana, como  
hogares inteligentes, edificios inteligentes, ciudades inteligentes u otras aplicaciones específicas [1].  
Algunos escenarios clave de uso de 5G claramente identificados son eMBB (  
Banda Ancha Móvil Mejorada), URLLC (Comunicaciones Ultraconfiables de Baja Latencia)  
y mMTC (Control de Transmisión Multimedia Móvil) (Comunicaciones Masivas Tipo Máquina  
)[2]. También es necesario abordar los nuevos desafíos técnicos  
inherentes al IoT en conjunto con 5G, que se pueden resumir en:  
escalabilidad y gestión de la red, interoperabilidad y heterogeneidad,  
garantía de seguridad y privacidad. En algunos casos, es necesario preservar la confidencialidad  
, la privacidad y/o el manejo adecuado de la información, de conformidad con las  
leyes establecidas por las entidades reguladoras, las cuales dependen de los organismos de control del  
procesamiento de datos y de la legislación de cada país. Este artículo analiza la evolución,  
el crecimiento y la estructuración de los entornos IoT, así como su integración con  
tecnologías adyacentes para ofrecer servicios. Finalmente, se analizan diferentes arquitecturas y  
se propone y aplica el modelo de seguridad IoTSeMo para arquitecturas IoT, lo cual  
es muy necesario, ya que la mayoría de los "dispositivos" tienen limitaciones de almacenamiento y procesamiento,  
por lo que los fabricantes de dispositivos y los desarrolladores de aplicaciones priorizan la funcionalidad pero  
sacrifican la seguridad.

## 2 Arquitecturas y componentes de IoT

Respecto a los componentes y la interacción de un entorno IoT, algunos autores  
proponen una arquitectura general de tres capas:  
capa de detección/percepción/hardware, capa de red/comunicación y capa de interfaces/servicios[3]–[5].

2.1 Capa de detección/percepción/hardware

En esta capa se ubican los sensores, lectores RFID, etiquetas, actuadores y  
gateways, constituyendo la infraestructura base a partir de la cual  
se obtienen los datos del entorno. Un sensor es un dispositivo que detecta un estímulo del  
entorno y lo convierte en un impulso eléctrico mediante un transductor,  
enviando una señal a otro dispositivo. Un sensor de propósito general realiza la función  
de recopilar información de su entorno para determinar la proximidad,  
señales de humo, medir la temperatura, la humedad, la luz, etc. [6]. Los actuadores son dispositivos  
que reciben una entrada, generalmente una señal eléctrica, y realizan una acción que la activa.

Los actuadores pueden ser físicos, ya sea en sí mismos o en otros dispositivos (por ejemplo, una bomba hidráulica), y  
también pueden realizar acciones lógicas como enviar un mensaje de texto o controlar los movimientos de un robot. Los actuadores pueden ser hidráulicos, neumáticos, eléctricos, térmicos/magnéticos o mecánicos. Otro componente importante en el entorno de IoT es la puerta de enlace, capaz de recibir, correlacionar y enviar información a otros nodos; por lo tanto, requiere mayor capacidad en términos de recursos computacionales [7]. En un entorno de IoT, la puerta de enlace actúa como intermediario de comunicaciones entre el sensor y los dispositivos conectados.  
  
  
  
  
  

Fig. 1. Tecnologías de conectividad IoT en términos de tasa de datos, cobertura y latencia [8].

En cuanto a los lectores, estos envían comandos modulados y  
onda continua (CW) para interrogar y activar las etiquetas. La etiqueta responde con  
su identificador único, y el lector reenvía esta respuesta a un servidor para verificar  
su autenticidad, comparando el identificador recibido con los almacenados  
. Si hay coincidencia,  
continúa el proceso de envío y recepción de información [9]. Tecnologías como ZigBee, 6LoWPAN y WirelessHART operan sobre  
redes inalámbricas personales de baja velocidad (LR-WPAN - IEEE 802.15.4). Otras  
tecnologías utilizadas en IoT no orientadas a bajas velocidades de datos, como  
WAVE (IEEE 1609), funcionan sobre WiFi (IEEE 802.11).  
Por otro lado, dependiendo de las restricciones en términos de ancho de banda,  
consumo de energía y alcance de cobertura, entre otros, podría ser adecuado utilizar otras  
tecnologías como Ethernet, Bluetooth, Long Range (LoRa), etc. La Fig. 1  
muestra varias tecnologías según la velocidad de datos, la cobertura y la latencia [8].

2.2 Capa de red/comunicación

Esta capa se encarga de la comunicación entre dispositivos IoT o con otros  
dispositivos, como servidores. Las redes utilizadas como medio de transporte pueden ser cableadas o  
inalámbricas, públicas, privadas o híbridas; estas redes deben cumplir con los requisitos de comunicación, baja latencia, ancho de banda y seguridad. También se requieren  
múltiples tecnologías y protocolos para interactuar con otros dispositivos en una red heterogénea.  

En esta capa, la capa de entorno se encarga de recibir datos de la  
capa de percepción, generalmente a través de un dispositivo de puerta de enlace, y enviarlos a la capa de aplicación mediante  
tecnologías como 3G, 4G, Wi-Fi, Bluetooth, ZigBee u otras. Otros dispositivos de esta  
capa son los enrutadores, responsables de verificar los datos recibidos, configurar  
las rutas y enviarlos a través de las diferentes redes; los  
repetidores, que amplifican la señal para que llegue  
correctamente a su destino; y los agregadores, que facilitan  
la integración y la gestión eficiente de grandes volúmenes de datos generados por  
los dispositivos conectados, proporcionan interfaces estandarizadas para la comunicación entre  
dispositivos heterogéneos, normalizan los datos para un análisis uniforme y envían  
la información procesada a otras plataformas o aplicaciones para su posterior uso.

2.3 Capa de interfaces/servicios/aplicaciones

En cuanto a los protocolos de mensajería utilizados en las redes IoT, emplean los patrones de solicitud/respuesta o  
publicación/suscripción. Entre ellos se encuentran: Java Message Service  
(JMS), Extensible Messaging and Presence Protocol (XMPP), Message Queuing  
Telemetry Transport (MQTT), MQTT for Sensor networks (MQTT-SN),  
Data Distribution Service (DDS), Constrained Application Protocol (CoAP) y  
Advanced Message Queuing Protocol (AMQP) [10]. Los  
modelos de comunicación más comunes en un entorno IoT pueden ser entre dispositivos (D2D), de  
un dispositivo a la nube (D2C), de un dispositivo a una puerta de enlace (D2G) y mediante un  
modelo de datos compartidos en el que diferentes dispositivos IoT se comunican con terceros  
[11]. Para realizar comunicaciones como Comunicación Masiva Tipo Máquina  
(mMTC), Comunicación Mejorada Tipo Máquina (eMTC),  
Sistema Global de Cobertura Extendida para Comunicaciones Móviles para el IoT (EC GSM-IoT)  
e IoT de Banda Estrecha (NB-IoT), es necesario contar con redes móviles de alta velocidad  
, por ejemplo, utilizando tecnologías como 5G, que ofrecen más de 10  
GBps y una latencia inferior a 1 milisegundo [12].

## 3 Otras arquitecturas de IoT

Aunque la arquitectura de tres capas es la más conveniente y fácil de implementar,  
existen otras propuestas de arquitectura IoT que incluyen la  
capa de Servicio de Gestión [13], ubicada entre la capa de comunicación y la de aplicación. Esta capa  
cuenta con motores de reglas de negocio y su función es procesar información,  
filtrar datos, formular lógicas de decisión y proporcionar respuestas en tiempo real. En otros  
casos, se incluye una capa de Procesamiento, situada por encima de la capa de red  
, que se encarga de almacenar, analizar y transformar la información para entregar  
un resultado refinado a la capa de aplicación. En algunos casos, también es responsable  
de la toma de decisiones en tiempo real basada en la información filtrada. Una  
capa adicional que se considera en otras arquitecturas IoT es la capa de Negocio, que  
abarca las reglas de negocio, el análisis de negocio y la gestión de procesos de negocio  
, garantizando así el cumplimiento de los objetivos empresariales. Desempeña un  
papel fundamental en lo que respecta a la privacidad y garantiza que los datos de usuario se almacenen de forma segura.

que sus propietarios tengan control sobre estos datos; además, permite ofrecer una  
experiencia mejorada mediante servicios personalizados basados ​​en perfiles y preferencias.  
En [14] se puede encontrar un análisis de las diferentes arquitecturas en capas.  
Otros marcos arquitectónicos para IoT pueden ser adecuados para un tipo  
de industria específico o depender de las tecnologías utilizadas. En [15]  
, Cisco presenta un marco con dos pilas paralelas de tres capas, como se muestra en la figura 2. Este  
marco busca simplificar la comprensión de una arquitectura IoT, donde cada  
capa cumple funciones predeterminadas y utiliza diferentes tecnologías para lograr su  
objetivo. Como se evidencia en otras arquitecturas analizadas, la  
pila funcional stackCore IoT es la base mínima para una arquitectura IoT. La  
pila de gestión de datos y computación stackIoT muestra la interacción de numerosos servicios  
que optimizan el uso de recursos, desde la capa física hasta la  
propia capa de aplicación, ya que la tecnología en la nube permite el acceso bajo demanda a recursos como  
redes, servidores, almacenamiento, aplicaciones y servicios, que se pueden aprovisionar  
y liberar [16] para procesar información y proporcionar mejores tiempos de respuesta.

Fig. 2. Arquitectura IoT simplificada [15]

3.1 Pila de computación y gestión de datos de IoT

Este modelo informático para entornos IoT define cómo y dónde se  
filtran, almacenan, agregan y analizan los datos. En una arquitectura tradicional, estas  
funciones se realizarían directamente en la nube de un centro de datos.

- La computación en la nube es un modelo que permite el acceso bajo demanda  
    a un conjunto de recursos informáticos, como almacenamiento, redes, servidores,  
    aplicaciones y servicios, que se pueden proporcionar rápidamente y con una mínima  
    gestión o interacción por parte del proveedor. Ofrece una  
    taxonomía de tres modelos de servicio: Software como Servicio (SaaS), Plataforma  
    como Servicio (PaaS) e Infraestructura como Servicio (IaaS). Según  
    cómo se comparten los servicios, los modelos pueden ser de nube privada, nube comunitaria o nube pública.

nube híbrida y proporciona cinco características principales: autoservicio bajo demanda, amplio acceso a la red, agrupación de recursos, elasticidad rápida
y servicio medido [17].

- Computación en la niebla (Fog Computing): El paradigma de la computación en la niebla ayuda a resolver algunas limitaciones  
    de la computación en la nube en un entorno de IoT, particularmente en lo que respecta  
    al almacenamiento y análisis de grandes volúmenes de datos. La computación en la niebla es una  
    capa intermedia entre la computación en el borde y la computación en la nube; funciona como  
    un intermediario que permite filtrar los datos recopilados por los sensores y enviar  
    resultados concretos a la nube, reduciendo así el ancho de banda requerido. La computación en la niebla puede  
    proporcionar servicios de computación, almacenamiento y redes ubicados entre los dispositivos finales  
    (sensores, actuadores, etc.) y los centros de datos tradicionales de computación en la nube,  
    con el fin de descentralizar la concentración de recursos y mejorar la calidad  
    del servicio. Esto permite la comunicación  
    entre dispositivos ubicuos, heterogéneos y descentralizados para realizar  
    tareas de procesamiento y almacenamiento sin la intervención de terceros. [16].
- El edge computing es un paradigma que permite procesar datos  
    cerca de la fuente, en lugar de en ubicaciones centralizadas. Es decir, el almacenamiento,  
    los recursos y el procesamiento de datos se acercan al lugar donde el usuario  
    consume la información, reduciendo así la latencia. Por ejemplo, tras  
    recopilar los datos, se analizan y/o se aplican operaciones de filtrado básicas.  
    El resultado se envía a la computación en la niebla (fog computing) y se recibe en gateways donde  
    se ejecutan funciones de filtrado más avanzadas y, en algunos casos, acciones de toma de decisiones  
    [18]. Los dispositivos que realizan el procesamiento en el edge se encuentran  
    en la misma red que la fuente de datos. Cabe  
    destacar que el edge computing puede procesar datos y enviar los resultados  
    directamente a la nube para su uso en aplicaciones; por lo tanto,  
    no requiere la existencia de la computación en la niebla.

## 4. Un nuevo modelo de seguridad por capas para arquitecturas IoT

## (Modelo de seguridad de IoT - IoTSeMo)

Según las diferentes arquitecturas de IoT analizadas, en este artículo  
se propone un nuevo modelo de seguridad por capas inspirado en la arquitectura simplificada de IoT  
propuesta por Cisco (Fig. 2) [15]. Este modelo utiliza la pila funcional principal de IoT junto con la  
pila de gestión de datos y computación de IoT, y considera que cada  
paradigma (Edge, Fog, Cloud) debe contar con las  
capas física, de comunicación y de aplicación. Esto permite ubicar los dispositivos, protocolos y aplicaciones, así como  
los aspectos de seguridad a considerar en cada uno,  
como se muestra en la Fig. 3. El objetivo es analizar y categorizar los aspectos de seguridad según  
los diferentes elementos utilizados en los paradigmas Edge, Fog y Cloud,  
o una combinación de estos, al desarrollar una aplicación para ofrecer servicios basados ​​en IoT  
. La utilidad del modelo radica en su capacidad para identificar claramente no  
solo la ciberseguridad y la seguridad de la información, sino también las necesidades de seguridad en función del  
tipo de dispositivos, los datos que se recopilan, almacenan, procesan y transfieren, así como  
la necesidad de implementar controles para proteger las capas física, de comunicación y de aplicación.

Fig. 3. Modelo de seguridad por capas IoTSeMo

Cada una de las capas del modelo se explicará a continuación.

- Capa de acceso a la red. Esta capa corresponde a las diferentes  
    tecnologías de acceso a la red (dispositivos y protocolos). Los sensores y actuadores (generalmente  
    ubicados en la capa de percepción en otras arquitecturas[3]–[5]) y, en general  
    , cualquier dispositivo de comunicación que opere en las capas 1 y 2 del  
    modelo de referencia OSI (física y de enlace) se ubican en esta capa. Algunas  
    tecnologías clasificadas como de borde, como LoRa, Bluetooth y Zigbee, no  
    tienen acceso al protocolo IP; por lo tanto, es esencial contar con una puerta de enlace  
    para proporcionar convergencia. De esta manera, es posible realizar  
    la traducción bidireccional de protocolos no enrutables al protocolo IP y viceversa  
    . Este componente se ubica entre la capa de acceso a la red  
    y la capa de comunicación. La puerta de enlace también tiene la función de administrar  
    los dispositivos ubicados en la capa de acceso a la red; por ejemplo, para monitorear cuándo un  
    nuevo dispositivo se une a la red o la abandona.
- Capa de comunicaciones: Esta capa se divide en dos subcapas:
    - Redes: Esta subcapa se encarga del direccionamiento global de todos  
        los dispositivos, por ejemplo, nodos sensores, actuadores, etc., y del enrutamiento de paquetes IP  
        .
    - Comunicaciones de extremo a extremo: Esta subcapa proporciona los protocolos TCP y UDP  
        . Asimismo, podría ofrecer comunicaciones seguras punto a punto  
        mediante el protocolo TLS.
- Capa de aplicación: Esta capa tiene dos subcapas: protocolos de aplicación TCP/IP
    y servicios elementales. En esta capa se encuentran los protocolos de capa de aplicación comunes, que facilitan la entrega bidireccional de datos
como MQTT, COAP, ZMQ; así como servicios elementales, por
ejemplo, almacenamiento, procesamiento, autenticación y cola de mensajes. Dependiendo
de la madurez de los servicios, se podrían generar servicios compuestos para
obtener información para la toma de decisiones y ofrecer servicios a aplicaciones inteligentes (ciudades inteligentes, transporte inteligente, edificios inteligentes, etc.), pero estos
servicios estarían fuera del modelo de seguridad, representados por el óvalo en
la parte superior, y como se propone en [19].

Fig. 4. Estudio de caso: Arquitectura de aplicación IoT [20]

## 5. Estudio de caso

Se analizará una aplicación representativa de IoT, con componentes en edge, fog y cloud,  
y se realizará el análisis y mapeo correspondiente según  
las capas del modelo de seguridad propuesto. La aplicación consiste en un  
sistema de notificación de proximidad en tiempo real que utiliza balizas IoT,  
dispositivos Bluetooth de baja energía que funcionan como transmisores de radio y se conectan a dispositivos móviles  
mediante señales de radiofrecuencia para localizarlos, enviar notificaciones  
o iniciar procesos en una aplicación [21]. Este tipo de aplicaciones generalmente se  
ofrecen a los usuarios sin medidas de seguridad, dado que la información que utilizan no se  
considera sensible. Sin embargo, esto no significa que no presenten  
riesgos de seguridad para el usuario, como el envío de notificaciones falsas sobre eventos de  
su interés para inducirlo a acercarse a un lugar con malas  
intenciones.  
La aplicación permite detectar la ubicación de los usuarios en un área determinada mediante balizas  
(en este caso, en el perímetro de una universidad), enviando mensajes personalizados  
a través de sus dispositivos móviles, basados ​​en sus preferencias y ubicación.

La aplicación informa a los usuarios sobre eventos cercanos para que puedan decidir si  
asistir o no [20]. Los usuarios pueden interactuar con la aplicación desde sus dispositivos para gestionar  
sus preferencias de notificación, por ejemplo, seleccionar categorías de interés, así  
como ver y eliminar notificaciones. Además, podrán calificar  
los eventos y escribir comentarios según sus impresiones durante el mismo. Con base  
en la información recibida de los usuarios, la aplicación podrá ofrecer  
información relevante y personalizada. La arquitectura de la aplicación se muestra en  
la Fig. 4. En esta arquitectura se identifican algunos componentes  
propios del paradigma edge, como balizas y teléfonos inteligentes. Por otro  
lado, algunos servicios se ubican en la categoría fog, como la puerta de enlace API  
y diferentes microservicios para emitir y notificar eventos según la  
información recibida, y otros componentes de software como Apache Kafka y  
Firebase Cloud Messaging (FCM) para poner en cola y notificar mensajes, respectivamente.  
Si un usuario pasa cerca de una baliza, esta detecta automáticamente su dispositivo móvil  
y le envía una notificación para informarle sobre un concierto de música clásica que tendrá  
lugar ese día en el conservatorio más cercano. El usuario puede  
optar por eliminar la notificación o programar su asistencia al concierto. Si  
asiste, podrá calificar el evento posteriormente.

Fig. 5. Modelo de seguridad IoTSeMo aplicado al caso de estudio

## 6. Aplicación del modelo de seguridad IoT - IoTSeMo

Ahora el caso de estudio se analiza y se mapea en el modelo IoTSeMo, de acuerdo  
con los protocolos, dispositivos, servicios y tecnologías utilizados por la aplicación (Fig.  
5).

- Capa de acceso a la red: Las tecnologías de acceso a la red utilizadas son:
    - Edge:Beacons, que se comunican con el smartphone mediante Bluetooth  
        . El usuario puede  
        acceder a la red a través de la aplicación mediante Wi-Fi o tecnología de datos móviles (4G, 5G).
    - Fog: La comunicación entre el teléfono del usuario y la  
        puerta de enlace API de la aplicación se realiza a través de Ethernet, ya que la puerta de enlace API está alojada en  
        un servidor local conectado a la red cableada.
    - Nube: Indiferente, porque los servicios podrían ser proporcionados por un tercero  
        .
- Capa de comunicación: Esta capa se subdividió en dos subcapas:
    - Conectividad: En esta arquitectura de aplicación existe convergencia IP, por lo que  
        el protocolo IP es común para edge, fog y cloud, y no es necesario  
        utilizar la puerta de enlace propuesta en el modelo de seguridad para el caso de estudio.
    - Comunicación de extremo a extremo: El protocolo utilizado por la aplicación del  
        caso de estudio es TCP para edge, fog y cloud.
- Capa de aplicación: Esta capa también se subdivide en dos subcapas:
    - Protocolos de aplicación TCP/IP: Los protocolos HTTP y JDBC se  
        utilizan en esta capa para edge, fog y cloud.
    - Servicios elementales para el estudio de caso: *Edge: En esta capa  
        no hay dispositivos ni protocolos para el estudio de caso . *Fog: Aquí se encuentra el API Gateway, que se comunica con diferentes servicios como eventos, estadísticas y personalización, entre otros. El API Gateway es un componente de la propia aplicación, distinto del Gateway en la arquitectura propuesta. El servicio de autenticación LDAP también se utiliza en esta capa para verificar la identidad de los usuarios y autorizarles a usar la aplicación. *Cloud: Aquí funciona Apache Kafka, que se utiliza para almacenar, poner en cola y enviar mensajes del servicio de notificaciones, y Firebase Cloud Messaging (FCM), que recibe los mensajes de Apache Kafka, los gestiona y los envía a los usuarios.  
          
          
          
          
          
          
          
          
          
          
        

El único servicio ofrecido es la notificación a los usuarios (óvalo en la parte superior del modelo).  
Tras mapear el caso de estudio de IoT en el modelo IoTSeMo, es posible analizar  
cada uno de sus componentes para asegurar la aplicación completa, tal como se aborda  
en [22], donde se analiza la capa física en la computación perimetral móvil. Este  
análisis se centra en la capa inferior del modelo de seguridad, particularmente en el entorno perimetral  
.

## 7. Conclusiones y trabajo futuro

El IoT se está aplicando en diversos contextos, pero esta tecnología conlleva  
riesgos de seguridad inherentes. Tras analizar diferentes arquitecturas de IoT y el enfoque de cada  
una, se deduce que el modelo IoTSeMo es una herramienta necesaria para  
analizar los protocolos, dispositivos y tecnologías empleados en un entorno IoT para  
cualquier tipo de aplicación, con el fin de identificar vulnerabilidades y aplicar los  
controles correspondientes para aumentar el nivel de seguridad de las aplicaciones.  
En la fase de diseño de software de una arquitectura IoT, es necesario establecer  
criterios de selección para cada componente. El modelo IoTSeMo puede resultar útil en  
esta fase con un enfoque descendente, para mapear cada componente de la  
arquitectura de la aplicación y facilitar la identificación de los responsables, la cronología, los costes,  
etc.  
Como trabajo futuro, se llevará a cabo la investigación pertinente para garantizar la seguridad en  
cada una de las capas del modelo de seguridad, analizando los aspectos que deben tenerse  
en cuenta según las tecnologías y aplicaciones más utilizadas en  
un entorno IoT, para proporcionar una guía que permita a los desarrolladores disponer de una  
herramienta de referencia para desarrollar aplicaciones IoT seguras.

## Referencias

```
[1] O. B. Akan, E. Dinc, M. Kuscu, O. Cetinkaya, and B. A. Bilgin, “Internet of
everything (ioe) - from molecules to the universe,”IEEE Communications
Magazine, vol. 61, no. 10, pp. 122–128, 2023.doi:10.1109/MCOM.001.
2200594.
[2] D. Mourtzis, J. Angelopoulos, and N. Panopoulos, “Design and develop-
ment of an edge-computing platform towards 5g technology adoption for
improving equipment predictive maintenance,” Procedia Computer Sci-
ence, vol. 200, pp. 611–619, Jan. 2022.doi:10.1016/j.procs.2022.
01.259.
[3] M. binti Mohamad Noor and W. H. Hassan, “Current research on internet
of things (iot) security: A survey,”Computer Networks, vol. 148, pp. 283–
294, 2019,issn: 1389-1286.
[4] E. Schiller, A. Aidoo, J. Fuhrer, J. Stahl, M. Ziörjen, and B. Stiller, “Land-
scape of iot security,”Computer Science Review, vol. 44, p. 100 467, 2022,
issn: 1574-0137.
[5] Q. Gou, L. Yan, Y. Liu, and Y. Li, “Construction and strategies in iot se-
curity system,” in2013 IEEE International Conference on Green Comput-
ing and Communications and IEEE Internet of Things and IEEE Cyber,
Physical and Social Computing, 2013, pp. 1129–1132.
[6] H. Mishra. “Commonly used sensors in iot.” (2019), (visited on 06/17/2019).
[7] K. Ashtonet al., “That ‘internet of things’ thing,”RFID journal, vol. 22,
no. 7, pp. 97–114, 2009.
[8] J. Ding, M. Nemati, C. Ranaweera, and J. Choi, “Iot connectivity technolo-
gies and applications: A survey,”IEEE Access, vol. 8, pp. 67 646–67 673,
2020.doi:10.1109/ACCESS.2020.2985932.
```

  
[9] J. Li, C. Wang, A. Li, et al., "Rf-rhythm: Secure and usable two-factor RFID authentication", en IEEE INFOCOM 2020 - IEEE Conference on Computer Communications, 2020, pp. 2194–2203. doi:10.1109/INFOCOM41043.2020.9155427.
[10] M. Aboubakar, M. Kellil y P. Roux, "A review of IoT network management: Current status and perspectives", Journal of King Saud University - Computer and Information Sciences, vol. 34, no. 7, pp. 4163–4176, 2022, issn: 1319-1578.
    [11] M. I. Malik, I. N. McAteer, P. Hannay, S. N. Firdous y Z. Baig, "XMPP architecture and security challenges in an IoT ecosystem", cited by: 4, 2018, pp. 62–73. doi:10.25958/5c52735166690.
[12] S. Li, L. D. Xu y S. Zhao, "5G internet of things: A survey", Journal of Industrial Information Integration, vol. 10, pp. 1–9, 2018, issn: 2452-414X.  
[13] L. Khalid, "Internet of Things (IoT)", en Software Architecture for Business. Cham: Springer International Publishing, 2020, pp. 107–127, ISBN: 978-3-030-13632-1. doi:10.1007/978-3-030-13632-1_7.
[14] N. M. Kumar y P. K. Mallick, "The internet of things: Insights into the building blocks, component interactions, and architecture layers", Procedia Computer Science, vol. 132, pp. 109–117, 2018, International Conference on Computational Intelligence and Data Science, ISSN: 1877-0509.
[15] D. Hanes, G. Salgueiro, P. Grossetete, R. Barton y J. Henry, IoT Fundamentals: Networking Technologies, Protocols, and Use Cases for the Internet of Things, 1st ed. Cisco Press, 2017, ISBN: 1587144565.
[16] P. Escamilla-Ambrosio, A. Rodríguez-Mota, E. Aguirre-Anaya, R. Acosta-Bermejo y M. Salinas-Rosales, "Distributing computing in the internet of things: Cloud, fog and edge computing overview," en NEO 2016: Results of the Numerical and Evolutionary Optimization Workshop NEO 2016 and the NEO Cities 2016 Workshop, Springer, 2018, pp. 87–115.
[17] F. Liu, J. Tong, J. Mao, et al., "Nist cloud computing reference architecture," NIST special publication, vol. 500, no. 2011, pp. 1–28, 2011.
[18] K. Bierzynski, A. Escobar y M. Eberl, "Cloud, fog and edge: Cooperation for the future?" En 2017 Second International Conference on Fog and Mobile Edge Computing (FMEC), IEEE, 2017, pp. 62-67.
[19] D. Darwish, "Improved layered architecture for internet of things", Int. J. Comput. Acad. Res. (IJCAR), vol. 4, no. 4, pp. 214–223, 2015.
[20] R. M. S. C. Aldana Juan Díaz Juan, Real-time proximity notification system based on IoT to promote the services of the vice-rectory of the environment at the Pontificia Universidad Javeriana. 2023.
[21] G. Sterling, J. Polonetsky y S. Fan, "Understanding beacons a guide to beacon technologies," en Future of Privacy Forum. Disponible en: https://fpf.org/wp-content/uploads/Guide_To_Beacons_Final.pdf, 2014.
[22] L. Chen, S. Tang, V. Balasubramanian, J. Xia, F. Zhou y L. Fan, "Physical layer security-based mobile edge computing for emerging cyber physical systems", Computer Communications, vol. 194, pp. 180–188, 2022, issn: 0140-3664.

Esta es una herramienta sin conexión; tus datos permanecen localmente y no se envían a ningún servidor.

[Comentarios e informes de errores](https://github.com/jzillmann/pdf-to-markdown/issues)