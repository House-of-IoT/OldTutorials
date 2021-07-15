
# Warning 

Please proceed with caution when dealing with eletrical components. This is NOT software, you can cause harm to you , your property and others.

# General

Note : I recommend soldering things with this type of project, but you could hack around soldering.
After following this tutorial you will have a fully functioning smart device that will notify you if your door is open.
You could monitor multiple doors with this smart device , but for this tutorial we will stick with one.

## Hardware

1. You would need to connect the wires to the reed switch like shown in the diagram below with the resistor apart of the circuit.

<img src = "https://github.com/House-of-IoT/DoorMonitor/blob/master/reedswitch.jpg" />


## Software

### Basic overview
1. You will need to download the latest version of python3.
2. You will need to download the latest version of pip.
3. you will need to install the dependencies in requirements.txt with pip.
4. you will need to a config.json to be setup properly.
5. your all set!! to run `python3 main.py`

### In Depth
The software for the door monitor requires a few things in order to run properly. This project requires you to have a config.json file that contains the credentials for connecting to your server(not the password). All smart devices have a config.py script that you can use to manually generate one of these files. You would clone the repository and run `python config.py` and enter the information. After you will be prompted with sensitive information that you need to connect to the server, like the password.

1. You will use the requirements.txt file to install all of the required dependencies for the project. You will navigate to the directory that have the file  `requirements.txt`.
2. You will run ` pip install -r requirements.txt --no-index --find-links file:///tmp/packages`
3. You will navigate to the directory that has the config.py file in it and run `python3 config.py` and enter the information that is asked for. It will ask for things like the host and port of the server you are trying to connect to.
4. You will run  `python3 main.py` and you will be asked for the password for the server as the last requirement to connect to your server. Keep in mind that you do not have to repeat any of the above steps when trying to connect the device again to the server. You will only need to run   `python3 main.py` assuming you didn't remove any dependencies or the `config.json` file.
