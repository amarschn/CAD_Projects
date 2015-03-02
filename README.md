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
![Actual Robot Assembly](/Images/MRSD_Semester_1_Actual_Assembly.JPG "Actual Robot Assembly")

This was my first mobile robot design, and I learned a lot from it. The large unfilled holes you see are for an inter-module connector. We were not able to finish a satisfactory inter-module connector in time for the end of last semester, and so the holes were used for ethernet and power wires.

I used laser-cut acrylic and aluminum extrusion as the mechanical structure of the robot. Due to time constraints I wanted something that was cheap, durable, and cost very little machining time. I had access to Makerbot 3D printers, which while useful for small parts are not useful for large, detailed, or load-bearing components.

Once all modules were assembled, the motor power was not always enough to get the robot moving over the rough pavement we demo'd on. The wear and tear of driving on rough pavement eventually caused a gear tooth in one of the motors' gearheads to crack (right before a demo of course), forcing us to change out the locomotion module for an existing mobile base for the final demo.


Semester 2 (now):
-----------------

This semester I have gone back to basics. I am re-designing the robot from the ground up, first focusing on the inter-module connection, as it is in many ways the most unique aspect of the robot. I came up with many different design possibilities, but eventually settled on a magnetic inter-module connector. Magnets offer many advantages, as the connection mechanical strength can be scaled to a point with larger magnets, and the disengagement between modules is linear. By this I mean that no special actions are required by the user to disengage a module other than pulling it. Additionally, by placing the magnets in certain pole orientations you can prevent the user from connecting 2 modules in an incorrect way.

This [paper](http://cba.mit.edu/docs/theses/10.06.knaian.pdf) considers many of the connector types I toyed with before settling on magnets. Ideally I would be able to prototype more of them, but there is not enough time before the end of the semester to fully explore all connector possibilities.

For the electrical connection I am using pogo pins, which are used to transmit power and data over 16 pins. I have used pogo pins before, and I think they are a no-brainer for applications such as this.

I am also using dowel pins as guide rods, which ensure an accurate pogo connection.

![Male Magnetic Connector](/Images/MRSD_Semester_2_Male_Magnetic_Connector.PNG "Male Magnetic Connector")

This is the male connector, which as you can see is not using all of the magnet placement holes. This is because there was not enough room in the motor module for mounting all of them (the aluminum extrusion supports got in the way). This design is in a state of change however, and I am planning on using a different magnet placement grid to allow for more magnets.

The first module we have tested this magnetic connector with is a "motor module". This is a new module, one step lower than a locomotion module. The plan is to have motor modules that can be swapped out of a locomotion module, these different motor modules can have different kinds of motors as well as different wheel attachments. Once connected each motor module will communicate these details to the brain, which will dynamically update the robot's model. Below you can see the current CAD model for the motor module.

![Motor Module](/Images/MRSD_Semester_2_Motor_Module.PNG "Motor Module")

We have now built 2 of these, and they work pretty well! The magnetic connector works and is relatively sturdy. The next steps are to rebuild a locomotion base which will accept motor modules of this size, and to add the magnetic connector to appropriate faces of the brain module. We also will be building sensor modules using the same form factor as the motor module. So say the locomotion module had 4 different module connectors, you could swap out different motors and sensors quickly and easily and have an entirely new kind of robot! I am pretty excited about it and think by the end of the semester we will have a very cool re-configurable robot.

![Actual Motor Module](/Images/MRSD_Semester_2_Actual_Motor_Module.JPG "Actual Motor Module")
![Motor Module Connector](/Images/MRSD_Semester_2_Actual_Magnetic_Connector.JPG "Motor Module Connector")

For the locomotion module, the plan is to have 4 module slots open to motor or sensor modules with the same form factor as the motor module seen above. I am trying to create a more visually pleasing aesthetic as compared to last semester. Below is one of the concepts for the module:

![Locomotion Module Concept](/Images/MRSD_Semester_2_Locomotion_Module_Concept.png "Locomotion Module Concept")

By using laser cut acrylic or delrin on the top and bottom, and a thin 3D-printed ABS shell, the robot will be much more sleek as well as well within the team's limited budget.

Automated Durometer:
--------------------

The files for this project are located in a different repository, which can be found [here] (https://github.com/amarschn/Durometer_Assembly). The top-level assembly is called 'Durometer_Assembly' and can be downloaded in STP format if necessary.

This was a brief project I worked on over Christmas break. The goal was to automate a durometer (device for measuring hardness of different materials, in this case different kinds of rubber) for a scientific devices manufacturer.

![Basic Durometer](/Images/Durometer_Manual_Assembly.PNG "Basic Durometer")

I did this project in Autodesk Inventor, as I wanted to try it out to see what all of the fuss was about. Once again, being a parametric CAD program it wasn't too different from Solidworks or Pro-E. The usual sketch/extrude/repeat process was mostly the same. My other focus was off-the-shelf material, as I did not have access to any kind of fabrication facilities during the majority of the break and so had to work with whatever I could get. McMaster was (once again) a godsend for this project.

In automating the durometer, I decided to implement a stepper-motor/lead screw system for raising and lowering the durometer. Steppers are relatively cheap and combined with lead screws allow for very accurate motion control, and no power draw during inactivity.

![Automated Durometer](/Images/Durometer_Stepper_Assembly_Labeled.png "Automated Durometer")
![Automated Durometer Detail](/Images/Durometer_Detail_View.png "Automated Durometer Detail")

This project is currently on hiatus due to school taking up the majority of my time, but I was able to build a working prototype before the end of the break. Unfortunately I cannot find a video of it operating, but I will post that once I find it!