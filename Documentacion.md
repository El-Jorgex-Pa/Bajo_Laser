# Proyecto Bajo Laser

Este repositorio hace parte del proyecto de un sintetizador que incorpora distintos instrumentos realizados por los estudiantes que se comunican a través de una FPGA y que a través de [Chuck](https://github.com/ccrma/chuck) se genere música.

Específicamente en este repositorio se encuentra un módulo que busca simular un bajo a través de láseres, fotorresistencias y potenciometros.

## Funcionamiento 

El módulo tiene 4 láseres que representan cada una de las cuerdas de un bajo, estos láseres siempre se encuentran encendidos; cuando el usuario interrumpa la luz de uno de los laseres, la fotorresistencia cambiará su estado y el efecto que tendrá será el de tocar la cuerda, de igual manera la interrupción de dos o más laseres a la vez se interpretará como el toque de más de una cuerda, por lo que sonará una nota diferente en cada combinación. 
Por otra parte, a través de un potenciometro

## Requerimientos funcionales

- Uso de LDR para la generación de una funete de luz estable.
- Implementación de un modulo con fotorresistencia incorporada para medir cuando se toca una nota.
- Generación de nota MIDI con chuck
- Uso de del chip SoC ESP32 como transmisor de datos entre la FPGA a través de red wifi.

## Diagrama de flujo

## Diagrama RTL


## Simulación verilog-gtkwave

## Logs


## Explicación de conexión con CHuck

Cada laser genera una nota en binario, que en total con los 4 laseres son 4 bits, por lo que se generan valores de 0 a 15 en decimal que son enviadas por medio de la ESP32 hacia la FPGA por el puerto UART para luego ser enviadas usando el protocolo OSC y finalmente procesar estos valores en Chuck.

En el procesamiento de los valores de cada laser, se definió a cada laser como la representación una nota que apunta a un valor de MIDI, yendo de esa forma de la nota más aguda a la más grave. Se recalca las notas principales de cada laser de forma individual: 

Para la combinación 0001, se tiene un Mi (64), para 0010 un La (69), para 0100 un Re (62), para 1000 Sol (67), para valores intermedios se tienen configurados otros valores.

Para todas la notas el volumen de sonido se mantiene constante y la duración de cada nota es de 250ms.



