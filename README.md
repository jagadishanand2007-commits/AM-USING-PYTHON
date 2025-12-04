# AM-USING-PYTHON
# Aim
To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 
# Apparatus Required
1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
# Theory
Amplitude Modulation (AM) is a method of transmitting information over a carrier wave by varying its amplitude in accordance with the amplitude of the input signal (message signal). The amplitude of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an AM signal is:
# Algorithm
1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

# Program
import numpy as np
import matplotlib.pyplot as plt
```
import numpy as np
import matplotlib.pyplot as plt

Am=4.0
Ac=8.0
fc=3390
fm=339
fs=33900
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
eam=(Ac+Am*np.cos(2*np.pi*fm*t))*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,1)
plt.plot(t,m)
plt.show()
plt.subplot(3,1,2)
plt.plot(t,c)
plt.show()
plt.subplot(3,1,3)
plt.plot(t,eam)
plt.show()
plt.show()
```
# Output Waveform
<img width="750" height="573" alt="image" src="https://github.com/user-attachments/assets/7d0ac303-ad71-4075-b278-132fd98e274b" />

## Tabular Column
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/26136e90-6fbc-43fd-b853-5e04d69d2b38" />


## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
