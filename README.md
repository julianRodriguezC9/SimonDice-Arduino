 -----------------------------------ESPAÑOL--------------------------------------------------    


# Proyecto Simon Dice con ESP32

## Descripción

Este proyecto consiste en la implementación del clásico juego "Simon Dice" utilizando una placa ESP32 y la plataforma de desarrollo Arduino. El juego presenta una secuencia de colores que el jugador debe repetir en el mismo orden. A medida que el juego avanza, la secuencia se hace más larga y más difícil, lo que pone a prueba la memoria y los reflejos del jugador.

El proyecto incluye una interfaz con un display LCD para mostrar instrucciones y puntajes, además de varios botones para la interacción del jugador. Los botones se asocian con los colores que se iluminan en los LEDs, y el jugador debe presionar los botones en el orden correcto para seguir el juego.

## Componentes

- **ESP32**: Placa de microcontrolador para manejar la lógica del juego.
- **Display LCD 16x2**: Para mostrar la información del juego como instrucciones, puntajes y el nombre del jugador.
- **LEDs RGB** (Rojo, Verde, Azul, Amarillo): Para mostrar los colores de la secuencia.
- **Botones**: Para que el jugador interactúe con el juego, presionando los botones correspondientes a los colores de la secuencia.
- **Buzzer**: Para emitir sonidos cuando el jugador presiona correctamente o incorrectamente un botón.
- **Potenciómetro**: Para seleccionar el modo de juego.

## Modos de Juego

El proyecto implementa varios modos de juego, cada uno con reglas y dificultades diferentes:

1. **Normal**: El modo estándar donde el jugador sigue una secuencia de colores que se va alargando con el tiempo.
2. **Cuántico**: Un modo con reglas de juego alteradas por efectos aleatorios.
3. **Rápido**: Un modo en el que la secuencia de colores debe repetirse más rápidamente.
4. **Trampa**: En este modo, la secuencia incluye trampas para confundir al jugador.
5. **Doble**: El jugador debe seguir dos secuencias simultáneamente.
6. **Apreton**: El jugador debe presionar los botones con más rapidez.
7. **Hardcore**: Un modo con dificultad extrema, donde el jugador tiene vidas limitadas.
8. **Reversa**: La secuencia de colores debe repetirse al revés.

## Funcionamiento

El juego comienza con una pantalla que invita al jugador a seleccionar el modo de juego a través del potenciómetro. A medida que el jugador selecciona el modo, el juego muestra una secuencia de colores en los LEDs, y el jugador debe presionar los botones correspondientes a esos colores en el mismo orden. Si lo hace correctamente, la secuencia aumenta en longitud. Si comete un error, pierde una vida.

El jugador tiene varias vidas dependiendo del modo de juego. Cuando se acaban las vidas, el juego muestra el puntaje final del jugador y lo guarda en el ranking.

## Características del Código

- **Interfaz LCD**: Muestra el modo seleccionado, las instrucciones del juego y el puntaje.
- **Selección del modo de juego**: Usando el potenciómetro y los botones, el jugador puede elegir entre varios modos de dificultad.
- **Control de LEDs y buzzer**: Los LEDs se iluminan en el orden de la secuencia, y el buzzer emite un sonido al presionar un botón.
- **Puntajes y clasificación**: El juego mantiene un ranking con los mejores puntajes de cada modo.

## Instrucciones de Uso

1. **Conectar los componentes**: Asegúrate de conectar correctamente los LEDs, botones, potenciómetro y el buzzer a los pines definidos en el código.
2. **Seleccionar el modo de juego**: Usa el potenciómetro para navegar por los modos de juego disponibles.
3. **Jugar**: Presiona los botones cuando los LEDs se iluminen. Intenta repetir la secuencia correctamente.
4. **Ver tu puntaje**: Al finalizar el juego, se mostrará tu puntaje en la pantalla LCD. Puedes ingresar tu nombre y ver tu clasificación.

## Pinout

| Componente        | Pin ESP32 |
|-------------------|-----------|
| Entrada Roja      | GPIO 16   |
| Entrada Verde     | GPIO 4    |
| Entrada Azul      | GPIO 2    |
| Entrada Amarilla  | GPIO 15   |
| LED Rojo          | GPIO 27   |
| LED Verde         | GPIO 14   |
| LED Azul          | GPIO 12   |
| LED Amarillo      | GPIO 13   |
| Potenciómetro     | GPIO 34   |
| Buzzer            | GPIO 23   |
| Brillo LCD        | GPIO 22   |
