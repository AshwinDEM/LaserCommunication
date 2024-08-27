# Laser Communication Project

## Overview

This project demonstrates a simple laser communication system using two Arduino boards (Uno and Nano) and two laser diodes. The system transmits messages from one Arduino to another using laser light.

## Components

- 1 x Arduino Uno
- 1 x Arduino Nano
- 2 x Laser Diodes
- 2 x Photodiodes or Solar Panels
- Breadboard and Jumper Wires

## Setup

### Transmitter (Arduino Uno)

1. Connect the laser diode to pin 4 of the Arduino Uno.
2. Connect the ground of the laser diode to the ground of the Arduino Uno.
3. Upload the `Transmitter.ino` code to the Arduino Uno.

### Receiver (Arduino Nano)

1. Connect the photodiode to an analog input pin of the Arduino Nano.
2. Connect the ground of the photodiode to the ground of the Arduino Nano.
3. Upload the `Receiver.ino` code to the Arduino Nano.

## Code Explanation

### Transmitter Code (`Transmitter.ino`)

The transmitter code reads a message from the serial input, converts it to binary, and transmits it using the laser diode.

#### Key Functions

- `setup()`: Initializes the laser pin as an output and starts the serial communication at 9600 baud.
- `loop()`: Waits for a message from the serial input, converts the message to binary, and transmits it using the laser diode.

### Receiver Code (`Receiver.ino`)

The receiver code reads the binary data from the photodiode, converts it back to a string, and prints the received message to the serial monitor.

#### Key Functions

- `setup()`: Initializes the photodiode pin as an input and starts the serial communication at 9600 baud.
- `loop()`: Reads the binary data from the photodiode, converts it back to a string, and prints the received message to the serial monitor.

## Usage

1. Open the Serial Monitor for both the transmitter and receiver Arduino boards.
2. Type a message in the Serial Monitor of the transmitter Arduino and send it.
3. The message will be transmitted via the laser diode and received by the photodiode.
4. The received message will be displayed in the Serial Monitor of the receiver Arduino.

## Notes

- Ensure that the laser diode and photodiode are properly aligned for optimal communication.
- Adjust the baud rate if necessary to match the communication speed of your setup.

## Future Improvements

- Implement error checking and correction mechanisms.
- Increase the range and reliability of the communication system.
- Add encryption for secure communication.
