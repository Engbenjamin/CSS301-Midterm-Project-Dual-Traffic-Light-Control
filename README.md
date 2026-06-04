# CSS301-Midterm-Project-Dual-Traffic-Light-Controller Finite State Machine
CSS301 Midterm Project-Dual Traffic Light-Controller Finite State Machine

------
### Project Selection/Summary
For this project, I will program and build a dual traffic light control Finite Sate Machine (FSM) utilizing a Terasic DE10Lite FPGA board. Through the board’s GPIO pins, it will control an dual external Red-Yellow-Green traffic light circuits, changing state depending on whether it senses a vehicle. The code will be adapted from a project online at FPGA4student.com while the external circuit will be designed and built separately.

-----
### Project Proof/Bill of Materials
•	Used Terasic DE10Lite FPGA Board

<img width="351" height="305" alt="image" src="https://github.com/user-attachments/assets/8a511655-ddfb-4a86-8a41-40bfab22516e" />

•	DE10Lite GPIO Connector to breadboard breakout board
<img width="530" height="384" alt="image" src="https://github.com/user-attachments/assets/b583dd51-8571-4835-91e2-5c3f552507a6" />





•	Parts already on hand
-2 breadboards
-Qty 6: 2N7000 NMOS enhancement-mode transistors
-Qty 6: 100Ω LED current limiting resistors
-Qty 2: Red LED
-Qty 2: Yellow LED
-Qty 2: Green LED
-Qty 1: Photoresistor
-Qty 1: 10MΩ resistor for photoresistor/car sensing circuit

•	Equipment used:
-DC power supply (UWB Electrical Engineering Labs)
-Digital Multimeter (UWB Electrical Engineering Labs)

-------

## Week 1 Journal
### Inception of the Traffic Light Controller Finite State Machine
During the first week of my engineering project, I received my Terasic DE10-Lite FPGA, GPIO breakout board, and cable to begin prototyping an external, dual-direction traffic light circuit controlled via Verilog.

### Hardware Prototyping and Testing
In the initial phase of development, I focused on establishing safe operating parameters for the external hardware. To protect the FPGA from overvoltage damage, I isolated the six LED circuits using an external 3.3V DC power supply, which matches the board’s 3.3V GPIO output. Assuming a 2.0V forward voltage drop and a 10–20mA target operating current per LED, my rough calculations dictated a 100Ω current-limiting resistor for each branch. Next, I constructed the physical prototype on a breadboard, integrating six separate channels consisting of an LED, a 100Ω resistor, and a 2N7000 NMOS transistor. Manually tying the transistor gates to the 3.3V supply rail, I used a digital multimeter to verify a safe operating current of 13–16mA per LED circuit.

### GPIO Integration and Verilog Verification
With a rough prototype of the external circuit complete, I shifted my focus toward establishing software control over the external components. I mapped the FPGA’s 2x20 GPIO connector through the breakout ribbon cable onto the breadboard. Subsequently, I drafted a simple Verilog program for testing purposes, mapping the physical onboard switches directly to the designated GPIO output pins. Testing verified that the pins properly toggled between 3.3V high and 0V low states, successfully driving the NMOS transistor gates to control the illumination of the LEDs.

### Conclusion
This week, I learned how to build 6 LED light control circuits as well as how to turn ON/OFF the individual lights through the GPIO pins. Now that I have most of the external circuit built, next week I will be program the logic for the circuit. 

<img width="775" height="548" alt="image" src="https://github.com/user-attachments/assets/6ec787ce-7f70-46ef-98ad-3895ca011029" />
<img width="780" height="468" alt="image" src="https://github.com/user-attachments/assets/aa61a276-70e6-46d5-9ef7-c5621dd5d2dc" />
