# Nigerian-Offline-Speech-Command-
This project demonstrates an offline speech recognition pipeline designed for low-resource African languages on Android devices. It was developed as part of **awadoc**, an AI-powered health assistant for Nigerian users with limited internet connectivity
# Offline Nigerian Voice Command Recognizer

**An offline-first voice command recognition system for Nigerian languages (Igbo, Hausa, Yoruba)**

This project demonstrates an offline speech recognition pipeline designed for low-resource African languages on Android devices. It was developed as part of **Awadoc**, an AI-powered health assistant for Nigerian users with limited internet connectivity.

## Key Features

- ✅ **Fully offline** - No cloud APIs required, runs entirely on-device
- ✅ **3 Nigerian languages** - Igbo, Hausa, Yoruba support
- ✅ **Closed-grammar command recognition** - ~30 fixed commands per language
- ✅ **Android deployment** - TFLite model optimized for low-end devices
- ✅ **Low-resource optimization** - INT8 quantized models (~5MB each)
- ✅ **Real-time inference** - <100ms latency on Android

## Technical Stack

| Component | Technology |
|-----------|-----------|
| Model Architecture | wav2vec2-xls-r / Custom KWS CNN |
| Training | PyTorch + Hugging Face Transformers |
| Deployment | TensorFlow Lite (TFLite) |
| Quantization | INT8 (quantization-aware training) |
| Android | Android Studio + TFLite Interpreter |
| Languages | Igbo, Hausa, Yoruba (low-resource African languages) |

## Project Structure
offline-nigerian-voice-command/
├── training/ # Model training scripts
│ ├── train_nigerian_commands.py # Fine-tune wav2vec2 for commands
│ ├── preprocessing.py # Audio preprocessing pipeline
│ └── convert_to_tflite.py # Export to TFLite
├── app/ # Android app
│ ├── MainActivity.java # UI + recording
│ ├── VoiceCommandRecognizer.java # TFLite inference
│ └── AudioPreprocessor.java # Audio processing
└── evaluation/ # Evaluation metrics
└── evaluate_commands.py # Per-command accuracy
