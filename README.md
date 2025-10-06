# Design-of-FIR-Filters-using-rectangular-window
#  DESIGN OF LOW PASS FIR DIGITAL FILTER 

# AIM: 
          
  To generate design of low pass FIR digital filter using SCILAB 

# APPARATUS REQUIRED: 

  PC Installed with SCILAB 

# PROGRAM 
```python
clc;
clear;
close;

// Filter specifications
forder = 33;                     // Filter order (odd number)
cutoff_frequency = 0.2;          // Normalized cutoff frequency (0 < cutoff <= 0.5)
window_type = "hm";              // Hamming window ("re" for rectangular, "hm" for Hamming, etc.)
window_params = [0, 0];          // Window parameters (for Kaiser and Chebyshev windows)

// Design FIR low pass filter and get frequency response
[h, h_freq, fr] = wfir("lp", forder, [cutoff_frequency, 0], window_type, window_params);

// Display filter coefficients
disp(h, "Filter Coefficients:");

// Plot magnitude response
scf(0);
subplot(2,1,1);
plot(fr, abs(h_freq));
xlabel("Normalized Frequency");
ylabel("Magnitude");
title("Frequency Response Magnitude of FIR Low Pass Filter");

// Plot magnitude in dB
subplot(2,1,2);
plot(fr, 20*log10(abs(h_freq)));
xlabel("Normalized Frequency");
ylabel("Magnitude (dB)");
title("Frequency Response (dB) of FIR Low Pass Filter");
```


# OUTPUT
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/30adb8f9-45d3-4cbf-9557-a99d2a9e27f8" />


# RESULT
THE DESIGN OF LOW PASS FIR DIGITAL FILTER IS SUCCESSFULLY COMPLETED USING SCILAB.
