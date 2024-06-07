## Day 3 Lets Blink

Now let's get our hands dirty and do some simple programming. Today we are going to run some basic programs and find out what register level programming is.

### Step 1: Arduino IDE and First Sketch

1. Two sections in the first sketch are seen.
```bash
void setup()

{ // one time code }

void loop()

{ the code that repeats infinity }
```
### Specs

1. Now I need to find out the board datasheet. This is the [kit](https://www.amazon.in/Compatible-Mega2560-Ultrasonic-including-30-Projects/dp/B097NP82MZ?th=1) that I have.Upon further inspection I found the exact board that came with the kit. Its an SMD type that costs about [280](https://rees52.com/products/rees52-smd-uno-r3-board-uno-r3-controller-board-uno-r3-smd-atmega328p-board-compatible-with-arduino-ide-rs5560) INR.
2. Board Details: REES52 UNO R3 Board SMD, Atmega328P Compacitable. RS5560.3. 1) Microcontroller: Atmega328P

2) Operating Voltage: 5V

3) Input Voltage( Recommended): 7~12v

4) Input Voltage limit: 5~20V

5) Analog I/O Pins: 6

6)Digital I/O Oins: 14

7) PWM Digital I/O Pins: 6a

8)Dc Current Per I/O PIN: 40mA ( so total current is 40mA X (14 ) ?)

9) Clock Speed : 16 MHz

10) SRAM: 2KB

11) Flash Memory: 32 KB

12) EEPROM: 1KB

13) USB to Serial Chip Model: CH340G
1. Since this is a clone of the SMD type of UNO R3, this is the datasheet of the [official Arduino SMD]
3. After finding the official guide for Blinking and [Arduino](https://docs.arduino.cc/tutorials/uno-rev3-smd/Blink/), it says that D13 is the BuiltIn Led. Ah, Arduino has 2 Naming Scheme. Each pin has both a digital pin number (e.g. D13) and a port/pin designation (e.g. PB5). D= Digital P=Pin.

### Blink
Letme try blinking it using both the naming convention.  
    Error:  

**FIX**: dont put d13 in the name, but use 13. Just the number

1. After digging deeper and deeper ! We struck the gold mine! Here is the register level programming we had been looking for!


See point 2 in above picture! Thats what I was after!

Pausing here for now! Unless I work later!

### Knowledge

1. UNO R3 SMD vs Normal UNO R3 = So basically the first one is Through Hole (TH) and the second one is SMD. Nothing else I think.
2. The Reason for 2 naming scheme : PB5 = Avr’s Notation D13= Arduino’s Notation


###

Additional tasks:

1\. Extract the program [hex](https://www.instructables.com/How-to-Get-Code-Program-Back-From-Arduino/). Some other day. You might need another AVR board for that.
