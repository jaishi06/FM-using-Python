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
import numpy as np
import matplotlib.pyplot as plt
Am = 3.2
Ac = 6.4
fm = 217
fc = 2170
fs = 21700
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
integral_m = np.cumsum(m) / fs
s = Ac * np.cos(2 * np.pi * fc * t + 2 * np.pi * kf * integral_m)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()

Output Waveform

<img width="856" height="567" alt="fm code new" src="https://github.com/user-attachments/assets/a42712e0-e882-4827-9cf9-b309cd60108b" />


Tabular Column

![WhatsApp Image 2025-11-27 at 21 14 45_11f0b183](https://github.com/user-attachments/assets/14eef3c3-8cde-45ff-8fe6-63d3cd306cc0)


Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
