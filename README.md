# Pneumonia Detection App

## Overview
A desktop application built with PyQt5 and TensorFlow/Keras to detect pneumonia from chest X-ray images. The app provides a simple GUI for users to upload an X-ray image, runs a pretrained VGG16-based model, and announces the result via Windows text-to-speech.

## Features
- **Upload X-ray Image**: Select a chest X-ray file using a file dialog.
- **Prediction**: Model infers whether the image shows signs of pneumonia or is normal.
- **Audio Feedback**: Uses Windows SAPI.SpVoice to speak the result aloud.
- **Animated UI**: Includes a looping GIF and custom styling for an engaging user experience.

## Requirements
- Python 3.7+
- Windows OS (for SAPI.SpVoice TTS)

### Python Packages
- PyQt5
- tensorflow
- keras
- numpy
- pillow
- pywin32

You can install all dependencies via:
```bash
pip install -r requirements.txt
```

## Installation
1. Clone this repository:
   ```bash
git clone https://github.com/yourusername/pneumonia-detection-app.git
cd pneumonia-detection-app

2. Ensure `chest_xray.h5` (the pretrained model file) and `picture.gif` (UI animation) are in the project root.
3. Install dependencies:
   ```bash
pip install -r requirements.txt


## Usage
1. Run the application:
   ```bash
python chest_xray.py

2. Click **Upload Image** and choose a chest X-ray file (PNG/JPG).
3. After uploading, click **Prediction** to analyze the image.
4. The app will display the result in the console and speak it aloud.

## File Structure

├── chest_xray.py      # Main application script
├── chest_xray.h5      # Pretrained Keras model
├── picture.gif        # GIF animation for GUI
├── patient.png        # Application icon
├── requirements.txt   # Python dependencies
└── README.md          # Project documentation


## Model Details
- **Architecture**: Based on VGG16 with custom classification head.
- **Input Size**: 224×224 RGB images.
- **Output**: Single probability score (0 = pneumonia, 1 = normal).
- **Preprocessing**: Uses `keras.applications.vgg16.preprocess_input`.

## Notes
- Designed and tested on Windows; text-to-speech uses SAPI.
- Ensure microphone/speaker drivers are working for audio feedback.

## Contributing
1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/YourFeature`.
3. Commit your changes and push: `git push origin feature/YourFeature`.
4. Open a pull request with a detailed description.


