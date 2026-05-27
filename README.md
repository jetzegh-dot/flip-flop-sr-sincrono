# Práctica: Flip-Flop S-R Activado por Flanco

**Estudiante:** Guadalupe Jetzemani Granillo Hernandez  
**Materia:** Sistemas Digitales  

## Descripción
Diseño, armado y simulación en Logisim de un Flip-Flop S-R síncrono utilizando compuertas AND y NOR, controlado por una señal de reloj dinámica (Clock) para analizar su comportamiento por flancos de subida.

## Evidencia del Circuito Funcionando
![Circuito Flip-Flop S-R](<Captura de pantalla 2026-05-26 201326.png>)

## Tabla de Verdad (Modo Síncrono)
| Clock (Reloj) | S | R | Q | ~Q | Estado / Comportamiento |
| :---: | :---: | :---: | :---: | :---: | :--- |
| 0 o 1 | X | X | Q(t) | ~Q(t) | **Memoria:** Bloqueado si el reloj no cambia. |
| ↑ | 0 | 0 | Q(t) | ~Q(t) | **Sin cambios:** Mantiene el estado anterior. |
| ↑ | 0 | 1 | 0 | 1 | **Reset:** La salida Q se limpia a 0. |
| ↑ | 1 | 0 | 1 | 0 | **Set:** La salida Q almacena un 1. |
| ↑ | 1 | 1 | 0 | 0 | **Estado Prohibido:** Condición indeterminada. |

## Comparativa: Latch S-R vs. Flip-Flop S-R
* **Latch S-R (Activado por Nivel):** Este dispositivo responde de manera continua. Mientras la señal de habilitación se mantenga en un nivel alto (1), cualquier cambio en los pines de entrada modifica la salida de forma inmediata, lo que lo hace más vulnerable al ruido del circuito.
* **Flip-Flop S-R (Activado por Flanco con Entrada Dinámica):** Es un sistema síncrono mucho más preciso. Cuenta con un indicador dinámico (el reloj) que le ordena al circuito tomar una "fotografía" de los estados de S y R únicamente en el instante exacto en que la señal de reloj pasa de 0 a 1 (flanco de subida). Fuera de ese milisegundo, las salidas ignoran por completo las entradas, garantizando un almacenamiento de datos estable y seguro.
