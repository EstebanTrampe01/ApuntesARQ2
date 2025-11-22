
---

## Parte 1:

## Una introducción a

## IoT industrial y mudanzas

## Hacia la Industria 4.0

¿Necesita ayuda con los conceptos básicos del **Internet Industrial de las Cosas** ( **IIoT** ) y desea aprender más sobre  
su importancia? Los dos primeros capítulos le brindarán precisamente eso: una introducción a la evolución digital y cómo ayudar a  
los responsables de la toma de decisiones a comprender el valor empresarial. Esta sección explica  
los componentes fundamentales del IIoT y la arquitectura empresarial, relacionándolos con la nube de AWS. Esta parte del libro también  
le ayudará a dar sus primeros pasos con el IoT y los principios de la arquitectura de soluciones.

La segunda mitad de esta sección profundiza en los enfoques de tecnología inalámbrica para el IoT. Este  
enfoque nos permite aprender conceptos clave y crear un ejemplo integral de recopilación de datos de  
campo. La arquitectura es una evolución, y exploraremos muchos conceptos de IoT comenzando por aquí. Además,  
daremos los primeros pasos en la recopilación, el procesamiento, el almacenamiento y la visualización de sus datos de IoT.

¡Forma parte del libro y comprende los siguientes capítulos!

- Capítulo 1, Bienvenidos a la revolución del IoT
- Capítulo 2, Anatomía de una arquitectura IoT
- Capítulo 3, Monitoreo ambiental in situ
- Capítulo 4, Monitoreo ambiental en el mundo real

# 1

## Bienvenidos a la revolución del IoT

Este libro está diseñado para arquitectos e ingenieros industriales que buscan orientación para adentrarse en el  
ámbito del IoT o la Industria 4.0. Ofrece ideas, enfoques, objetivos y consejos para facilitar su avance  
y lograr un mayor éxito. Para quienes se inician en la arquitectura de TI o el IoT, nuestro objetivo  
es responder a muchas de sus preguntas iniciales o, al menos, guiarlos para que formulen las preguntas correctas. Queremos  
sentar las bases en estos primeros capítulos antes de profundizar en los detalles técnicos. Cualquier persona  
que se adentre en estos temas se beneficiará de estos capítulos iniciales, especialmente quienes no tengan conocimientos técnicos  
y deseen comprender el porqué y el cómo del IoT industrial. Por ello, tenga en cuenta que  
proporcionamos información histórica y arquitectónica, orientación y algunas buenas prácticas desde una  
perspectiva de TI y desarrollo de sistemas. Si el tema se torna demasiado técnico, está advertido.

En este capítulo, queremos sentar las bases para comprender la Industria 4.0 y ayudarle a entender  
hacia dónde se dirige y por qué es importante. Analizaremos por qué la actual Revolución Industrial  
y la Industria 4.0 son tan relevantes, conoceremos el estado actual de la tecnología y aprenderemos  
cómo puede desarrollar su visión y declaración de valores para impulsar tecnologías como el IoT en su  
organización.

Vamos a tratar los siguientes temas principales:

- Industria 4.0 y la digitalización de la industria
- Cómo el IoT puede apoyar la Industria 4.0 a gran escala
- Convergencia: TI, OT y gestión trabajando juntas
- Aprovechar una buena arquitectura para impulsar el progreso

En los próximos capítulos, profundizaremos en el funcionamiento del IoT industrial y aprenderemos a implementar  
y usar esta fascinante tecnología. Pero no se vayan. Necesitamos comprender  
mejor su historia y descubrir sus orígenes. Hemos elegido **Amazon Web Services** ( **AWS** ) como  
proveedor de servicios de hiperescala para nuestros ejemplos prácticos. AWS es un actor clave en este sector y  
cuenta con una excelente hoja de ruta de productos y una visión clara del IoT industrial. Hablaremos más sobre esto  
en los siguientes capítulos.

4 Bienvenidos a la revolución del IoT

### Requisitos técnicos

No hay requisitos técnicos específicos para este capítulo. Los lectores de todos los niveles deberían poder
comprenderlo claramente. Nuestro enfoque es sentar las bases para entender por qué el IoT industrial está posicionado como uno de los
siguientes grandes avances de la tecnología y cómo puede avanzar con su adopción en su industria.

### Industria 4.0 y la digitalización de la industria

```
Many so$ware architects are sometimes wary of the hype around new technology. Great ideas and
visions are pivots that lead us into the future and guide us in taking advantage of new technology in
both our business and personal lives. However, the road to the current state of technology is paved
with great ideas that never made it out of the concept phase, and overly aggressive marketing and sales
around new (good and bad) technologies have made everyone just a little more cautious.
```

```
Usually, at the early stages of some technologies, marketing and sales teams jump in and take over,
looking for any opportunity to push an idea or build a prototype with any potential customer, attempting
to work together with customers to build a vision of what the future could be. But then comes the
hard work of architecture, design, prototyping, rollout, testing, production, and support. Sometimes,
the state of the technology isn’t quite ready, and reality intervenes. If you have been burned enough
times, it gets harder to reach back in.
```

```
Fortunately for us, Industry 4.0 has made it well past the starting gate and into the reality of many
organizations. Even though it has been making progress for most of the last decade, there is still a fair
amount of work to be done before it can be considered mainstream technology in many organizations.
!e evolution and improvements in hardware, such as sensors and processors, so$ware protocols,
and integration tools, make retrieving real-time or near real-time data from almost any device or area
more accessible and safer. !e why of data capture and Industrial IoT is what we will be discussing in
este capítulo, mientras que el cómo se discutirá en el resto de este libro.

La Industria 4.0, o la cuarta Revolución Industrial, se concibe comúnmente como la automatización y
digitalización de la industria y los sistemas de fabricación. Las tecnologías de IoT y nube se han convertido en facilitadores críticos
de este esfuerzo y proporcionan la capacidad de integrar y automatizar maquinaria para volverse más
inteligente y adaptativa. Idealmente, esto incluye la adopción de inteligencia artificial y aprendizaje automático para
permitir que los sistemas se automonitoreen y diagnostiquen o predigan problemas que puedan ocurrir.

Esta descripción proporciona un poco de visión futurista, connotando una especie de enfoque de ascenso de las máquinas,
pero nos da un buen punto de partida sobre el cual basar nuestra discusión.

### Una lección de historia muy breve

```
History books and most university classes on this topic will agree that the world has undergone three
previous industrial revolutions. For us, how we got to where we are is maybe not as important as where
we are going, so we won’t belabor the history here, but we’ll provide some background to aid in your
organizational discussions and help us pinpoint the reason for and the focus of this book.
```

```
A very brief history lesson 5
```

#### La primera revolución industrial

La primera Revolución Industrial tuvo lugar a finales del siglo XVIII, cuando
comenzó la mecanización basada en la energía hidráulica o de vapor. Tradicionalmente se ha considerado que su inicio
se produjo en la década de 1780, con el diseño y la construcción del primer telar mecánico. Si bien era relativamente fácil de fabricar, replicar y transportar, esto permitió la
primera gran transición de la producción manual a la automatización mediante herramientas mecánicas.

**Progreso industrial temprano**

Por supuesto, existen precursores de la primera Revolución Industrial. Recientemente, en un viaje a los
Países Bajos, pude visitar algunos molinos de viento que avanzaron la industria en la región ya en la
década de 1600, proporcionando mejoras a industrias como la molienda, el tejido y la producción de madera.
Aunque la tecnología de los molinos de viento había estado en servicio moviendo agua en la región durante
siglos antes de esto, esta pequeña evolución en el aprovechamiento de la tecnología para otros tipos de trabajo
permitió a los Países Bajos avanzar hacia una nueva era, especialmente notable en la construcción naval. Desafortunadamente,
la tecnología no podía exportarse tan fácilmente ya que las máquinas impulsadas por el viento eran principalmente un
factor definitorio de la región. Sin embargo, el ingenio de los holandeses y el uso innovador
de engranajes, palancas y tornillos ayudaron a construir la base para futuros avances industriales, evolucionando
desde, por ejemplo, animales de granja para extraer agua o agricultura.

El hecho de que gran parte del trabajo se realizara con vapor también fue importante. La eficiencia de la máquina de vapor  
había mejorado enormemente para entonces, y ahora era más ligera y transportable. El carbón, y la capacidad  
de extraerlo en cantidades significativas, era esencial para alimentar estas máquinas de vapor. Adaptar estas  
mismas máquinas para que se movieran en una dirección o realizaran un movimiento a un grado diferente de movimiento  
permitió una mayor flexibilidad y complejidad en el uso industrial. El telar tuvo un papel destacado en esta fase  
porque la industria textil era intensiva en mano de obra, y se convirtió en una de las primeras industrias en adoptar y  
beneficiarse de las nuevas tecnologías.

#### La segunda revolución industrial

La segunda revolución industrial, a menudo denominada revolución tecnológica, comenzó a  
finales del siglo XIX y fue un motor fundamental para el mundo moderno en el que vivimos hoy. La expansión de casi  
todo lo que conocemos y utilizamos en la actualidad se inició durante este período. Comenzando con el desarrollo  
de los ferrocarriles y el telégrafo, la industria se expandió aún más, llevando consigo el gas, el agua, el alcantarillado y la electricidad, e  
impulsando la globalización hacia el final de la era colonial.

La expansión de la electricidad y las líneas de montaje/producción tuvo lugar durante este período. La historia atribuye a  
Henry Ford la invención de la línea de montaje en 1913, lo que allanó el camino para la producción en masa avanzada.  
A Ford también se le atribuyen avances en el motor de combustión, el acero y los nuevos combustibles y materiales  
que impulsaron este emocionante período de cambios y transformaron, una vez más, numerosas industrias.

6. Bienvenidos a la revolución del IoT

#### La tercera revolución industrial

Las líneas de tiempo están un poco entrelazadas porque los avances se realizaron frecuentemente y se prestaron hacia
cada fase distinta de la evolución tecnológica. Estas revoluciones pueden parecer casi continuas si
se rastrean de principio a fin con suficiente detalle y avances. Siempre ha habido avances significativos
que destacan el final de la última y el comienzo de la siguiente fase de avance.
La tercera Revolución Industrial comenzó a finales del siglo XX y se llama la Revolución Digital. Esto
se registra como un cambio de la tecnología analógica a la tecnología digital. La invención de internet y
las tecnologías informáticas más pequeñas nos permitieron entrar en la era de la información.

La invención del transistor en 1947 es un punto de partida crítico para esta era. Sin embargo, pasaron varias
décadas antes de que esta tecnología se adaptara lo suficiente como para ser útil a gran escala, con la capacidad de
diseñar y crear circuitos integrados que consistían en cientos de transistores. Finalmente, esto permitió
la creación del microprocesador de un solo chip en 1971 por Intel, permitiendo que las computadoras de escritorio
estuvieran fácilmente disponibles.

#### Avanzando y la cuarta revolución industrial

Esperemos que esta breve lección de historia sobre las tres revoluciones industriales anteriores te haya ayudado a
comprender dónde comenzamos y te haya asistido a visualizar cómo la manivela tecnológica gira continuamente.
Antes de que te des cuenta, el avance ha ocurrido. Además, cada revolución ha agregado
un valor tremendo, avanzando la civilización, aumentando la productividad y la seguridad, y moviendo al mundo entero
un paso más adelante.

La cuarta Revolución Industrial no debería tener objetivos menos elevados, con aún más potencial de impacto
en la civilización en su conjunto. Admito que esto suena un poco demasiado color de rosa, pero piensa en ello en términos de los efectos
en la humanidad y el mundo en el que vivimos. La eficiencia en sí misma significa menos desperdicio, menos uso de energía y
potencialmente menos contaminación e impacto en el medio ambiente. Eso, en sí mismo, debería hacer que un esfuerzo para
avanzar valga la pena, y que estas mejoras puedan ayudar a aumentar la productividad, la calidad y
los ingresos es la guinda del pastel.

Manten esto en mente mientras profundizas en este libro y determinas cómo aplicar algunas de las ideas a
tu industria. El objetivo inmediato puede ser ahorrar o ganar más dinero; sin embargo, por dentro, deberías
saber que con suerte estás haciendo tu pequeña parte para ayudar a salvar el mundo.

Lograr la visión de la Industria 4.0 requiere esfuerzo y tiempo y no se puede completar todo de una vez.
Esto es especialmente cierto para las operaciones industriales heredadas o de campo marrón que a veces han estado en
servicio durante décadas. Además, algunas industrias producen resultados muy variados basados en condiciones externas,
como la agricultura.

Antes en este capítulo, analizamos la definición estándar de Industria 4.0. Es una declaración visionaria,
y hay muchas empresas en el camino hacia el logro de esa visión. Sin embargo, muchas empresas están
recién comenzando o pensando en cómo comenzar. La Industria 4.0 se trata de datos y la gestión
de esos datos. Junto con los datos viene el análisis necesario, la información, el conocimiento y la capacidad innata de mejorar centrándonos en lo que realmente importa. La Industria 4.0 nos permite superar el
enfoque tradicional que ha caracterizado las últimas décadas. La historia nos enseña que, en cada etapa del cambio, prácticamente en todos los
sectores, muchos consideraron que el cambio era innecesario o demasiado rápido.

### Cómo el IoT puede apoyar la Industria 4.0 a gran escala

Los autores de este libro llevan más de 10 o 12 años trabajando en el ámbito del IoT,  
desde que era poco más que una palabra de moda. Al pensar en IoT, nos vienen a la mente  
dispositivos económicos y fáciles de usar, como electrodomésticos o relojes conectados. Esta nueva generación de hardware económico  
ha abierto los ojos a las posibilidades que ofrece la tecnología con un coste mínimo, pero la industria  
suele requerir un nivel de hardware diferente.

Podemos utilizar hardware y software de IoT para alcanzar los objetivos de la Industria 4.0, proporcionando un  
conjunto de tecnologías robustas y de alta resistencia que permiten la instrumentación y medición de  
los equipos y su entorno. Es importante recordar que la industria suele operar en  
condiciones ambientales extremas, y la opción más económica no siempre es la más adecuada. Debe considerarse un equilibrio entre coste y  
fiabilidad, ya que si es necesario reemplazar un componente con demasiada frecuencia, se puede  
perder valor en esfuerzo, tiempo o datos mientras se espera el cambio.

Hablemos de los aspectos clave a considerar al incorporar el IoT como parte de la solución. Digamos que vamos  
a colocar un sensor sencillo sobre o cerca de un dispositivo para medir la temperatura. No es necesario ser  
específicos por ahora, pero consideremos las condiciones a las que podríamos enfrentarnos, como las siguientes:

- **¿** Resisten sus sensores y equipos las condiciones y presiones ambientales?  
    Los equipos industriales en campo pueden estar expuestos a entornos adversos. ¿Requieren el sensor y  
    el transmisor correspondiente una clasificación de **protección** **IP** ( protección contra la entrada de agua y polvo ) o una clasificación **NEMA** ( **Asociación** **Nacional de Fabricantes Electrónicos** )? La clasificación IP protege la carcasa contra el acceso a los componentes internos y la entrada de líquidos, polvo o suciedad, lo cual es esencial para entornos exteriores exigentes. Una clasificación IP67 indica una carcasa sólida protegida contra la entrada de polvo y la inmersión temporal en agua hasta unos pocos centímetros. Las clasificaciones NEMA son similares a las IP, pero ofrecen protección adicional contra la corrosión y para ubicaciones peligrosas. En algunos entornos, como el de petróleo y gas, se requiere una carcasa NEMA Clase I o Clase II debido a la presencia de líquidos corrosivos, gases o vapores inflamables o polvo combustible. Estas condiciones y requisitos ambientales pueden añadir costes y tiempo adicionales a su esfuerzo por obtener, probar y posiblemente certificar sus componentes para su uso en el "campo".  
      
      
      
      
      
      
      
      
      
    
- **Fácil de implementar (y mantener)** : Simplifique al máximo el proceso para garantizar la rapidez y precisión  
    en la implementación de equipos. Esto asegura que la implementación y el registro de sus sensores y  
    equipos sean sencillos, prácticamente infalibles, para el técnico en el sitio. Al implementar un sensor  
    en un equipo o ubicación, debemos asegurarnos de que, una vez instalado y  
    en funcionamiento, podamos vincularlo a la ubicación correcta. De lo contrario, el esfuerzo es inútil y ninguno de  
    los datos posteriores será fiable. Existen varias opciones al respecto. Aplicaciones móviles con

8 Bienvenidos a la revolución del IoT

```
barcodes and even manual con"guration are "ne as long as the setup can be done correctly and
consistently. Additionally, the sensor should be easy to attach and place. OK, simple is not always
possible, but as much pre-con"guration as possible should be considered, leaving the engineer
to do as little as possible on-site to complete the setup and installation. Runbooks should be
well-de"ned and include any troubleshooting information that might be needed in the "eld.
!is is especially true if the deployment people are not experienced in the new technology.
```

- **Escalabilidad** : Debe considerarse la capacidad de desplegar rápidamente numerosos sensores en el campo. Esto puede  
    significar docenas, cientos o miles de sensores en múltiples ubicaciones o en todo el mundo.  
    Tanto el hardware como el software pueden ser un factor importante al pensar en la escalabilidad. Una solución fácil  
    de implementar y configurar puede desplegarse por miles; sin embargo, si el software o el almacenamiento  
    no están configurados para gestionar los datos, puede resultar en un esfuerzo desperdiciado. La tecnología en la nube ayudará  
    con la parte del software, aunque los requisitos de la aplicación para visualizar y analizar los datos deben  
    poder mantenerse al día a medida que el sistema crece. Esto significa que los sistemas de datos y el análisis deben diseñarse  
    para soportar los millones de lecturas potenciales que se pueden esperar de todos esos sensores.
- **Confiable** : Esto garantiza que los sensores y el sistema de monitoreo funcionen correctamente durante un largo período.  
    No se trata solo de que un sensor o nodo sea resistente, sino de confiabilidad. La confiabilidad es mucho  
    más importante porque ahora hablamos de la electrónica, no de la carcasa y  
    el empaque del nodo. ¿Tienen las conexiones de la electrónica selladas o pegadas? ¿Están los sensores  
    encapsulados o protegidos de alguna otra manera? Encapsular significa rellenar o rodear la electrónica con  
    algún tipo de gel o resina epoxi, protegiéndola así del polvo,  
    las vibraciones o los líquidos. Por supuesto, antes de llegar a este extremo,  
    se recomienda el control de calidad y el uso de componentes de alta calidad. Aplicar pegamento termofusible en las conexiones puede ser  
    la primera línea de defensa contra el aflojamiento de los cables. Si opta por encapsular los componentes, tenga en cuenta que es irreversible; por lo tanto, si una pieza falla, será necesario  
    reemplazar todo el conjunto, lo cual puede resultar costoso.  
    Realice un análisis de costo-beneficio del  
    mejor enfoque basado en su industria para tomar las decisiones de diseño correctas.
- **Seguridad** : Asegúrese de que los datos y los sistemas estén protegidos contra actores maliciosos o el robo de datos por parte de  
    terceros no autorizados. Abordaremos la seguridad a lo largo de este libro. El uso de tecnología IoT  
    puede generar vulnerabilidades de seguridad en todo el flujo de datos. Hay varios aspectos  
    a considerar. Garantice la seguridad de los datos durante su transmisión ascendente y proteja los puntos finales para  
    evitar la introducción de datos falsos en el sistema que puedan influir en los resultados o las acciones. Dado que hablamos  
    de los puntos finales en sensores o nodos, la seguridad física es el primer paso a considerar  
    . ¿Es necesario implementar alguna medida de seguridad física en el lugar de despliegue? De no ser así, ¿qué  
    tipo de monitoreo de manipulación se puede implementar para alertarle si algo parece anómalo? Una vez que  
    los datos llegan a la nube, se pueden aplicar los métodos tradicionales de seguridad informática, pero con el equipo en  
    el campo, su sistema puede enfrentarse a muchos tipos diferentes de amenazas.

```
If you are in the industry already, you will already know some of this; if you are an operator, you will
know your environment intimately. But it is still worth considering the environment and de"ning
some basic requirements alongside your goals. !is is an excellent point to think about the domain
you are considering and create a simple checklist with critical criteria that you can build on as we go
```

```
How IoT can support Industry 4.0 at scale 9
```

¡Adelante! Estas consideraciones están interrelacionadas y nos impulsan hacia un objetivo común.  
El uso de los criterios anteriores, junto con otros que se irán añadiendo, puede ayudarle a tomar decisiones  
y a comunicar a los demás las expectativas sobre la tecnología.

#### Tecnología de sensores

Utilizamos el término **tecnología de sensores** en un sentido amplio para incluir tanto el sensor o sensores empleados en  
la instrumentación de un entorno, como el **nodo sensor** que lee los datos del sensor y  
los transmite al receptor. Actualmente, los tratamos por separado porque no siempre van de la mano.  
La tecnología de sensores está en constante evolución, al igual que los protocolos de transmisión, como **las redes de** **área amplia de baja potencia  
**( **LPWAN** ) y el 5G. Los sensores que desee utilizar pueden tener características específicas  
y no siempre serán compatibles con un nodo sensor para la transmisión de datos mediante el  
protocolo definido. Permítanme compartir un ejemplo.

Hace varios años, en plena efervescencia del desarrollo del IoT (es broma, sigue siendo una efervescencia), uno de  
los autores participó en una propuesta para una gran ciudad de Nevada; seguramente ya se imaginan cuál.  
Nuestro socio era una startup de IoT; de hecho, era mucho más que una startup, con millones de dólares de  
financiación, pero era relativamente nueva en el sector. La empresa contaba con una  
tecnología de comunicación fascinante, que debería haber sido una fuerte competidora de la tecnología celular y la mayoría de  
las tecnologías LPWAN. Consumía poca energía y podía enviar datos a distancias muy largas, superando con creces a otras  
tecnologías como LoRa (de largo alcance).

Esta empresa invirtió mucho dinero y recursos en intentar vender y desarrollar su red, y  
dado que se requerían menos torres o puntos de acceso para cubrir un área, creían que podrían abarcar grandes zonas,  
como una ciudad, con relativa facilidad y a menor costo. Si bien esto probablemente era cierto, no se tuvo  
en cuenta que no había sensores ni nodos de sensores disponibles para la red.  
El proveedor de la red proporcionaba los chips, pero el costo, el tiempo y el esfuerzo para  
implementarlos eran excesivos para los proveedores de sensores. En esencia, el proveedor de sensores o el consultor tuvo que apostar por el éxito del sistema basándose en  
poco más que la confianza en la empresa de red. En retrospectiva, nos alegra no haber hecho esa apuesta.

Lamentablemente, esta estrategia resultó fallida, ya que la inversión fue demasiado significativa y  
compleja en comparación con otras opciones más disponibles en ese momento, que utilizaban protocolos como LoRa, Sigfox y  
LTE. Me sigue decepcionando que la empresa no tuviera la visión para detectar esta deficiencia en su estrategia, y  
que ahora se haya convertido en una empresa rezagada en el sector del IoT.

La conclusión clave aquí es tener en cuenta lo siguiente:

- ¿Puede su nodo sensor o unidad de transmisión comunicarse con la nube utilizando el  
    protocolo elegido, o el conjunto de protocolos si necesita redundancia?
- ¿Puede su nodo sensor comunicarse con su sensor o conjunto de sensores para leer las  
    mediciones y transmitir los datos?

Aquí puede haber discrepancias, ya que los propios sensores pueden usar distintos protocolos.  
Por ejemplo, SDI-12 es un protocolo de comunicaciones serie estándar utilizado en agricultura y meteorología.

#### Tecnología de sensores

Utilizamos el término **tecnología de sensores** en un sentido amplio para incluir tanto el sensor o sensores empleados en
la instrumentación de un entorno, como el **nodo sensor** que lee los datos del sensor y
los transmite al receptor. Actualmente, los tratamos por separado porque no siempre van de la mano.
La tecnología de sensores está en constante evolución, al igual que los protocolos de transmisión, como **las redes de** **área amplia de baja potencia
**( **LPWAN** ) y el 5G. Los sensores que desee utilizar pueden tener características específicas
y no siempre serán compatibles con un nodo sensor para la transmisión de datos mediante el
protocolo definido. Permítanme compartir un ejemplo.

Hace varios años, en plena efervescencia del desarrollo del IoT (es broma, sigue siendo una efervescencia), uno de
los autores participó en una propuesta para una gran ciudad de Nevada; seguramente ya se imaginan cuál.
Nuestro socio era una startup de IoT; de hecho, era mucho más que una startup, con millones de dólares de
financiación, pero era relativamente nueva en el sector. La empresa contaba con una
tecnología de comunicación fascinante, que debería haber sido una fuerte competidora de la tecnología celular y la mayoría de
las tecnologías LPWAN. Consumía poca energía y podía enviar datos a distancias muy largas, superando con creces a otras
tecnologías como LoRa (de largo alcance).

Esta empresa invirtió mucho dinero y recursos en intentar vender y desarrollar su red, y
dado que se requerían menos torres o puntos de acceso para cubrir un área, creían que podrían abarcar grandes zonas,
como una ciudad, con relativa facilidad y a menor costo. Si bien esto probablemente era cierto, no se tuvo
en cuenta que no había sensores ni nodos de sensores disponibles para la red.
El proveedor de la red proporcionaba los chips, pero el costo, el tiempo y el esfuerzo para
implementarlos eran excesivos para los proveedores de sensores. En esencia, el proveedor de sensores o el consultor tuvo que apostar por el éxito del sistema basándose en
poco más que la confianza en la empresa de red. En retrospectiva, nos alegra no haber hecho esa apuesta.

Lamentablemente, esta estrategia resultó fallida, ya que la inversión fue demasiado significativa y
compleja en comparación con otras opciones más disponibles en ese momento, que utilizaban protocolos como LoRa, Sigfox y
LTE. Me sigue decepcionando que la empresa no tuviera la visión para detectar esta deficiencia en su estrategia, y
que ahora se haya convertido en una empresa rezagada en el sector del IoT.

La conclusión clave aquí es tener en cuenta lo siguiente:

- ¿Puede su nodo sensor o unidad de transmisión comunicarse con la nube utilizando el
    protocolo elegido, o el conjunto de protocolos si necesita redundancia?
- ¿Puede su nodo sensor comunicarse con su sensor o conjunto de sensores para leer las
    mediciones y transmitir los datos?

Aquí puede haber discrepancias, ya que los propios sensores pueden usar distintos protocolos.
Por ejemplo, SDI-12 es un protocolo de comunicaciones serie estándar utilizado en agricultura y meteorología.

sensores y puede ser desafiante de leer si el nodo sensor no está diseñado para ello. El protocolo fue
definido a finales de los años 80 y transmitía caracteres ASCII a través de una sola conexión de datos. Hay
muchos ejemplos de protocolos serie en uso para sistemas industriales que pueden tener décadas de antigüedad pero siguen siendo
el estándar.

Otro ejemplo es si necesitas sensores calibrados, como sensores de temperatura, que deben seguir
estándares NIST para asegurar que los resultados se adhieran a los estándares. Si los sensores de temperatura calibrados que usan
tu protocolo de comunicaciones definido no están disponibles comercialmente, entonces tienes opciones limitadas.

Cada día parece que el mundo de los sensores se vuelve un poco más brillante a medida que una amplia gama de sensores, dispositivos de borde,
y unidades transmisoras o nodos se vuelven más fácilmente disponibles. Muchos de los protocolos más populares
están disponibles, con nuevos llegando lentamente a medida que la nueva tecnología de red es mejor adoptada por la
comunidad y se vuelve más fácilmente disponible. Sin embargo, todavía hay brechas de soluciones de sensores para
muchas situaciones.

Una de nuestras opciones favoritas para este problema es de una empresa llamada Libelium de Zaragoza,
España. Libelium ofrece una mezcla robusta de enfoques de mezclar y combinar para sensores y opciones de comunicación
de todo tipo diferente. Por ejemplo, puedes elegir sensores para medir la calidad del aire, la calidad del agua,
seguridad y agricultura o para integración en protocolos industriales como Modbus. Puedes elegir un
protocolo de comunicación para conectar los sensores y enviar datos de medición a una aplicación existente
o servicio web. Los protocolos incluyen el uso de cualquier cosa desde LoRa hasta Wi-Fi hasta 4G. Este enfoque flexible
hace que sea fácil cuando intentas adherirte a un protocolo de comunicación estándar pero no puedes encontrar un
sensor apropiado que funcione con tu estándar elegido.

El costo ciertamente puede ser un factor, especialmente a escala, y aunque los precios parecen estar continuamente bajando,
aquí es donde el mito del IoT, nuevamente, parece interponerse en el camino de la Industria 4.0. Obtienes lo que
pagas, y esto puede ser crucial en condiciones ambientales duras y áreas donde necesitas
proporcionar un enfoque estándar.

#### TI frente a OT

```
!ere is still a lot of confusion around information technology ( IT ), operational technology ( OT ),
and this idea of convergence. But essentially, it is a simple concept to understand.
IT is something we are all familiar with in our daily lives. We run applications on our phones or laptops.
Many of these applications run on servers or in the cloud and process data-producing orders, sales, and
directives or provide some type of analysis. !is is the IT world that we know today. It’s a reasonably
open world, and access can be gained from anywhere (provided security concerns are followed).
```

```
OT, especially legacy systems, can be considered a more closed environment. OT ends within the walls
of the factory. When you think of OT, think of supervisory control and data acquisition ( SCADA ),
which is also run by servers but interacts with devices within a de"ned area of control. At a large
scale, consider a power plant or water treatment plant. !e pump shuts off when the water in a tank
gets too high. Too low, and it starts back up again. Monitors and alerts allow operators to visualize
and help manage what is taking place with appropriate alarms and controls.
```

```
How IoT can support Industry 4.0 at scale 11
```

#### Industria 4.0 y alineación organizacional

La figura 1.1 ilustra cómo las diferentes áreas de la empresa se integran para formar parte de un panorama general. Para  
que funcionen, existe una fuerte interdependencia entre TI, operaciones, negocios y gestión; todos  
los interesados ​​deben colaborar para obtener los beneficios.

```
Figure 1.1 – Industry 4.0 organizational alignment
```

¿Y qué tiene de especial? Lo más importante es que el objetivo principal de TI es proporcionar a la empresa y a la gerencia  
la información y la capacidad necesarias para respaldar las decisiones y operaciones de la compañía. ¿Cuántos  
widgets se produjeron? ¿O cuántos barriles se procesaron? ¿Cuántos se vendieron y a qué precio?  
El éxito o el fracaso de la empresa depende de que esta información y estos datos estén disponibles de forma más rápida y precisa para  
obtener una ventaja competitiva. A menudo, lo que falta es una visión en tiempo real de la producción de widgets  
o del procesamiento de barriles. Las fábricas de nueva construcción o modernizadas pueden proporcionar información en tiempo real, pero en  
los sistemas heredados, incluso los relativamente nuevos, esa información está oculta. Y en la producción, modificar  
(ingeniería inversa) dispositivos y máquinas anula la garantía y, si no se hace correctamente, puede provocar  
complicaciones. Con la aparición del IoT, podemos trasladar algunos de esos datos del mundo cerrado de la tecnología operativa (TO)  
al mundo de TI, a menudo más integrado, donde se pueden utilizar de forma más eficaz.

El objetivo de este libro es obtener los datos ocultos, almacenarlos y procesarlos, y luego utilizar esta  
información de manera efectiva.

12 Bienvenidos a la revolución del IoT

```
!e business is not the only one to bene"t from introducing new data. Operational teams will gain
insight into the equipment and production that they didn’t have before. Uptime and maintenance can
be improved, cost reduced, and throughput increased as a new understanding, and a new normal of
the environment begins to emerge. !e full bene"t of digitalization should become clear in the rest
of this chapter and throughout this book as we share examples of collecting data and then using that
data to realize value across the organizational spectrum.
```

#### Puedes llegar allí desde aquí

```
Industry 4.0 is driven by IoT, but it is just one part of the picture. A big part, granted, as it allows
visibility into equipment and operations as never before. A longer roadmap is required to achieve the
vision of digitizing your industry and the transformative changes that can take place.
```

```
Important note
We are not a fan of big, complicated, eye-chart-type visuals, so throughout this book, we will
keep the visuals simple and coherent to allow you, the reader, to immediately understand the
concept rather than asking you to try and understand something overly complex.
```

```
Figure 1.2 illustrates a basic roadmap toward digitizing your industry or moving toward Industry 4.0.
We have broken this down into four primary areas of consideration for improvement. Within each of
these areas, there is a vast number of considerations both on the technical and business side to consider.
For many, the status quo or current state of their process is operate. Consider this business as usual, and
maybe decades-old processes that, for the most part, just work. !ere may be some instrumentation,
perhaps even a lot, but no cohesion or integration across machines, systems, or plants. Everyone knows
we can do better, but how do we move forward? Figure 1.2 illustrates a set of steps for continuous
improvement in your equipment and environment. Instrumentation and acting on it improves both
the business and technical responses of the organization.
```

```
Figure 1.2 – Industry 4.0 roadmap
```

```
How IoT can support Industry 4.0 at scale 13
```

Analicemos cada paso del proceso descrito. Hemos clasificado cada área según los  
cambios técnicos, ya que ese es el enfoque de este libro. Sin embargo, esto puede adaptarse a sus  
necesidades principales.

##### Instrumento y conexión

Para ir más allá del estado operativo general, se requiere una visibilidad profunda de sus sistemas y entorno.  
Considere esta etapa como la fase de instrumentación, cuyo objetivo es comenzar a recopilar datos de sus sistemas y  
entorno. La otra cara de la moneda es saber qué se debe instrumentar y por qué.  
Este esfuerzo de instrumentación y recopilación de mediciones es donde las áreas de negocio y operaciones pueden  
colaborar para asegurar que los datos recopilados sean necesarios y comprender cómo se utilizarán para  
impulsar los procesos y el negocio.

Por lo general, no es la mejor estrategia implementarlo todo de golpe. Si bien puede parecer que más  
es mejor y que no se pierde nada con hacerlo, invertir tiempo y dinero en equipos,  
personal, ancho de banda y almacenamiento para datos que nunca se utilizan termina siendo una mala inversión.  
Una vez implementado, puede requerir mantenimiento continuo para datos que no aportan valor.

Otra pregunta clave es cuántos datos se necesitan. Esto depende de la velocidad de las mediciones  
y la recopilación de datos. Algunos sistemas pueden generar cientos de mediciones por segundo. ¿Cómo  
y dónde se debe almacenar y analizar esta información? ¿Es necesario que toda se almacene en la nube? ¿Podemos  
procesarla en el borde y proporcionar resultados agregados? ¿Cuáles son las ventajas y desventajas de cada  
enfoque para gestionar estos datos? Las áreas de negocio y operaciones deben participar activamente en estas  
conversaciones para definir el nivel de detalle necesario y cómo se utilizará. Esto, a su vez, puede  
impulsar las decisiones de TI para la gestión y el procesamiento de datos.

##### Línea base y análisis

Definir el entorno operativo normal de su sistema puede ser una experiencia reveladora. A menudo  
(de hecho, con frecuencia) desconocemos qué es lo normal para nuestros equipos hasta que  
lo medimos y lo visualizamos gráficamente. Los sistemas SCADA suelen ofrecer información sobre presión,  
temperatura y características de flujo, pero no todas las operaciones industriales se basan en SCADA, o bien,  
esta información permanece oculta para todos, excepto para los operadores de equipos en planta. La información que se obtiene aquí puede  
ser enorme. Medir unos pocos valores puede proporcionar información más detallada sobre el  
estado de funcionamiento de un equipo o de un sistema completo y, como veremos más adelante, impulsar la eficiencia  
y detectar posibles problemas de mantenimiento. Comprender el rendimiento y las condiciones del sistema  
a una tasa de producción conocida puede ser muy útil, así como plantearse preguntas como: ¿qué sucede cuando  
aumenta la tasa de producción y cómo afecta esto al estado de la máquina?

Definir una línea base puede llevar mucho tiempo; no se hace en un día ni en una semana. Prepárese para al menos varios  
ciclos de producción, que podrían ser actividades estacionales que duren meses o años. Idealmente,  
la mayoría de los ciclos no son tan largos, pero si su sector se ve afectado por el clima o  
las condiciones ambientales, existe esa posibilidad. Puede obtener información valiosa de forma continua familiarizándose  
con su línea base a lo largo del proceso, pero las fluctuaciones e influencias inesperadas solo aparecen  
con el tiempo.

14 Bienvenidos a la revolución del IoT

##### Predicción y alerta

```
From a technical side, we have many opportunities. Now that systems are being more closely monitored,
you should expect to see variations in the data as problems occur, and equipment shuts down. Maybe
there were some unexpected vibrations or a temperature rise before it occurred. Can we monitor
for a particular set of variances? Do the vibrations occur when a part is ready for replacement or
maintenance? !is is the beginning of condition-based maintenance, where new data or real-time
monitoring of the environment can alert the operator to a possible set of conditions that may fail.
To accomplish this, we need to start to build predictive models. Tooling today can make it a relatively
straightforward process to create a predictive model; however, much of the work in the baseline phase
will help you determine which data to prepare for modeling. Generally, we are looking at data to help
predict downtime or failures of equipment or systems; however, does the data do this? We will dive into
some details about predictive modeling and how to use this in your architecture in the coming chapters.
We can o$en start our journey by using simple thresholds or comparisons on speci"c values or sets.
!is is especially true when you know what speci"c events or conditions you are looking for but are
not quite sure how predictive models will advance your cause. Does the temperature rise above a
speci"c degree? Does the energy usage on a pump get higher while the pressure gets lower? !ese are
simple examples, granted, but powerful tools in helping to determine when something might need
to be checked. At this point, we are still triggering more manual alerts, effectively telling someone
to check something. !is could be as simple as an email or SMS, or a more advanced trouble ticket
being opened automatically on your enterprise asset management system.
```

```
But really, we can now take this further into the business side of things and better understand production
cycles and issues and capacity constraints, not only of "nished products but subprocesses that may
cause bottlenecks.
```

##### Automatización y mejora

```
Industry 2.0 and 3.0 brought a lot of automation into manufacturing and processing. Our focus is more
on the automation of the overall business and what is produced. !e ability to monitor and eventually
steer your production closer to real-time allows the business to be more agile and respond more easily
to customer demands. !is is a topic well beyond the scope of this book, and would possibly include
connecting customer demand, supply, and ful"llment, as well as the digitalized production or factory
that is our focus here.
However, with a deeper analysis of your historical data over time, a more detailed analysis can occur
of where and when improvements can be made.
```

#### La visibilidad lo es todo

```
We probably can’t say this enough. Possibly, this is the gist of the entire book, along with some focus on
what to do a$er you have better visibility. It was mentioned before that understanding your baseline,
or the normal operating conditions of your environment can provide clear insight into what is truly
```

```
How IoT can support Industry 4.0 at scale 15
```

Esto ocurre en condiciones normales y cuando se produce algún tipo de anomalía. Esto solo es posible con una instrumentación precisa.  
Esto es cierto en casi cualquier industria o ciencia. La mayoría de los expertos explicarán que la instrumentación del  
entorno permite obtener nuevos conocimientos con una precisión antes inalcanzable.  
Los desarrolladores de software que han utilizado una inspección más profunda, como la instrumentación o inyección de bytecode, pueden  
explicar fácilmente la ventaja de una mayor visibilidad de los aspectos de un sistema en funcionamiento. Lo mismo se  
aplica a los sistemas físicos y a la capacidad de visualizar y analizar las características físicas de un  
equipo o un entorno.

Otro aspecto a considerar son las operaciones globales o ampliamente distribuidas. Los equipos o sistemas modernos  
pueden contar con toda la instrumentación necesaria para el funcionamiento seguro y eficiente del proceso.  
Sin embargo, ¿qué sucede con los sistemas distribuidos geográficamente en vastas áreas? Combinar e  
incluso comparar información de sistemas a nivel global puede brindar nuevas oportunidades para la toma de decisiones.

A lo largo de este recorrido debería existir un bucle de retroalimentación que permita realizar ajustes y actualizaciones en toda la  
cadena de monitorización.

#### Las empresas impulsan la innovación

Una búsqueda rápida en internet te proporcionará abundante información sobre IoT, listas específicas de ideas, ejemplos  
y casos de uso para su implementación en tu sector, así como el valor que aporta. A veces, existen  
casos de uso interesantes, pero con frecuencia están impulsados ​​por el marketing y las ventas para promocionar su solución. Si no  
tienes un buen conocimiento del sector, esto puede resultar engañoso. Anteriormente, mencionamos  
que el hecho de poder instrumentar algo no siempre significa que debas hacerlo.  
Debes tener en cuenta el tiempo y el coste. Considera el coste de añadir sensores para recopilar información,  
así como los costes de recopilación y mantenimiento de datos para seguir haciéndolo.

Los departamentos de TI, operaciones y negocios deben colaborar para comprender sus  
objetivos. Es fundamental contar con expertos en la materia que expliquen cómo lograrlos e  
interpreten los datos clave para alcanzarlos. El departamento de operaciones, por su parte, conoce mejor que nadie el  
desarrollo, la fabricación y la producción de materiales o bienes. Los responsables de negocios saben cómo fijar precios, vender  
y distribuir esos bienes a los clientes finales. Si bien existen matices en los negocios y las operaciones que algunos  
departamentos pueden no comprender a fondo o con los que otros no estén de acuerdo, la colaboración para lograr una mayor visibilidad  
y control puede ser una poderosa herramienta para competir en el mercado global.

La verdad es que las empresas y la gerencia tal vez no sepan qué instrumentación necesitan a nivel detallado.  
Sin embargo, sí saben qué información necesitan para tomar decisiones, como una mayor **eficacia** **general de los equipos  
**( **OEE** ), informes de tiempos de inactividad o pronósticos más detallados para las líneas de servicio a lo largo del  
tiempo. La OEE es un proceso para medir la productividad de la fabricación mediante el análisis de la disponibilidad  
y el rendimiento de los equipos, así como la calidad de la producción. De esta manera, las operaciones pueden tomar  
decisiones informadas sobre cómo obtener y proporcionar dicha información. Se trata de un proceso complejo que  
aquí se simplifica considerablemente, pero esperamos que sirva de guía para comprender que ninguna área de la empresa  
debe trabajar de forma aislada en este ámbito.

16 Bienvenidos a la revolución del IoT

Hasta ahora, hemos proporcionado una visión general de la Industria 4.0, la digitalización de la industria
y el IoT Industrial. Hay múltiples enfoques para lograr una mejora sistemática en tu
producción y gestión de equipos y procesos, y la hoja de ruta es un enfoque. Avanzando,
queremos profundizar en algunos de los aspectos técnicos de iniciar tu viaje y adoptar
una mentalidad y enfoque de digitalización. ¿Cuáles son los pasos y objetivos para avanzar y obtener
valor incremental en el camino? Además, ¿cuáles son los escollos en la adopción y cómo comprender qué tan
difícil será? Exploraremos más la idea de instrumentación, análisis y convergencia
para proporcionar valor a todas las partes interesadas.

### La convergencia: TI, OT y gestión

### juntos

```
Rarely does an opportunity come around in the industry for all aspects of the organization to come
together for everyone’s bene"t. Industry 4.0 allows that to happen. !e digitalization of industry can
bene"t all aspects, allowing the business to make better decisions around schedule, price, and volume
and providing operations with better tools to make decisions about maintenance, downtime, and
upgrades of equipment within a plant or factory.
```

```
Evolving toward IoT and Industry 4.0 allows for many things to occur. Maintenance cycles can be
improved, which positively affects planning and production. !e roadmap toward the continuous
improvement in your maintenance approach outlined in Figure 1.3 provides an idea of how your
outlook and planning can be improved over time.
```

```
Figure 1.3 – Driving toward common operational goals
```

```
!is is not an overnight process to achieve results with instrumentation and monitoring improvements, so
we wanted to talk about the progression and the maturity curve that might be adopted moving forward.
```

#### Mantenimiento reactivo y preventivo

Muchas empresas se encuentran en las primeras dos categorías de mantenimiento reactivo o preventivo.

**El mantenimiento reactivo** consiste básicamente en mantener nuestros equipos en funcionamiento hasta que se averían. Cuando un
equipo o una línea de producción falla, o cuando detectamos algún problema con la máquina, la reparamos
. Por ejemplo, reemplazamos la correa cuando se rompe. Esto es útil en algunos casos donde la reparación es sencilla
y relativamente económica, pero si necesitamos pedir piezas o el reemplazo es costoso, podría
ocasionar tiempos de inactividad inesperados y una baja productividad si la avería se produce en medio de un
ciclo de producción importante.

**El mantenimiento preventivo** es un poco mejor. A menudo se basa en el calendario o quizás en el uso
(número de horas), similar a cambiar el aceite de un coche cada pocos miles de kilómetros. Puede gestionarse
mediante una herramienta de gestión de activos empresariales implementada para administrar el inventario y realizar el seguimiento
de los activos a partir de las incidencias o siguiendo las directrices del fabricante para la programación
del mantenimiento. Así, en nuestro ejemplo anterior, la correa se reemplaza cada pocos miles de
horas según la recomendación del fabricante.

La ventaja del mantenimiento preventivo radica en que permite programar mejor los tiempos de inactividad y
reducir los imprevistos. Si bien puede ser el mejor resultado posible con una instrumentación exhaustiva,
podría no ser suficiente. Un riesgo es el exceso o la falta de mantenimiento de los activos
, lo que puede incrementar los costos de mantenimiento o reemplazo.

Aunque avancemos en la optimización, no creo que lleguemos a reemplazar por completo este
tipo de mantenimiento. Los accidentes ocurren y el mantenimiento correctivo es necesario. Y sí, esa correa debe
reemplazarse según el programa recomendado. La maquinaria de producción casi siempre requiere atención constante
. Pero la ventaja a largo plazo es que no tienes que dedicarle la misma atención que si estuvieras en
el ejército, donde, si no estás entrenando o durmiendo, estás realizando mantenimiento preventivo
a tus vehículos, armas, etc., lo necesites o no. Claro que, en este caso, el
objetivo final es mantenerte con vida, así que, en ese contexto, no es algo malo.

#### Mantenimiento basado en la condición

A medida que comenzamos a inicializar los datos y a recopilar más información de los activos individuales, podemos pasar  
al mantenimiento predictivo. Podemos analizar con mayor detalle las condiciones en tiempo real de cada activo.  
Mediciones como la producción actual, combinadas con las condiciones solares o comparadas con otros  
módulos solares, nos ayudan a comprender si un componente tiene un rendimiento inferior al esperado y si requiere una  
revisión más exhaustiva.

Con **el mantenimiento basado en la condición** , adquirimos el hábito de no realizar el mantenimiento ni demasiado pronto  
ni demasiado tarde, sino de acuerdo con los datos reales del equipo y su rendimiento.

#### mantenimiento predictivo

**El mantenimiento predictivo** o **prescriptivo** va un paso más allá al incorporar **modelos** **de aprendizaje automático
**para eliminar el factor humano del proceso de monitorización y proporcionar información
basada en lo aprendido sobre las condiciones óptimas de funcionamiento. Algunos argumentan que se trata de
dos cosas distintas.

El mantenimiento predictivo ayuda a prever problemas potenciales o resultados con tu entorno.
El mantenimiento prescriptivo ayuda a proporcionar recomendaciones basadas en esos resultados. Ninguno de
estos es nuevo para nosotros. Considera la aplicación de navegación en tu teléfono, que te informa con anticipación sobre
un retraso en tu ruta. Muchas de estas aplicaciones prescribirán rutas alternativas y determinarán
el ahorro de tiempo o el retraso.

Eventualmente, algunas compañías pueden inclinarse hacia el mantenimiento basado en riesgos, que te ayuda a considerar el
riesgo de que esta pieza falle. ¿Cómo se verá afectada la producción? ¿O qué tiempo de inactividad puede ocurrir si falla? Esencialmente, ¿cuál es mi costo si continúo funcionando y ocurre una falla?

#### Acérquese con precaución

```
We h a v e all seen or heard of the don’t-touch-it mentality from production teams who just need to keep
their system running. When systems are old, decades old, there can be a lot of lost knowledge about
how those systems work. Parts may be hard to replace, and sometimes, things work that shouldn’t.
!ese are some of the challenges that operations teams face, and it can be hard for anyone outside
those teams who need to get a better look at what is happening inside.
```

```
!ese types of environments and equipment need to be approached with an abundance of caution.
Trust is a big factor, and sometimes IT needs to earn trust and not come in like a knight on a white
horse, suggesting it will "x all the problems of the day. Everyone in the organization needs and wants
progress, from the boardroom all the way to the equipment operator on the shop &oor. However, moving
too fast in some challenging environments is the easiest way to lose trust within the organization.
We h a v e found from experience in many different industries that most operators love to share
information about how they do their job, how they treat their equipment, and, mostly, how things
could be made better. Having worked in consulting for many years, it is incredible what you can learn
when you talk to subject matter experts in the "eld, learning everything from farming to fracking,
with experts always being generous with their time when approached respectfully. Here are a few
simple steps as an approach to this. Some of these tactics seem almost silly to say out loud, but they’re
essential to keep in mind:
```

- **Escuchar y aprender** : Comprender qué saben todas las partes interesadas sobre un sistema y cómo funciona.  
    ¿Cuáles son sus preocupaciones, grandes y pequeñas, y qué sugerencias pueden aportar para mejorarlo  
    en el futuro?
- **Defina el éxito** : Comprenda qué significa el éxito, ya sea para un equipo,  
    una línea de producción completa o la planta. Conocer su objetivo final le ayudará a mantenerse enfocado y en el camino correcto.
- **Investiga y comparte** : Infórmate sobre las opciones disponibles para la instrumentación y  
    el despliegue de sensores. Comparte lo aprendido con los operadores y analicen las ventajas y  
    desventajas. No te aferres a una sola opción hasta alcanzar un consenso general sobre lo que podría  
    funcionar. Incluso si estás seguro de tener razón, no está de más que todos te apoyen mediante  
    la búsqueda de consenso.

```
Leveraging good architecture to drive progress 19
```

- **Proceda con cautela** : buscar culpables cuando algo sale mal puede ser un desastre, no solo  
    para las personas involucradas sino para el proyecto en su conjunto.

Realizar pruebas piloto (o simulaciones rápidas en el mundo ágil) puede ser una estrategia viable.  
Probar diferentes sensores o interfaces sin un compromiso total permitirá evaluar las ventajas  
y desventajas del enfoque y compartir los resultados con las partes interesadas.

Por supuesto, todas estas directrices se centran en los equipos de producción, donde un error puede causar  
problemas graves, como paradas de producción o incluso averías mayores. Un sensor de temperatura independiente no  
requiere tanto esfuerzo, pero probablemente no sea prudente elegir el primero que se vea y usarlo sin más.  
Incluso los sensores de bajo impacto deben evaluarse según algunas de las directrices mencionadas anteriormente. Hemos  
descrito algunas consideraciones para la adquisición de equipos y sensores, pero no hemos abordado el  
método para determinar si el sensor puede proporcionar las mediciones correctas. Asegúrese de  
analizar las tolerancias del equipo, las fluctuaciones de temperatura, presión y vibración. Esto  
le permitirá elegir sensores que funcionen dentro de las tolerancias de la máquina y proporcionen mediciones a  
la frecuencia adecuada.

### Aprovechar una buena arquitectura para impulsar el progreso

Los arquitectos son grandes defensores de los patrones y estándares. Seguir un método similar y probado es  
común en casi cualquier tipo de trabajo o industria, especialmente en aquellas que producen  
resultados físicos o tangibles. El tamaño o la resistencia del material pueden determinar en gran medida cómo construir algo, y  
ayudan a definir el tiempo y el costo de la construcción. Podemos aplicar esto directamente a la construcción de  
algo menos tangible, como el software. Con la Industria 4.0, tenemos lo mejor de ambos mundos: hardware  
y software, lo que nos permite utilizar técnicas de ingeniería tradicionales y, con suerte,  
procesos de ingeniería de hardware y software rigurosos.

En el ámbito del software, solemos llamarlas buenas prácticas, pero no siempre son las mejores para todos. A veces,  
lo que funciona para una empresa o equipo puede no funcionar para otro. De igual manera, existen diferencias entre  
sectores o entornos. Por ello, nuestro objetivo no es prescribir exactamente cómo funcionan las cosas,  
sino proporcionar un conjunto de modelos preliminares basados ​​en las buenas prácticas generalmente aceptadas del sector,  
que pueden adaptarse a su situación o solución.

A lo largo de este libro, compartiremos enfoques y patrones que se pueden adoptar, pero no temas  
seguir tu propio camino (dentro de lo razonable). Además, la tecnología cambia con el tiempo. Lo que  
hoy puede ser la mejor práctica, mañana podría no serlo, ya que surgen nuevos enfoques para alcanzar tus objetivos.

#### Observabilidad

Ya hemos mencionado el concepto de observabilidad en este capítulo, pero repasémoslo con más detalle. La observabilidad
no es exactamente lo mismo que la monitorización, pero existen diversas opiniones sobre cuál
es la diferencia. El nombre no es tan importante, pero conceptualmente es fundamental comprender la diferencia. Nuestra mejor
definición para complementar las técnicas de monitorización con un enfoque observacional es la siguiente.

La monitorización implica recopilar datos de sensores, registros y métricas de producción o máquinas. Esto te permite
comprender el estado actual de un sistema, ya sea una máquina o incluso los componentes
dentro de tu aplicación IoT. La monitorización te permite saber si algo está funcionando y
cuándo un sistema o pieza de equipo está caído.

La observación va un poco más allá y te permite saber mejor por qué algo está caído o no funciona
al nivel óptimo. La observación requiere monitorización y posiblemente instrumentación adicional en
múltiples niveles. Considera las siguientes posibilidades:

- **Para comprender cómo interactúan los sistemas** : En TI, es frecuente que un sistema o proceso afecte  
    a otro, pero eliminar las posibles causas para llegar a la raíz del problema puede resultar complejo.  
    Por ejemplo, una página web carga lentamente, pero el problema radica en que la base de datos está sobrecargada  
    o en que la consulta es más compleja y requiere más tiempo para completarse.
- **Para comprender mejor el funcionamiento interno de un sistema** : En el ejemplo anterior  
    sobre la base de datos, solo mediante una instrumentación más profunda, como la inyección de bytecode en el  
    código fuente, pudimos comprender lo que sucede. La instrumentación a nivel de código fuente también  
    nos permite ver cómo interactúan los componentes y comprender las interdependencias en  
    el proceso.

Para resumir, podemos definir claramente la diferencia entre monitorización y observación:

- La instrumentación permite la monitorización, que te avisa si algo falla.
- La monitorización permite la observabilidad, lo que te indica por qué algo falla.

Como mencioné, hay diferentes interpretaciones (he visto ejemplos donde esto está invertido), pero
esto parece tener más sentido. En realidad, el objetivo final es algo que todos queremos lograr. Queremos
visibilidad completa en nuestros sistemas y procesos para que podamos manejar problemas y mejorar el resultado.

#### La repetibilidad reduce los costos

A medida que avances hacia la digitalización avanzada, habrá muchas partes móviles. Tanto el hardware
como el software deberán adaptarse constantemente a medida que la solución evolucione. Para implementaciones grandes donde
hay mucho equipo, o el entorno está ampliamente distribuido, puede requerir mucha ayuda para desplegar
y administrar el equipo. Los elementos a considerar incluyen los siguientes:

- ¿Qué tipo de equipo está utilizando y puede ser desplegado o configurado para manejar múltiples  
    usos o tipos de equipo?
- ¿Cuál es el tipo de equipo de monitoreo de sensores más adecuado (  
    equipo de propósito único o multipropósito)?
- ¿Cómo se comporta el equipo de monitorización de sensores en términos de coste, formación, instalación  
    y mantenimiento?
- ¿Cuánta formación práctica será necesaria? ¿Una simple instalación plug and place, o una compleja  
    formación en configuración y gestión con manuales de operación?
- ¿Cómo deberá adaptarse el software a medida que se implementen sensores y monitores?

A medida que tus soluciones evolucionen, ten en cuenta estas directrices y cómo puedes optimizar la implementación y
la gestión, garantizando la máxima repetibilidad posible. Si
es necesario configurar sensores y recopiladores de datos, ¿requiere el software y la nube alguna personalización? Considera
aspectos como las etiquetas personalizadas. A gran escala, ¿cuánto trabajo supondrá recopilar y almacenar datos de cientos
de equipos y miles de etiquetas?

### Resumen

El objetivo principal de este libro es la implementación del IoT industrial y el aprovechamiento de la tecnología en la nube de AWS  
para lograr la digitalización de su industria y entorno. Este capítulo se diseñó para  
sentar las bases y brindar una comprensión básica de la Industria 4.0, incluyendo su propósito y una perspectiva del  
futuro, lo que le ayudará a comprender mejor la visión final. Una hoja de ruta y una  
visión sólidas, guiadas por los objetivos comerciales y coordinadas con los equipos de operaciones y producción, pueden ayudarle a  
mantenerse en el camino correcto y garantizar que todos se involucren en el proceso.

En los próximos capítulos, nos centraremos en los detalles técnicos sobre cómo lograr algunos de estos objetivos  
para instrumentar, recopilar y utilizar datos en su entorno. ¡Esta es la parte más interesante del  
proceso para los entusiastas de la informática interesados ​​en aprender y usar nuevas tecnologías! La llegada del IoT ha  
puesto el hardware al alcance de los ingenieros de software, quienes no siempre tienen la oportunidad de  
trabajar con ambos. Hardware, software, redes y análisis ahora se consideran la pila completa para  
la mayoría de los ingenieros de IoT y abren nuevas oportunidades para soluciones interesantes en el sector industrial.

En el próximo capítulo, describiremos nuestro enfoque general de planificación de la arquitectura. Explicaremos los  
principales niveles de arquitectura y los componentes clave para construir una plataforma de IoT industrial exitosa y escalable.  
Comenzar con los conceptos básicos proporcionará un punto de partida para adaptar algunos conceptos de arquitectura útiles  
a su entorno, ya sea al iniciar o continuar su desarrollo de IoT. También hablaremos sobre las funciones del  
arquitecto de TI y los diferentes tipos de roles de arquitecto, y analizaremos cómo puede contribuir al máximo  
al éxito del proyecto.

Por ahora, ¡tómese una taza de café, siéntese en su sillón favorito y disfrute!

# 2

## Anatomía de una arquitectura IoT

Al comenzar a pensar en la arquitectura y el conjunto de soluciones, es fundamental tener una idea clara de  
hacia dónde nos dirigimos. En el Capítulo 1, "Introducción a la evolución del IoT", analizamos la importancia de  
alinear los equipos de negocio y producción con sus objetivos. Sin embargo, en este capítulo nos centraremos  
en el aspecto de TI e IoT y en cómo alcanzar dichos objetivos desde una  
perspectiva arquitectónica: cómo se deben recopilar los datos, cómo fluyen y se gestionan a través del sistema,  
dónde comienza su procesamiento y qué etapas de procesamiento se deben considerar.  
Finalmente, aprenderemos cómo poner esos datos, junto con el análisis y la información resultante, a disposición de la  
empresa para la toma de decisiones.

Estas decisiones se basan en múltiples factores, como su sector, objetivos comerciales, disponibilidad de  
datos recopilados y el tipo, la ubicación y la velocidad de los datos que recopila. Este capítulo pretende  
ofrecer una orientación inicial en su enfoque y toma de decisiones, guiándolo a través de las opciones  
disponibles. Este libro se ha centrado en el uso de **Amazon Web Services** ( **AWS** ) como  
proveedor de servicios en la nube para todos los ejemplos; sin embargo, en este capítulo, continuaremos enfocándonos en conceptos  
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

### Requisitos técnicos

Una buena comprensión de las tecnologías y servicios en la nube será útil en este capítulo. Aunque
estamos mirando las cosas de manera más genérica, uno de nuestros objetivos en este libro es proporcionar asesoramiento de diseño e
implementación sobre la construcción de soluciones utilizando AWS. Por lo tanto, algún conocimiento general de
AWS y algunos de los servicios IoT será útil para tu comprensión pero no es necesario.
Si estás familiarizado con otro proveedor de nube, probablemente puedas mapear esos servicios directamente en
las capas que presentamos.

### Pensamiento arquitectónico

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

#### Modelos de referencia

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
deberían funcionar las cosas. En sistemas o entornos complejos, podemos comenzar con niveles para ilustrar conceptos  
de forma sencilla. Esto permite que las partes interesadas no técnicas comprendan el enfoque sin tener que analizar  
detalles técnicos complejos que pueden no ser de su interés o que no comprendan completamente.

Si partes de cero y solo quieres hacerte una idea de cómo podría ser,  
considera los mejores productos del mercado y las mejores prácticas de algunos proveedores líderes. Puede ser complicado, ya que  
existe una fuerte tendencia a depender exclusivamente de los planes de ciertos proveedores y usar solo sus productos. Sin embargo,  
también puede proporcionarte el punto de partida necesario para comprender cómo algunas de las tecnologías más recientes  
pueden funcionar en tu entorno. Avanza poco a poco y con paso firme hasta que logres discernir  
la tecnología adecuada para tus objetivos.

### Componentes arquitectónicos para IoT

Para comprender hacia dónde vamos, a veces debemos saber de dónde venimos. La historia
de las tecnologías de la información y la automatización industrial puede ayudarnos a entender cómo funcionan las cosas hoy en día, y podemos
aprovecharla a medida que la tecnología evoluciona. Uno de esos primeros modelos de referencia es la
Arquitectura de Referencia de Purdue, desarrollada a mediados de la década de 1990. Una de las características clave del modelo de Purdue es la
definición de capas o niveles de separación para los sistemas industriales.

ISA-95 es el estándar para la automatización de sistemas de control empresarial, basado en el
modelo Purdue y que continúa evolucionando. El objetivo de ISA-95 es definir estándares para
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
implementación práctica de algunas de las tecnologías que se abordan. Sin embargo, las lecciones aprendidas en este libro
pueden aplicarse a su análisis de AE ​para determinar el mejor camino a seguir para su organización.
Los patrones que surjan de este trabajo pueden implementarse en toda la empresa como estándares futuros.

Esta es una herramienta sin conexión; tus datos permanecen localmente y no se envían a ningún servidor.