## SECRET KNOCK DETECTING DOOR LOCK

### Problem Statement :-
* Designing a circuit that recognises a secret unique knock on the door to open the electrical door lock.

### Components required :-

* Arduino UNO.
* Piezo sensor/speaker (senses the vibration of the door).
* 2 LED's (Red and green to indicate the state of door lock).
* Small 12V DC Solenoid lock.
* Relay module
* 6-12V power battery (supplied to solenoid lock and arduino)
* Resistors (as per requirement)
* Jumper wires
* Thick sheet of cardboard (acts as the body of the door)

### Ideation : 

Knocking on the door => Vibration converted to electrical signals by __Piezo sensor__ => Signals sent to Arduino Microcntroller => Output signals sent to relay module => LED lights green on the correct knock pattern. 

* First of all, the whole circuit/system would be fitted on thick sheet of cardboard/wood with the help of screws or even cellotape can do the job. The piezo sensor would be tightly fitted onto the board so that it can sense the vibration.

* The Arduino can control the devices which runs on up to 5V so if we want to control the devices which runs on more than 5V(solenoid lock at 12V) or the A.C devices then we will have to use a __relay module__ through which we can control A.C as well as DC devices.

* Appropriate power connections of around 6-12V would be made to the Arduino and and Solenoid lock.

* The LED's (red and green) would act as an indicator for our locking mechanism. If the knock pattern is correct, the green LED would blinkand if its incorrect then the red LED would blink.

* __Programming Arduino__ - The coding part is, by far and large, the __most important aspect__ of this project. When the door is knocked, vibration is generated which is sensed by the piezo sensor. Depending upon the intensity of vibration, the piezo sensor would send a binary value to the Arduino microcontroller which could be extracted by __analogRead()__ function. The code has to take into account many factors such as the threshold value above which the vibration would be considered as a knock, relative time difference between two knocks, speed of the knocks, the accuracy of the knock, maximum amount of time to wait for the knock after which we consider it as finished etc. 

### Possible shortcomings - 
* In case of a power shortage from the battery or shortcircuit, the lock may get jammed and eventually unable to be opened.

* In order to reset the knock, certain part of the code needs to be reprogrammed which is quite tedious a task if we ne need to reset it on a regular basis.

### Proposed solutions - 

* There should be a way of opening the lock manually in a very rare case of a shortcircuit or power shortage (I have not found a proper solution on this but still working on it).

* A pushbutton can be introduced in our circuit. This pushbutton when pressed, a new knock pattern can be set and saved as soon as the pushbutton is released. This process is much easier than tampering with the code for every reset.

### Budget breakup - 

__COMPONENTS__ | __SOURCE__ | __AMOUNT__
---------------|------------|-----------
__Arduino UNO__ |[Robu.in](https://robu.in/product/arduino-uno-r3-ch340g-atmega328p-devlopment-board/?gclid=CjwKCAjw5cL2BRASEiwAENqAPm1363y6PHruwR4HZrCDOHBhFJybFAob8DRmG8mG2TuNo6A76F-weBoCHaMQAvD_BwE), [Amazon.in](https://www.amazon.in/Uno-ATmega328P-Compatible-ATMEGA16U2-Arduino/dp/B015C7SC5U/ref=sr_1_2?crid=CCF3GHU8HMD7&dchild=1&keywords=arduino+uno&qid=1590762741&sprefix=Arduino%2Caps%2C253&sr=8-2)| INR 300-350 (possible tax and delivery service included)
 __12V Solenoid Lock__ |[Amazon.in](https://www.amazon.in/Electronicspices-Electric-Assembly-Electronic-Container/dp/B084T32RWH/ref=sr_1_4?crid=3ALVDR8R5X8HX&dchild=1&keywords=solenoid+lock+12v&qid=1590762853&sprefix=Solenoid+lock%2Caps%2C271&sr=8-4)| INR 400-500
__Piezo sensor__ |[Amazon.in](https://www.amazon.in/Electronic-Ceramic-Elements-Sounder-Piezoelectric/dp/B084T3W148/ref=sr_1_4?dchild=1&keywords=piezo+sensor&qid=1590816005&sr=8-4)| INR 60-70
__Relay Module__ |[Amazon.in](https://www.amazon.in/REES52-5VRELAY-Channel-Arduino-Raspberry/dp/B01HXJDBII/ref=sr_1_1?crid=2AN95LXQS3X1T&dchild=1&keywords=relay+module+for+arduino+uno&qid=1590763629&sprefix=Relay+Module%2Caps%2C254&sr=8-1), [Robu.in](https://robu.in/product/1-channel-isolated-5v-relay-module-opto-coupler-for-arduino-pic-avr-dsp-arm/)| INR 100-150
__6-12V Battery__ |[Amazon.in](https://www.amazon.in/CREATOR-6F22-VOLTS-Power-Batteries/dp/B01N5AJ7JH/ref=sr_1_17?dchild=1&keywords=9V+battery&qid=1590814675&sr=8-17), [Robu.in](https://robu.in/product/9v-original-hw-high-quality-battery-5pcs/https://robu.in/product/9v-original-hw-high-quality-battery-5pcs/)| INR 100-150 (pack of 5 batteries)
__LED__ |Already available in plenty at home| INR 0
__Resistors__ |[Robu.in](https://robu.in/?category=&s=resistors&search_posttype=product) | INR 50-60 (A pack of 40 resistors of any specification)
__Jumper Wires__ |A pack of 35 wires already available at home| INR 0
__TOTAL__|| INR 1000-1100

    
