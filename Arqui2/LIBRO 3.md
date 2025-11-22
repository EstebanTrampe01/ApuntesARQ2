

---

# 2

## Anatomía de una arquitectura IoT

Al comenzar a pensar en la arquitectura y el conjunto de soluciones, es fundamental tener una idea clara de  
hacia dónde nos dirigimos. En el Capítulo 1, "Introducción a la evolución del IoT", analizamos la importancia de  
alinear los equipos de negocio y producción con sus objetivos. Sin embargo, en este capítulo nos centraremos  
en el aspecto de TI e IoT y en cómo alcanzar dichos objetivos desde una  
perspectiva arquitectónica: cómo se deben recopilar los datos, cómo fluyen y se gestionan a través del sistema,  
dónde comienza su procesamiento y qué etapas de procesamiento se deben considerar.  
Finalmente, aprenderemos a poner esos datos, junto con el análisis y la información resultante, a disposición de la  
empresa para la toma de decisiones.

Estas decisiones se basan en múltiples factores, como su sector, objetivos comerciales, disponibilidad de  
datos recopilados y el tipo, la ubicación y la velocidad de los datos que recopila. Este capítulo pretende  
ofrecer una orientación inicial en su enfoque y toma de decisiones, guiándolo a través de las opciones  
disponibles. Este libro se ha centrado en el uso de **Amazon Web Services** ( **AWS** ) como  
proveedor de servicios en la nube para todos los ejemplos; sin embargo, en este capítulo, continuaremos centrándonos en conceptos  
que, en su mayoría, pueden adaptarse a diversas soluciones en la nube. En este capítulo, abordaremos los  
siguientes temas principales:

- Pensamiento arquitectónico
- Componentes arquitectónicos para IoT
- Uniendo todo
- Definir estándares

A medida que avancemos por las capas arquitectónicas, identificaremos varios productos y servicios de AWS  
que se pueden aplicar en cada una. Esto le ayudará a comprender mejor cómo  
se pueden aplicar los diferentes servicios. Estos son solo ejemplos iniciales de los distintos tipos de servicios disponibles, sin  
centrarnos en si son o no los adecuados. En capítulos posteriores, profundizaremos  
en las capas y tomaremos decisiones concretas sobre qué servicios utilizar para nuestra  
solución específica.

24 Anatomía de una arquitectura IoT

## Requisitos técnicos

Una buena comprensión de las tecnologías y servicios en la nube será útil en este capítulo. Aunque
estamos mirando las cosas de manera más genérica, uno de nuestros objetivos en este libro es proporcionar asesoramiento de diseño e
implementación sobre la construcción de soluciones utilizando AWS. Por lo tanto, algún conocimiento general de
AWS y algunos de los servicios IoT será útil para tu comprensión pero no es necesario.
Si estás familiarizado con otro proveedor de nube, probablemente puedas mapear esos servicios directamente en
las capas que presentamos.

## Pensamiento arquitectónico

Construir una gran arquitectura IoT requiere una buena comprensión de los pasos involucrados y cómo todo
encaja. La mayoría de nosotros conocemos los conceptos básicos, al menos conceptualmente, de cómo recopilar datos de varias maneras
y luego mover datos a la nube, pero armar un flujo de extremo a extremo que te permita procesar,
almacenar y visualizar datos y el análisis posterior es el desafío. Hay muchas formas de lograr
estos objetivos, y no pensarlo a fondo podría tener consecuencias. Esto podría ser costoso si se requiere un rehacer
en el futuro. Por otro lado, demasiado análisis y sobretrabajar tu arquitectura
también puede tener el efecto de costarte más tiempo y esfuerzo, tanto inicialmente como a largo plazo.

Los arquitectos a menudo necesitan caminar una línea muy delgada entre el enfoque tradicional de diseñar para cada
ocurrencia (¿y si necesitamos esta función o esa característica en el futuro?), y un enfoque más ágil
de construir solo lo que necesitas, cuando lo necesitas. A menudo tiendo hacia el último enfoque, especialmente
cuando sé que el tiempo y el presupuesto no están a nuestro favor. A todos les encanta superar las expectativas, pero
esto puede ser problemático si arriesgas no cumplir ninguna expectativa como resultado de intentarlo.

### Modelos de referencia

```
In today’s world, generally, we can start with a reference model. Reference models are a wonderful
thing in IoT, or really in any technical or architectural endeavor. It wasn’t too long ago that we were
"guring things out as we went, literally building the reference models for the future. Reference models
provide bene"ts in several areas.
First, reference models guide us on how things can "t together. Most reference models are based
on best practices taken from other teams or cloud providers who have been there; done that! As a
starting point, this can remove some of the initial concerns around if you are doing it the right way. It
is never one-size-"ts-all in this "eld, so adapting a model or approach to your environment is probably
necessary. You may prefer a different cloud provider or have a unique environment that needs to be
heavily customized. Adapting and building your interpretation is perfectly understandable and expected.
```

```
Second, reference models provide a way to communicate across the organization where you are headed.
Depending on the level of detail, this will ensure that all stakeholders understand and agree on the
approach, that the implementation team knows how to move forward, and that there is consistency
across the organization as your Industry 4.0 plan moves forward.
```

```
Architectural components for IoT 25
```

Al crear un modelo de referencia, es importante evitar diseñar modelos  
o diagramas demasiado complejos. A veces, esto es necesario, pero con frecuencia se convierte en una experiencia abrumadora, donde pocos  
interesados ​​comprenden toda la complejidad. Debes saber que esto nos molesta especialmente. Un mejor enfoque  
consiste en dividir el modelo en diferentes niveles de complejidad, comenzando con un diagrama de nivel 0 (nivel general) y  
luego profundizando con modelos adicionales para los niveles 1, 2 y 3 de detalle.

A menudo, los modelos de referencia se utilizan para comunicar al equipo técnico y de negocio cómo  
deberían funcionar las cosas. En sistemas o entornos complejos, podemos empezar con niveles para ilustrar conceptos  
de forma sencilla. Esto permite a las partes interesadas no técnicas comprender el enfoque sin tener que adentrarse en  
detalles técnicos complejos que pueden no ser de su interés o que no comprendan del todo.

Si partes de cero y solo quieres hacerte una idea de cómo podría ser,  
considera los mejores productos del mercado y las mejores prácticas de algunos proveedores líderes. Puede ser complicado, ya que  
existe una fuerte tendencia a depender exclusivamente de los planes de ciertos proveedores y usar solo sus productos. Sin embargo,  
también puede proporcionarte el punto de partida necesario para comprender cómo algunas de las tecnologías más recientes  
pueden funcionar en tu entorno. Avanza poco a poco y con paso firme hasta que logres discernir  
la tecnología adecuada para tus objetivos.

## Componentes arquitectónicos para IoT

Para comprender hacia dónde vamos, a veces debemos saber de dónde venimos. La historia  
de las tecnologías de la información y la automatización industrial puede ayudarnos a entender cómo funcionan las cosas hoy en día, y podemos  
aprovecharla a medida que la tecnología evoluciona. Uno de esos primeros modelos de referencia es la  
Arquitectura de Referencia de Purdue, desarrollada a mediados de la década de 1990. Una de las características clave del modelo de Purdue es la  
definición de capas o niveles de separación para los sistemas industriales.

ISA-95 es el estándar para la automatización de sistemas de control empresarial, basado en el  
modelo Purdue y en constante evolución. El objetivo de ISA-95 es definir estándares para  
la interconexión de sistemas de control de producción y sistemas de TI empresariales, centrándose en las capas 3 y 4 del  
modelo de referencia Purdue. Es aquí donde, generalmente, los protocolos operativos, como los protocolos de bus de campo, se integran con  
las redes de TI o Ethernet.

En gran medida, nos adentramos en el ámbito de **la Arquitectura Empresarial** ( **AE** ) y definimos la  
arquitectura, los estándares y la visión para toda la organización. Pero también debemos integrar esa visión  
con las dependencias, restricciones y objetivos operativos. Uno de los objetivos de definición de la AE es instaurar  
disciplina en la arquitectura, al tiempo que se proporcionan las capacidades que la organización  
necesita para operar y evolucionar.

La arquitectura empresarial (AE) es un tema amplio que actualmente se divide entre arquitectura técnica y arquitectura de negocio, lo cual implica  
considerar muchos aspectos. Este libro ofrece una visión general de diversas áreas, pero también se centra en la  
implementación práctica de algunas de las tecnologías que se analizan. Sin embargo, las lecciones aprendidas en este libro  
pueden aplicarse a la debida diligencia de su AE para determinar el mejor camino a seguir para su organización.  
Los patrones que surjan de este trabajo pueden implementarse en toda la empresa como estándares futuros.

26 Anatomía de una arquitectura IoT

### Diseño por capas

La arquitectura de referencia de Purdue define seis niveles divididos en varias zonas. Este es un gran
comien zo para comprender la automatización digital y la integración de sistemas industriales, y queremos
proporcionar una sensación de familiaridad para aquellos que ya están cómodos con estos niveles. Pero la tecnología evoluciona
a un ritmo rápido, y nuestra pila tecnológica tiene más que probablemente mayor capacidad que la disponible anteriormente. Así que, para adaptarnos según sea necesario para acomodar los cambios tecnológicos (la manivela tecnológica está
siempre girando) con el tiempo, nuestra pila se verá diferente.

Nuestro enfoque es realmente ver nuestro modelo más desde el punto de vista de la arquitectura IoT y en la nube.
Estamos enfocados en la nube, debemos llevar datos a la nube y almacenar, analizar y presentarlos tan
eficientemente y robustamente como sea posible. Esto nos permite aprovechar al máximo las últimas mejores prácticas
y puntos de vista arquitectónicos para esta tecnología. Luego podemos incorporar controles y sistemas industriales
según sea apropiado para nuestros objetivos:

Figura 2.1 – Esquema de arquitectura por capas

La Figura 2.1 es nuestra primera mirada a una arquitectura de referencia por capas. He evitado dar a estas capas números específicos
ya que creo que debería haber cierta fluidez basada en tus circunstancias. Sin embargo, este modelo
puede mapearse fácilmente al modelo Purdue, u otros modelos industriales, o modificarse completamente según
tu experiencia y preferencias.

También existe la posibilidad de que, con tantos esfuerzos de digitalización, algunos modelos iniciales no se ajusten a su  
visión. La ruta de comunicación más estricta entre el sensor y el usuario final puede fallar a medida que  
evolucionan nuevos protocolos de comunicación y sensores que permiten la comunicación directa desde el sensor a la nube. Nuestro  
objetivo es mantener este modelo de arquitectura flexible y permitirle incluir consideraciones adicionales en  
su diseño, para que pueda asegurarse de que su arquitectura se ajuste a los objetivos  
y estándares de la organización, y no a la visión de otra persona.

Las grandes organizaciones con numerosas instalaciones pueden enfrentarse a desafíos adicionales, sobre todo cuando existe poca  
estandarización y homogeneidad entre las fábricas. Algunos de estos desafíos exceden el alcance  
de este libro. Esperamos poder ofrecerles orientación para aprovechar la nube en su proceso, pero  
la implementación de una estructura y la aplicación de la arquitectura empresarial en cualquier gran organización requieren un esfuerzo considerable.

Los consultores suelen referirse a los procesos como un importante motor de cambio, y esto es muy cierto. La  
mejor solución técnica puede fracasar si los procesos internos o de negocio no cambian. Es difícil que  
fuerzas externas influyan en este cambio dentro de la organización. Debe surgir desde dentro,  
y nuestra responsabilidad es demostrar por qué un cambio o una reestructuración de procesos será mejor para todos.  
Comunicar el valor para la organización y el beneficio real para cada parte interesada es el  
principal desafío en este proceso.

### Definir las capas

Las capas de la Figura 2.1 son una representación simplificada de lo que podrían considerarse sus  
intentos de diseño iniciales, que es el tema central de este capítulo. Definir cada capa nos ayudará a definir  
cómo podríamos utilizarlas y a establecer límites claros entre ellas. Al considerar los  
límites entre capas, es importante tener en cuenta las opciones de comunicación, los protocolos y la seguridad a medida que  
los datos cruzan los límites definidos.

Si bien dedicaremos algo de tiempo a definir cada una de las capas, nuestro objetivo final es utilizarlas en  
nuestra arquitectura. Una pregunta clave es: ¿por qué? ¿Por qué presentamos y sugerimos una  
arquitectura en capas? Este enfoque ofrece numerosas ventajas y su uso se remonta a décadas atrás, desde  
los primeros enfoques de arquitectura de computación distribuida multicapa hasta las prácticas recomendadas actuales en la nube.

El uso de capas permite agrupar funciones similares, como la ingesta, el almacenamiento o el análisis de datos, en  
áreas distintas. Esto permite que la lógica de procesamiento o la lógica de negocio residan juntas.  
Además, el uso de capas fomenta la separación de responsabilidades. Si bien esto es bastante obvio, conviene aclarar  
que la ingesta, el almacenamiento o la transformación de datos deben realizarse en una sola capa. Esto  
facilita la implementación de cambios en funcionalidades específicas si estas funciones se encuentran agrupadas en  
una misma área. Por ejemplo, la decodificación de mensajes de datos suele cambiar al agregar nuevas mediciones  
o al implementar un sensor diferente con un tipo de mensaje específico. Limitar estos cambios a una  
capa y un conjunto de servicios específicos ayuda a gestionar el cambio en todo el entorno.

28 Anatomía de una arquitectura IoT

```
Another consideration is that most of the data collection, transformation, and analysis can happen
in more or less real time. In many cases, this can be clari"ed as “near” real-time analysis since the
expectation is not instantaneous. A delay of several minutes or more should be expected as data winds
its way from the machine through processing and becomes available for analysis. If the expectation
is quicker data availability, then edge analysis is where you might turn, where network latency and
data transformation will not introduce the expected delays.
```

```
Like most modern architecture work, ensuring that the contract between layers and systems is well-
de"ned allows for !exibility as data moves up the stack. In this section, we will brie!y describe each
layer for clarity and then provide more detail on how different layers can be implemented in theory.
```

#### Sensores y controladores de dispositivos

En esta sección, describiremos las primeras dos capas. La primera capa consiste en sensores y actuadores para
medir y controlar sistemas físicos. La segunda capa está compuesta por controladores de dispositivos y
sistemas. Inicialmente, nuestro enfoque está en recopilar datos en la fuente. Esto requiere colocar sensores dentro del
entorno, adjuntándolos al equipo directamente, o conectándolos a fuentes disponibles existentes.
En el próximo capítulo, profundizaremos en los detalles sobre el abastecimiento, configuración y distribución de sensores en el
campo, mientras exploramos el concepto de monitoreo ambiental.

Definimos un sensor como un dispositivo de medición que puede recopilar datos analógicos o digitales directos de, o sobre,
un sistema. En realidad, es un transductor, que convierte energía de una forma a otra, que mide
cosas como temperatura o presión y proporciona un voltaje analógico o digital basado en esa
medición. Solo, este dispositivo no hace mucho. A menudo recibe algo de energía o una señal de datos y
luego devuelve un voltaje resultante o algún tipo de código serial para identificar el valor que está leyendo. Para hacer
uso de esa lectura, el sensor requiere una conexión a algo que pueda activar la lectura, leer
la salida (y a menudo los valores de potencia y entrada) del sensor, interpretar el valor y enviarlo a
sistemas en espera. Nos referimos a la cosa que lee y transmite el valor del sensor real como un
nodo, aunque, en términos industriales, a menudo se le llama Unidad de Telemetría Remota (RTU):

Figura 2.2 – Sensores y controladores de dispositivos

La figura 2.2 se centra en las capas iniciales de la arquitectura. Los nodos sensores suelen estar conectados a múltiples
sensores (o transductores), proporcionando valores de medición como temperatura, presión, luz,
etc. Generalmente, son dispositivos cerrados con varios sensores integrados o conectados, que se comunican con
una red o entorno en la nube como un único dispositivo, incluyendo diversas mediciones en el mensaje.
Es importante mantener una distinción lógica, una jerarquía de dispositivos en la red y
una ubicación definida de los dispositivos conectados dentro del sistema. Estas mediciones son valores independientes de diferentes
tipos, y es necesario gestionarlas y registrarlas para que, posteriormente, durante el análisis, se puedan
analizar o comparar valores similares como un conjunto. En otras palabras, la temperatura y la humedad son mediciones independientes
y deben tratarse como tales, incluso si provienen del mismo dispositivo.

Los actuadores, por otro lado, son dispositivos de control que regulan los dispositivos finales a través de las entradas
de las capas superiores. Son responsables del cambio físico en el estado del comportamiento de los
dispositivos finales. Tener la capacidad de activar dispositivos de forma remota y más autónoma ayuda a gestionar
empresas desde un solo centro de mando y control inteligente. Al hacer esto en tiempo real, la seguridad
es una consideración clave. Profundizaremos en esto más adelante en este libro en el Capítulo 9.

**Más o menos capas**

Durante este libro, habrá muchas preguntas de tipo arquitectónico y de convención a considerar.
Por ejemplo, ¿las redes de control industrial son parte de la capa de sensores o de la capa de controladores?
¿Agregamos una capa intermedia para acomodar controladores locales como PLCs o redes de sistemas cerrados
como SCADA? ¿O deberíamos mapear estas capas más cerca del modelo Purdue para proporcionar
mejor consistencia con las arquitecturas de referencia? Esto depende en gran medida de tu entorno existente
y estándares arquitectónicos. Puede ser el caso donde agregues múltiples capas para
acomodar diferentes redes de control dentro de tu fábrica. En muchos casos, tu red industrial
está separada de tu red empresarial y esto afectará tu diseño. En este
capítulo, hemos presentado el caso más simple que puede modificarse o construirse sobre él, para mostrar
la interacción con tus sistemas industriales y facilitar el flujo y análisis de datos. Considera esto
el caso más básico que se ajustará a la mayoría de los entornos, pero expandir esta arquitectura es, en la mayoría
de los casos, casi seguramente requerido.

**Patrones de automatización**

Hemos dividido las primeras dos capas en tipos distintos de sistemas definidos en la siguiente lista. Esto
nos ayudará a definir un conjunto inicial de patrones, basados en el tipo de sensor o red, y la forma en que
los datos se acceden desde el piso de la fábrica. Para organizaciones grandes, el objetivo es definir patrones y
enfoques para acceder a datos a través de una gran fábrica o muchas fábricas. Esto puede volverse complejo, pero si puedes
estandarizar el hardware, software y adquisición de datos basados en el tipo de dispositivo, máquina
o línea de ensamblaje, has ganado gran parte de la batalla.

A largo plazo, esto puede simplificar el despliegue, monitoreo y gestión de tu infraestructura de instrumentación.
Para aquellos que no están tan familiarizados con la Tecnología Operativa (OT) y lo que pueden estar
enfrentando, estos tipos principales de entornos consisten en lo siguiente:

**Sistemas de control industrial**: Generalmente, asociamos SCADA con este grupo. **SCADA**
es el acrónimo de **Sistemas de Control y Adquisición de Datos (Supervisory Control and Data Acquisition Systems**). Se utiliza comúnmente
junto con equipos de control adicionales, como **controladores lógicos programables**
( **PLC** ) y RTU. En conjunto, este equipo, con un sistema de red industrial de bus de campo que utiliza un
protocolo definido como Modbus, BACnet o Probus, se emplea para controlar
sistemas industriales grandes o distribuidos en tiempo real.

Estos sistemas suelen ser de lazo cerrado, especialmente los sistemas heredados
con varias décadas de antigüedad. La extracción de datos de estos sistemas puede requerir la conversión
de un formato a otro para permitir su envío a sistemas externos, como la nube.

Técnicamente, esto es mucho más fácil hoy en día con la gran cantidad de hardware y software que
atiende a este tipo de instrumentación. Puede haber desafíos internos dentro del equipo de producción
en cuanto a qué se instrumenta y cómo, siendo la prioridad número uno evitar cualquier
interrupción en la producción en curso.

- **Redes IP de dispositivos** : Las redes IP de dispositivos son más modernas en su enfoque tecnológico,  
    interactuando con redes de TI mediante protocolos comunes que facilitan la comunicación con  
    aplicaciones IP o TCP estándar. Generalmente, pensamos en dispositivos o sistemas de esta categoría que  
    ya utilizan protocolos fácilmente compatibles. MQTT es un buen ejemplo.  
    Se trata de un protocolo sencillo y ligero que utiliza TCP para enviar mensajes. La  
    cabecera del mensaje se compone de cadenas simples, pero en muchos casos, el paquete de datos puede cifrarse o  
    codificarse por motivos de seguridad o para limitar su tamaño.  
    Existen múltiples proveedores en este sector, ya sea interactuando con sistemas de control industrial, controlándolos  
    o proporcionando instrumentación junto a ellos. Al abordar la integración, es  
    fundamental evaluar los sistemas existentes y determinar si  
    existen puntos de integración disponibles. En muchos casos, los proveedores trabajan para ofrecer una solución completa para  
    la digitalización del entorno. Si este es el caso y usted está abierto a ello, el problema está resuelto.  
    Sin embargo, la realidad es que nadie ofrece todas las soluciones necesarias, y la integración de  
    componentes diversos es la dura realidad de muchos equipos de operaciones en todo el mundo.
- **Redes IoT** : Las redes IoT, como **las redes de área amplia de baja potencia** ( **LPWAN** ), constituyen una  
    categoría amplia y están diseñadas para incorporar sensores y nodos que no se conectan a  
    las redes cableadas tradicionales en entornos industriales. Existen varios protocolos y sistemas inalámbricos recientes  
    que permiten la instrumentación sin necesidad de acceder al funcionamiento interno  
    del equipo. Algunos de ellos llevan varios años en el mercado y han sido probados en  
    entornos exigentes. Estos dispositivos suelen ser de bajo consumo y su alcance  
    y la cantidad de datos que pueden enviar desde cada nodo pueden variar. Las  
    **redes de largo alcance** ( **LoRa** ) o **LoRaWAN** se han convertido en una opción popular cuando se debe considerar el consumo de energía  
    o el tamaño del dispositivo y se  
    requiere un alcance de hasta varios kilómetros. Una alternativa como 4G o 5G puede ser una buena opción si se requiere una red pública,  
    por ejemplo, en exteriores o zonas urbanas, y no es posible instalar gateways. Analizaremos con  
    más detalle algunas de estas opciones en los próximos capítulos.

Con tantas opciones, la situación puede diversificarse rápidamente. Ese es precisamente el punto clave. ¿Cómo  
abordamos los sistemas heredados y los distintos entornos de forma estructurada? Si se construye una nueva  
fábrica hoy en día, gran parte de esta instrumentación puede estar integrada, junto con  
los sistemas de ejecución de fabricación, lo que contribuye al control operativo y la eficiencia. Pero existen  
miles (¿millones?) de granjas industriales, fábricas y plantas que pueden beneficiarse de una mayor  
digitalización. Incluso en el primer caso, con maquinaria moderna integrada y adquisición de datos, necesitamos  
un lugar donde transformar, almacenar y analizar estos datos. Obtener datos de los sistemas existentes, aunque  
a veces supone un reto, es posible. Pero surge la pregunta: ¿y ahora qué?, y debemos analizar  
qué hacer con los datos recopilados.

32 Anatomía de una arquitectura IoT

#### Servidores y aplicaciones perimetrales

En contraste con la capa de sensores anterior, que en muchos casos puede definirse estrechamente, la capa de controladores
es mucho más amplia y abarca desde la lógica de escalera simplemente definida dentro de los PLCs hasta
servidores edge completos que analizan y preprocesan flujos de datos en vuelo en tiempo real. Mencionamos
esto brevemente en el recuadro Más o menos capas – pueden requerirse capas adicionales para acomodar
diferentes redes y sistemas de fabricación o control según tu entorno:

Figura 2.3 – Servidores edge y la capa de aplicaciones

En pocas palabras, podemos ver esta capa, delineada en la Figura 2.3, como donde los datos se extraen del
entorno y se preparan para ser reenviados o procesados en la siguiente capa o en la nube. Esto puede
hacerse interactuando con un conjunto existente de sistemas como una interfaz Modbus, interactuando con un
historiador local o interfaz SCADA, o incluso recibiendo datos de sensores directamente a través de una red
cableada o inalámbrica local. Los dispositivos edge como controladores y servidores pueden servir a diferentes propósitos, como
los siguientes:

- Ayudar a convertir datos de protocolos propietarios o no informáticos a un formato más estándar de TI,
    como MQTT.
- Reducir los problemas de latencia al transferir datos locales a la nube, debido al volumen potencialmente alto
    de datos que se pueden generar. Los datos se pueden almacenar para su posterior transferencia, preprocesar, agregar
    o filtrar según sea necesario.
- Realizar análisis y control in situ (en el borde de la red) en función de las condiciones actuales de
    forma más actualizada y en tiempo real.

Los controladores cerrados tradicionales como PLCs o PACs también pueden existir en esta capa, o dentro del entorno,
con adaptadores que reciben datos de estos dispositivos para reenviarlos y analizarlos por parte de las operaciones. No todos
los dispositivos en esta capa necesitan ser dispositivos inteligentes. Algunos se usan simplemente para interpretar, traducir o reenviar
datos a la nube. Esto es más a menudo que no el caso real cuando se está comenzando o con sistemas de menor prioridad.
Simplemente queremos visualizar las operaciones de una manera más significativa para monitorear la consistencia,
el rendimiento o las métricas a nivel de equipo.

**WAN o VPN a la nube**

Aunque no es precisamente una capa, la WAN está definida dentro de la arquitectura; debemos tomarnos un momento para
discutir la división lógica y física entre la recolección de datos en las instalaciones y el análisis dentro
de la nube. La división entre la fábrica y la red corporativa (o la nube) puede ser
simple o compleja, dependiendo de cómo TI empresarial haya estructurado las interfaces de red y
la implementación de seguridad. A menudo, hay un camino definido para el flujo de datos desde dentro hacia fuera de
las paredes de la fábrica, y es vital definir este transporte de manera segura. El objetivo es proteger ambas redes
de intrusiones y garantizar la integridad de los datos.

Incluso en casos donde estés usando un transporte de terceros como LoRa o 4/5G, puedes
controlar la salida de datos donde fluye dentro de tu red. En algunos casos, donde se usa transporte más público,
como LTE, esto puede no ser posible, por lo que la seguridad física es esencial para tus
puntos finales, y debes confiar en la seguridad de la red de terceros para proteger tus datos.

#### Gestión de dispositivos

Hemos separado la gestión de dispositivos en una capa independiente, como se muestra en la Figura 2.4; sin embargo, esto
no necesariamente dependerá de tu entorno. La gestión de dispositivos se centra en la incorporación,
la administración y la seguridad de tus dispositivos de forma simplificada. Con cientos o miles de dispositivos,
administrarlos y organizarlos puede resultar complejo. Esto es especialmente cierto si los dispositivos cambian
con frecuencia. La administración de certificados también se puede gestionar en esta capa, sobre todo con
sistemas perimetrales inteligentes, donde es necesario garantizar la seguridad de los dispositivos antes de que se comuniquen con tu plataforma.

Figura 2.4 – Capa de gestión de dispositivos

Los gemelos digitales, también conocidos como réplicas digitales, son otra forma de rastrear
y administrar tus dispositivos. Una réplica digital es una representación de tu dispositivo que mantiene
su estado y configuración actuales. Esto te permite interactuar con la réplica en lugar de hacerlo
directamente con el dispositivo y aplicar cambios para ver cómo reacciona o para implementarlos en el dispositivo.

Una réplica de dispositivo también tendrá la última configuración y estado conocido del dispositivo, incluso si el dispositivo
está desconectado. Los usuarios pueden ver cuál fue esa última configuración antes de que se desconectara o desconectara del
sistema.

#### Ingesta de datos en la nube

Aquí es donde comienza la recopilación de datos para la nube. Ingerir e interpretar datos en una variedad de
formatos puede ser un desafío. Pero si lo desglosamos e identificamos patrones, se vuelve manejable y
quizás hasta divertido. Nuestro enfoque está en recopilar datos de fábricas, campos y equipos que se utilizan en
la fabricación y la industria. El tipo de mediciones recopiladas puede tener un amplio rango en su tipo,
volumen e importancia de los datos para los procesos operativos y comerciales.

Los patrones de ingesta probablemente serán específicos para tu organización y tus datos pero no poco comunes en
la industria. AWS proporciona varios servicios para que puedas ingerir y transformar datos, y dependiendo del
formato, protocolo, volumen y velocidad de tus datos, esto impulsará parte de tu toma de decisiones
en esta área. Rara vez hay un enfoque único para todos, especialmente para soluciones industriales con muchas
soluciones heredadas, y a menudo, un enfoque es tan bueno como otro, siempre que se esté haciendo
progreso hacia adelante. A menudo, puede depender de tu experiencia, habilidades y preferencia en estas áreas técnicas:

Figura 2.5 – Ingesta de datos

La Figura 2.5 describe algunos de los enfoques de ingesta de datos disponibles. Hay otra área gris entre
la ingesta de datos, y la transformación y almacenamiento de datos. ¿Almacenas los datos crudos directamente antes de que sean

```
Architectural components for IoT 35
```

¿Transformado de alguna manera? #Esto puede brindar una sensación de mantener la coherencia y precisión de los datos, para  
poder rastrearlos hasta los originales cuando algo parece estar mal o la información se pone en duda.  
#Hay muchas ideas sobre cómo llenar el almacenamiento de datos sin procesar:

- Consideremos la cantidad de transformación que se realiza en el borde de la red antes de que los datos y los valores de medición  
    lleguen a la nube. La actividad en el borde se utiliza a menudo para reducir el ancho de banda o aumentar  
    el tiempo de respuesta con flujos de datos de gran volumen. La integridad y la precisión de los datos podrían verse  
    comprometidas en niveles inferiores de la arquitectura.
- Considere si conviene transformar ligeramente los datos antes de almacenarlos como datos sin procesar. Algunos datos llegan  
    como cadenas binarias o seriales, codificadas para reducir su tamaño durante la transmisión. ¿  
    Deberían almacenarse tal cual o convertirse en texto legible y valores antes de su almacenamiento?
- Finalmente, considere el costo y el esfuerzo que implica almacenar datos sin procesar a largo plazo. El  
    beneficio puede superar con creces el costo si se cuestiona la autenticidad de los datos y se puede rastrear  
    su origen.

Alternativamente, puede haber requisitos legales que exijan que esta información se almacene sin procesar y  
sin modificaciones. Esto podría ser obligatorio y, por lo tanto, es una opción a considerar en su estrategia. Sin embargo, puede  
haber diferentes requisitos para distintos flujos de datos, pero lo mejor es definir sus  
requisitos y estándares de almacenamiento de datos sin procesar y mantenerlos consistentes.

#### Almacenamiento y transformación de datos

El almacenamiento y la recuperación son aspectos críticos a considerar, especialmente con grandes volúmenes de datos.  
Existen muchas opciones, y es necesario analizarlas detenidamente teniendo en cuenta sus  
necesidades actuales y futuras (aún desconocidas). Algunas opciones incluyen:

- lago de datos
- Almacén de datos
- Híbrido lago/almacén

Analicemos cada uno de estos puntos con un poco más de detalle.

**Estructura del lago de datos**

Utilizar un lago de datos como repositorio ofrece gran flexibilidad y la capacidad de almacenar todos  
los datos actuales y futuros de forma rentable, fácilmente gestionable y útil para su transformación y análisis posterior.  
Un lago de datos se asemeja más a un enfoque de almacenamiento de objetos o archivos (como la  
estructura de carpetas de Windows) que a un almacén de datos, que es más relacional. El concepto de almacén de datos existe  
desde hace décadas y sigue siendo una forma muy común y útil de almacenar y analizar  
datos relacionales. Su principal inconveniente es que los datos deben estar formateados y estructurados para que puedan integrarse  
correctamente en el almacén de datos, mientras que un lago de datos simplemente almacena cualquier tipo de archivo en cualquier formato.

36 Anatomía de una arquitectura IoT

```
In AWS, the most common data lake approach is to use Simple Storage Service ( S3 ) and store your
data as !at "les within a very well-de"ned folder structure or hierarchy. In addition, you can and
should use multiple areas within your data lake to store and transform data in different stages as it is
processed. You can think of these as different lakes with streams attaching them, with the water getting
cleaner as it !ows from the "rst lake to the last. Many layers of processed data can exist within your
lake, but we will narrow it down to a few of what we consider the key layers:
```

```
Figure 2.6 – Data transformation and storage
```

```
Figure 2.6 outlines one approach for designing your data lake environment and storing your data.
Let’s break down this approach in more detail:
```

- **Capa de datos sin procesar** : La capa de datos sin procesar es donde se capturan o ingieren inicialmente todos los datos. Estos datos  
    generalmente no están listos para su consumo o uso para análisis. La ventaja principal de esta capa es que  
    los datos se pueden ingerir y almacenar rápidamente. Esto facilita y agiliza  
    el diseño de la entrada del flujo de datos, ya que en este punto se realiza poca transformación.  
    Existen varias reglas o estándares comunes para la capa de datos sin procesar. Seguir estas  
    convenciones es opcional, pero para algunas industrias que requieren una trazabilidad estricta y garantizar  
    la integridad de los datos, estas reglas básicas son útiles:  
    A. Los datos se almacenan en su formato original o sin procesar. Puede ser necesario realizar algún análisis de mensajes para  
    determinar en qué parte del lago de datos se deben escribir los datos. Sin embargo, el mensaje original sin procesar  
    es el que se almacena con todos los metadatos adjuntos.

```
Architectural components for IoT 37
```

```
B. Data is immutable or cannot be changed once it is stored. Additionally, this lake should
be secure. It does not seem likely that access to this data is required, so lock it down and
protect the integrity of the store.
A potential design point arises around the folder structure of the storage, or schema if you
will. #is needs to be well-de"ned, ensuring that data can be found and managed easily as data
grows and more sources contribute to the lake. #e format of the structure can be !exible and
should be de"ned based on your needs. Time series data can take a familiar structure to allow
you to "nd speci"c data by type or source; for example, Source  Component  Type  Year
 Month  Day  Hour  <Minute>:<Second>. However, your needs may vary, depending
on the type of data and your industry.
```

**Definir un esquema**

Estructurar los datos es un desafío común con cualquier tipo de almacenamiento, ya sea un  
lago de datos, una base de datos relacional o incluso una base de datos de series temporales. Existen muchos ejemplos en la  
web, pero los diferentes enfoques suelen depender de las necesidades específicas de cada usuario. Definir la  
estructura o el esquema adecuado para los datos es una de las primeras tareas que deben realizarse, y  
a menudo, es cuando se dispone de menos información sobre cómo se adquirirán o  
utilizarán los datos. Nuestro consejo es avanzar con cautela y lentamente. Lo más probable es que no se tome una  
decisión errónea o desastrosa, pero es fácil arrepentirse posteriormente y terminar  
invirtiendo tiempo y esfuerzo en eliminar la deuda técnica mediante una reestructuración.

- **Capa de datos formateados** : La transformación y el formateo iniciales deben ocurrir al mover  
    los datos de la capa de datos sin procesar a la capa formateada. Tan pronto como los datos se depositan en la capa de datos sin procesar,  
    puede comenzar este proceso de transformación. Esto significa que los datos comienzan a tener significado y estructura  
    a medida que se procesan en esta capa.  
    En la capa de datos sin procesar, los datos conservan su formato original en la medida de lo posible, pero a medida que los formateamos, transformamos  
    y estandarizamos, este formato desaparece y una cadena hexadecimal de 16 bytes se transforma en  
    un conjunto de valores reales, como temperatura y humedad. El esquema o la estructura de carpetas es similar,  
    pero más granular, ya que almacenamos mediciones individuales con marcas de fecha y hora para facilitar  
    su gestión en la siguiente capa.  
    El proceso ETL de datos sin procesar a datos formateados probablemente no sea complejo, pero puede variar considerablemente si se  
    reciben datos de diversos sistemas y soluciones. Cada tipo o fuente puede tener un  
    esquema de codificación diferente para los datos de medición, con el fin de garantizar el menor uso de ancho de banda posible. Con  
    una buena codificación, se pueden almacenar múltiples mediciones en una cadena muy pequeña que se transmite a través de  
    una conexión serial o inalámbrica. Sin embargo, la decodificación de esas cadenas será específica para  
    cada tipo de paquete de datos.  
    Además, los datos se pueden reestructurar en esta capa, pasando de cadenas sin procesar a un  
    formato de datos columnar si es necesario. Algunos de los datos dentro de la capa de datos sin procesar pueden ya estar en un  
    formato útil, pero los datos verdaderamente sin procesar en su formato original se pueden transformar y consolidar en  
    formatos de archivo más útiles como CSV, Parquet, Apache ORC o Avro. Cada formato tiene ventajas y desventajas.

38 Anatomía de una arquitectura IoT

```
disadvantages based on the amount of data, and how you might use it within your analysis. We
can also strip away some of the metadata that may come with the message if it is not necessary
for subsequent analysis.
Access to data in this layer may also be restricted based on your data governance policies and
analytics needs. #e value of this layer is to quickly convert your data into a more readable and
structured format for easier consumption.
```

- **Capa de datos curados** : Finalmente, llegamos a la capa de datos curados. Aquí comenzamos a estructurar  
    los datos de forma útil para el análisis y el negocio. Los datos formateados se pueden reestructurar en esta  
    capa y combinar, agregar o transformar según sea necesario; por ejemplo, cuando  
    se requiere calcular valores adicionales a partir de mediciones sin procesar existentes. Un excelente ejemplo para  
    el sector agrícola sería calcular **la evapotranspiración** ( **ETO** ) a partir de los datos meteorológicos  
    recibidos en las últimas 24 horas. Se trata de un valor calculado de alta complejidad derivado  
    de datos sin procesar, lo cual resulta beneficioso para el análisis de datos.  
    La estructura de esta capa puede ser bastante compleja, ya que también puede combinar datos de  
    otras fuentes, como sistemas financieros o empresariales. Los datos de esta capa se pueden reformatear e  
    integrar en un almacén de datos o métodos analíticos. Cabe esperar que los datos se desnormalicen en esta  
    área a medida que se conozcan mejor las necesidades del negocio y se puedan trasladar a  
    sistemas de bases de datos más tradicionales, almacenes de datos, sistemas de análisis empresarial o modelos de aprendizaje automático.  
    El acceso a esta capa ofrece la mayor libertad dentro de la organización, pero aun así debe  
    restringirse según las necesidades. La mayor parte del análisis se realizará transfiriendo datos desde esta  
    capa a sistemas o bases de datos externas, lo que proporciona una capa adicional de abstracción al  
    propio lago de datos.

```
"ree-layer approach – more or less?
In this section, we outlined three main layers within the data lake architecture; however, this
is just one example of how you might create your data lake structure. Some people prefer to
name their lakes Bronze, Silver, and Gold. It is also perfectly OK to have more or fewer layers,
depending on any number of factors, such as the size and type of your data, or any legal
requirements you may need to consider. We say this again and again within this book, one
size does not !t all, and, as architects, our job is to research and understand the best-of-breed
approach and reference architecture and then apply them to our organizational goals.
```

```
Metadata management
It is probably the case that you will need to store some information about your data, such as the
source(s) and destination within your data lake, refresh intervals, type, format, life cycle, transformation
information, and security considerations. Additionally, you will need information about the sensors,
types, and locations. For example, you may have some data stored under a speci"c component ID;
however, there is no information in the data stream about where that component is located, how old
it is, or which factory it belongs to. A set of metadata can be used as a lookup when necessary to get
all this additional information about your system.
```

```
Architectural components for IoT 39
```

Una base de datos es el lugar más probable para almacenar esta información y se puede consultar fácilmente para encontrar  
los datos relevantes para sus necesidades. Existe un enfoque más reciente llamado Data Lakehouse,  
que combina la estabilidad y flexibilidad de un lago de datos con la facilidad de consulta de un almacén de datos.  
Este enfoque puede tener muchas ventajas y debería considerarse si está comenzando su  
iniciativa de IoT. Sin embargo, puede diseñar su conjunto de tablas a medida utilizando AWS Relational Data Service.  
Dependiendo del alcance de su iniciativa, puede ser útil crear una interfaz para su metasistema  
que facilite la implementación, configuración y administración de sus metadatos.

#### Análisis y aprendizaje automático

Subiendo un nivel en la arquitectura, llegamos a la parte más interesante. Gran parte del trabajo en  
las capas anteriores consiste en la instalación de tuberías y cableado, algo fundamental y que también puede resultar entretenido (para  
los aficionados como nosotros), y es necesario que quede lo más correcto posible, teniendo en cuenta lo que sabemos (o desconocemos)  
en esta fase inicial del proceso.

Sin embargo, una vez que comenzamos a recopilar datos de nuestros sistemas (y en algunos casos, puede tratarse de una  
cantidad ingente), queremos avanzar rápidamente al siguiente paso e intentar comprenderlos  
mejor, con la esperanza de utilizarlos para mejorar nuestras operaciones y producción, y demostrar rápidamente su valor.  
En el Capítulo 1, «Introducción a la evolución del Internet de las Cosas», hablamos extensamente sobre el aspecto empresarial del uso de datos y  
la importancia de asegurarnos de recopilar los datos correctos por el motivo adecuado. De lo contrario, podríamos vernos inmersos en  
un elevado esfuerzo de almacenamiento y procesamiento de datos con un beneficio empresarial mínimo.

```
Figure 2.7 – Analytics and machine learning
```

#Hay dos áreas principales de enfoque en esta capa, como se muestra en la Figura 2.7. #Se dividen porque  
pueden tener objetivos distintos.

40 Anatomía de una arquitectura IoT

**Aprendizaje automático**

El aprendizaje automático es un tema emocionante y relativamente nuevo que muchas organizaciones ven como uno de los
objetivos principales para adoptar una estrategia de Industria 4.0 o basada en datos. En un entorno industrial, hay un
par de objetivos que esperamos al implementar el aprendizaje automático:

- **Análisis de datos de sensores de la máquina** : El objetivo es presentar un flujo de datos y utilizar un  
    modelo de aprendizaje automático para establecer una línea base y buscar variaciones, con la esperanza de detectar posibles  
    problemas que deban examinarse antes de que se agraven. Idealmente, este análisis  
    podría incorporar múltiples flujos de datos (o numerosas mediciones) para determinar cómo  
    funcionan en conjunto los componentes del sistema y si existe algún problema relacionado  
    en el equipo.
- **Análisis de vídeo o imagen** : El análisis de imagen es similar, con la diferencia de que revisa una transmisión de vídeo o  
    imágenes estáticas y determina si existen anomalías en el producto que se muestra en la imagen.  
    Se detectan problemas como de color, ubicación o superficie, y se puede determinar si  
    existe un problema en la línea de producción que deba solucionarse.

```
#ere are other types of models of course, and we will touch upon them in Chapter 12, Advanced
Analytics and Machine Learning. For example, consider a demand water balance model for a large
utility that processes several factors, including weather, demand history, supply, costs, and more, to
predict demand at the consumer level for a future period, thus allowing the utility to optimize its water
sourcing strategy and minimize cost. #is type of analysis is much more advanced than what we can
describe here, but requires both sensor data from !ow meters and demand systems, along with many
external variables to augment the analysis effort.
In addition, image analysis is not something that we will cover in this book. It is a specialized topic
that is well covered in online sources and other available books. Data streams, however, are something
that we need to understand better, such as what is available and how we might approach achieving
our goals in this area. It is relatively straightforward to train a model so that it detects objects or
anomalies in an image and can provide a tremendous bene"t in evaluating output quality early in
manufacturing processes.
```

**Análisis de negocio**

Hay una diferencia entre el análisis de negocio, que está enfocado en el futuro, y la inteligencia de negocio,
que mira más explícitamente al pasado. Se podría argumentar que este análisis debería moverse a
una capa superior ya que es una actividad realizada por un usuario final y, más específicamente, un analista de negocio.
El objetivo del análisis es usar datos para generar insights sobre cómo están funcionando las cosas, cómo
funcionarán o dónde pueden ocurrir problemas.

**Esfuerzos tempranos para encontrar eficiencia**

Uno de los primeros proyectos de IoT para uno de los autores fue con un gran club de golf en el desierto del suroeste.
Este club en particular era de clase mundial con múltiples campos, varios de ellos reconocidos por la PGA.
El sistema de riego era bastante complejo y el agua se movía alrededor y entre los diferentes
campos hacia estanques y arroyos, desde donde podía usarse para el riego y mantener los
campos y el paisaje en óptimas condiciones. Una vez que la instrumentación estuvo en su lugar, que incluía
monitorear todo, desde tasas de flujo de agua, datos de bombas, niveles de lagos y datos meteorológicos, hasta la
humedad del suelo en los campos y greens, había un gran sistema para ver datos del sistema en tiempo real.
Nuestro objetivo final era encontrar eficiencia, reducir desperdicios y costos, y buscar anomalías
en el sistema a medida que ocurrían.

De todos modos, en cierto punto, durante esas etapas iniciales, exportamos datos a Excel y construimos
gráficos, tratando de entender las relaciones del sistema. Luego discutimos nuestro análisis con el
cliente para ver si esto era interesante para ellos – cosas como flujo de agua versus uso de energía
para determinar la eficiencia de la bomba o posible deterioro. El mayor desafío fue tratar de
estimar la dureza del green (esto determina qué tan rápido rodará la pelota) y cómo el clima, la
cantidad de riego de la noche anterior, y más lo afectarían. Esto fue seriamente algo difícil
de determinar ya que había tantas variables involucradas. Y esos algoritmos aún se están
ajustando hoy.

El aprendizaje automático a menudo comienza con análisis y aprender a entender los datos y la relación
para saber qué es normal, qué podría mejorarse y cómo se ven los datos antes, durante
y después de que ocurran anomalías.

Podríamos intercambiar o combinar iniciativas de análisis dentro de la capa de visualización e informes. Como  
mínimo, dejemos que el análisis y la visualización trabajen conjuntamente para proporcionar  
información mejor y más completa. El análisis proporciona al analista o a los usuarios de negocio las herramientas necesarias para comprender mejor  
lo que sucede a nivel de producción. La información se puede combinar con la de otras plantas y  
sistemas corporativos para determinar dónde se pueden realizar mejoras o cambios. ¿Cuántos widgets  
fabricamos y enviamos el mes pasado y cuál es nuestra predicción en función del funcionamiento de los sistemas?  
Esta es una pregunta bastante básica que se puede responder con relativa facilidad.

Pero más allá de eso, surgen algunas preguntas más esclarecedoras sobre los sistemas subyacentes  
que fabrican esos componentes. ¿Están disminuyendo su rendimiento o aumentando su temperatura? ¿Necesitamos solicitar  
un mantenimiento preventivo para que vuelvan a funcionar correctamente, o podemos prolongar su vida útil? La instrumentación y  
la evaluación comparativa de sus equipos le ayudarán a responder estas preguntas. Y proporcionar datos precisos y válidos  
con las herramientas adecuadas le permitirá formular las preguntas correctas.

**Análisis de borde**

Aunque el edge computing y el análisis residen oficialmente en una capa completamente diferente, merece la pena
repasarlos brevemente. Sus beneficios son bien conocidos:

- **Reacción en tiempo real**: Cuando las cosas suceden rápidamente, no podemos esperar a que se resuelvan los problemas de latencia que
    puedan surgir al enviar datos a la nube. En algunos procesos de fabricación, milisegundos
    cuentan. Si algo está mal o se pierde, podría significar miles o millones de dólares
    en reparaciones de equipos, o bienes manufacturados que necesitan ser descartados debido a problemas de calidad.

- **Ralentizaciones por exceso de ancho de banda**: Esto puede deberse a la alta velocidad o, específicamente, a la alta
    frecuencia de los datos de medición. Considera un sensor que mide la presión cientos de veces
    por segundo. Ahora, multiplica eso en una fábrica. Esto puede generar una gran cantidad de datos que se intentan enviar
    a la nube. Preprocesar o almacenar esos datos localmente tiene sentido según tus casos de uso
    para su revisión y análisis. Podría almacenarse y transferirse por otra ruta para evitar sobrecargar el ancho de banda
    de los datos de mayor prioridad.

Menciono estas ideas porque algunos análisis son esenciales y necesitan hacerse rápidamente y eficientemente,
mientras que algunos pueden hacerse a un ritmo más pausado. Consideraremos esto más cuando nos enfoquemos en
procesamiento y análisis edge en futuros capítulos con más detalle.

#### Visualización e informes

En muchos casos, los usuarios solo quieren ver datos, especialmente al principio del programa, y generalmente en formato de gráfico
con la capacidad de ver diferentes escalas de tiempo o comparar diferentes mediciones o áreas entre
sí. Esto podrían ser datos sin procesar formateados lo suficiente para que estén listos para graficar. La capa de visualización
y generación de informes se representa en la Figura 2.8.

Este concepto de ver datos sin filtrar de tus sistemas se usa durante las etapas iniciales para ayudarte
a comprender mejor el entorno. ¿Cómo se ve lo normal? Encuentro esta pregunta fascinante.
Los operadores a menudo saben qué es normal, pero no siempre los detalles específicos. Pueden oír, oler o sentir si
algo está mal, pero no pueden definirlo o medirlo con precisión. Una vez que se obtiene una nueva visión sobre un
entorno operativo, una vez que ese entorno o equipo está instrumentado de nuevas maneras,
saber qué es normal se vuelve mucho más fácil y específico. Una vez que se aprende esa visión, con el tiempo,
un operador o analista puede definir y detectar mejor las anomalías, y esto puede incorporarse a modelos
de aprendizaje automático:

Figura 2.8 – Visualización y generación de informes

Incluso con un análisis de datos básico, se puede lograr mucho. Tomemos como ejemplo una bomba simple.  
Se pueden responder preguntas básicas, como el consumo de energía frente al caudal. Al incluir los costos de energía, se puede determinar  
cuánto se ahorra al reducir o aumentar el caudal. Desde el  
punto de vista de la generación de informes y la inteligencia empresarial, existen dos opciones principales:

- **Informe** : Un informe ofrece una vista de los datos con herramientas adicionales que permiten al usuario explorarlos  
    en detalle o visualizarlos de diferentes maneras; por ejemplo, con mayor granularidad  
    , como en intervalos de tiempo de segundos o subsegundos. Los analistas pueden usar las herramientas de informes para  
    responder preguntas sobre el funcionamiento de las máquinas, detectar anomalías abstractas o determinar dónde  
    se pueden implementar mejoras en la planta.
- **Panel de control** : Un panel de control es más específico, ya que muestra el estado de los  
    sistemas en tiempo real. A menudo, se configura un panel de control en operaciones, donde  
    se pueden detectar posibles problemas para determinar qué ubicaciones están activas o tomar otras decisiones sobre  
    el equipo en tiempo real.

#is no es nuevo para quienes conocen las herramientas de BI y de generación de informes, pero ayuda a definir el objetivo para planificar  
el camino a seguir y compartir información y avances. #is permitirá a las partes interesadas y a quienes dependen  
de los datos comprender el proyecto y contribuir a su desarrollo de forma significativa.

**Aplicaciones personalizadas frente a aplicaciones preconfiguradas**

Existen numerosos productos **listos para usar** que incluyen funciones de visualización y generación de informes como parte de su solución. Puede resultar tentador comenzar con una solución ya existente, como la que forma parte de tu ERP, gestión de activos, arquitectura empresarial o quizás otro producto. Sin embargo, hay varios aspectos a considerar con este enfoque inicial.

Muchos de estos productos ofrecen excelentes capacidades de generación de informes y análisis, pero principalmente dentro de su propio
dominio de datos. Incorporar datos de otras fuentes puede resultar complejo. Por ejemplo, los datos en tiempo real pueden
provenir de sensores, sistemas de adquisición de datos o directamente del sistema de registro histórico. En algunos
casos, estos datos pueden combinarse con los datos de pedidos, costos y uso para comprender la posible relación costo-beneficio
ante posibles anomalías. Además, el historial y el esfuerzo de mantenimiento pueden integrarse
para ayudar a comprender cuándo y qué tipo de mantenimiento se realizó por última vez, o si está programado para un
futuro próximo.

Todo esto, en conjunto, puede dificultar cualquier solución predefinida que se esté considerando. Sin embargo,
también puede resultar prohibitivo en términos de costos desarrollar una solución de este tipo desde cero. Como arquitectos, estas son las opciones
que debemos analizar para determinar la mejor solución para nuestra organización, tanto hoy como en el futuro.

**¿Cuánto desarrollo personalizado se requiere?**

En proyectos anteriores, los autores han construido algunos productos de inteligencia empresarial o
análisis bastante complejos y personalizados desde cero. Esto fue impulsado por un par de objetivos clave:

- En primer lugar, el IoT era todavía bastante nuevo, y realizar análisis en múltiples flujos de datos de series temporales relacionadas
    era algo nuevo para la mayoría de las herramientas de informes de la época.
- En segundo lugar, el objetivo era proporcionar una interfaz fácil de usar que permitiera a los usuarios visualizar diferentes
    flujos de datos y diferentes zonas horarias en varias plantas o regiones. No esperábamos que nuestros
    usuarios fueran expertos ni que tuvieran que aprender a usar una herramienta de inteligencia empresarial compleja.
- En tercer lugar, estábamos creando productos comerciales que se ofrecerían a los clientes como
    producto o servicio. Con el desarrollo a medida, no teníamos que preocuparnos por los costos de las licencias ni por
    los problemas de integración.

Hoy en día, el mundo es un poco diferente. Muchos sistemas de control industrial y productos de terceros proporcionan
mucho de este tipo de capacidad de análisis. Además, puede haber diferentes tipos de usuarios dentro de tus
organizaciones, analistas que pueden aprender y trabajar con herramientas complejas para comprender mejor los patrones en
el entorno y usuarios empresariales u operativos que pueden estar más interesados en paneles y
gráficos que muestren qué sucedió la semana pasada y qué sucederá la próxima semana dado el plan actual.

## Uniendo todo

```
#at’s it so far – for the layers at least. #is reference approach should give you a feel for what you
need to consider as your starting point. It is far from the "nal architecture, but if you don’t have any
idea where to start, it hopefully provides something to think about.
We h a v e t r i e d t o c r a m a l o t o f i n f o r m a t i o n i n t o t h i s c h a p t e r t o h e l p y o u u n d e r s t a n d t h i s r e f e r e n c e
architecture and some of the reasons why it was put together in this manner. Everyone has to start
somewhere, and without knowing much yet, about how we are going to solve some of our digitization
efforts, this is a good starting point. We can now focus on implementing parts of this architecture and
use it to test out our solutions and standardize patterns.
Figure 2.9 outlines the complete strawman architecture. It is a lot to consider at once, but we have tried
to keep it high-level and consumable for most people. We are only scratching the surface:
```

```
Bringing it all together 45
```

Figura 2.9 – Arquitectura de paja propuesta

46 Anatomía de una arquitectura IoT

```
We will switch gears in the next section and talk a little about architecture and development best
practices. #is is an architecture book a%er all! But really, we want to talk about a few topics that will
help as you continue down your path. We all get busy, but at this stage in our project, it is too easy to
start making big mistakes that can cost you down the road.
```

## Definición de estándares

Como arquitectos, tenemos múltiples objetivos:

- Definir la arquitectura y la selección de productos es una función que busca servir al negocio y  
    satisfacer y mejorar los requisitos y objetivos que la organización y el negocio pretenden  
    alcanzar.
- Definir una arquitectura que sea funcional, robusta, escalable, segura y, a la vez, lo más rentable  
    posible.

Otra pieza del rompecabezas es establecer los estándares y convenciones para que los equipos de desarrollo e
implementación los sigan dentro de la organización. Es igualmente importante que la organización
tenga estos estándares que puedan aplicarse antes de que comience cualquier esfuerzo real.
Como arquitecto empresarial, es posible que no estés haciendo revisiones de código con el equipo; sin embargo, deberías
considerar seriamente establecer algunas pautas para que los arquitectos de aplicaciones y líderes de equipo las sigan, así
como asegurar que el proyecto tenga el alcance necesario para permitir tiempo para que se sigan prácticas más rigurosas de ingeniería de software.

```
"e role of standards
Several years ago (OK, many), one of the authors published a book called Application Architecture
for WebSphere, where a whole chapter was devoted to setting and following standards and
conventions within a project and team. At that time, the cloud was relatively new, so everyone
was building and deploying applications in-house or within private data centers. However, many,
if not most, of the guidelines that were described back then still hold today in some fashion,
requiring some modi"cation in the application to provide updates in technology.
#e main point here is that standards are really important, especially for large teams or long-
running projects. We all know the stories about code that shouldn’t be touched, and we also
know just as well that a little bit of foresight could have helped to avoid these issues. As an
architect, it is our job to reduce potential issues, ensure code quality, and help our project nicely
live into the future. Not inde"nitely, mind you (that is another story about over-architecting
because of some abstract potential use cases), but into the foreseeable future as many things
continue to live well beyond their natural time.
```

```
#is means ensuring that standards are followed, code and infrastructure are well reviewed and
documented, and the goal of the project meets existing requirements. Our job is to pass on to the next
development, or architect, a project that you can be proud of. To start, let’s de"ne some simple concepts:
```

```
De!ning standards 47
```

- Una **norma** es una regla estricta que describe cómo se debe hacer algo.
- Una **convención** es más bien una sugerencia. Es una guía sobre cómo hacer algo, pero no es  
    necesario seguirla al pie de la letra.

Los estándares son probablemente uno de los aspectos más importantes en la creación de aplicaciones y entornos,  
sin embargo, se suelen pasar por alto como una oportunidad para alcanzar los objetivos. Existen numerosas guías  
en internet, y elaborar un conjunto razonable de reglas no debería ser difícil para  
los arquitectos experimentados que comprenden las tecnologías elegidas.

En la industria del software, hemos aprendido mucho a lo largo de los años, y también que no siempre es  
posible seguir estándares estrictos y, al mismo tiempo, cumplir con los objetivos que la empresa o el proyecto han marcado.  
Los gerentes quieren resultados más rápidos, económicos y de mejor calidad, y las estrategias de marketing de muchos proveedores  
los han convencido de que esto es posible. Si se trabaja con metodologías ágiles (y, seamos sinceros, ¿quién no lo hace?), las cosas pueden  
cambiar rápidamente, y con ciclos de sprint cortos, las revisiones de código rigurosas no siempre son viables.

```
A comment about methodology
#e statement about agile is a little skewed since we all know there is a right way and an incorrect
way to adopt any practice or method. We wouldn’t want agile or methodology pundits to think
we don’t know the difference. We do, and we cry (and possibly something bad happens to
kittens) every time it gets twisted into some cruel form of punishment to get more done, faster,
from a development team. It’s wrong, but it’s o%en the reality of development projects today.
```

### Recomendaciones básicas para la revisión de proyectos

Como mínimo, hay algunas cosas bastante sencillas que puedes hacer para facilitar la supervivencia de proyectos largos.  
Aquí te menciono algunas para que empieces. Son cosas que podrías hacer una vez al trimestre o  
quizás dos veces al año, lo que ayudará a mantener el proyecto encaminado si no puedes o no quieres supervisar más de cerca  
el proceso de desarrollo:

1. De vez en cuando, revise su sistema de gestión de código fuente:

```
 Do the project and repository names make sense?
 Are the names consistent?
 Is there a brief one- or two-line description about that set of code explaining its use?
 Is the main description page current and does it do a good job describing the module and
its usage?
It is no fun when new team members come online and can’t make heads or tails out of the 300
repositories on your project (yes, we have been there).
```

48 Anatomía de una arquitectura IoT

2. Revisa la documentación de tu arquitectura:

```
 Are your overall diagram(s) accurate and up to date?
 Are there major !ow changes that need to be updated?
 Can you tell from the documentation how things are structured, and what major components
are in use in the system?
#ings happen fast in this space, and the architecture can change considerably over time. You
need an accurate set of diagrams to review with your team and share with others who are asking
about your project. Updating constantly is a big ask, but twice a year should be achievable,
depending on the amount of churn in your environment.
```

3. Reúnanse periódicamente con todo el equipo para analizar las inquietudes sobre la calidad del producto. Dediquen  
    un breve periodo de tiempo, quizás un día al mes o al trimestre, a una mesa redonda  
    o sesiones de trabajo para abordar problemas menores. Este equipo puede estar compuesto únicamente por miembros del equipo de desarrollo  
    , pero puede ampliarse para incluir  
    a miembros de arquitectura, gestión e infraestructura con el fin de compartir problemas o mejorar los procesos de trabajo en el futuro.

```
 Are there things that we can do better?
 What is out of alignment that we can "x today?
Make this non-combative and focus on what the team can do to improve. O%en this can be
done during a sprint review regularly, but to work, the feedback has to be incorporated into
the sprints ahead, which may affect velocity.
Additionally, you can use tooling to ensure that standards are followed, or conventions are used.
Static code analysis tools can be very helpful in ensuring some type of code quality. If you are not a
code monkey, please remember that 100% adherence to static analysis is not always possible, or if so,
then it comes at a price. So, use these tools judiciously to ensure your effort is cost-effective, as well
as the highest quality.
```

### Establecer expectativas

```
#ese guidelines are not magic, and management needs to be aware and involved in every aspect of
the constant battle between turning out a quality product and doing it quickly and cheaply. #is is not
always possible since, in large development organizations, there is a separation between development,
architecture, and product management. #is is by design so that one team cannot make decisions
at the expense of another. In companies where development is a by-product of doing business, this
is usually never the case. Management holds all the cards, both good and bad, depending on the
project’s outcome.
```

```
Summary 49
```

Es valioso construir una buena relación y confianza con la gerencia. A veces, hay  
que sopesar el grado de supervisión (y la calidad potencial) frente a la rapidez en la ejecución de un proyecto.  
Debemos encontrar ese equilibrio en nuestros proyectos para garantizar que se perciba cierta calidad  
sin dejar de cumplir con nuestros objetivos de entrega.

La información y las directrices presentadas hasta ahora no son secretos; son tareas bastante básicas.  
Las hemos descrito aquí para ayudarte a familiarizarte con el tema a medida que avanzas más rápido de lo que imaginas  
. Si incorporas algunas de estas prácticas a tu rutina, te serán de gran ayuda en el futuro.  
Esto no te exime de establecer y seguir estándares y convenciones más estrictos. Sin embargo, si  
el tiempo y los recursos son limitados y la presión empresarial es demasiado alta, puedes cubrir estas necesidades con  
un conjunto mínimo de actividades.

## Resumen

Esto era mucho que abarcar en un solo capítulo, y apenas estamos empezando. Si eres nuevo en IoT y arquitectura,  
intentamos que fuera significativo y comprensible. Si ya tienes experiencia en estos temas, esperamos que  
te haya servido como repaso o te haya permitido considerar alternativas a tu enfoque actual.

En definitiva, tenemos un buen punto de partida, y podemos desarrollarlo a medida que analicemos  
diversos ejemplos. Esta arquitectura evolucionará conforme integremos las piezas, ya sea  
incorporando nuevos servicios o conectándolos de diferentes maneras para lograr nuestros objetivos. Nuestro  
consejo es que, por ahora, disfruten del proceso mientras conectan los puntos y consideran alternativas según su  
entorno y sus necesidades.

En el próximo capítulo, comenzaremos a analizar la recopilación de datos de dispositivos IoT básicos de diversas maneras.  
Inicialmente, nos centraremos en la monitorización ambiental, lo que implica la instalación de sensores directamente en el  
entorno para medir algo más que máquinas, ya sea una fábrica, un oleoducto o gasoducto, o  
una granja o bosque en una ubicación remota. Recordemos que la industria puede estar en cualquier lugar y que muchas de las lecciones  
aprendidas en un sitio pueden aplicarse en muchas otras situaciones.

Esta es una herramienta sin conexión; tus datos permanecen localmente y no se envían a ningún servidor.

[Comentarios e informes de errores](https://github.com/jzillmann/pdf-to-markdown/issues)