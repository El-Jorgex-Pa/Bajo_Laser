# Proyecto Bajo Laser

Este repositorio hace parte del proyecto de un sintetizador que incorpora distintos instrumentos realizados por los estudiantes que se comunican a través de una FPGA y que a través de [Chuck](https://github.com/ccrma/chuck) se genere música.

Específicamente en este repositorio se encuentra un módulo que busca simular un bajo a través de láseres, fotorresistencias y potenciometros.

## Funcionamiento 

El módulo tiene 4 láseres que representan cada una de las cuerdas de un bajo, estos láseres siempre se encuentran encendidos; cuando el usuario interrumpa el haz, la fotorresistencia cambiará su estado y el efecto que tendrá será el de tocar la cuerda. Por otra parte, a través de un potenciometro