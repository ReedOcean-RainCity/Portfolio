# Kinematic Simulations
****
Acronym | Meaning
---|---
SCARA | Selective Compliance Assembly/Articulated Robot Arm, a type of robot arm with rotational joints along only one plane
FK | Forward Kinematics, a way to describe how the position and sstate of a robot changes, as each point of articulation, or actuation, is adjusted
IK | Inverse Kinematics, the reverse of FK, IK calculates the possitions of the points of articulation, or actuation, based on a desired position of the robot in question
****
project zip file| Project name | Executive summary
---|---|---
[Scara_Name.zip][file] | SCARA Name Tracer | A series of scripts written in octave, that simulates the actuation of a SCARA as it traces out a portion of a name 
****
## Table of Contents
- [3D Model of a Simple Robotic Arm][proj]
  - [Objectives][obj]
  - [Development][Dev]
  - [Results][res]
****
## 3D Model of a Simple Robotic Arm

##### Fig. 1.  Top down view of the simulation
![image][im-sc]
##### Fig. 2.  Near isometric view of finished simulation
![image][im2-sc]

### Objectives
To apply learned knowledge and skills regarding the kinematics, and simulation of, a SCARA, in order to further develop, and demonstrate, skill and understanding in the calculation and simulation of a robot's forward and inverse kinematics.

### Development
Before the programming can begin, it is necessary to calculate the forward, and inverse kinematicss of the robot in question. The FK are required to be calculated first, as the IK can only be calculated using the results from the FK. Thus, after the FK equations of the SCARA were formulated, the results were used to algebraically determine the IK. With the equations of the FK and the IK thus defined, a set of two scipts is then created so that they can calculate the FK and the IK respectively.

In the main program, we feed the desired position of the arm into the IK script, which will tell us the final possition of our joints, and then we can calculate the trajectory using the initial position, final position, and the travel time for the joints. Then, using DK, we can then determine the position of the arm, as the joints articulate towards their final position. Then, with the information from the DK, we can then create a visual representation of the movement of the arm.

### Results
The final product is a series of scripts, that combine together in the main program, to simulate the motion of a SCARA tracing out a name. In total, 5 scripts are rquired, one to calculate the DK of the arm, one to calculate the IK, one to calculate the joint trajectories, and one to draw the simulated arm.

<!--- figures and image sources --->
[fig-1]: #fig-1--top-down-view-of-simluation
[im-sc]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/assets/135147457/b3cc64e8-6545-4fef-a3b6-8a416d131916
[fig-2]: #fig-2--near-isometric-view-of-finished-simulation
[im2-sc]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/assets/135147457/2fba7794-a2db-47e0-bd49-da4339b73685



<!--- File Paths --->
[file]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/blob/f7b45707823a4dc83277b13cee43c65c72ea2a48/Kinematic%20Simulations/Scara_Name.zip
<!--- Project --->
[proj]: #3d-model-of-a-simple-robotic-arm
[obj]: #objectives
[dev]: #development
[res]: #results
