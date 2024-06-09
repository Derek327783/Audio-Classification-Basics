# Audio Classification Basics
- This project utilises the UrbanSound8k dataset which comprises of 8732 audio files that have 10 classes from air_conditioner to street_music.

## 1. Feature Extraction 
- There are various feature extraction methods used for audio signals and they can be categorised by which domain they belong to and the ideal ones to use will be dependent on the various use cases such as environmental sounds, speech or music.

### 1.1. Time Domain (x:time, y:amplitude)
- **Zero-Crossing Rates**: The number of times the signal's amplitude crosses the x-axis.
- **Amplitude Descriptors**: Statistical values such as Root-Mean-Square (RMS), peak amplitude and standard deviation of the whole signal.
- **Short Time Energy**: Similar to the RMS amplitude descriptor but now the values are calculated in each frame of fixed size in the signal.
- **Linear Predictor Coding**: In a nutshell this method aims to condense information about the signal as a vector of coefficients where the coefficients are the weights that are learned by assuming that at each signal point, it can be reconstructed by past signal points weighted by different coefficients.

### 1.2. Frequency Domain (x:frequency,y:magnitude)
Note that the magnitude here is a pseudo-representation of how similar the original wave is to a sine wave of that frequency.

- **Peak Frequency**: This finds the frequency of the highest magnitude that is the frequency that the original wave is most similar to.

### 1.3. Time-Frequency Domain (x:time,y:frequency, colour:magnitude)
This is attained by taking the short time fourier transform (STFT) of the entire signal giving a spectrogram.
- **Spectrum shaped based features**: These features extract information from each frame of the spectrogram such as spectral centroid, spectral bandwidth and spectral flux.

