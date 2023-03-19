# Small-demonstration-of-smart-house
![image](https://user-images.githubusercontent.com/72800099/226204231-a6c669b9-d6dc-4f43-a560-08d24ec828a7.png)

EXPLANATION
It has some sensors to measure rain, fire and light using Stm32l073RZT6 board.
Operational procedure of the circuit is as follows:
-When there is no water(rain) coming to the water level sensor, only green LED 
is on and if there is light outside(LDR is used) buzzer is on with the green LED.
-When there is some water but not fully raining,only yellow LED is ON. (Flame 
and LDR sensors dont effect this phase since it is not a common phase and water 
level sensor is not that sensitive. So, mostly red or green LEDs are on.)
-When there is decent amount of water on the sensor, only red LED is on. And if 
the fire sensor is sensing some flame, buzzer is on with the red LED.


DESIGN
In design phase of my circuit, since I didnt take a circuit from internet and put it 
to the breadboard I had to design a circuit which I could test and implement the 
sensors I have to the IOC concept. Firstly my plan was to create a simple water 
level sensor controlled LEDs and buzzer so they can give a response to the
sensor(rain).Water Level Sensor has three connections: +(DC input) –(GND) 
and S(Analog Out). Thus, I had to use ADC module in my microprocessor. I 
used a video for potantiometer as a reference since they both give analog input 
to the board. Then I decided to make use of LDR and Flame sensors which was 
logical to use since this is a IOC project. LDR and Flame sensors give digital 
output so it was simpler to implement to the circuit. I wrote a few if statements 
and used these buttons as a way to create a buzzer alarm.

![image](https://user-images.githubusercontent.com/72800099/226204462-d69fba69-724f-44a3-8492-a30f54ce65d6.png)

IOC Pin Layout of the Stm board

In my circuit I used;

*1 mini / 1 standard breadboard

*1 Water level sensor

*1 Flame Sensor

*1 LDR Sensor

*3 LEDs

*1 Buzzer

*3 220Ω Resistors

*Male-Male Jumper Cables

*Stm32L073RZT6 Nucleo-64 Board

![image](https://user-images.githubusercontent.com/72800099/226204317-ab5cc3ac-5dcc-4a02-8c33-de29a201a6f9.png)

Settings of my ADC module(I only changed Continuous Conversion Mode to On)



