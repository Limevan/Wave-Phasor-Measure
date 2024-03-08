# Wave-Phasor-Measure
Uses the EFM8 microcontroller to read the Vrms and phase difference (in degrees) of a wave generated using a wave function generator.

This project implements a simple peak detector and a zero cross, for a test wave and a reference wave. 

<h3>Functionality</h3>
The peak detector measures the peak voltage for a sinusoidal wave and sends the voltage through a pin on the EFM8 microcontroller using an ADC input. 

The zero cross detector converts the sinusoidal curve into a square wave indicating when the wave is positive and negative. The output is sent through pins on the microcontroller to read when the wave is positive (1) or negative (0). Phase difference is calculated using built-in timers, timed between the positive portion of the test wave and reference wave.

The peak voltage is converted to rms, and displayed on a 16x2 LCD display with the phase difference. The values are also sent through serial port.

<h2> Running the Program </h2>
The main program is located in the EFM8_ADC.c file, can also test other programs:
    <li>PeriodEFM8.c</li>
    <li>PhaseDifference.c</li>

The file can be opened on CrossIDE, and flashed to the EFM8 board.

<h2>Credit</h2>
This project was built off of example code and information provided by Dr. Jesus Calvino-Fraga.
