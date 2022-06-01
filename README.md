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
#

## Physics and Astronomy with Compact Binary Coalescences
##### Black holes: "densest" objects in the universe, not even light can escape-completely dark
##### Neutron stars: still unimaginably dense, but not completely dark-extreme matter
##### Black holes and neutron stars are the byproducts of the end stage of stellar evolution: massive star --> supernova --> neutron star or black hole (stellar graveyard)
##### WHen two compact objects coalesce, they source loud graviation waves
###### 3 phases: inspiral, merger, and ringdown
#### Graviational waves encode source properties
##### The masses of the two compact objects
##### The spin of the compact objects
##### Where and when the mergers occured
##### How squishy neutron stars are
#### Learning about the full populaiton of compact objects
##### A population model describes the distribution of masses, spins, etc. across multiple events
##### Example: fit a power law to black hole masses
###### Population parameters: power law slope, minimum and maximum black hole mass
#

## CBC Searches
#### Compact binary coalescenses
##### As objects orbit, they lose energy to GWs: the orbit shrinks and speeds up releasing more energy to GWs
##### Frequency and amplitude of GWs increases monotonically
###### Creates a runaway process leading to inspiral and merger
##### Waveforms model the inspiral, merger, and ringdown of the binary
##### Intrinsic parameters: masses and spins
##### Extrinsic parameters: sky position, inclination, time of arrival, phase
#### Assumptions of the LIGO data
##### We assume that strain data from the detectors consists of a possible signal and additive noise
##### We assume that the noise is stationary and Gaussian
###### Stationary: the noise properties are constant in time
###### Gaussian: the noise values follow normal distribuitons which we can transform to have 0 mean
#### Matched filtering as cross correlation
##### If we know what the signal looks like, we can use matched filtering to find signals in the data
###### Matched filtering is a correlation of a template waveform with the data
###### Matched filter output is the signal-to-noise ration SNR time-series
##### Matched filtering output
##### Peaks in the SNR time-series are used to identify triggers in the data
##### Coincident SNR peaks in the data from multiple detectors increases the significance
#### Modeling the waveforms
##### Matched filtering releis on knowing the shape of the signal
###### For CBC waveforms we can model the signals with template waveforms
##### We construct template banks of waveforms that vary over the instrinsic parameters
###### 4D template banks - {m1, m2, s1z, s2z}
#### How many templates do we need?
##### If the signal perfectly matches the template we have an optimal SNR
###### Any mismatch causes an SNR loss
##### Costruct banks with a dense grid of templates such that any signal will be close enough to the nearest template
###### Can easily create hundreds of thousands of templates (makes a computational burden)
#### Revisiting our assumptions: in reality, LIGO data is not well modeled
##### Non-stationary over short and long time scales: we must continuously track the noise properties and update our estimate of the PSD
###### Short duration non-Gaussian artefacts in the data are glitches (can be a major problem for matched filtering searches)
##### Non-Gaussian
###### The only characterization of the LIGO noise is from observations
##### LIGO noise is colored not white meaning that the power is not distributed evenly across the frequencies
###### The PSD varies across frequency bins so the data needs to be whitened before filtering
#### Matched filtering with real search pipelines
##### Inpractice, real search pipelines must come up with solutions to handle non-ideal noise properties
##### Filtering millions of templates over months of data is a huge computational burden
###### To make this feasible, real-search pipelines need to find ways to make the process more efficient
##### The 3 CBC searches: GstLAL, MBTA, and PyCBC each use slighltly different  methods
#### GstLAL: non-Gaussian data
##### Solution 1: gating
###### Remove stretches of data with large non-Gaussian features before matched filtering
###### We have to be careful to not accidently gate a real signal
##### Solution 2: signal consistency tests
###### Matched filtering doesn't produce just a SNR peak but a time-series of SNR data
###### Compare the SNR time series shape ot the predicted shape for a template waveform
##### Solution 3: iDQ (integrated data quality)
###### Use machine learning and data from auxillary channels to identify glitches
###### Clean data: boost significance of candidates
###### Glitchy data: reduce significance of candidates
#### GstLAL: LLOID method (Low latency online inspiral detection)
##### Reduce computational burden
##### Improve efficiency and lower the latency of the search
##### Step 1: time slicing and down sampling
###### Take advantage of monotonic increase in signal frequency
###### Use lower sampling rate at earlier parts of the signal to avoid oversampling
###### We can slice waveforms into freqncy bands then downsample each one to save computations
##### Step 2: singular value decomposition (SVD)
###### Our template banks are highly redundant
###### Transform to a reduced set of basis waveforms
###### Filter with the vasis waveforms then reconstruct the physical templates after filtering
#### Matched filtering with MBTA and PyCBC
##### PyCBC and MBTA both regularly perform matched filtering in the frequency domain
##### Perform FFT on blocks of data, then correlate the data witht he template waveforms
###### Typical block length = 2048 seconds
#### Matched filtering with BMTA and PyCBC: non-Gaussian data
##### MBTA and PyCBC both use gating and signal consistency tests similar to GstLAL
###### They do not use iDQ but rather vetoes to reject triggers from times identified to have poor data quality
##### MBTA: re-filter high mass templates
###### Heavy BBH systems can be mistake for glitches due to their short duration
###### MBTA re-filters templates with durations of <3 sec without gating first
###### This helps to avoid accidently gating real signals
#### Matched filtering with MBTA
##### Step 2: multi-banding
###### Filter with waveforms split into two frequency bands: low and high
###### Reconstruct the real templates after filtering
