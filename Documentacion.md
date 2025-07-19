# Proyecto Bajo Laser

Este repositorio hace parte del proyecto de un sintetizador que incorpora distintos instrumentos realizados por los estudiantes que se comunican a través de una FPGA y que a través de [Chuck](https://github.com/ccrma/chuck) se genere música.

Específicamente en este repositorio se encuentra un módulo que busca simular un bajo a través de láseres, fotorresistencias y potenciometros.

## Funcionamiento 

El módulo tiene 4 láseres que representan cada una de las cuerdas de un bajo, estos láseres siempre se encuentran encendidos; cuando el usuario interrumpa el haz, la fotorresistencia cambiará su estado y el efecto que tendrá será el de tocar la cuerda. Por otra parte, a través de un potenciometro.

## EL LASER COMO CUERDA

Este proyecto busca construir un instrumento digital experimental, donde módulos láser económicos simulan las cuerdas de un bajo eléctrico. Cuando una persona interrumpe uno de estos rayos láser con la mano, se genera una señal que será interpretada como si se hubiese pulsado una cuerda, activando una respuesta digital.
