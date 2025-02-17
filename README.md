# Srujanjalojiltspice
# LIC_exp
linear integrated circuits
# Experiment-1
Question:the power given is p=100uW , perform DC analysis , Transient analysis and AC analysis for the given circuit and check what happens when the width is increased or decreased of each mosfet.
# Design-1:
![Screenshot 2025-02-17 203301](https://github.com/user-attachments/assets/34f375f2-53e2-4fe4-be1a-a775aeb92a99)

Aim:To determine the DC operating point, calculate the gain using transient and AC analysis. Components: MOSFET, resistor, DC power supply. Procedure: Connect the circuit as described above. Attach the RD resistor to the drain terminal, the DC power supply to the gate terminal, and the source to ground. Set the input voltage to 0.4V and Vdd to 1.8V. Using the power formula p=vi with power = 50µW and voltage = 1.8V, we can find the current to be 27µA. By adjusting the MOSFET’s width and length, we can achieve the desired drain current Id. Given that the length is 180nm, adjusting the width to 72.2um will yield the required current.

   1.DC analysis:
     Inorder to simulate the DC analysis we have to select the option called [DC op pnt] in the 
     edit simulation command and run the simulation,we can see the vales obtained from the DC 
     analysis in the figure below
     
![Screenshot 2025-02-17 200552](https://github.com/user-attachments/assets/4ec257a8-f1d4-4964-88a0-04c48b4a910f)

   2.Transient Analysis:
     Inorder to simulate the transient analysis we have to select the option called transient 
     analysis in the edit simulation and give the stop time as 5ms and run the simulation,the 
     graph in the below figure shows the transient response of the design.
     ![Screenshot 2025-02-17 202815](https://github.com/user-attachments/assets/cefa281b-81c8-4bc1-bc21-a8d6dd67b931)

   3.AC analysis:
     Inorder to perform the ac analysis we need to select the ac analysis option in the edit 
     simulation command and we should give the values as shown below
     ![Screenshot 2025-02-17 203123](https://github.com/user-attachments/assets/4c9f78be-4dd6-4987-a24a-462312458059)
     the graph shown is the ac analysis
     ![Screenshot 2025-02-17 203720](https://github.com/user-attachments/assets/5d1152ce-4ac3-42c2-82b0-8f568867f9c6)

     Result:

     DC analysis

     The calculated drain current aligns with the expected value based on power and voltage, 
     with Id = 27uA. By adjusting the MOSFET's channel dimensions L = 180nm and W = 72.2um the 
     current requirement was successfully met. The circuit performs as expected under DC 
     conditions.

     Transient Analysis

     The transient response graph shows the circuit's behavior over time. The response is 
     smooth, with no unexpected delays or distortions. The circuit reacts appropriately to 
     changes, indicating that it is stable and functions as expected.

     AC Analysis

    The AC response graph confirms that the circuit remains stable across various frequencies. 
    the gain of -9.94 dB and the phase shift, which is nearly 180deg, align with theoretical 
    expectaions. The circuit consistently performs well throughout the tested frequency range.

    Inference

    The experiment confirms that by selecting the appropriate MOSFET dimensions, the drain 
    current can be effectively controlled. The width of the MOSFET significantly impacts the 
    drain current, indicating that any variation in width directly affects the output current. 
    Increasing the width results in a higher Id, while decreasing the width reduces Id. The 
    design aligns with theoretical predictions and matches the practical values observed in the 
    experiment.

     


