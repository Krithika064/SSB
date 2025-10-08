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
am=3.5;
fm=295;
fs=29500;
ac=7.0;
fc=2950;
t=0:1/fs:2/fm
m1=am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,m1);
c1=ac.*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,c1);
m2=am*cos(1.57-(2*3.14*fm*t));
c2=ac.*cos(1.57-(2*3.14*fc*t));
a=c1.*m1;
b=c2.*m2;
c=a+b;
d=a-b;
subplot(4,1,3);
plot(t,c);
subplot(4,1,4);
plot(t,d);
```

OUTPUT WAVEFORM
<img width="1919" height="1118" alt="Screenshot 2025-10-08 221702" src="https://github.com/user-attachments/assets/1a737f3d-7608-443b-873b-68bfe7c89aa6" />

TABULATION
![WhatsApp Image 2025-10-08 at 22 19 06_8300ff15](https://github.com/user-attachments/assets/a596a7c9-3247-4ec8-8a4f-090ebce0f1c6)

RESULT:

Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.





