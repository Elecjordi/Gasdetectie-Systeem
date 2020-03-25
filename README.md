Gas detection system

I made a gas detection system for the industry with various controls. I did this using a microcontroller and as a sensor I used a gas sensor. The microcontroller I used is ESP32 and the gas sensor is an XNX Honeywell transmitter with LEL sensor. The purpose of the gas detection system is when gas is measured, this gives different actions.
First one has a pre-alarm where a flashing light is controlled. The green led that indicates 'everything okay' goes out and the red led of pre-alarm goes on. At the same time we monitor the readout on the Oled and on the Blynk app. The display also changes from ok to pre-alarm.
The fan is controlled at 50%. The fan is switched to a switching stage of 12V via the BC548C transistor. The base of the transistor is switched via a PWM pin, we call this pulse with modulation. The value is shown on a second display.  
If the value of the gas continues to increase, one reaches 50% LEL at the main alarm. At the main alarm a flashing light and a siren are activated. This is both done with the BC548C transistor with a switching stage of 12V.
The red led of the pre-alarm goes over to the red led of the main alarm. This also happens on the display and the Blynk app. Also appears on the display the message main alarm. The fan is controlled to 100%. This is also made visible on the 2nd display.  
When something goes wrong with the meter it goes to a value of 2mA. For this an orange LED will light up and on the display and Blynk the message meter goes wrong. On the Blynk app I also made a bar graph which increases with the measured value.
All data can be seen on the system itself, on the created displays and on the Blynk app.
Created by Jordi De Greef  
