# EXP NO: 6 DSBSC-using-Python

DSBSC Modulation and Demodulation using NumPy and Matplotlib

Aim:

To implement and analyze DSBSC modulation using Python's NumPy and Matplotlib libraries.

Apparatus :

                      Software: Python with NumPy and Matplotlib libraries
                      Hardware: Personal Computer

Algorithm:

           1. Initialize Parameters: Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency(fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp).

           2. Generate Time Axis: Create a time vector for the signal duration based on the sampling frequency.

           3. Generate Message Signal: Define the message signal as a cosine wave.

           4. Generate PM Signal: Apply the PM modulation formula to obtain the modulated signal.

           5. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.

Program:

    import numpy as np
    import matplotlib.pyplot as plt
    Am = 20.4
    fm = 404
    Ac = 40.8
    fc = 4040
    fs = 40400
    t = np.arange(0, 2/fm, 1/fs)
    m = Am * np.cos(2 * np.pi * fm * t)
    c = Ac * np.cos(2 * np.pi * fc * t)
    s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
    s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
    s = s1 - s2
    plt.subplot(3,1,1)
    plt.plot(t, m)
    plt.subplot(3,1,2)
    plt.plot(t, c)
    plt.subplot(3,1,3)
    plt.plot(t, s)

Output Waveform:

<img width="558" height="413" alt="download" src="https://github.com/user-attachments/assets/49a5909a-9267-4577-afc6-cc47edf0ee5a" />


Tabular Column:

![WhatsApp Image 2025-10-15 at 13 10 35_676949bb](https://github.com/user-attachments/assets/d786c2bf-4ada-424b-994c-5ddf6bbb8a21)


Result:

The message signal, carrier signal, and DSBSC signal will be displayed in separate plots.

Thus DSBSC is implemented using numPy and Matplotlib.
