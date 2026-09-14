# 2.-Design-implement-and-simulatioin-of-Integrator-and-Differentiator
**AIM:**
To design , implement and simulate  an integrator and differentiator circuits

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range	Quantity
1.	Signal Generator	3 MHz	1
2.	DSO	30 MHz	1
3.	Dual RPS	(0 – 30) V	1
4.	Op-Amp	µA741	1
5.	Bread Board		1
6.	Resistors	1K,10K,100K,	2
7.	Capacitors	0.1µF,0.01µF	1
8.	Connecting wires and probes	As required	
9.  LT SPICE software

**THEORY:**

**INTEGRATOR**
A circuit in which the output voltage waveform is the integral of the input voltage waveform is the integrator. Such a circuit is obtained by using a basic inverting amplifier configuration if the feedback resistor Rf is replaced by a capacitor Cf . The expression for the output voltage is given as,
Vo = - (1/Rf C1 ) ∫ Vi dt

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. Normally between fa and fb the circuit acts as an integrator. Generally, the value of fa < fb . The input signal will be integrated properly if the Time period T of the signal is larger than or equal to Rf Cf . That is,
T ≥ Rf Cf

The integrator is most commonly used in analog computers and ADC and signal-wave shaping circuits.

**DESIGN:**
 
To obtain the output of an Integrator circuit with component values R1Cf = 0.1ms , Rf = 10 R1 and Cf = 0.01 µF and also if 1 V peak square wave at 1000Hz is applied as input.
We know the frequency at which the gain is 0 dB, fb = 1 / (2π R1 Cf) Therefore fb = 	 Since fb = 10 fa , and also the gain limiting frequency fa = 1 / (2π Rf Cf)
We get , R1 =	and hence Rf = 	

**DIFFEERENTIATOR:**

The differentiator circuit performs the mathematical operation of differentiation; that is, the output waveform is the derivative of the input waveform. The differentiator may be constructed from a basic inverting amplifier if an input resistor R1 is replaced by a capacitor C1 . The expression for the output voltage is given as,
Vo = - Rf C1 ( dVi /dt )

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. A resistor Rcomp = Rf is normally connected to the non-inverting input terminal of the op-amp to compensate for the input bias current. A workable differentiator can be designed by implementing the following steps:
1.	Select fa equal to the highest frequency of the input signal to be differentiated. Then, assuming a value of C1 < 1 µF, calculate the value of Rf.
2.	Choose fb = 20 fa and calculate the values of R1 and Cf so that R1C1 = Rf Cf.

The differentiator is most commonly used in wave shaping circuits to detect high frequency components in an input signal and also as a rate–of–change detector in FM modulators.
 
**DESIGN (DIFFERENTIATOR):**

Design an op-amp differentiator that will differentiate an input signal with fmax = 100HZ Select fa = fmax = 100 HZ = 1 / 2πRFC1
Let C1 = 0.1μF
Then RF = 1 / 2π(102)(10-7)
= 15.9KΩ
Now choose fb = 10fa = 1 / 2πR1C1 Therefore, R1 = 1 / 2π(103)(10-7)
= 1.59KΩ Since RFCF = R1C1
We get, CF = (1.59*103*10-7) / 15.9*103
= 0.01μF


**PROCEDURE:**
1.	Connections are given as per the circuit diagram
2. + Vcc and - Vcc supply is given to the power supply terminal of the Op-Amp IC.
3.	By adjusting the amplitude and frequency knobs of the function generator, appropriate input voltage is applied to the inverting input terminal of the Op- Amp.
4.	The output voltage is obtained in the CRO and the input and output voltage waveforms are plotted in a graph sheet.

 
**INTEGRATOR:**
  **CIRCUIT DIAGRAM**
  
<img width="673" height="342" alt="image" src="https://github.com/user-attachments/assets/cb9bb860-2f76-498a-b894-eca11d8dfcc9" />


  **MODEL GRAPH:**
  
<img width="587" height="360" alt="image" src="https://github.com/user-attachments/assets/33902be2-5eb2-4096-9dc7-86ba4caca099" />

<img width="762" height="472" alt="image" src="https://github.com/user-attachments/assets/3637de74-f46b-4bdb-8652-eaa203695036" />



  **TABULATION:**
<img width="900" height="1600" alt="WhatsApp Image 2026-09-14 at 9 59 21 PM" src="https://github.com/user-attachments/assets/e968194e-2f2d-47c0-9678-52535547ca3d" />
<img width="900" height="1600" alt="WhatsApp Image 2026-09-14 at 9 59 21 PM (1)" src="https://github.com/user-attachments/assets/526f9f49-f91e-4a26-a99f-494346bf81a6" />


**MODEL CALCULATION:**

**DIFFERENTIATOR:**
  **CIRCUIT DIAGRAM**
  
  <img width="636" height="367" alt="image" src="https://github.com/user-attachments/assets/698594d6-e334-4800-b999-62f89b0dae79" />



  **MODEL GRAPH:**
  
<img width="451" height="552" alt="image" src="https://github.com/user-attachments/assets/03bef15d-041e-4f01-a83f-b3b754b77c66" />


  **TABULATION:**

<img width="900" height="1600" alt="WhatsApp Image 2026-09-14 at 9 59 21 PM (2)" src="https://github.com/user-attachments/assets/0a808a6c-7776-4029-961d-972bac4d28c2" />
<img width="900" height="1600" alt="WhatsApp Image 2026-09-14 at 9 59 21 PM (3)" src="https://github.com/user-attachments/assets/8cd5c7df-7246-436d-8388-5feddf4b2a41" />




 **Graph**

 <img width="900" height="1600" alt="WhatsApp Image 2026-09-13 at 6 25 09 PM" src="https://github.com/user-attachments/assets/7b331dfc-a360-423a-82f5-24d3b9d5f4fa" />
 <img width="900" height="1600" alt="WhatsApp Image 2026-09-13 at 6 25 10 PM (1)" src="https://github.com/user-attachments/assets/aae627eb-34d3-4f00-b1b3-02a7bf68cdda" />




**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**
  <img width="900" height="1600" alt="WhatsApp Image 2026-09-14 at 10 02 29 PM" src="https://github.com/user-attachments/assets/db49cefe-b02a-4913-82f4-f13e0ce01812" />
<img width="900" height="1600" alt="WhatsApp Image 2026-09-14 at 10 02 29 PM (1)" src="https://github.com/user-attachments/assets/cb4d1274-a694-485c-b8b1-0a5ce1e15904" />


**RESULT:**
Thus the Integrator and Differentiator are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
