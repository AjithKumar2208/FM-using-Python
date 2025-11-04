# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program 
```

import numpy as np
import matplotlib.pyplot as plt
Am=5.6
Ac=11.2
fm=464
fc=4640
fs=464000
b=4.9
t=np.arange(0,2/fm, 1/fs)
m=Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
efm=Ac*np.cos((2*3.14*fc*t) + b*np.sin(2*3.14*fm*t))
plt.subplot(3,1,3)
plt.plot(t,efm)

```
Output Waveform

<img width="554" height="413" alt="image" src="https://github.com/user-attachments/assets/5777bfb6-9700-4154-914b-a48a0ccc4d06" />



Tabular Column

![WhatsApp Image 2025-11-04 at 21 43 55_dd5966c4](https://github.com/user-attachments/assets/aa932a7d-668e-4a9e-9947-1d146a943bd5)



Calculation

![WhatsApp Image 2025-11-04 at 21 49 26_ccb77f44](https://github.com/user-attachments/assets/822d696b-7a66-433d-8472-339db105cbb9)



Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
