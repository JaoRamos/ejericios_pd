# Ejericios PD (UNQ)
Ejercicios de práctica para Introducción a la Programación aplicada al Sonido (UNQ) 2024.

**Sugerencias para cada ejercicio**
- Primero dibujar un diagrama de flujo de la señal
- Identificar entradas y salidas de cada objeto
- Pensar en el orden lógico de las conexiones
- Probar exhaustivamente el patch una vez armado
- Experimentar modificando valores y conexiones


<br>

## Ejercicio 1: "Hola Mundo" sonoro

**Consigna**\
Conectar los elementos necesarios para escuchar un tono 
constante. Experimentar cambiando manualmente el valor de frecuencia del 
oscilador.

**Elementos minimos:**
- 1 objeto [osc~] configurado a 440 Hz
- 1 objeto [dac~] para la salida de audio

**Objetivos:** 
- Crear el patch más simple que produce un tono sinusoidal.
- Entender el flujo básico de señal
- Aprender a crear objetos y conexiones
- Experimentar cambiando la frecuencia manualmente

<br>

## Ejercicio 2: Control de amplitud y frecuencia

**Consigna:**\
Crear un patch donde puedas controlar tanto la frecuencia como el 
volumen del oscilador en tiempo real. La frecuencia debería poder 
variar entre 50 y 2000 Hz, y la amplitud entre 0 y 1.

**Elementos minimos:**
- 2 objetos [number] (uno para frecuencia y otro para amplitud)
- 1 objeto [osc~]
- 1 objeto [*~] para control de amplitud
- 1 objeto [dac~]

**Objetivos:** 
- Introducir control numérico interactivo
- Modificar parámetros en tiempo real
- Aprender sobre multiplicación de señales
- Experimentar con diferentes combinaciones de frecuencia y amplitud

<br>

## Ejercicio 3: Envolvente simple ADSR

**Consigna:**\
Crear un patch que genere un tono con una envolvente ADSR simple. 
Al presionar un bang, el sonido debería tener un ataque, decaimiento, 
sostenimiento y liberación controlados. Experimentar con diferentes 
valores de tiempo y nivel en el mensaje de la envolvente. En este caso, 
dejaremos fijo el sustain por un tiempo predeterminado, eventualmente 
esto puede controlarse con mensajes MIDI.

**Elementos minimos:**
- 1 objeto [loadbang]
- 1 objeto [message] con valores para la envolvente
- 1 objeto [vline~]
- 1 objeto [osc~]
- 1 objeto [*~]
- 1 objeto [dac~]
- 1 objeto [bang] (para disparar la envolvente)

**Objetivos:** 
- Introducir el concepto de automatización
- Aprender sobre mensajes y el objeto vline~
- Crear sonidos más musicales
- Modificar los tiempos y niveles de la envolvente

<br>

## Ejercicio 4: Sintetizador MIDI básico

**Consigna:**\
Construir un sintetizador simple que responda a notas MIDI. 
El patch debe poder recibir notas MIDI, convertirlas a 
frecuencias y generar el tono correspondiente. Verificar 
que el sintetizador responda correctamente a diferentes notas 
y a la velocidad MIDI.

**Elementos minimos:**
- 1 objeto [notein]
- 1 objeto [mtof]
- 1 objeto [osc~]
- 1 objeto [*~] para la amplitud
- 1 objeto [dac~]

**Objetivos:** 
- Tener una primera aproximación a MIDI
- Aprender sobre conversión de notas a frecuencias
- Tocar con un teclado MIDI
- Introducir conceptos de interfaz musical

<br>

## Ejercicio 5: Delay simple

**Consigna:**\
Crear un efecto de delay simple que permita: 
- Escuchar la señal directa del micrófono
- Agregar una línea de delay
- Controlar el nivel de la señal procesada
- Crear feedback/retroalimentación controlado (opcional)
- Experimentar con diferentes tiempos de delay
  

**Elementos minimos:**
- 1 objeto [adc~] para entrada de audio
- 1 objeto [delwrite~] (nombrar el buffer de delay)
- 1 objeto [delread~] (usar el mismo nombre de buffer)
- 2 objetos [*~] (uno para el nivel de señal directa y otro para el feedback)
- 1 objeto [dac~]

**Objetivos:** 
- Crear un primer procesador de efectos
- Aprender sobre entradas de audio
- Entender el concepto de retroalimentación
- Experimentar con diferentes tiempos de delay y niveles de feedback

