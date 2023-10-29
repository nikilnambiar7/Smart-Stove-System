<h3>09/14/23 - Proposal Due</h3>
Submitted proposal, discussed design with machine shop, and finished the team contract. 

<h3>09/19/23 - Redesigned System</h3>
The rail system we had originally proposed was too difficult, so we had to propose alternate ideas. We intiially came up with an idea to have a linear actuator
to clamp on the stove knob, and a motor to rotate the knob. The issue came with how to disengage the motor. The motor will always be engaged in this configuration.

<h3>09/22/23 - Finalized Design</h3>
We came up with another way to disengage the motor, but the issue was this solution was incredibly mechanically complex. Instead
we have finalized a new design with the machine shop. We've opted for a setup comprising a stepper motor, servo motor, pulley system, 
and a rotary encoder to constantly monitor the stove knob's position. This configuration enables users to adjust the stove settings manually or remotely.

<h3>09/26/23 - Design Document work</h3>
On the design doc, I mainly focused on adding all the diagrams and visual aids. In addition to that, I also worked on creating the parts list, schedule, labor costs
and the tolerance analysis. The tolerance analysis required some learning about mechanical engineering fundamentals such as gear ratios with pulleys and torque from 
motors.

<h3>10/02/23 - Design Review and starting PCB design</h3>
During the design document review, a new feature was suggested: integrating a timer to automatically shut off the stove.
Additionally, we progressed by selecting the final components for our design and visited both the machine shop and ECEB shop to procure the necessary parts.

<h3>10/06/23 - PCB Review</h3>
We participated in a PCB review session and received valuable feedback on our schematic. It became apparent that further research on our specific components was necessary to find appropriate footprints.
Additionally, we recognized the need to delve into the USB to UART bridge technology to ensure efficient transmission and reception of data from our microcontroller.

<h3>10/11/23 - First Round of PCB Orders</h3>
We were not able to submit the files for the first round of PCB orders, as we could not pass the audit on pcbway due to our footprints
not being completely correct. We decided to begin using easyEDA to design our schematic and layout for our PCB since it is better lined up
for the components and footprints we are trying to use. We also finished the teamwork evaluation form.

<h3>10/13/23 - Finalized Design with Machine shop</h3>
We finalized the design with the machine shop and provided them with all of the components that would be going into our mechanical design. In addition, we tested copies of the parts we were using on our
breadboard

<h3>10/17/23 - Second Round of PCB Orders</h3>
We were unable to complete the design by the second round of orders due to issues with the stepper motor driver datasheet. However, we will fix this issue.

<h3>10/19/23 - Finished PCB layout</h3>
We have completed our PCB schematic and layout and have passed the audit on pcbway, we plan our ordering the PCB before the third round.
We have also finished the front-end design for our application and have started to look into communication between a back-end mySQL server
and the ESP32 microcontroller.

<h3>10/23/23 - Individual Progress Report </h3>
Unfortunately, the individual progress report has been taking most of our time this week so we were not able to progress much. However, we did order our PCB ourselves.

<h3>10/26/23 - Front End Design </h3>
Worked on converting my front end figma design to a Swift UI to use for our app. In this front-end, I added api endpoints to send information to the back end server about what the user
set as their levesls


