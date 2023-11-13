# Programming and Simulation of Kuka Robots in RoboDK
****
Acronym | Meaning
---|---
DK | Development Kit, is a package of software tools, or sometimes programs, that aid in the development of new software, or programs
****
project zip file| Project name | Executive summary
---|---|---
[ConveyorAndArm_ASSEMBLY.rdk][file] | Conveyor Belt Simulation | A program that simulates the interactions between a conveyor belt and a robotic arm in RoboDK 
****
## Table of Contents
- [Conveyor Belt Simulation][proj]
  - [Objectives][obj]
  - [Development][Dev]
  - [Results][res]
****
## Conveyor Belt Simulation

##### Fig. 1.  Simulation of robotic arm and conveyor belt in RoboDK
![screenshot of robot arm and conveyor belt][im-sc]
##### Fig. 2.  Nesting structure of elements in the simulation
![image][im2-sc]


### Objectives
To apply learned skills about programming in the RoboDK environment to a robotic arm and conveyor belt, in order to further develop, and demonstrate, skill and understanding in programming robotic arms in industrial settings.

### Development
Before the program could be developed, it wass necessary to set up the working space. It was necessary to download[^1] the models for the robotics arm, the gripper, and the conveyor belt (the table model comes default with RpbpDK program). Then, with all the models in the library, it becomes possible to load the objects into the scene, and arrange them as shown in [figure 1][fig-1]. Once the elements were placed within the scene, it Becomes possible to start assigning the targets for the arm and the belt, as well as ssetting up the gripper's functionality.

Once the gripper was setup, and the elementss properly branched, as in [figure 2][fig-2], programming can begin. The main program is contstucted using a series of 5 unique subroutines. The subroutines handle the following procedures:
- Repositioning of the conveyor belt (Coveyor Belt)
- Pickng the object off of the conveyor belt and placing it on the table (ARM take)
- Picking the object off of the table, and placing it back on the conveyor belt (ARM replace)
- Opening the gripper (H_OPEN)
- Closing the gripper (H_CLOSE)
The ARM take and replace routines make calls to the H_OPEN and H_CLOSE in order to grab and release the object, and the main program calls the Conveyor Belt routine, and then the take and replace routines, each with a 500ms delay.

### Results
The final product is a simulation, and a series of programs, that then direct a KUKA KR 6 R900-2 robotic arm to grab an object off of a conveyor belt, and then place it back. 

Reviewing the code now, I would make the following alterations:
- Change attatchment, and detattchment, of the object to the gripper to occour during the openning and closing of the gripper


<!--- Footnotes --->
[^1]: https://robodk.com/library
<!--- figures and image sources --->
[fig-1]: #fig-1--simulation-of-robotic-arm-and-conveyor-belt-in-robodk
[im-sc]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/assets/135147457/7966f905-b80c-41a8-b1d7-5043e037933d
[fig-2]: #fig-2--nesting-structure-of-elements-in-the-simulation
[im2-sc]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/assets/135147457/2f848dd6-1954-486e-bf16-02db4a071ad2

<!--- File Paths --->
[file]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/blob/56e76c7a63457d678533ad9c87dfb5eb072c2529/Robot%20Simulations%20and%20Programming/Robo_DK/ConveyorAndArm_ASSEMBLY.rdk
<!--- Project --->
[proj]: #conveyor-belt-simulation
[obj]: #objectives
[dev]: #development
[res]: #results
