# nixie-clock-hardware
Hardware for controlling six VFD IV-17 and two VFD IV-1 tubes as clock (HH:MM:SS) 

![asssembled VFD-clock](img/photo_2024-12-29_21-03-52.jpg "asssembled VFD-clock")

![asssembled VFD-clock](img/photo_2024-12-29_21-03-55.jpg "asssembled VFD-clock")

### Requirements for rev 1.0
* efficient step-boost converter up to 50V
* multiplexing
* control syncronous addressable LEDs
* PWM control
* I²C interface
* connector for ESP (UART)
* time syncronisation line for every second

### Known issues in rev 1.0
* octal buffer for PWM use seems do not works for dimming
  * workaround: dimming solved by adding turn-off points in mulitplexing routine (firmware-based solution)
* SPI is not suitable for controlling 20-bit shift register
  * cut traces and wire up to another pins

### Pictures (rev 1.0)

![pcb top](img/top.png "vfd-clock PCB v1.0 top view")

![pcb bottom](img/bottom.png "vfd-clock PCB v1.0 bottom view")

