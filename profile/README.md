# Sphinx 2022

This is the project done for the [NOI Hackathon in Schenna - 2022](https://hackathon.bz.it/), precisely for the **FOS Group's challenge**.

## The challenge 

The challenge consisted in developing embedded software that supported low-energy bluetooth communication, with the challenge, not so relevant, example of sending photos sent by an ESP32.

## A bit of history

After having decided an approach to follow for the Lifeware's challenge, consisting in using machine learning (regression algs.) to determine an equation from input / outputs. Because the team did not have huge experience with AI, after some attempts the team decided to pass to the FOS challenge. Even if some aspects could not be faced in detail due to the reduced amount of time, a prototype with a simple behaviour has been developed.

## The software

The repos of the software are: 
- [**esp32-high-level**](https://github.com/Sphinx2022/esp32-high-level): It contains the ESP32 code used for the working prototype, that was high-level and not so focused in sparing energy.
- [**esp32-optimized-entwurf**](https://github.com/Sphinx2022): It contains the ESP32 code regarding the draft, the prototype the could have been delivered with more time and that uses BLE.
- [**sphinx-app**](https://github.com/Sphinx2022/sphinx-app): A simple app developed with **Flutter**, by using a template since the frontend was not considered important.

## The high-level prototype

The high level prototype uses normal bluetooth and sends the taken photos to a connected client. A draft that is focused on low energy consumption but that sends just increasingly numbers and works with another ESP32 as client. The draft uses callbacks to detect if no user is connected and potentially adapt its behaviour in base of that. This would also make it easier to use deep sleep (that would be in any case used for the sleep between different photos.

## How to use it

Both the repos are based on Arduino IDE and the standard tools to interact with an ESP32 with camera. The only lib, used for the high-level one is BluetoothSerial.
