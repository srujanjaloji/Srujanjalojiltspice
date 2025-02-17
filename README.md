
# LIC_exp
linear integrated circuits
# Experiment-1
Question:the power given is p=100uW , perform DC analysis , Transient analysis and AC analysis for the given circuit and check what happens when the width is increased or decreased of each mosfet.
# Design-1:
![Screenshot 2025-02-17 223447](https://github.com/user-attachments/assets/16ba1212-cb63-4995-9d30-f1966a94b1d0)


Aim:To determine the DC operating point, calculate the gain using transient and AC analysis. Components: MOSFET, resistor, DC power supply. Procedure: Connect the circuit as described above. Attach the RD resistor to the drain terminal, the DC power supply to the gate terminal, and the source to ground. Set the input voltage to 0.4V and Vdd to 1.8V. Using the power formula p=vi with power = 50µW and voltage = 1.8V, we can find the current to be 27µA. By adjusting the MOSFET’s width and length, we can achieve the desired drain current Id. Given that the length is 180nm, adjusting the width to 72.2um will yield the required current.

   1.DC analysis:
     Inorder to simulate the DC analysis we have to select the option called [DC op pnt] in the 
     edit simulation command and run the simulation,we can see the vales obtained from the DC 
     analysis in the figure below
     
![Screenshot 2025-02-17 223731](https://github.com/user-attachments/assets/c7e9dddd-bb71-494e-9426-01d31cecedbe)


   2.Transient Analysis:
     Inorder to simulate the transient analysis we have to select the option called transient 
     analysis in the edit simulation and give the stop time as 5ms and run the simulation,the 
     graph in the below figure shows the transient response of the design.
     ![Screenshot 2025-02-17 223831](https://github.com/user-attachments/assets/f255c94f-851b-4137-90b7-07178d61e32c)

   3.AC analysis:
     Inorder to perform the ac analysis we need to select the ac analysis option in the edit 
     simulation command and we should give the values as shown below
     ![Screenshot 2025-02-17 224038](https://github.com/user-attachments/assets/104bf2af-b0ce-416e-a748-64eab9f52413)

     the graph shown is the ac analysis
     ![Screenshot 2025-02-17 223948](https://github.com/user-attachments/assets/29dda469-e17e-49c1-8919-36d5a2431bce)


     Result:

     1.DC analysis:

     The calculated drain current aligns with the expected value based on power and voltage, 
     with Id = 27uA. By adjusting the MOSFET's channel dimensions L = 180nm and W = 72.2um the 
     current requirement was successfully met. The circuit performs as expected under DC 
     conditions.

     2.Transient Analysis:

     The transient response graph shows the circuit's behavior over time. The response is 
     smooth, with no unexpected delays or distortions. The circuit reacts appropriately to 
     changes, indicating that it is stable and functions as expected.

     3.AC Analysis

     The ac response graph confirms us that the circuit will remain stable at different 
     frequencies,the circuit mainitains its performance across the tested frequency range.

    Inference

    The experiment confirms that by selecting the appropriate MOSFET dimensions, the drain 
    current can be effectively controlled.The width of the MOSFET significantly impacts the 
    drain current, indicating that any variation in width directly affects the output current.
    Increasing the width results in a higher Id, while decreasing the width reduces Id.The 
    design aligns with theoretical predictions and matches the practical values observed 
    in the experiment.


# Design-2

![Screenshot 2025-02-17 202320](https://github.com/user-attachments/assets/e216f2bb-7e24-436e-8c86-d88d0840e2d4)

   Aim : To find DC operating point find gain using transient analysis and AC analysis.

   Components : Mosfets M1 and M2 DC power supply.

   Procedure :

   Make the circuit connections as show abovce.
   Connect dc power supply to the gate terminal.
   Connect the source terminal to the ground.
   Set the input voltage by obtaining Vtc curve and Vdd to 1.8 V.

   Using the Formula for Power

   P=vi

   We will get the Values of Id

   Id= 27uA


   we have to get the output current Id for the given circuits by adjusting the values of L & W of both the MOSFETS

   
   by adjusting the value of width and length of the mosfet we will get the current Id 
   As length is given 180nm by adjusting we will get width=0.61um this value of width and length is for both the mosfet


   1.DC Analysis:

   
   To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation
     the figure below is the values obtained from the DC analysis
    
   ![Screenshot 2025-02-17 200103](https://github.com/user-attachments/assets/e687b280-d032-4260-8452-b10457103dfc)


   2. Transient Analysis

   
   To perform transient analysis we have to select the transient analysis in the edit simulation
   and give the stop time as 5ms and run the simulation .
   and the graph velow shows the transient response of the design.
   
   ![Screenshot 2025-02-17 200245](https://github.com/user-attachments/assets/05c9b471-494c-4c2e-9338-4be22166a47d)


   3. AC analysis
 

   TO perform AC analysis we have to select the ac analysis in the edit simulation command given the values as shown below

   ![Screenshot 2025-02-17 184334](https://github.com/user-attachments/assets/b5b9b5b2-cc27-459c-87d9-27411895f901)

   the Graph shown is the ac analysis


   ![Screenshot 2025-02-17 200501](https://github.com/user-attachments/assets/4071bada-50cb-40a9-a838-694d6bf27e26)


   RESULTS:

  1.DC analysis
  
  
  The calculated drain current Id aligns with the expected value based on power and voltage  where the value of Id = 27um 
  By fine-tuning the channel dimensions  of both MOSFETs  the desired current was achieved L=180nm and W=0.61um for both mosfets
  The circuit operates correctly within the selected DC parameters 

  
  2.Transient Analysis:

  The transient response graph confirms that the circuit transitions smoothly over time.
  The circuit responds effectively to input variations, indicating stable operation.

  
  3.AC Analysis:

  The AC response graph confirms that the circuit maintains stability over the tested frequency range.
  The circuit functions as expected under AC conditions.


  INFERENCE:


 the experiment validates that by choosing the correct mosfet dimensiions the drain current can be effectively regulated.

  The voltage transfer characteristics  helped to select the correct operating voltage  for saturation.

 M1  has a stronger influence on ID, meaning its width significantly affects the output current  Increase in width increases Id  and vice-versa.
M2 has a smaller influence on ID  meaning changes in its width result in only minor changes  in Id. Increase in width increases ID by small value and vice-versa.

     


