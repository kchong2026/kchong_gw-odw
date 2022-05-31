# Introduction to GW Data Analysis
##### Notes from the videos follow:
## Time Series Data
##### Nyguist frequency = fs / 2
###### Discretely sampled data with sampling rate fs can represent a continuous signal which only has frequency content below the Nyquist freqency
##### Data can only contain frequency content below the Nyquist frequency: higher frequency signals will be lost or "aliased" to lower frequencies
#
## Frequency Domain Data
##### Time-series data may be represented in the frequency domain
###### Fourier Transform or FFT (Fast Fourier Transform) used to transform between the domains
###### Shows amount of energy in each frequency bin
##### Noise can be characterized by its statistical properties
###### "Nice" noise is Guassian and stationary
##### A power-spectral density (PSD) can be used to characterize the average noise power in each frequency bin
###### Can estimate a PSD as a median or average FFT over multiple segments 
###### Amplitude spectral density: (ASD)
