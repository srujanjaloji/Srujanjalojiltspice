# LIC EXPERIMENT-3
linear integrated circuits
# Aim:
Design and analyze the differential amplifier for the following steps VDD=3.3v, P<=3mw, Vicm =1.72v,Vocm=1.81v,Vp=0.7v perform DC analysis,transient analysis,frequency response and extract the parameters.

Differential Amplifier:

A differential amplifier consists of two transistors, M1 and M2, with their source terminals connected together. When different voltage signals are applied to the gate terminals of these transistors, the current flowing through M1 and M2 varies accordingly. However, if the gate terminals receive identical voltage inputs, the currents through both transistors remain equal. This arrangement is known as a "Common-Mode Input Voltage Differential Amplifier." Regardless of the load resistor used, it is essential to ensure that MOSFETs M1 and M2 do not operate in the Triode region. For the amplifier to function correctly, both transistors must stay in the Saturation region.

![image](https://github.com/user-attachments/assets/3c5dd8db-5be5-4177-aeb6-1e8dcb67f5c0)

Procedure : Make the circuit connection as given above. connect the resister at the source terminal of both mosfet now calculate the value of Iss as power and vdd is given and calculate the Id1 and Id2 now calculate the Rss and Rd

To find the all the values of resistor and current value. we need solve the given queston specification.
P=2.5mA

Iss=P/VDD=2.5*10^-3/3.3=0.7575mA

Is1=Is2=Iss/2=0.3787mA

RD=VDD-Vocm/Iss=3.3-1.81/0.3787*10^3=3.93kΩ

Rss=Vp/Iss=0.7/0.757*10^-3=0.924kΩ

Finially by solving we get

Iss=0.7575mA

I1=I2=0.3787mA

RD=3.93kΩ

Rss=0.924kΩ


# Circuit-1
Components Required: MOSFET(M1,M2 and M3), Resistor,voltage supply's

![Screenshot 2025-03-09 222825](https://github.com/user-attachments/assets/36817283-107f-48cd-8e2b-443592a0c076)



Now to get the desired values of output voltage and current we have to vary the width and length of both the mosfet we got Length=180nm and width=2.0558um

![Screenshot 2025-03-09 223254](https://github.com/user-attachments/assets/44c83e0e-02f1-45db-8d40-979793f962b5)


# DC analysis:
To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation the figure below is the values obtained from the DC analysis
 ![Screenshot 2025-03-09 223410](https://github.com/user-attachments/assets/dfd93663-0cc4-4a37-b2b2-396fd88df033)


Here in dc analysis we got the vout as expected and id1 and id2 we got the same

# Transient analysis:
To perform transient analysis we have to select the transient analysis in the edit simulation and give the stop time as 5ms and run the simulation . and the graph velow shows the transient response of the design.
![Screenshot 2025-03-09 223609](https://github.com/user-attachments/assets/95e4c12d-532e-4dea-97e8-343183083e1d)

voltage gain 
AV=voutp-p/vinp-p

AV=(1.875-1.7504)/(1.7705-1.6709)

AV=1.251

# AC analysis:
TO perform AC analysis we have to select the ac analysis in the edit simulation command given the values as shown below
![Screenshot 2025-03-09 223716](https://github.com/user-attachments/assets/5ccdaac2-1c29-4128-b2d8-a7977ee94eff)


Gain in db= 20log(AV)

  =20log(1.251)
 
  =1.945

  # Circuit-2:
  Now replace the R3 resister with a current source : connect a current souce of 0.9mA

![Screenshot 2025-03-09 225638](https://github.com/user-attachments/assets/e851919d-0a4a-41c9-9400-8ef9075614d2)



# DC analysis:
To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation the figure below is the values obtained from the DC analysis

![Screenshot 2025-03-09 225139](https://github.com/user-attachments/assets/f66af5d6-8bc5-44e6-96a4-0c4ea8f77c8e)


 # Transient analysis:

 To perform transient analysis we have to select the transient analysis in the edit simulation and give the stop time as 5ms and run the simulation . and the graph b
 elow shows the transient response of the design

we have to give deg of 180deg to one mosfet and 0deg to the other mosfet and ac amplitude 1 for one mosfet and 0 for other mosfet

![Screenshot 2025-03-09 230118](https://github.com/user-attachments/assets/0f508a26-9d26-44d8-9317-0a53f9f24c5f)



voltage gain 
AV=voutp-p/vinp-p

AV=(1.9708-1.6531)/(1.7709-1.6684)

AV=3.09951

# AC analysis:
![Screenshot 2025-03-09 225746](https://github.com/user-attachments/assets/b9d0000f-8f5a-491f-b931-c10e020ea144)


Gain in db= 20log(AV)

  =20log(2.598)

  =9.825

  # Circuit-3:
Now replace the R3 resister with a Mosfet : Given vp=0.4v and wkt vt=0.36v we got the gate voltage of the new mosfet as 0.866v

![Screenshot 2025-03-09 234444](https://github.com/user-attachments/assets/cfc48ad8-6cb0-4468-b52a-12b8bc7c97b6)




To get the output voltage and vp and current desired value we have to vary the width and length of the  mosfets

![Screenshot 2025-03-09 232412](https://github.com/user-attachments/assets/7697bb6a-91f0-4809-b0d6-73d3757a0287)![Screenshot 2025-03-09 232422](https://github.com/user-attachments/assets/5e520066-c801-4397-9a8f-be0d985a64ee)



# DC analysis:
![Screenshot 2025-03-09 234407](https://github.com/user-attachments/assets/4bf0c05d-bc58-443d-b291-41dbf23c7644)




# Transient analysis:
give ac amplitude as 1 for one mosfet and 0 for other mosfet
![Screenshot 2025-03-09 234324](https://github.com/user-attachments/assets/0b11a8ca-1a59-42ff-b50c-833ae79f9106)



# AC analysis: 

![Screenshot 2025-03-09 234216](https://github.com/user-attachments/assets/aa76b850-516c-4fcd-be96-b981dbf62a56)




# INFERENCE:
In this experiment, we seen the operating principles of a differential amplifier and its types and setups.  

There are three kinds of setups were used: resistor, current source, and NMOS. All the setups work in different ways, which causes a change in Voltage gain and stability of a MOSFET.  

 When resistor is connected, it gives low CMRR, lower voltage gain, but high bandwidth, and it also provides negative feedback.  
 But when using a current source, it works opposite to the resistor setup because it has higher voltage gain, higher CMRR, but a little reduced bandwidth than the resistor setup.  
 The CMOSN setup gives the highest voltage gain among all.  

From this, we can understand which setup is useful in which situation:  

1. Need more Bandwidth -  Use Resistor setup  
2. Need more Gain - Use CMOSN setup  
3. Need better CMRR - Use Current source or CMOSN setup













  
