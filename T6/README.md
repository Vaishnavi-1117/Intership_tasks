# T6 - Background Noise Detector

## Objective

This project detects whether an audio recording is clean or noisy before it is sent to a Speech-to-Text (STT) engine.

## Technologies Used

- Python
- Librosa
- NumPy
- Google Colab

## Methodology

1. Load the WAV audio file.
2. Calculate RMS (Root Mean Square) energy.
3. Estimate the background noise floor from low-energy frames.
4. Estimate the speech level from high-energy frames.
5. Compute an estimated Signal-to-Noise Ratio (SNR).
6. Classify the audio as **Clean** or **Noisy** based on an energy threshold.

## Sample Output

```json
{
  "file": "sample_clean.wav",
  "average_rms": 0.096,
  "noise_floor": 0.0137,
  "speech_level": 0.1848,
  "snr_estimate_db": 22.59,
  "flag": "clean"
}
```

```json
{
  "file": "sample_noisy.wav",
  "average_rms": 0.0433,
  "noise_floor": 0.0017,
  "speech_level": 0.1447,
  "snr_estimate_db": 38.69,
  "flag": "noisy"
}
```

## Installation

```bash
pip install librosa numpy
```

## Run

```bash
python background_noise_detector.py
```
