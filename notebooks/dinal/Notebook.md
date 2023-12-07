<h3>09/14/23 - Proposal Due</h3>
Submitted proposal, discussed design with machine shop, and finished the team contract.

<h3>09/19/23 - Redesigned System</h3>
The rail system we had originally proposed was impractical, so we had to come up with new ways to turn the stove knob.
We have narrowed it down to a new design; using a linear and a rotary actuator to manipulate the knob.

<h3>09/22/23 - Finalized Design</h3>
We have finalized our design with the machine shop. We have decided to use a stepper motor, servo motor, pulley system, and a rotary encoder
to keep track of the position of the stove knob at all times, as well as allow the user to adjust the setting of the stove either manually
or remotely.

<h3>09/26/23 - Design Document work</h3>
Worked on design document, specifically the ethics and safety, power subsystem, pulley subsystem, physical design, and problem and solution.

<h3>10/02/23 - Design Review and starting PCB design</h3>
At the design document review, we were approached with an additional feature to include a timer to automatically turn the stove off.
We also began finalizing the parts we would use for the final design, and went to the machine shop and ECEB shop to gather parts.

<h3>10/06/23 - PCB Review</h3>
Attended PCB review session and got some feedback on our schematic. We realized we need to research more about our speficic components
so that we could find valid footprints to use. We also need to research the USB to UART bridge so that we can effectively send and receive
data from our microcontroller.

<h3>10/11/23 - First Round of PCB Orders</h3>
We were not able to submit the files for the first round of PCB orders, as we could not pass the audit on pcbway due to our footprints
not being completely correct. We decided to begin using easyEDA to design our schematic and layour for our PCB since it is better lined up
for the components and footprints we are trying to use. We also finished the teamwork evaluation form.

<h3>10/13/23 - Finalized Design with Machine shop</h3>
We finalized the design with the machine shop and provided them with all of the components that would be going into our mechanical design.

<h3>10/17/23 - Second Round of PCB Orders</h3>
We were unable to complete the design by the second round of orders due to issues with the stepper motor driver datasheet.

<h3>10/19/23 - Finished PCB layout</h3>
We have completed our PCB schematic and layout and have passed the audit on pcbway, we plan our ordering the PCB before the third round.
We have also finished the front-end design for our application and have started to look into communication between a back-end mySQL server
and the ESP32 microcontroller.

<h3>10/22/23 - App Schematics & Individual Progress Reprot</h3>
We have placed the order for out PCB and expect to receive it by the end of October. Meanwhile we are continuing to work on setting up the App and our backend server. Nikil and I are working on setting up the backend and the communication between the ESP32 module and the App and vice versa via both websocket and http communication protocols. Throughout the week I also completed the Individual Progress Report assignment.

<h3>10/25/23 - Front-End of App is Finished</h3>
We have finished the front end of our application and have continued to set up communications with the backend while waiting for the PCB to arrive.

Front End Design: (https://github.com/nikilnambiar7/Smart-Stove-System/blob/main/notebooks/dinal/frontEnd.PNG)

<h3>10/31/23 - Assembling the PCB</h3>
The PCB arrived this week so we have begun soldering components onto board. Since none of us have that much experience soldering it is taking sometime. We also realized that we are missing some components needed for our sensors to be properly connected. We have ordered these and they should be coming within the next 2 days. Furthermore, we are continuing to work on the App and also are exploring breadboarding with the devboard.

<h3>11/5/23 - PCB Assembly Complete</h3>
We have finished soldering PCB. Looking to test it soon.

<h3>11/6/23 - Working with Servo motor & Finished backend</h3>
Nikil and I tested out the Servo motor on our finished project with our PCB, which worked with a few issues. We will debug these issues tomorrow. We were also running into a "cannot find port" error when it came to trying to upload code to our ESP32 MCU. On the other side of things the backend is looking good. We were able to set up an API endpoint at our backend and GET the information from our backend with our App. Now all we have to do is work on posting data and the functionality of the App will be complete.

<h3>11/8/23 - Front-End & Back-End fully integrated</h3>
Completed the Front End of our application and integrated it with our backend server. This means that any data that we want to send and receive from our application to our server is possible and complete. Looking next to set up bidirectional communication between server and MCU. Additionally, looking to test out servo, rotary encoder, and LM35.

toApp Table: (https://github.com/nikilnambiar7/Smart-Stove-System/blob/main/notebooks/dinal/toApp.PNG)

fromApp Table: (https://github.com/nikilnambiar7/Smart-Stove-System/blob/main/notebooks/dinal/fromApp.PNG)

<h3>11/9/23 - Tested Servo and LM35 with PCB</h3>
We finished soldering the new components to our breadboard and began trying to upload code to it. We ran into some complications with the port not being read correctly again, but we were quickly able to remedy this error by downloading a few external libraries and modules. We then tested out PCB with our Servo motor and LM35. The LM35 was giving junk data at first, but we were able to use a different library which was able to output very reasonable data. The servo motor worked flawlessy and is able to tension our pulley as expected.

<h3>11/10/23 - Getting LM35 Data to our Back-End</h3>
We were able to send the data from our LM35 temperature sensor to our back-end server via websocket connections to the ESP32 microcontroller. This data is being sent on a loop currently and will be used to write some logic later this week.

LM35 Data: (https://github.com/nikilnambiar7/Smart-Stove-System/blob/main/notebooks/dinal/lm35.PNG)

<h3>11/11/23 - Everything working as expected except Stepper Motor and Rotary Encoder</h3>
The two components that aren't working as expected are the stepper motor and rotary encoder. The rotary encoder appears to be outputting junk data. We have got a replacement one that should be arriving soon, which we are hoping will have useful data. We have been following proper procedures from the datasheet and online tutorials regarding how to test it, but it seems to be too sensitive and cannot differentiate between clockwise and counterclockwise. Regarding the stepper motor we have followed the wiring schematic provided by multiple datasheets and nothing seems to get the motor to fully turn. So far all we are able to do is hear a slight jolt when we provide the PCB power. This at least means that the motor is receiving some amoutn of power.

<h3>11/12/23 - Debugging Issues from yesterday</h3>
Stepper motor still not working as expected. Voltage at driver is at expected 10V indiciating the boost module is working. The replacement rotary encoder came in today so we plan on testing this in a couple days in office hours to also get help with the stepper motor. 

<h3>11/13/23 - Setting up bidirectional communication between ESP32 and back-end server</h3>
We worked on setting up bidrectional communication between the MCU and server. Used GETs to receive data from Server on the MCU and POSTs to relay data from MCU to server. This took some time to write up, but worked as expected. With this feature working, we will be able to send sensor data to our server and also receive input data from the user via the app. Next step is finishing up the logic between these two endpoints.

<h3>11/14/23 - Office Hours for Motor</h3>
We were not able to make the stepper motor work with the help of office hours, but now we believe that the issue is that we need more power, which either means increase voltage at the driver or we need more current to drive through the motor. Unfortunately, the new rotary encoder is also providing data that can't be used to track the position of the stove knob accurately. It is only tracking movement in one direction and when we stop rotating the knob the data continues to indicate the knob is turning. Everything is wired correctly according to the datasheets for this product yet it is not functioning as expected. We are discussing next steps and how to proceed without the use of the rotary encoder.

<h3>11/15/23 - Finished logic with servo motor and app</h3>
We have decided shift our focus on setting up full end to end logic with LM35, Servo motor, ESP32, Server, and App. Wanted to ensure that we could we get it closest to what we envisioned our project would look like with the rotary encoder and stepper motors working. Once the rest of the components of the project are working as expected we will revisit the issues with the encoder and motor.

<h3>11/16/23 - Finding different solutions for WiFi issue</h3>
The IllinoisNet WiFi network has an additional layer of security as it requires a username and password to log onto. We looked for alternatives and decided to use a phone hotspot. This works slower, but still gets the job done. We can expect there to be slight delays with communication between our MCU and server due to this weaker connection.

<h3>11/28/23 - Final Demo</h3>
Completed the Final Demo with everything we had planned to work. Complications with the encoder and motor prevented 100% functionality.

<h3>11/30/23 - Mock Presentation</h3>
Set up slides for mock presentation and delivered mock presentation. Received feedback to add more pictures about our project and to explain how the end to end should look like.

<h3>12/5/23 - Final Presentation</h3>
Completed final presentation.

<h3>12/6/23 - Final Paper</h3>
Completed final paper and submitted.
