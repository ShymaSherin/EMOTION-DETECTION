# EMOTION-DETECTION
Here’s the revised README file without the example section:

---

# Emotion Recognition and Speech Transcription

This repository contains a Python-based project for detecting emotions from both facial expressions and speech, as well as transcribing speech to text. It uses OpenAI’s Whisper model for speech recognition and a pre-trained CNN model for facial emotion detection. The project also incorporates machine learning techniques for emotion classification based on audio features.

## Features

* **Facial Emotion Detection**: Detect emotions (Happy, Sad, Angry, Neutral, etc.) from images using a pre-trained mini-XCEPTION model.
* **Speech-to-Text Transcription**: Convert audio from MP3/MP4/WAV files to text using Whisper.
* **Audio Emotion Detection**: Classify emotions (Happy, Sad, Angry, Neutral, etc.) from audio features.
* **Multi-modal Processing**: Process both images and audio files simultaneously to detect emotions and transcribe speech.

## Prerequisites

Before running the project, make sure you have the following installed:

* Python 3.x
* Required Python libraries: `whisper`, `keras`, `opencv-python`, `librosa`, `scikit-learn`, `moviepy`, `transformers`, `ffmpeg`

You can install the required libraries by running:

```bash
pip install whisper keras opencv-python librosa scikit-learn moviepy transformers
```

For installing `ffmpeg`, use:

```bash
sudo apt update && sudo apt install -y ffmpeg
```

## Setup Instructions

1. Clone this repository:

```bash
git clone https://github.com/yourusername/emotion-recognition-speech-transcription.git
cd emotion-recognition-speech-transcription
```

2. Install required Python libraries (listed above).

3. Download the pre-trained facial emotion detection model (Mini-XCEPTION):

```bash
wget https://github.com/oarriaga/face_classification/raw/master/trained_models/emotion_models/fer2013_mini_XCEPTION.102-0.66.hdf5 -O emotion_model.h5
```

4. Set up Whisper (OpenAI's speech-to-text model):

```bash
pip install git+https://github.com/openai/whisper.git
```

5. Upload your image (JPG/PNG) and audio (MP3/MP4/WAV) files when prompted.

## How It Works

### Image Processing (Facial Emotion Detection)

1. The uploaded image is processed by OpenCV to detect faces.
2. The detected face is passed to a pre-trained emotion classification model.
3. The emotion is predicted based on the face detected in the image, and it is displayed.

### Audio Processing (Speech-to-Text Transcription & Audio Emotion Detection)

1. The uploaded audio file is converted into a WAV file using `moviepy` and processed by the Whisper model to generate a transcript and detect the language.
2. Audio features are extracted (MFCC, pitch) and used to predict the emotional state of the speaker using a pre-trained Support Vector Classifier (SVC).
3. The detected emotion and transcription are returned along with the language.

## File Structure

* `emotion_model.h5` - Pre-trained emotion classification model.
* `whisper_model` - OpenAI Whisper model (loaded dynamically).
* Python scripts (in the repository) for processing images and audio.

---

This version removes the example section. Let me know if you need any other changes!
