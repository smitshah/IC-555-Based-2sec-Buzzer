# IC-555-Based-2sec-Buzzer

**Problem statement:**

Design a circuit using IC 555 that will switch the buzzer ON for 2sec after giving a trigger pulse only.


**INTRODUCTION:**

The objective of this project is to familiarize ourselves with the various applications of Schmitt Trigger using IC 555 and to recognize their use in real life conditions. Our topic was to create a circuit which would turn the Buzzer on only when a trigger pulse is applied. These circuits can be used in real life applications like buzzer alarms, doorbells, buzzers during quizzes, timers etc. Our buzzer is meant to buzz only for 2 seconds after an interval of two seconds. Hence, we used resistors of value such that our Ton and Toff would come to be approximately 2 seconds each. This project’s aim is to help us in brushing up our skills of recreating a given circuit on two software’s, KiCAD and LTSpice. It is also meant to construct the circuit on the breadboard and PCB after the process of etching.


**MATERIALS USED:**
* NE555
* 220kΩ Resistor
* 100kΩ Resistor
* 10µF Capacitors
* Buzzers 
* Connecting wires
* Power supply
* Breadboard
* Copper Clad


**CHOOSING THE CORRECT CIRCUIT DIAGRAM:**

Our first step for this project was to find the most appropriate and efficient circuit diagram that would help us achieve the required output. After a lot of consultation from textbooks and online websites, we chose a circuit diagram that was best for our application. 

![Circuit Diagram](https://user-images.githubusercontent.com/42312238/80623896-8886f800-8a68-11ea-8f61-6a3c7b8888ab.jpg)

We recreated the circuit diagram on LTspice, a software that allows us to replicate the circuit diagram with the appropriate components connected to it, to run the simulation and achieve and actual output of the circuit. Using the software, we observed the output for various values of resistors and capacitors. Resistor R1 is responsible for Ton value and R2 is responsible for Toff value. After a lot of trial and error, we got our require values of R1, R2, C1 and C2 for the needed Ton and Toff values of 2 seconds. R1 came out to be 100K ohm, R2 came out to be 220K ohm and C1 and C2 both came out to be 10uF. As this circuit keeps switching from ON to OFF, it is called an Astable Multivibrator circuit, using IC555. 


The LTspice circuit diagram and output of the software is as shown:

Circuit Diagram:

![LTspice Circuit Diagram](https://user-images.githubusercontent.com/42312238/80623927-95a3e700-8a68-11ea-9f7a-30081aaa05f5.png)


Output *(Ton and Toff is approximately 2 seconds each)*:

![LTspice Output](https://user-images.githubusercontent.com/42312238/80623956-a05e7c00-8a68-11ea-8bf9-657421917062.png)


**BREADBOARD MOUNTING:**

Following the circuit diagram chosen, we get the appropriate components and place them on the breadboard. Breadboard connections are temporary connects and help us to identify if our circuit is actually working or giving us the required output with the live working components in place. It also helps us to certain if the components are in correct working order or no.

![Breadboard](https://user-images.githubusercontent.com/42312238/80623991-ace2d480-8a68-11ea-98f2-55ac4b7ca7b7.jpg)


**KiCAD SCHEMATIC:**

After the testing of the circuit using the breadboard, we move onto the next software, KiCAD. Using KiCAD we can lay the foundation of our final PCB circuit. We start off with a rough schematic of our circuit which will closely resemble the circuit that we had produced on LTspice. The schematic gives us a general idea of what the circuit may comprise of and how many components are used. After this, we move onto footprint allocation, which is the process where the software identifies which exact components we are using and their respective dimensions so that the process of soldering may take place properly without any issues with the size of the components or so. 


The schematic and footprint allocation for our circuit is as below:

KiCAD Schematic:

![KiCad Schematic](https://user-images.githubusercontent.com/42312238/80624036-bec47780-8a68-11ea-9a26-b2cdc5b67ca6.png)


Footprint Allocation to the Schematic:

![Footprint](https://user-images.githubusercontent.com/42312238/80624062-c5eb8580-8a68-11ea-860f-f07e2a899f53.png)


**KiCAD GERBER FILE GENERATION:**

After footprint allocation, we move to net-list generation which is the process of importing the footprint allocation onto a virtual PCB. Here, we can place the components in the most effective manner onto our PCB board and can hence visualise how our final PCB structure look like by viewing the virtual 3D model. We can then complete the tracking and override them to make it most effective. We can choose the layers of the PCB we need in our final output and create a gerber file of it. We can save the gerber file in PDF format also. This PDF file is collection of all the layers of the PCB that we choose to have. Out of all of these files, the most important one is B.Cu file. It is the back copper tracking between all these components of our final PCB.

Final PCB Layout:

![Final PCB Layout](https://user-images.githubusercontent.com/42312238/80624112-d865bf00-8a68-11ea-8580-b3054a47e3bc.png)


The 3-D view of front-side and back-side our PCB is as below:

![3D front](https://user-images.githubusercontent.com/42312238/80624142-e4518100-8a68-11ea-9c26-7bcc26392c9d.png)
![3D back](https://user-images.githubusercontent.com/42312238/80624152-e74c7180-8a68-11ea-8973-81ed49780026.png)


**TONER TRANSFER:**

Toner transfer is the process by which we create our actual track of our circuit. We take the B.Cu file (PDF Format) and get it printed on a photo paper with a good quality ink. After the printout is taken, it is placed upside down on the copper clad and is taped down to it. We then cover it with a piece of cloth and heat it with the help of Iron. We press it down and run the iron over it until the ink is transferred onto the copper clad from the paper. This process of transferring ink from photo paper onto copper clad is called toner transfer.


**ETCHING:**

Etching is a method used for the production of the PCBs where acid is used to remove unwanted copper from a prefabricated laminate. This is done by applying a temporary mask (in our case, ink), that protects part of the laminate from the acid and leaves the desired copper layer untouched. The etching solution used by us is ferric chloride. Thus, we dip the PCB in boiling FeCl3 solution and wait until the excess copper is dissolved off and only our tracks of circuit remains. After this is done, we take out the board and clean it using water.


**DRILLING AND SOLDERING:**

After cleaning the board, we proceed to drill the board using a PCB drilling machine. We make holes of diameter approximately 1mm. Holes are made wherever components have to be placed. After all the holes are drilled, we proceed to place the components in their respective slots following the PCB layout. Once the components are placed, we solder them so that they stay in place and the connections are complete. We also solder other wires where external connections are required. After soldering, we clean our PCB with IP(Iso-propyl Alcohol) so that the residue of solder is removed. Now our circuit is ready to use. 

Now, we provide the trigger pulse to the input terminal of our circuit and check the operation of the buzzer. If all the above process are carried out in the correct manner, then our buzzer should buzz with the appropriate time intervals.


Actual PCB *(Circuit on Copper Clad)*:

![Actual PCB front](https://user-images.githubusercontent.com/42312238/80624194-f8957e00-8a68-11ea-91af-83241b44ed83.jpg)
![Actual PCB back](https://user-images.githubusercontent.com/42312238/80624202-fb906e80-8a68-11ea-975b-66b3ffbe208d.jpg)



**CONCLUSION:**

Hence, through this project we saw how to create a buzzer circuit using IC 555 and saw all the processes required to achieve our final circuit. This project helped us in brushing up our skills for PCB designing which may be of great use for us in the future. These skills help us develop working circuits right from scratch until the very end. Hence, we can come up with circuits wherever we are, by just learning these few steps. 

