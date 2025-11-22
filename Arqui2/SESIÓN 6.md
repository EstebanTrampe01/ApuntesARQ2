# Automatización Industrial

**Control manual:** como cuando una persona cierra o abre una válvula cuando esa persona percibe si es suficiente según su criterio de vista

![[Pasted image 20251120214101.png]]

**Variables de un Sistema:** 
Es un proceso industrial pero con variables

![[Pasted image 20251120214517.png]]

**variables de entrada** es un conjunto de variables, que cuando se conoce su valor permite conocer la respuesta (variable salida) en base a una señal de entrada o perturbación.

**Planta** es un equipo físico con el objetivo de lograr una función (como un horno, motor, reactor)
**Proceso** serie de operaciones controladas con un objetivo
**Perturbación** señal de comportamiento que no se puede predecir que pueda alterar de mala manera los valores de un salida de un sistema.
**Re-alimentación (feedback)**  mide su propia salida para ver si hay errores
**Sistema de regulación automática**: usa el feedback para mantener una valor deseado aun con perturbaciones  (es una aplicación del lazo cerrado)
**Control de bucle (lazo) abierto** el sistema no revisa su salida, no corrige si algo sale mal, solo ejecuta las instrucciones.
**Control en bucle (lazo) cerrado**  el sistema si revisa su salida, compara referencia y corrige su error. se corrige con su feedback

### Revolución Electrónica;
**1769 Revolución Mecánica:**
reguladores electrónicos

**1952 Electrónica analógica**
Amplificador Operacional Philbrick

**1971 Electrónica Digital**
Microprocesador 4004

--- 
## Control de lazo (o bucle) abierto

![[Pasted image 20251120220915.png]]

La señal de entrada actúa sobre el regulador para obtener con el actuador el efecto deseado en las variables de salida.
- El regulador no comprueba el valor de la salida y es sensible a las perturbaciones sobre la planta
- 
![[Pasted image 20251120221222.png]]

## Control en lazo (o bucle) cerrado

![[Pasted image 20251120221410.png]]

- Ahora la salida se mide con un sensor y se compara con el valor de la entrada
- deduciendo el sistema de control como responder mejor ante las perturbaciones

![[Pasted image 20251120221430.png]]

--- 
## Sistema de Fabricación Industrial

Los componentes comunes de una planta industrial como ensayo de fábricas:
- Máquinas
- Sistemas de manipulación o transporte de materiales
- Sistema de control por computador
- Recursos humanos

**Tipos de máquina de producción**
- **Manuales** supervisados por un operativo, la maquina proporciona la fuerza y la energía y el trabajador proporciona el control
- **Semiautomáticas**  un programa en la máquina ocupa parte del ciclo y el operario la otra parte.
- **Automática** las máquinas operan en largos períodos de tiempo sin intervención del operario. nomas hay que vigilar por un número de ciclos

**Tipos de sistemas de manipulación de material**
- **Carga** mueven unidades hasta las máquinas de producción
- **Colocación o posicionamiento** cuando se necesita exactitud, para situar la unidad en una posición determinada.
- **Descarga** al terminar la producción se retira la unidad finalizada y se transporta o se retira

**Funciones de los sistemas de control por computador**
Es como el sistema que controla las computadoras que hacen una tarea en especifico

- Comunicar instrucciones a los trabajadores
- Descarga de programas de piezas a las máquinas controladas por computadoras
- control o coordinación de sistemas de  transformación y transporte de materia
- planificación de la producción de planta
- Diagnóstico de averías o fallas
- Supervisión de seguridad de procesos
- Control de calidad

**Funciones de los recursos humanos**
- **Operarios**: realizan el trabajo manual o semiautomático o controlan el automático.
- **Operadores informáticos o programadores** encargados de programar o hacer correcciones de las maquinas

**Realización tecnológica de control**
- **1950 Control Todo / Nada**
	- Lógica de control cableado de componentes electrotecnia
	- de elementos todos/nada
- **1960 Control Analógico**
	- Circuitos electrónicos analógicos 
	- Aparece PID (Proporcional integral derivativo)
- **1970 Control digital con datos muestreados**  
	- Uso de microprocesadores
	- tecnología digital
	- mayor flexibilidad 
	- sistemas DCS
- **1980 Control de eventos discretos**
	- respuesta ante eventos
	- señales binarias
	- teorías de estados
	- sistemas PLC  (Controladores lógicos programables

---
## Tipos de sistemas Automatización Industrial

**Magnitudes de las que se habla en la industria**
- **Continuos**: variables con infinitos valores como los flujos, temperatura.
- **Discretos**: valores binarios como ON/OFF, llego o no llego

**Tipos de procesos industriales**
- **Continuos**: control analógico como los metales básicos, farmacéuticos, generación de energía.
- **Discretos**: control por eventos discretos como los aviones, maquinaria 

**Zonas de una planta de fabricación**

![[Pasted image 20251120225553.png]]

**Sistema de control en una planta de fabricación**

![[Pasted image 20251120225654.png]]

**Control en los tipos de procesos industriales**
- **Continuos**: control analógico
	- DCS: Distributed Control System
- **Discretos**: control por eventos discretos 
	- PLC: programmable logic control

![[Pasted image 20251120225914.png]]

![[Pasted image 20251120225940.png]]

