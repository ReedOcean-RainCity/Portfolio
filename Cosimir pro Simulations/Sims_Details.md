# Programming and Simulation of Kuka Robots in Cosimir Pro
****
project zip file| Project name | Executive summary
---|---|---
[Project_U4.zip][1] | Stack and Sort | A program to stack and sort objects based on colour onto a palette 
[REACT.zip][2] | Dynamic Reactions | A program to allow a Kuka arm to use a sensor to dynamically react to the changing position of a cube
****
## Table of Contents
- [Project 1: BlockSort][proj-1]
  - [Objectives](#objectives)
  - [Development](#development)
  - [Results](#results)
- [Project 2: Dynamic Reactions](#project-2-dynamic-reactions)
  - [Objectives](#objectives-1)
  - [Development](#development-1)
  - [Results](#results-1)
****
## Project 1: Block Sort
<!--- SC of project goes here --->
### Objectives
This project's aim was to develop a program for a Kuka robot, integrated with certain peripherals, to be able to detect and sort objects into distinct groupings.  
### Development

### Results

```MELFA-BASIC
1 SPD 20
2 DEF PLT 1,P4,P6,P3,P7,4,4,2	'PALLETE
3 DEF INTE M1	'ITERATE
4 M1=1
5 DEF INTE M2	'RED
6 M2=0
7 DEF INTE M3	'GREEN
8 M3=4
9 DEF INTE M4	'BLUE
10 M4=8
11 DEF INTE M5	'OTHER
12 M5=12


13 MOV P1

14 WHILE (M1>=1) AND (M1<=8)

15 IF M_IN(4)=1 THEN 19 ELSE 16
16 M_OUT(1)=1
17 M_OUT(1)=0
18 GOTO 15

19 M_OUT(2)=1
20 IF M_IN(1)=1 OR M_IN(2)=1 OR M_IN(3)=1 THEN 34 ELSE 21

21 M5=M5+1
22 GOSUB *GRAB
23 CNT 1,20,15
24 P10=PLT 1,M5
25 SPD 50
26 MOV P10,-50
27 SPD 20
28 MVS, 45
29 HOPEN 1
30 MVS, -50
31 MOV P8
32 CNT 0
33 GOTO 78

34 SELECT M_IN(1) AND M_IN(2) AND M_IN(3)

35 CASE M_IN(1)=1
36 M2=M2+1
37 GOSUB *GRAB
38 CNT 1,20,15
39 P10=PLT 1,M2
40 SPD 50
41 MOV P10,-50
42 SPD 20
43 MVS, 45
44 HOPEN 1
45 MVS, -50
46 MOV P8
47 CNT 0
48 BREAK


49 CASE M_IN(2)=1
50 M3=M3+1
51 GOSUB *GRAB
52 CNT 1,20,15
53 P10=PLT 1,M3
54 SPD 50
55 MOV P10,-50
56 SPD 20
57 MVS, 45
58 HOPEN 1
59 MVS, -50
60 MOV P8
61 CNT 0
62 BREAK

63 CASE M_IN(3)=1
64 M4=M4+1
65 GOSUB *GRAB
66 CNT 1,20,15
67 P10=PLT 1,M4
68 SPD 50
69 MOV P10,-50
70 SPD 20
71 MVS, 45
72 HOPEN 1
73 MVS, -50
74 MOV P8
75 CNT 0
76 BREAK

77 END SELECT




78 WEND

79 MOV P1
80 END

81 *GRAB
82 M1=M1+1
83 MOV P2,-50
84 MVS, 50
85 HCLOSE 1
86 MVS, -50
87 M_OUT(2)=0
88 MOV P8
89 RETURN
```
Fig. 1.   Source code for block sort

****
## Project 2: Dynamic Reactions
<!--- SC of project goes here --->
### Objectives

### Development

### Results


[1]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/blob/c56d572d72d2be7890daec2abd9e4d288f0bba3e/Cosimir%20pro%20Simulations/Project_U4.zip
[2]: https://github.com/ReedOcean-RainCity/my-WIP-portfolio/blob/c56d572d72d2be7890daec2abd9e4d288f0bba3e/Cosimir%20pro%20Simulations/REACT.zip
[proj-1]: #project-1-block-sort
