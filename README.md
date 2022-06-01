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
#

## Binary Black Hole Signals
##### Compact Binary Coalescence: (CBC) 
##### CBC Waveform: GW Frequency = 2x Orbital Frequency
###### Lots of signal energy at low frequency: black hole system spends a longer time at lower frequencies (many low frequency orbits)
###### "Cut-off" near the merger frequency
##### Spectrogram (Q-transform): x = time and y = frequency (illustrated by colored bands)
##### How long is the waveform?
###### Black holes orbit more millions (or billions) of years but LIGO only "sees" events for a few seconds or less
###### Shot noise dominates at high frequencies (uncertainties in the number of photons), controls noise at low frequencies (radiation and seismic pressures), and thermal noise (from molecular movement) is rather consistent throughout
###### LIGO is most sensitive in "The Bucket": ~100-300 Hz
###### Beam splitter suspensions: 300 Hz
###### "Violin" modes: 500 Hz and 1000 Hz
#

## Finding Signals in Noise
##### Use filtering to reduce noise
###### Highpass filter: "passes" (or keeps) only high frequencies
###### Lowpass filter: passes only low frequencies
###### Bandpass filter: keeps signal only in the pass band
###### Whitening: "Flatten" the data so there is equal noise at all frequencies
