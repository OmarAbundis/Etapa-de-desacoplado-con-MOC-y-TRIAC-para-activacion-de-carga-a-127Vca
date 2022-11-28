# Etapa de desacoplado con MOC y TRIAC para activación de carga eléctrica a 127Vca

En este trabajo se describe de qué manera se puede realizar una etapa de desacoplado utilizando un MOC3043 o equivalente, para que en el momento que se reciba un 1 lógico (5Vcd) se active una carga que funcione con 127Vca controlada por un TRIAC BT137.



## Introducción

En muchos proyectos actuales del internet de las cosas, se hace necesario que un microcontrolador mande un uno lógico, 5 Vcd, para que se ponga en funcionamiento un actuador (una carga) el cual funciona con 127 Vca, lo cual de manera directa no es posible realizarse, se hace necesario considerar una etapa de acoplamiento electrónico.

El aislamiento entre el microcontrolador, por ejemplo el ESP32-CAM, y la carga de 127Vca se hace utilizando un optoacoplador MOC3043 (o equivalente), que es un circuito integrado que incluye un LED que controla a un fototriac, en su interior. Este dispositivo está diseñado para usarse como interfaz de sistema lógicos en equipos que tienen que alimentarse con 127 Vca del suministro de la red eléctrica. Sus características más significativas son:

-	Encapsulado DIP6.
-	Su voltaje de aislamiento de 7500V.
-	Su fototriac interno permite el control de la casi totalidad de los grandes triacs.
-	Cuenta con un detector de cruce por cero interno, lo que permite economizar un número de componentes externos.

Cuando al instante de la conmutación de un triac no coincide con un cruce por cero del voltaje de la red el cambio repentino en la corriente produce un ruido eléctrico de alta frecuencia que introduce interferencias en la red eléctrica.


## Material necesario

- 1 Resistor de 100ohms. (Café,Negro,Café,Dorado)
- 1 Resistor de 220ohms. (Rojo,Rojo,Café,Dorado)
- 1 Resistor de 330ohms. (Naranja,Naranja,Café,Dorado)
- 1 Resistor de 360ohms. (Naranja,Azul,Café,Dorado)
- 1 BT137 (TRIAC)
- 1 [MOC3043, optoacoplador](https://www.datasheetq.com/MOC3043-doc-Motorola)
- 1 Capacitor de 10nF (103)
- Alambres con aislante para conexión (UTP)
- Jumpers MM

## Instrucciones de operación

## Material de referencia

Palacios Municio, E. Remiro Domínguez, F. López Pérez, L.J. (2006) *Microcontrolador PIC16F84 Desarrollo de proyectos.* Ed. Alfaomega Ra-ma
