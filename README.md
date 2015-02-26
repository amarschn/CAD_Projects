# CAD_Projects





MRSD Project:
=============

In this project my team and I (4 members) are focused on creating a modular robotic platform. Modules have been broken out based on different functions, such as perception, locomotion, and brain. We use ROS for inter-module communication over ethernet.

For this modular platform we built a mobile robot for the first semester consisting of a perception module, locomotion module, and brain module. The perception module was a pan/tilt Kinect camera which could be used for line sensing and tele-operation. The locomotion module was a differential drive system using 2 DC motors and caster wheels for support. The brain module was an Intel-i3 computer running ROS and controlling all other modules, a 24V battery, and voltage converter.

More details can be found at:
https://sites.google.com/site/mrsdproject201415teamd/

Semester 1:
-----------

Below is a picture of the full assembly of the last semester's robot.
![Robot Assembly](/Images/MRSD_Semester_1_Full_Assembly.PNG "Robot Assembly")

The design of this robot was rather rushed, and so I focused on minimal build time and easy access to internal components (which proved smart, as the team and I had to dis-assemble and re-assemble the robot many times during testing in order to get access to electronic components). This was my first heavy use of Solidworks, as at Qualcomm I used Pro-Engineer/Creo. Overall I found the 2 programs more similar than different so the learning curve was not too bad.

At Qualcomm I used a top-down design method when constructing assemblies, which has it's pros and cons, but this time around I tried a different tack. I used a text file ("globals.txt") that contained global variables such as module height, width, etc.. I then imported the "global" variables into given Solidworks parts to access the variables I needed. This allowed me to quickly tweak robot physical parameters and have the changes affect all parts at once.

Here is the actual robot once constructed:
![Actual Robot Assembly](/Images/MRSD_Semester_1_Actual_Assembly.PNG "Actual Robot Assembly")

This was my first mobile robot design, and I learned a lot from it. The large unfilled holes you see are for an inter-module connector. We were not able to finish a satisfactory inter-module connector in time for the end of last semester, and so the holes were used for ethernet and power wires.

I used laser-cut acrylic and aluminum extrusion as the mechanical structure of the robot. Due to time constraints I wanted something that was cheap, durable, and cost very little machining time. I had access to Makerbot 3D printers, which while useful for small parts are not useful for large, detailed, or load-bearing components.

Once all modules were assembled, the motor power was not always enough to get the robot moving over the rough pavement we demo'd on. The wear and tear of driving on rough pavement eventually caused a gear tooth in one of the motors' gearheads to crack (right before a demo of course), forcing us to change out the locomotion module for an existing mobile base for the final demo.


Semester 2 (now):
-----------------

This semester I have gone back to basics. I am re-designing the robot from the ground up, first focusing on the inter-module connection, as it is in many ways the most unique aspect of the robot. I came up with many different design possibilities, but eventually settled on a magnetic inter-module connector. Magnets offer many advantages, as the connection mechanical strength can be scaled to a point with larger magnets, and the disengagement between modules is linear. By this I mean that no special actions are required by the user to disengage a module other than pulling it. Additionally, by placing the magnets in certain pole orientations you can prevent the user from connecting 2 modules in an incorrect way.

This [paper](http://cba.mit.edu/docs/theses/10.06.knaian.pdf) considers many of the connector types I toyed with before settling on magnets. Ideally I would be able to prototype more of them, but there is not enough time before the end of the semester to fully explore all connector possibilities.

For the electrical connection I am using pogo pins, which are used to transmit power and data over 16 pins. I have used pogo pins before, and I think they are a no-brainer for applications such as this.

I am also using dowel pins as guide rods, which ensure an accurate pogo connection.

![Male Magnetic Connector](/Images/MRSD_Semester_1_Actual_Assembly.PNG "Male Magnetic Connector")


Automated Durometer:
--------------------

