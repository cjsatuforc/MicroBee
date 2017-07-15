# MicroBee
MicroBee -- A micro quad-rotor helicopter based flying sniffer robot. It is equipped with three MOX sensors, a CC3D Atom board (flight controller), an ATTiny85 micro-controller, and four brushed motors.

The flight control (FC) routine is written based on the CleanFlight version 1.12.1. The FC is modified to provide 3 Analog channels on the CC3D Atom board, and the I/O pins of the board has been fully utilized. In the main loop of FC, the ADC values of three analog channels are transmitted via UART1 port using MicroBee serial protocol at 25 Hz. The UART1 port is connected to a transparent serial wireless module, so MicroBee sends ADC values to the ground station every 40 ms.

The ATTiny85 mc is used to monitor the voltage of the Lipo 1S battery. A micro DC-DC converter is used to level up the voltage of the battery to 5 V. The voltage value is transmitted to the FC via UART2.

The movement of the MicroBee is controlled via a PPM encoder, the position of the microbee is measured by the Opti-Track Motion Capture system.
