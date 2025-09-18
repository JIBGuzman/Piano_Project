# Digital Piano Project

## Overview
This project implements a digital piano and music box using the TM4C123GXL microcontroller. It combines hardware interfacing and software programming to create an interactive musical device capable of both real-time playing and automated song playback.

## Features
- **Dual Modes:**
  - **Piano Mode:** Play individual notes using push buttons representing piano keys.
  - **Auto-Play Mode:** Automatically plays pre-programmed songs.
- Multiple octaves supported, with LED indicators showing the current octave.
- User controls through onboard switches for mode selection, octave changes, and song cycling.
- Sound generation via a 6-bit R2R DAC and a 64-sample sinusoidal wave lookup table.
- Interrupt-driven design for responsive button handling and precise tone generation using SysTick timer.

## Hardware Components
- TM4C123GXL LaunchPad microcontroller
- 7 push buttons assigned to piano keys C, D, E, F, G, A, B (GPIO PD0-PD3, PD6, PD7, PA7)
- 2 onboard switches for mode toggling and octave/song control (Port F pins)
- 6-bit R2R Digital-to-Analog Converter on Port B (PB0-PB5)
- LEDs on Port C (PC4, PC5, PC6) to indicate octave

## Software Implementation
- Interrupts handle button presses and switch inputs for responsive control.
- SysTick timer generates interrupts at frequencies corresponding to musical notes.
- Multiple octaves implemented by cycling frequencies via lookup tables.
- Auto-Play Mode cycles through four songs:  
  - Happy Birthday  
  - Mary Had a Little Lamb  
  - Twinkle Twinkle Little Star  
  - Old MacDonald Had a Farm  
- Mode and octave/song selection via onboard switches with instant feedback.

## Usage Instructions
1. The system starts in Piano Mode by default.
2. Use push buttons to play notes assigned to piano keys.
3. Press Switch 2 to cycle through octaves (lower C, middle C, upper C). The LEDs indicate the current octave.
4. Press Switch 1 to toggle between Piano Mode and Auto-Play Mode.
5. In Auto-Play Mode, Switch 2 cycles through the available songs.
6. Switching back to Piano Mode stops the song playback.

## Challenges and Learning
- Managing continuous interrupt-driven sound generation while handling button input.
- Correct frequency calculation and lookup for accurate note production.
- Debugging persistent playback issues related to timer and DAC operation.
- Integrating hardware and software effectively for low-latency, real-time interaction.

## Contributors
- Jonathan Cerniaz
- Joseph Guzman
- Afzal Hakim
- Robby Rimal

## Additional Resources
- Video Demo Part 1: [Delay and UART Tests](https://www.youtube.com/watch?v=vM_ZWoqO4cc)
- Video Demo Part 2: [I2C Test](https://www.youtube.com/watch?v=L3Zt2sT_ms0&list=LL)
- Video Demo Part 3: [Color Sensor Test](https://www.youtube.com/watch?v=uP8757Ir24M)
- Video Demo Part 4: [Gyroscope Test](https://www.youtube.com/watch?v=wUv1AqBdJyE)
- Video Demo Part 5: [Servo Test](https://www.youtube.com/watch?v=wHUlNNXiDM0)
- Video Demo Part 6: [LCD Test](https://youtu.be/GPVm0zbWn10?si=2Yl-lmT-MDjyQyzq)
- Video Demo Part 7: [Full System Test](https://youtu.be/tVYpw0OcfmA)


