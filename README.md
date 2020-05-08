# Parking Lot Car Counter using IC4026

Searching for free parking places in urban traffic conditions is a serious mobility problem. A study provides results regarding the parking situation in Schwabing, a district of Munich, Germany. For this area, an annual total economical damage of 20 million Euros (about 25 million US dollars) has been estimated, caused only by the traffic searching for free parking lots. It would thus be a great benefit for the driver of a vehicle to have up-to-date knowledge on free parking places near the destination area.

With the increasing growth of automotive industry, the demand for intelligent parking service is expected to grow rapidly in the near future. This emerging service will provide automatic management of parking lots by accurate monitoring and making that information available to customers and facility administrators.

#### The counter will provide acurate count of the number of vehicles at entry and exit points of the parking lot. The facility administrator can use this information to avoid overcrowding and better operations.

# Background

## IC4026

![IC Pinout](https://circuitdigest.com/sites/default/files/inlineimages/IC-4026-Pinout.gif)

  4026 IC  is a 4000 series IC. It is a CMOS seven-segment counter IC and can be operated at very low power. It is a decade counter, counts in decimal digits (0-9). It is used to display numbers on seven segment displays and it increment the number by one, when a clock pulse is applied to its PIN 1. Means more the clock pulse rate, faster the numbers change in 7 segment Display.
  
  ## Seven Segement Display
  
  ![Seven Seg](https://components101.com/sites/default/files/component_pin/7-segment-display-pin-diagr_0.png)
  
  The seven segments displays are the oldest yet one of the efficient types of display used in embedded applications. This display has nothing more than 8 LED inside it. These 8 LEDs are separated into each segments which can be named as a,b,c,d,e,f,g,DP as shown in the picture above. These entire 8 segment LEDs have one end of their pins pulled out of the module as shown above and the other ends are connected together and pulled out as the Common pin. So to make an LED of a particular segment glow we just have to power common pin along with the segment pin. This way we can power more than one segment at a time to represent the numeric number 0-9 and also few Alphabets as shown on the graphic image below. We also have an option to show a decimal point using the DP pin.
  
  ![Working gif](https://components101.com/sites/default/files/inline-images/7-segments_display_working.gif)
  
  ### Truth Table for implemetation 
  
  ![table](https://electronicsforu.com/wp-contents/uploads/2016/04/5Z9_nov_44-1.png)
  
### Implementation  

- A light source and light sensor is used to detect the car and display it on the seven-segment display with the help of 4026 counter
- The light source and the light sensor placed in such a way that the car will cross the light path when he enters in to the parking lot.
 - The resistance of LDR decreases when intensity of light falling on it increases and vice versa (resistance increases when intensity of light falling on it decreases). We are utilizing this property of LDR to act as a sensor, since a varying voltage drop can be obtained with varying light.
  - The light beam from torch is continually hit on the LDR so the resistance of LDR is low and the voltage drop across LDR and ground is less than 0.6V
  - When a car passes through the light beams, light will not fall on the LDR so the resistance of LDR become high. In this circuit, amount of light is varying because of the obstruction from the car, there will be no light falling on the sensor. 
  - When the transistor is ON, the potential at collector becomes LOW and when the transistor become OFF, the potential at collector will be HIGH.
- As soon as the car crosses the light beam, a LOW and HIGH voltage transition occurs at the collector.
- This transition is fed to the clock of IC 4026, and, it will start count with the clock and display on seven-segment display. 
- IC 4026 will increment the count when each car enters in to the parking lot. It is a combined counter and display driver IC which is designed to drive 7 segment display.
  
>I've uploaded the circuit diagram, feel free to 
  >reach out to me if you've any questions. I've also uploaded
  > Proteus simulation files, so you can have a better understanding
  >of the project.
  
### Hers's a screen grab from my simulations.
  
![monitorSim](https://github.com/aniket1499/decadeCountIC4026/blob/master/screenGrab.png?raw=true)
  
You'll find a high quality version [here.](https://github.com/aniket1499/decadeCountIC4026/blob/master/counterSim.bmp) 
