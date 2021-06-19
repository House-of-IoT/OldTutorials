
# General

After following the below instructions you will have a fully functioning RC car with audio/video streaming that has cloud functionality and can be controlled via HOI-Web/Mobile.

## Hardware


1. First you would need to get two Dc motors , one to control the front wheel direction and one to control the movement of the rear wheels. It may seem like too much to buy all the individual parts to assemble an rc car , so I instead bought a simple RC car from walgreens and stripped the plastic body off of it. After stripping the plastic body off of the toy car , I had a full skeleton of an RC that has the wires to the motors in a easy to modifiy position. Here is one similar to the one I had : http://www.newbright.com/products/rc-truck-assortment-4-door-jeep-3/
2. You would need to connect the DC motors to a motor driver(L298n motor driver) like in the below picture. 
Why You may ask? The raspberry pi gpio pins `can not` safely output the amout of voltage needed to run a DC motor ,so we are using a Motor driver with an external power supply.
<img src = "https://github.com/House-of-IoT/Ralph/blob/master/L298N-Pinout.png"/>
3. You would need to connect your 12v power supply to the above motor driver. The positive wire should connect to the port that says "Motor VCC 5V-35V" and the negative wire should connect to the port that says "Ground".
