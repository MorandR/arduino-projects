
# Lamp "Clapper" Project

## Utilizing Decibel level

### Description
Arduino Project which takes in signal from user or source and transmit the dB levels received to turn on and turn off light.
Like the established “The Clapper”, this experiment will reflex from a given sound and pattern. When the user claps twice, the light will either turn on or off.

### Introduction
This project was inspired from a college student’s perspective. After hours of lectures, study sessions and being away from the dorm, we are drained by the end of day and still have to research or review assignments. During moments of late night studying we are sometimes far from the lights and tend to fall asleep; at least I do at times... 👀. This project is the solution to simply our life by "vocally" triggering the lights without getting out of our comfty bed. 

### Materials

- Lamp with a power plug
- Arduino Uno R3 Board 
- Sound Sensor Module 
- Relay Mondule
- BreadBoard
- 9V Battery
- 9V Battery Clip
- Dupont Wires <br/>
- Developers Tool: Arduino IDE 1.8.19

<!--Links and Price for materials-->
<!--Arduino: $26.79
 https://www.amazon.com/dp/B008GRTSV6?psc=1&ref=ppx_yo2ov_dt_b_product_details -->
<!--Sound Sensor Modules: $6.29
  https://www.amazon.com/dp/B00XT0PH10?psc=1&ref=ppx_yo2ov_dt_b_product_details-->
<!--Relay Module: $5.50
 https://www.amazon.com/dp/B00VRUAHLE?psc=1&ref=ppx_yo2ov_dt_b_product_details -->
<!--BreadBoards: $10.99
 https://www.amazon.com/dp/B09YN9PVY2?psc=1&ref=ppx_yo2ov_dt_b_product_details-->
<!--9V Battery Clips: $5.99
 https://www.amazon.com/dp/B01AXIEDX8?psc=1&ref=ppx_yo2ov_dt_b_product_details -->
<!--Dupont Wires: $6.98
 https://www.amazon.com/dp/B01EV70C78?ref=ppx_yo2ov_dt_b_product_details&th=1-->
<!-- -->

[//]: # (This is a comment)

[comment]: <> (comment)

 <img  alt='lamp.gif' src="./visuals/lamp_clapper_visual2.gif" width="168" height="275"/>
  
Identify the positive wire (usually copper) on the lamp’s cord:  <br/>
The lamp’s plug has two blades of different widths. <br/>
The widest blade is known as the neutral blade as the narrow blade is known as the hot blade.  <br/>
The hot blade is connected to the positive wire  <br/>
The neutral blade is connected to the neutral wire  <br/>

 <img  alt='plug_label' src="./visuals/plug_label.png" width="275" height="152"/>

#### Electrical Wiring Instructions:

Cut the wire corresponding to the hot blade <br/>
Cut off the polar wire  to reveal only the copper. <br/>
Relay Module (terminal side): <br/>
Insert the plug-sided wire in the NO input <br/>
Insert the lamp-sided wire in the COM input (middle) <br/><br/>

<img  alt='relay_pinout' src="./visuals/relay_pinout.png" width="275" height="136"/>

#### <ins> Relay pins to Arduino </ins> <br/>
Connect Relay Ground (-) pin to Arduino Ground pin <br/>
Connect Relay 5V VCC  (+) pin to Arduino 5V power <br/>
Connect Relay Input Signal (S) pin to Arduino’s Digital socket (between 2 and 13 ONLY) <br/>

#### <ins> Sound sensor pins to Arduino </ins> <br/>
Connect Sensor output (OUT) pin to Arduino’s Digital socket (between 2 and 13 ONLY) <br/>
Connect Sensor Ground (GND) pin to Arduino Ground pin <br/>
Connect Senor VCC pin to the Adruino 5V Power <br/>

You may now begin the fun!

Comments are displayed in the code itself. Click [here](./lamp_clapper.ino) to view the code and comments.

### Glossary

COM – Common terminal <br/>
GND (Ground) – the reference point for all signals or a common path in an electrical circuit where all of the voltages can be measured from. <br/>
NC (Normally Closed terminal)  – keep the Relay closed so no circuit flows through, unless a signal is sent to open and stop the circuit. <br/>
NO (Normally Open terminal) – allows circuit to come through automatically unless a signal is sent to close the circuit. <br/>
VCC (Voltage Common Collector) – the higher voltage with respect to GND (ground). <br/>


### Conclusion and Discoveries

While trying to tune the sound sensor to pick up certain levels, the range seen was 33dB - 1023dB. This must've been a very sensitive sensor, but was still able to get the job done. Also, being that the sound sensor can only receive sound measured in dB, we would have to look into other supplies that would allow us to use and pick up certain frequencies to activate the light or maybe another project! <br/>
To capture the claps, I've used a variable to measure the time difference and activate the relay switch if the difference is within a fixed range.

### References

Plug labels - https://www.boulderufixitclinic.org/lamp-repair <br/>
Knowledge - https://randomnerdtutorials.com/guide-for-relay-module-with-arduino/




