# Programming and Simulation of Kuka Robots in Cosimir Pro
****
Acronym | Meaning
---|---
RGB | red-green-blue, reffers to colour systems that use varying levels of red, green and blue light to create other colours
****
project zip file| Project name | Executive summary
---|---|---
[Project_U4.zip][p-u4] | Stack and Sort | A program to stack and sort objects based on colour onto a palette 
[REACT.zip][react] | Dynamic Reactions | A program to allow a Kuka arm to use a sensor to dynamically react to the changing position of a cube
****
## Table of Contents
- [Project 1: BlockSort][proj-1]
  - [Objectives][P1-obj]
  - [Development][P1-Dev]
  - [Results][P1-res]
- [Project 2: Dynamic Reactions][proj-2]
  - [Objectives][P2-obj]
  - [Development][P2-dev]
  - [Results][P2-res]
****
## Project 1: Block Sort
##### Fig. 1.  Simulation of robot arm sorting coloured blocks
![screenshot of robot arm sorting coloured blocks][sort-sc]

### Objectives
To apply learned skills about programming in MELFA-BASIC to a robotic arm equipped with colour sensor and a designated sorting region using Cosimir Pro, in order to further develop, and demonstrate, skill and understanding in programming robotic arms in industrial settings.

### Development
Before the program could be developed, it wass necessary to set up the working space. Using the model Libraries function of Cosimir Pro, the RGB colour sensor, blocks holder, and palette were selected and placed within the scenery, as shown in [figure 1][fig-1]. Once the elements were placed within the scene, it is neccesary to connect the required inputs and outputs to, and from, the robot arm, so that they can be incorporated in the code.

The program was developed by first planning out the series of events, and then working out the outlines of an algorithm. With that completed, the program was developed with a rapid prototyping approach of setting down a framework, and then ittertaively testing, debugging, and re-writing the code, until the final product was completed.

### Results
The final product is a simulation, and a program, that can identify and sort 4 categories of coloured blocks. The code makes use of one subroutine to grab a block from the block holder, and haver above the palette, and the main routine sorts the blocks, tracks the next position for each colour and then returns the arm to the idle hover position.

Reviewing the code now, I would make the following alterations:
- Create a subroutine to handle the placement of bloack onto the palette, leaving the calculation of the position within the original case strucure
- Change the palette variable to use variables to determine how many rows and columns to make
  - Change the position variables for each block colour to be dynamically calculated based on the row and column variables
- Alter the placement target so that the orientation of the actuator matches the hover possition

****
## Project 2: Dynamic Reactions
##### Fig. 2.  Simulation of robot arm detecting moving object
![screenshot of robot arm reacting to moving object][react-sc]


### Objectives
To apply learned skills about programming in MELFA-BASIC to a robotic arm equipped with colour sensor and a designated sorting region using Cosimir Pro, in order to further develop, and demonstrate, skill and understanding in programming robotic arms in industrial settings.

### Development
Before the program could be developed, it wass necessary to set up the working space. Using the model Libraries function of Cosimir Pro, the distance sensor, and rotating table were selected and placed within the scenery, as shown in [figure 2][fig-2]. Once the elements were placed within the scene, it is neccesary to connect the required inputs and outputs to, and from, the robot arm, so that they can be incorporated in the code.

Using the same aproach as before, the rotating table was programmed to rotate 90° every loop, and the arm would move forward until it detects the object with its sensor, backing away until it is no longer active. 

### Results
The program demonstrates a very simple approach to having the robotic arm react to elementss in its environment.

Reviewing the code now, I would make the following alterations:
- Define a subroutine to rotate the table (if possible multi-thread and have table rotate independant of arm)
- Create subroutines for the operation of the arm
  - a forward moving, sweeping motion to detect objects
  - a retreating, obstacle avoiding, motion

<!--- Footnotes --->
[^1]: The source code was built with [this guide][1] as reference
<!--- Refs --->
[1]: https://www.slideshare.net/ruben_loredo/programacion-melfa-iv
<!--- figures and image sources --->
[fig-1]: #fig-1--simulation-of-robot-arm-sorting-coloured-blocks
[sort-sc]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/assets/135147457/18ce8692-669e-494c-81b8-03f48109614c
[fig-2]: #fig-2--simulation-of-robot-arm-detecting-moving-object
[react-sc]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/assets/135147457/64afa54f-1b93-4658-9e15-75f3124171a3
<!--- File Paths --->
[p-u4]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/blob/c56d572d72d2be7890daec2abd9e4d288f0bba3e/Cosimir%20pro%20Simulations/Project_U4.zip
[react]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/blob/c56d572d72d2be7890daec2abd9e4d288f0bba3e/Cosimir%20pro%20Simulations/REACT.zip
<!--- Projects --->
<!--- 1 --->
[proj-1]: #project-1-block-sort
[P1-obj]: #objectives
[P1-dev]: #development
[P1-res]: #results
<!--- 2 --->
[proj-2]: #project-2-dynamic-reactions
[P2-obj]: #objectives-1
[P2-dev]: #development-1
[P2-res]: #results-1
