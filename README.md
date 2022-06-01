# Introduction to GW Data Analysis
##### Notes from the videos follow:

## Time Series Data
#### Nyquist frequency = fs / 2
##### Discretely sampled data with sampling rate fs can represent a continuous signal which only has frequency content below the Nyquist freqency
##### Data can only contain frequency content below the Nyquist frequency: higher frequency signals will be lost or "aliased" to lower frequencies
#

## Frequency Domain Data
#### Time-series data may be represented in the frequency domain
##### Fourier Transform or FFT (Fast Fourier Transform) used to transform between the domains
###### Shows amount of energy in each frequency bin
##### Noise can be characterized by its statistical properties
###### "Nice" noise is Guassian and stationary
##### A power-spectral density (PSD) can be used to characterize the average noise power in each frequency bin
###### Can estimate a PSD as a median or average FFT over multiple segments 
###### Amplitude spectral density: (ASD)
#

## Binary Black Hole Signals
#### Compact Binary Coalescence: (CBC) 
##### CBC Waveform: GW Frequency = 2x Orbital Frequency
###### Lots of signal energy at low frequency: black hole system spends a longer time at lower frequencies (many low frequency orbits)
###### "Cut-off" near the merger frequency
#### Spectrogram (Q-transform): x = time and y = frequency (illustrated by colored bands)
#### How long is the waveform?
###### Black holes orbit more millions (or billions) of years but LIGO only "sees" events for a few seconds or less
###### Shot noise dominates at high frequencies (uncertainties in the number of photons), controls noise at low frequencies (radiation and seismic pressures), and thermal noise (from molecular movement) is rather consistent throughout
##### LIGO is most sensitive in "The Bucket": ~100-300 Hz
###### Beam splitter suspensions: 300 Hz
###### "Violin" modes: 500 Hz and 1000 Hz
#

## Finding Signals in Noise
#### Use filtering to reduce noise
###### Highpass filter: "passes" (or keeps) only high frequencies
###### Lowpass filter: passes only low frequencies
###### Bandpass filter: keeps signal only in the pass band
###### Whitening: "Flatten" the data so there is equal noise at all frequencies
#

# GW Open Data Workshop
##### Notes from the video follow:

## Gravitational wave detectors
#### Contributions to sensitivitiy
##### Quantum shot
##### Quantum radiation pressure
##### Thermal
##### Seismic
##### Newtonion
#### Calibrating with photons
##### Well calibrateed auxillary laser sends light to mirrors
##### Calibration lines are always pressent in observational data to monitor the accuracy of calibration
#### Calibration uncertainty
###### Systematic error reports how well we understand our calibration
#

## Public data
##### 3 events during O1, 8 events during O2, 44 events during O3a, 35 events during O3b (90+ confident events in the GWTC)
#### Catalogs
##### A catalog corresponds to a public release, or a publication
###### GW Transient Catalog (GWTC)
###### GWTC-1: O1 and O2 runs
###### GWTC-2: O3a runs
###### GWTC-3: O3b runs
#### Event versions
##### A detection can be analyzed multiple times for different reasons (different calibration, cleaning techniques, publications, ...)
###### Every new analysis produces a new version of the event and versions typically belong to different catalogs
#### Event Strain Data
##### Download strain files around the event
###### Formats: GWF, HDF, TXT
###### Sampling: 4kHz, 16kHz
###### Length: 32s, 4096s
#

## Data Quality
#### Strain data: post processing
###### Raw time series
###### Whitened data
###### Bandpassed data
##### Q transfrom allows us to visualize the data in time frequency space
###### Helps explain noise morphology, noise identification and classification, and potential correlations with other parts of the instrument
#### Improving sensitivity
##### Higher laser power
##### New test mirrors
##### Light squeezing
##### Fixing sources of noise
###### Seismic noise at low frequency and shot noise (uncertainty in the number of photons hitting the detector: quantum noise) at high frequency limit sensitivity
#### Noise transients
##### Also known as glitches or excess power over a short duration
##### Detected using the omicron tool
##### Caused by ground motion, thunderstorms, changes in humidity...
##### Transients can mask a real GW signal, reduce our confidence in the detection, reduce the astrophysical range and introduce problems for the parameter extimation
#### Detector characterization tools and transient noise reduction
##### What to do about the transient noise?
###### Identify the noise
###### Look for potential correlations with the auxillery channels and subsystems
###### Perform tests to simulate the noise
###### Fix the source of noise to reduce or eliminate it
###### Develop Vetoes
##### Detchar Tools
###### GravitySpy: uses Omicron triggers as the input and the output is the predicted glitch category 
###### Q Transform: visualizing glitch morphology in the time-frequency plane
###### Hveto: finds statistic correlations between noise in GW strain channel and auxillary channels then assigns a significance
###### Gwdetchar Scattering
###### Omicron
###### CAT Vetoes
###### Hardware injections: when we inject a signal that physically actuates one of the test masses (establishes safety of vetoes, safe and unsafe auxillary channels)
###### Summary pages
#### O3 Summary:
##### Split between O3a (April 1, 2019 - Sept. 30, 2019) and O3b (Nov. 1, 2019 - March 27, 2020)
##### 74 GWs detected, 39 in O3a and 35 in O3b
##### Includes  signals from BBH, BNS and NSBH
#### Preparations for O4
##### Scheduled for Dec. 2022
##### Higher sensitivity: a lot more GWs
