# ATmega32 Stop Watch System

## Description

This project implements a versatile Stop Watch system using an ATmega32 Microcontroller with the following specifications:

1. **Microcontroller:** ATmega32 with a 1 MHz clock frequency.
2. **Timer Configuration:** Timer1 is configured in CTC (Clear Timer on Compare Match) mode to count the Stop Watch time.
3. **Display:** Six Common Anode 7-segment displays are multiplexed using a 7447 decoder and NPN BJT transistors.
4. **Port Configuration:** The 7447 decoder is connected to the first four pins in PORTC, and the first six pins in PORTA are used for enable/disable control of the seven-segment displays.
5. **Start:** The Stop Watch counting starts automatically when power is connected to the MCU.
6. **Reset:** External Interrupt INT0, triggered by a falling edge, is used to reset the Stop Watch time.
7. **Pause:** External Interrupt INT1, triggered by a rising edge, is used to pause the Stop Watch.
8. **Resume:** External Interrupt INT2, triggered by a falling edge, is used to resume the Stop Watch.
9. **Mode Control:** A push button connected to pin PB7 controls the mode of the Stop Watch. If pressed, the Stop Watch counts down; otherwise, it counts up.
10. **Time Adjustment:** Push buttons on PORTB allow for the adjustment of hours, minutes, and seconds.
11. **Buzzer Alarm:** In countdown mode, if the time reaches zero, a buzzer alarm will sound.

## Hardware Setup

### Components Required:

- ATmega32 Microcontroller
- Six Common Anode 7-segment Displays
- 7447 Decoder
- NPN BJT Transistors
- Push Buttons (for Reset, Pause, Resume, Mode Control, and Time Adjustment)
- Buzzer (for alarm)
- Resistors and Capacitors (as required)
- Breadboard or PCB for Circuit Assembly
- Power Supply (5V)

### Wiring Instructions:

- Connect the ATmega32 pins according to your schematic.
- Wire the six 7-segment displays using multiplexing technique as shown in the schematic.
- Connect the 7447 decoder to the first four pins of PORTC.
- Use the first six pins of PORTA for enabling/disabling the six 7-segment displays.
- Configure external interrupts INT0, INT1, and INT2 as described in the project specifications.
- Connect the push button for mode control to pin PB7.
- Use push buttons on PORTB for time adjustment.
- Connect a buzzer to a suitable pin (e.g., PBx) to sound the alarm when the countdown reaches zero.

## Development Environment and Code

- **Development Environment:** This project was developed using the Eclipse IDE. The AVR Eclipse Plugin was utilized to write, compile, and upload code to the ATmega32 microcontroller. The code can be found in the 'src' directory.

## Simulation

The project was tested and simulated using Proteus Design Suite. The simulation allowed for a comprehensive evaluation of the circuit and code behavior before deploying it on the hardware.

## Usage

1. Connect the hardware components according to the wiring instructions.
2. Power up the system.
3. The Stop Watch will start counting as soon as power is connected.
4. Use the external push buttons as follows:
   - INT0 (Falling Edge): Reset the Stop Watch time.
   - INT1 (Rising Edge): Pause the Stop Watch.
   - INT2 (Falling Edge): Resume the Stop Watch.
   - PB7 (Mode Control): Press to switch between countdown and countdown modes.
   - Use push buttons on PORTB for time adjustment.
5. If in countdown mode, when the time reaches zero, the buzzer alarm will sound.

## Contributing

Feel free to contribute to this project by submitting pull requests. If you have any suggestions, bug reports, or feature requests, please open an issue.

---

Please review the updated README to ensure it meets your requirements.
