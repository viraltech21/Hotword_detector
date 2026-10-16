# HotWord Detection using MFCC and DTW

A Python-based hotword detection system that identifies a predefined spoken word from audio recordings using **Mel-Frequency Cepstral Coefficients (MFCC)** and **Dynamic Time Warping (DTW)**.

## About the Project

This project implements a customizable hotword detection system using audio feature extraction and temporal pattern matching. It supports training a target hotword and checking audio recordings for a match.

## Features

- **MFCC Feature Extraction:** Extracts audio features for speech pattern representation.
- **Dynamic Time Warping (DTW):** Measures similarity between audio feature sequences.
- **Custom Hotword Training:** Allows users to train the system to recognize a selected hotword.
- **Voice Activity Detection (VAD):** Uses amplitude-based detection to reduce silence and extraneous noise in recordings.
- **Variable Sampling Frequencies:** Supports configurable audio sampling frequencies.
- **Automatic DTW Thresholding:** Helps personalize detection by setting a suitable matching threshold.

## Technologies Used

- Python
- NumPy
- SciPy
- PyAudio
- MFCC
- Dynamic Time Warping (DTW)

## Project Structure

```text
Hotword_detector/
├── hotword_detection/
│   ├── dtw.py
│   ├── hwDetector.py
│   ├── mfcc.py
│   ├── wordRecorder.py
│   └── test/
├── bin/
│   ├── trainHotword.py
│   └── checkHotword.py
├── setup.py
└── README.md
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/viraltech21/Hotword_detector.git
cd Hotword_detector
```

### 2. Install the project

```bash
python -m pip install .
```

**Note:** PyAudio may require additional system audio libraries or build tools, depending on your operating system.

## Usage

### Train a hotword

Run:

```bash
python bin/trainHotword.py
```

Follow the prompts in the script to record and train your chosen hotword.

### Test hotword detection

Run:

```bash
python bin/checkHotword.py
```

Follow the prompts to record audio and check for the trained hotword.

## How It Works

1. Audio is recorded from the input device.
2. MFCC features are extracted from the audio signal.
3. DTW compares the extracted features with the trained hotword pattern.
4. A matching threshold is used to determine whether the hotword is detected.

## Author

**Harshit Dwivedi**

GitHub: [@viraltech21](https://github.com/viraltech21)

## References

- [MFCC Tutorial](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum)
- [Dynamic Time Warping](https://en.wikipedia.org/wiki/Dynamic_time_warping)
- [GitHub Repository](https://github.com/viraltech21/Hotword_detector)
