# Infared motion detector
 Simple smart device that senses body heat movement and sends alert to the GeneralSever.
# General
This device aims to send alerts whenever it senses body heat from an unknown source. This device can be placed anywhere with the proper insulation/setup.
This device uses Passive Infared Sensors(PIR sensors) as the primary sensing functionality, this project could be combined with many other features to create
awesome devices.

## Hardware

1.You will need 1xRaspberry Pi 4.

2.You will need 2xPIR Sensors.

3.You will need Female to Female dupont jumper wires.

You will need to connect both of the power pins of the pir sensors to the two constant 5v pins on the raspberry pi, the power pin of the pir sensor is the one connected to the  blue wire in the below picture. You will need to connect both of the ground pir pins to available ground pins on the raspberry pi(the one in the picture below is connected to the purple wire). You will need to connect both output pins to the pin 23(GPIO) and pin 24(GPIO) of the raspberry pi(the one in the picture below is red). 

<img src = "https://github.com/House-of-IoT/InfaredMotionDetector/blob/master/pir_wiring.png"/>


##  Software

### Basic overview

1. You will need the latest version of Rust
2. You will need the latest version of python to use the config generator.
3. You will need to generate a `config.json` file.
4. You will need to build and run the project with `cargo install` followed by `cargo run`.
5. You are all set!!

### In-depth

The software for the Infared Motion Detector requires a few things in order to run properly. This project requires you to have a `config.json` file that contains the credentials for connecting to your server(not the password). All smart devices have a config.py script that you can use to manually generate one of these files. You would clone the repository and run `python config.py` and enter the information. After you will be prompted with sensitive information that you need to connect to the server, like the password.

1. You will need to build and run the project with `cargo install` followed by `cargo run`.
2. You will need to enter the password to the server.
3. You are all set to install the device.
