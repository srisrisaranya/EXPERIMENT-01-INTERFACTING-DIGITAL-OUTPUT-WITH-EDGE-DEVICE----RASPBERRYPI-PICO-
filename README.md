# EXPERIMENT-01-INTERFACTING-DIGITAL-OUTPUT-WITH-EDGE-DEVICE---(RASPBERRYPI-PICO)
### NAME SARANYA S
### DEPARTMENT B.E CSE-IOT
### ROLL NO 212223110044
### DATE OF EXPERIMENT 

### AIM
To interface a digital output device (LED) with the Raspberry Pi Pico and control it using MicroPython.

## APPARATUS REQUIRED
Raspberry Pi Pico
LED (Light Emitting Diode)
330Ω Resistor
Breadboard
Jumper Wires
USB Cable
 ## THEORY

 ![image](https://github.com/user-attachments/assets/abeabf63-f321-471e-a991-3adaa9043a8b)

 
### FIGURE-01 RASPI PICO PINOUT DIAGRAM 



 Raspberry Pi Pico is a microcontroller board based on the RP2040 chip. It supports MicroPython, making it suitable for IoT and embedded applications.
The Raspberry Pi Pico is a compact microcontroller board featuring a 40-pin layout, including power, ground, GPIO, and communication interface pins. It operates with a dual-core ARM Cortex-M0+ processor and supports MicroPython and C/C++ programming. The power pins include VBUS (5V from USB), VSYS (1.8V to 5.5V input), 3V3(OUT) (regulated 3.3V output), and multiple ground (GND) connections. The board offers 26 multi-purpose GPIO pins (GP0 to GP28), which can be used for digital input, output, PWM, and communication interfaces such as I2C, SPI, and UART. It also features three analog-to-digital converter (ADC) pins (GP26, GP27, GP28), used for reading analog sensor values, along with an ADC_VREF pin to set the reference voltage. For communication, I2C (SDA, SCL), SPI (MOSI, MISO, SCK), and UART (TX, RX) interfaces are mapped across different GPIO pins, allowing seamless connectivity with sensors and peripherals. All GPIO pins support PWM (Pulse Width Modulation), making it useful for motor control, LED brightness adjustment, and sound applications. The BOOTSEL button enables USB mass storage mode for firmware flashing, while the DEBUG pins (SWD interface) provide debugging capabilities. With its low power consumption, flexible GPIO options, and rich interface support, the Raspberry Pi Pico is widely used for IoT, embedded systems, robotics, and automation projects.


## Working Principle:

The LED is connected to one of the GPIO pins of the Pico.
The MicroPython script sets the GPIO pin HIGH to turn the LED ON and LOW to turn it OFF.
CIRCUIT DIAGRAM
Connect the anode (longer leg) of the LED to GP15 via a 330Ω resistor.
Connect the cathode (shorter leg) of the LED to GND (ground).


## PROGRAM (MicroPython)

# LED WITH TIME DELAY:
```
from machine import Pin
import time
print("Hello pico")
led = Pin(0, Pin.OUT)
while True:
    led.value(1)
    print("LED IS ON")
    time.sleep(1)
    led.value(0)
    print("LED IS OFF")
    time.sleep(1)
 ```
THREE LED IN SERIES WITH TIME DELAY:
```
from machine import Pin
import time
print("Hello pico")
led1=Pin(0,Pin.OUT)
led2=Pin(1,Pin.OUT)
led3=Pin(2,Pin.OUT)
while True:
    led1.value(1)
    print("LED is ON")
    time.sleep(1)
    led1.value(0)
    print("LED IS OFF")
    time.sleep(1)
    led2.value(1)
    print("LED is ON")
    time.sleep(1)
    led2.value(0)
    print("LED IS OFF")
    time.sleep(1)
    led3.value(1)
    print("LED is ON")
    time.sleep(1)
    led3.value(0)
    print("LED IS OFF")
    time.sleep(1)
```
# LED AND BUZZER IN SERIES WITH TIME DELAY:
```
from machine import Pin
import time
print("Hello pico")
led1=Pin(0,Pin.OUT)
led2=Pin(1,Pin.OUT)
led3=Pin(2,Pin.OUT)
buzzer=Pin(4,Pin.OUT)
while True:
    led1.value(1)
    print("LED is ON")
    time.sleep(1)
    led1.value(0)
    print("LED IS OFF")
    time.sleep(1)
    led2.value(1)
    print("LED is ON")
    time.sleep(1)
    led2.value(0)
    print("LED IS OFF")
    time.sleep(1)
    led3.value(1)
    print("LED is ON")
    time.sleep(1)
    led3.value(0)
    print("LED IS OFF")
    time.sleep(1)
    buzzer.value(1)
    print("LED is ON")
    time.sleep(1)
    buzzer.value(0)
    print("LED IS OFF")
    time.sleep(1)
```
# FIGURE -01  LED WITH TIME DELAY OUPUT: 
<img width="1918" height="974" alt="Screenshot 2025-08-09 215838" src="https://github.com/user-attachments/assets/65a7a6a2-6acf-44e6-9dd2-0478d0911717" />


# FIGURE -02 THREE LED IN SERIES WITH TIME DELAY OUTPUT: 
<img width="1919" height="976" alt="Screenshot 2025-08-09 222153" src="https://github.com/user-attachments/assets/0202e145-22b7-46f3-86de-b616f40c4d8e" />

# FIGURE -03  LED AND BUZZER IN SERIES WITH TIME DELAY OUTPUT:
<img width="1919" height="976" alt="Screenshot 2025-08-09 222951" src="https://github.com/user-attachments/assets/e16d941d-6938-4d65-827f-adb7b4e90f60" />


## RESULTS
The LED connected to the Raspberry Pi Pico successfully turns ON and OFF at  user defined time  confirming the proper interfacing of a digital output.
