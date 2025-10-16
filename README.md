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
am = 5.6;
fm = 464;
ac = 11.2;
fc = 4640;
fs = 46400;
t = 0:1/fs:3/fm;

m1=am*cos(2*3.14*fm*t);
subplot(2,2,1);
plot(t,m1);
title('Message signal m1');

c1=ac*cos(2*3.14*fc*t);
subplot(2,2,2);
plot(t,c1);
title('Carrier signal c1');

m2=am*sin(2*3.14*fm*t);

c2=ac*sin(2*3.14*fc*t);

s1=c1.*m1;
s2=c2.*m2;
slsb=s1+s2;
subplot(2,2,3);
plot(t,slsb);
title('S LSB');

susb=s1-s2;
subplot(2,2,4);
plot(t,susb);
title('S USB');

OUTPUT WAVEFORM
<img width="757" height="673" alt="image" src="https://github.com/user-attachments/assets/af71d9e6-39df-4f63-a8a5-8078c83f719a" />

TABULATION
<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/7651e0ea-5779-4180-a8b5-572e973abccd" />









RESULT:

Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.





