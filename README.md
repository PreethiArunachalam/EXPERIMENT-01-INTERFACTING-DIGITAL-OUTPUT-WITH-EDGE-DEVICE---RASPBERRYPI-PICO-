# EXPERIMENT-01-INTERFACTING-DIGITAL-OUTPUT-WITH-EDGE-DEVICE---RASPBERRYPI-PICO-
## NAME: PREETHI A A 
## DEPARTMENT: CSE(IoT) 
## ROLL NO: 212222110035 
## DATE OF EXPERIMENT: 24/02/2025 

### AIM
To interface a digital output device (LED) with the Raspberry Pi Pico and control it using MicroPython.

## APPARATUS REQUIRED
Raspberry Pi Pico
LED (Light Emitting Diode)
330Ω Resistor
Breadboard
Jumper Wires
USB Cable
Computer with Thonny IDE
## THEORY
Raspberry Pi Pico is a microcontroller board based on the RP2040 chip. It supports MicroPython, making it suitable for IoT and embedded applications.

Digital Output refers to controlling external devices like LEDs, buzzers, or relays using GPIO (General Purpose Input Output) pins. A GPIO pin can be set to HIGH (3.3V) or LOW (0V) to turn the device ON or OFF.

## Working Principle:

The LED is connected to one of the GPIO pins of the Pico.
The MicroPython script sets the GPIO pin HIGH to turn the LED ON and LOW to turn it OFF.
CIRCUIT DIAGRAM
Connect the anode (longer leg) of the LED to GP15 via a 330Ω resistor.
Connect the cathode (shorter leg) of the LED to GND (ground).


## PROGRAM (MicroPython)
## LED BLINK:
```
from machine import Pin
from utime import sleep

print("Hello, Pi Pico!")

led = Pin(0,Pin.OUT)
while True:
  led.toggle()
  sleep(0.5)
```
## LED TOGGLE:
```
from machine import Pin
from utime import sleep

led1 = Pin(0, Pin.OUT)
led2 = Pin(1, Pin.OUT)
led3 = Pin(2, Pin.OUT)
while True:
    led1.toggle()
    sleep(0.5)
    led2.toggle()
    sleep(0.5)
    led3.toggle()
    sleep(0.5)
```
## LED WITH BUZZER:
```
from machine import Pin
from utime import sleep

print("Hello, Pi Pico!")

led1 = Pin(0,Pin.OUT)
led2 = Pin(1,Pin.OUT)
led3 = Pin(2,Pin.OUT)
buzz = Pin(3,Pin.OUT)
while True:
  led1.toggle()
  sleep(0.5)
  buzz.toggle()
  sleep(0.5)
  led2.toggle()
  sleep(0.5)
  led3.toggle()
  sleep(0.5)
```
## OUPUT  
## LED BLINK:
![Screenshot 2025-02-24 113645](https://github.com/user-attachments/assets/b5202ebc-855e-4206-898a-87d6f89146a3)

## LED TOGGLE:
![Screenshot 2025-02-24 104526](https://github.com/user-attachments/assets/b6587cbc-4c7a-4c81-bf97-5dcd1c726cc6)

## LED WITH BUZZER:
![image](https://github.com/user-attachments/assets/02000313-b0e9-471e-9024-c5347bf66187)

 
## RESULTS
The LED connected to the Raspberry Pi Pico successfully turns ON and OFF at 1-second intervals, confirming the proper interfacing of a digital output.
