# SSB

EXP NO: 3	SSB-SC-AM MODULATION using SCILAB

AIM:

To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

Note: Keep all the switch faults in off position


Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: The baseband signal that will be modulated.
•	Carrier Signal: A high-frequency signal used for modulation.
•	Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.
3.	SSBSC Modulation:
•	Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.
4.	SSBSC Demodulation:
•	Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.
•	Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.
5.	Visualization:
•	Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.


PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="704" height="178" alt="image" src="https://github.com/user-attachments/assets/32ee29b3-0d95-4192-9762-972d50c05c90" />
<img width="706" height="167" alt="image" src="https://github.com/user-attachments/assets/bff0d8fd-d679-444e-af37-0b34585853c1" />

Program
```
clc;
clear;

Am = 9.09;
fm = 842;
Ac = 18.18;
fc = 8420;
fs = 84200;

t = 0:1/fs:2/fm;

em1 = Am*cos(2*%pi*fm*t);

subplot(4,1,1);
plot(t, em1);

em2 = Am*sin(2*%pi*fm*t);

ec1 = Ac*cos(2*%pi*fc*t);

subplot(4,1,2);
plot(t, ec1);

ec2 = Ac*sin(2*%pi*fc*t);

edsbsc1 = em1 .* ec1;
edsbsc2 = em2 .* ec2;

elsb = edsbsc1 + edsbsc2;

subplot(4,1,3);
plot(t, elsb);

eusb = edsbsc1 - edsbsc2;

subplot(4,1,4);
plot(t, eusb); 
```
OUTPUT WAVEFORM

<img width="1007" height="902" alt="image" src="https://github.com/user-attachments/assets/217b6d6f-1ab1-4b68-9599-2a009375582c" />


TABULATION



<img width="4241" height="2608" alt="72158d61-f560-4673-af58-473d97ac9a97~1" src="https://github.com/user-attachments/assets/72ac6a3d-2d67-48a1-81ae-e073fec92b97" />









RESULT:

Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.





