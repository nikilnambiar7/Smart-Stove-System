
<h3>09/14/23 - Initial Project Proposal Due</h3>
Completed project proposal. Discussed initial design implementations with machine shop. Ran into some issues regarding the rail system and turning the knob. Completed team contract and assigned general roles for who will be completing what part

<h3>09/19/23 - Further Redesigned System</h3>
Original rail system design was flawed due to not having a solid disengaging system. The problem was that there would be no way to for the user to turn the knob since the motors would be connected to the knob preventing manual rotation. After further discussion we came up with a new design idea which was making use of a linear and rotational actuator. 

<h3>09/22/23 - Finalized Project Design</h3>
After heading into the machine shop and having further discussion we were able to finalize the design. The primary changes we made was having two motors. One for engaging the pulley system (tensioner) and the other to drive the pulley subsystem. Additionally, we decided to use a rotary encoder to track position. 

<h3>09/26/23 - Design Document </h3>
For the past two days I have been working on the design document. My primary parts was dealing with setting up the microcontroller schematics and coming up finishing the subsystem requirement and verification tables for the subsystem. Additionally, I was responsible for the sensory and motor subsystems. This involved reading the datasheets and understanding how these sensors worked so that we can easily incorporate them into our project. 

<h3>10/02/23 - Design Review </h3>
At the design doc review I realized we needed to understand our project more in-depth. Especially when it came to power ratings and exactly what features we want to include and how these would be included. Additionally, one of the TAs brought up a great suggestion in that we should include a timing feature where if the user sets a time limit on the app the stove will manually turn off after the timer runs out. Additionally, we finalized the parts that we will be using and asked at ECEB shop for said parts. 

<h3>10/06/23 - PCB Review Session</h3>
When we attended the PCB review session we realized there was a lot more that we had to do. Understanding how to properly assign footprints really confused us as we didn’t really know if the footprints we were selecting would be valid or not. Additionally, there were some additionally components that we realized we needed. This includes a USB to UART bridge that would be used to program our microcontroller. 

<h3>10/11/23 - First Round of PCB Orders</h3>
We weren’t able to make the first round of PCB orders as we can not pass both the audit on PCBway and the DRC check. After realizing that many of the footprints we want for our parts weren’t available on KiCad, we looked towards other alternatives. We stumbled upon EasyEDA which we found easier to use and also to have a wider variety of part selections. Additionally, we completed the teamwork evaluation form. 

<h3>10/13/23 - Finalized Design with Machine shop</h3>
Continued to work on PCB design. I am in charge of the microcontroller unit but am also helping out with other systems. Additionally, we gave our parts to the machine shop and finalized our design. 

<h3>10/17/23 - Second Round of PCB Orders</h3>
Continued to work on PCB design. As a group we are really struggling with setting up the stepper motor driver and following the data sheet. Additionally, organizing the PCB and preventing silk screen crossover is really hard. We are thinking about just submitting our PCB order without trying to clean up the silk layer as that should have no impact on the PCB’s functionality

<h3>10/19/23 - PCB layout and front-end design</h3>
After passing the PCBway audit and finishing our PCB layout and schematic, we intend to order the PCB before the third round.
Additionally, we have completed the application's front-end design and begun investigating communication between the ESP32 microcontroller and a back-end mySQL server.

<h3>10/22/23 - App Design</h3>
Ordered PCB. We are expecting to receive the PCB around October 31. Meanwhile we are continuing to work on setting up the App and our backend server. Dinal and I are in charge of setting up the backend, while also working on setting up the communication between the ESP32 module and the App and vice versa via both websocket and http communication protocols. 

<h3>10/26/23 - App design cont. </h3>
We have finished the front end. Additionally, we our continuing to work on the backend and are still awaiting PCB.

<h3>10/31/23 - PCB arrival </h3>
PCB has arrived. We have started soldering the board. Since none of us have that much experience soldering it is taking sometime. Additionally, we are missing some parts that we need for the board. These should be coming within the next 2 days. Furthermore, we are continuing to work on the App and also are exploring breadboarding with the devboard. 

<h3>11/5/23 - PCB arrival </h3>
We have finished soldering PCB. Looking to test it soon. 

<h3>11/6/23 - Tested Servo Motor, finished backend </h3>
Dinal and I tested out the Servo motors on our finished project with our PCB. This worked with some complications. We will have to look into debugging this tomorrow. We were also running into a cannot find port error when it came to trying to upload code to our ESP32 MCU. On the other side of things the backend is looking good. We were able to set up an API endpoint at our backend and GET the information from our backend with our App. Now all we have to do is work on posting data and then the App will be finished. 

<h3> 11/7/23 - FrontEnd complete </h3>
Completed the Front End of our application and integrated it with our backend server. This means that any data that we want to send and receive from our application to our server is possible and complete. Looking next to set up bidirectional communication between server and MCU. Additionally, looking to test out servo, rotary encoder, and LM35.

<h3> 11/9/23 - Tested Servo and LM35 with PCB </h3>
Finished soldering rest of the components to our breadboard. We then tested out PCB with our Servo motor and LM35 to first see if we can program the ESP32 and then test if it can receive signals from LM35 and send signals to Servo motor. There were some initial probelms again programming the ESP32 regarding port issues, but after downloading some necessary modules we were able to complete the tasks. The LM35 was giving some problems, but that was due to us not using the right library. The servo motor worked flawlessy and is able to tension our pulley system.

<h3>  11/11/23 - Steppper motor and rotary encoder</h3> 
The two components that aren't working as expected are the stepper motor and rotary encoder. Regarding the rotary encoder it looks like it is giving junk data we have got a replacement one which should be arriving soon. Hopefully that will resolve the issue. We have been following proper procedures from the datasheet and online tutorials regarding how to test it, however, it is really finicky right now. Regarding the stepper motor we have tested many different coil configurations and the best we can hear is an initial jolt. Will look to using debugging tools with voltmeres and amp meter.

<h3> 11/13/23 - Further work with stepper and rotary encoder + tested bidirectional communciation between MCU and server  </h3>
Stepper motor still not working as expected. Voltage at driver is at expected 10V indiciating the boost module is working. Replacement rotary encoder just came in today, will test this tomorrow as well as hit office hours for stepper motor. Since these components weren't working, worked on setting up bidrectional communication between the MCU and server. Used GETs to receive data from Server on the MCU and POSTs to relay data from MCU to server. This took some time to write up, but worked as expected. 

<h3> 11/14/23 - Rotary encoder and stepper motor</h3>
Office hours weren't really able to help with the stepper motor. We believe that the issue is that we need more power, which either means increase voltage at the driver or we need more current to drive through the motor. The new rotary encoder behaves exactly the same as the old one. We tried to make sense of the data, but the data actually makes no sense. Supposed to output a -1 for every counterclockwise degree rotation and a +1 for every clockwise degree rotation. However, even while it's stationary the rotary encoder is siginaling that it is rotating. 

<h3> 11/15/23 - Finished logic with servo motor and app</h3>
Decided to forego rotary encoder and stepper motor for right now. Focused on setting up full end to end logic with LM35, Servo motor, ESP32, Server, and App. Wanted to ensure that we could we get it closest to what we envisioned our project would look like with the rotary encoder and stepper motors working.

<h3> 11/16/23 - Tweaked logic a bit and looked into wifi </h3>
Right now we weren't able to set up WiFi on IlllinoisNet since there is an additional layer of security. We looked for alternatives and decided to settle on using a hotspot. This works slower, but still gets the job done.

<h3> 11/28/23 - Demo</h3>
Completed demo. There were a few complications, but after resetting ESP32 everything worked as expected.

<h3> 11/30/23 - Mock Presentation</h3> 
Set up slides for mock presentation and delivered mock presentation. Received feedback to add more pictures about our project and to explain how the end to end should look like.

<h3>12/4/23 - Presentation Slides</h3>
Finished presentation slides and went to a couple of run throughs.

<h3> 12/5/23 - Presntation </h3>
Completed presentation. 

<h3>12/6/23 - Final Paper</h3>
Completed final paper. That's the end. 

