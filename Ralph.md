


##Warning
Please proceed with caution when dealing with eletrical components. This is NOT software, you can cause harm to you , your property and others.


# General

After following the below instructions you will have a fully functioning RC car with audio/video streaming that has cloud functionality and can be controlled via HOI-Web/Mobile.

YOU WILL NOT NEED TO DO ANY SOLDERING TO SUCCESSFULLY COMPLETE THIS PROJECT!

## Hardware

1. First you would need to get two Dc motors , one to control the front wheel direction and one to control the movement of the rear wheels. It may seem like too much to buy all the individual parts to assemble an rc car , so I instead bought a simple RC car from walgreens and stripped the plastic body off of it. After stripping the plastic body off of the toy car , I had a full skeleton of an RC that has the wires to the motors in a easy to modifiy position. Here is one similar to the one I had : http://www.newbright.com/products/rc-truck-assortment-4-door-jeep-3/
2. You would need to connect the DC motors to a motor driver(L298n motor driver) like in the below picture. 
Why You may ask? The raspberry pi gpio pins `can not` safely output the amout of voltage needed to run a DC motor ,so we are using a Motor driver with an external power supply.

<img src = "https://github.com/House-of-IoT/Ralph/blob/master/L298N-Pinout.png"/>

3. You would need to connect your 12v power supply to the above motor driver. The positive wire should connect to the port that says "Motor VCC 5V-35V" and the negative wire(one ground from your pi and one the ground from your power supply should both be in this port) should connect to the port that says "Ground". These ports have screws that you would need to loosen , then you will place an exposed portion of your wire into the port and then tighten it which will give you a solid connection. 
4. Next there are ports at the bottom labeled IN1 , IN2, IN3, IN4(the other pins on the edge are for controlling the speed of the motors but for this tutorial we will only focus on a general static speed with the 4 pins listed).These 4 pins control 2 motors, each motor have two corresponding pins. One of these two pins control the forward movement , one control the backwards movement. These pins are only on when they have power flowing through them , which will be when you set the value of a gpio pin to 1.
5. You will need to connect the Female to Female dupont jumper [wires](https://www.amazon.com/GenBasic-Piece-Female-Jumper-Wires/dp/B077NH83CJ/ref=asc_df_B077NH83CJ/?tag=hyprod-20&linkCode=df0&hvadid=309750549985&hvpos=&hvnetw=g&hvrand=6244468396297283499&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9021724&hvtargid=pla-567322001486&psc=1) to the motor driver pins and the raspberry pi GPIO pins that you will use to control it.

## Software
