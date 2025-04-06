# Current mirror circuit

## Introduction

A current mirror is a circuit designed to replicate a current flowing through one active device by controlling the current in another active device within the same circuit. Its main purpose is to maintain a constant output current, regardless of variations in the load. Current mirrors are extensively used in analog integrated circuits—such as operational amplifiers—for providing biasing and acting as active loads.

They play a crucial role in ensuring that the current in one part of the circuit is accurately duplicated in another, which is vital for the stability and performance of analog systems. As one of the most fundamental building blocks in analog electronics, current mirrors find application in bias generation, active loading, and signal processing. Their ability to maintain a consistent current despite external changes makes them indispensable in the design of integrated circuits (ICs).

## Theory

The fundamental concept of a current mirror is to create a duplicate of a reference current in another part of the circuit. The most common approach involves using two transistors configured so that the base-emitter voltage (V_BE) of the first transistor—through which the reference current flows—is also applied to the second transistor. Since the transistors share the same V_BE and are typically matched, the second transistor conducts a current that closely mirrors the reference current.

This simple configuration allows the circuit to accurately replicate current, making it ideal for use in analog designs where constant bias currents are needed, or where current control is crucial.

Basic Current Mirror

![image](https://github.com/user-attachments/assets/428db9c0-b099-4581-9b57-156bdb51592c)

The simplest current mirror is typically built using either two identical BJTs or MOSFETs.

For BJTs:
The base and collector of the first transistor (used to set the reference current) are connected together, forcing it to operate in the active region. The base-emitter junctions of both transistors are connected in parallel, so they share the same V_BE. If the transistors are perfectly matched, this means the collector currents will be equal, effectively "mirroring" the reference current in the output branch.

For MOSFETs:
The gate and drain of the first MOSFET are tied together, putting it in saturation mode. The gates of both transistors are connected, ensuring that both devices have the same V_GS. Assuming identical device parameters and neglecting channel length modulation, both transistors will conduct the same drain current.

IREF = K'nCox (VGS - V TH)2

and

Iout = mn Cox (VGS - V TH)2

If we take ratio of two equations, we get,


Iref=Iout

## CIRCUIT DIAGRAM 1

![image](https://github.com/user-attachments/assets/790e3ea4-7a07-4d9e-9706-de67fbfd9ac3)

## Design Question

Design a current mirror circuit which has a gain of AV = -10V/V, power supply of Vdd = 1.8V, and power of P <= 1mW. Find reference current (Iref), output current (Id), and total current (Itotal). Perform DC and AC analysis for mirror ratio 1:1, 1:2.

### Design

The MOSFET should be in saturation region

V1>Vth

i.e 0.5>0.366


Itaotal=P/Vdd
Itotal=0.55mA

Itotal=Iref + Ip Iref=Ip=(Itotal)/2

Iref=Ip=0.27mA

### Simulation Outcones

This document presents the simulation results for the current mirror circuit with different L (length) values of MOSFETs. The simulation was conducted for three cases with varying L values.

## Case 1: L = 180 nm

### Simulation Output

![image](https://github.com/user-attachments/assets/df1af797-5733-440d-bb50-839b7041b803)

### Analysis

- Observation 1: W = 2.38u.
- Observation 2: W/L ratio of M1 and M2 transistors are maintained same 

## Case 2: L = 500 nm

### Simulation Output
 ![image](https://github.com/user-attachments/assets/d6cfb2b4-367b-4888-9b12-52dd8e94a3e0)

### Analysis

- Observation 1: W = 6.0649u
- Observation 2: W/L ratio of M1 and M2 transistors are maintained same i,e 1:1 .

## Case 3: L = 1 µm


### Simulation Output

![image](https://github.com/user-attachments/assets/9261a6f9-eac2-419b-8297-90e51494b21a)

### Analysis

- Observation 1: W=12.46u.

- Observation 2: W/L ratio of M1 and M2 transistors are maintained same i,e 1:1 .

## Special Case: W/L Ratio of M1:M2 = 1:2

![image](https://github.com/user-attachments/assets/b0b8e354-04cb-4daa-8e68-d78631fbc2d7)


### Analysis

- **Observation 1**: Width is kept at 180nm and length were M1:M2 = 2.38u:4.76u
- **Observation 2**: W/L ratio of M1 and M2 transistors are maintained same i,e 1:2 .

  ## Transient analysis 
### SIMULATION OUTPUT







![Screenshot 2025-03-24 020658](https://github.com/user-attachments/assets/a2c43cd8-6813-4cc8-abf4-eeddf8768689)

- **Observation** MaxOutSwing =  1.175V<sub>p-p</sub>
  
## AC ANALYSIS
### SIMULATION OUTPUT


![Screenshot 2025-03-24 021536](https://github.com/user-attachments/assets/0eed4042-a21b-4a33-97ae-8d705ae847a0)


- **Observation** BW = 2.122GHz 


## **ADVATAGES**
  <p>
1] Does not become sensitive to PVT parameters .

 ![Screenshot 2025-03-24 002513](https://github.com/user-attachments/assets/3310f5dd-6f76-45e0-ace9-0c2b4ff571cc)

 2] Rejecting voltage biasing.
 
 # Results


| Case       | L (Length) | W (Width) | W/L Ratio |
|------------|------------|-----------|-----------|
| Case 1     | 180 nm     | 2.38 µm   | 1:1       |
| Case 2     | 500 nm     | 6.0649 µm | 1:1       |
| Case 3     | 1 µm       | 12.46 µm  | 1:1       |
| Special    | 180 nm     | 4.76 µm   | 1:2       |


## Inferences

- Maintaining consistent W/L ratios for the MOSFETs ensures predictable operation of the current mirror.
- As the length (L) of the MOSFETs increases, the width (W) also increases to maintain the same W/L ratio.
- The special case with a W/L ratio of 1:2 shows that the current mirror can be adjusted for different mirroring ratios.
- The total current (I_total) was calculated based on power supply and constraints, resulting in I_total = 0.55 mA, with I_ref and I_p each being 0.27 mA.
- Ensuring MOSFETs operate in the saturation region (V_1 > V_th) is crucial for proper functioning of the current mirror.

  ## CIRCUIT DIAGRAM 2
![image](https://github.com/user-attachments/assets/7d2cbe1e-88d8-4500-aa88-74487d6b3bc2)

### DC ANALYSIS 

![image](https://github.com/user-attachments/assets/ed562f99-b64b-44a9-b439-5413c8368bcc)


- **Observation** We can observe that current accross M6 and M3 transistors are almost double because of 1:2 W/L ratio 

- **Observation** We can observe that current accross M5 and M4 transistors are same because of 1:1 W/L ratio 

### TRANSIENT ANALYSIS 
![image](https://github.com/user-attachments/assets/e7c8540a-1c43-4fba-a4ab-9f1a69178629)


- **Observation** A<sub>v</sub>=Vout/V<sub>in</sub>
- <p>
i,e = 1.53/0.099 =15.45 v/v


### AC ANALYSIS 

![image](https://github.com/user-attachments/assets/c17724f5-842e-41b3-b787-99a0176e08f5)

- **Observation** B<sub>w</sub>=1.94G<sub>Hz</sub>

## INFERENCE 


 ### Current Accuracy
- **1:1 Ratio**: Higher accuracy owing to identical transistor sizes.
- **1:2 Ratio**: Slight difference observed due to varying transistor widths.
- **Inference**: The 1:1 ratio offers superior current matching.

### Transistor Sizing
- **1:1 Ratio**: Utilizes smaller transistors, thus requiring less chip area.
- **1:2 Ratio**: Necessitates larger transistor widths, leading to increased area consumption.
- **Inference**: The 1:1 ratio is more efficient in terms of chip area usage.

### Output Resistance
- **1:1 Ratio**: Exhibits higher output resistance, as a longer channel length (L) reduces lambda, thereby increasing r<sub>out</sub>.
- **1:2 Ratio**: Shows slightly lower output resistance since larger transistor widths may introduce mismatch, slightly affecting lambda.
- **Inference**: The 1:1 ratio provides better stability due to higher output resistance.

### Power Consumption
- **1:1 Ratio**: Consumes less power due to the use of smaller transistors.
- **1:2 Ratio**: Consumes slightly more power because of the increased transistor sizes.
- **Inference**: The 1:2 ratio results in higher power consumption due to larger devices.

### Design Complexity
- **1:1 Ratio**: Easier to implement and match.
- **1:2 Ratio**: Requires precise selection of transistor width.
- **Inference**: The 1:1 ratio is simpler to design and optimize.











