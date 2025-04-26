# LSTM
# Text-to-Speech with Voice Cloning

This project demonstrates how to generate natural-sounding speech from text using a pre-trained Tacotron 2 and WaveGlow model, with optional voice cloning capabilities via SV2TTS (Transfer Learning from Speaker Verification to Multispeaker Text-To-Speech Synthesis).

## Features

- Text-to-speech synthesis using Tacotron 2 and WaveGlow
- Voice cloning using pretrained SV2TTS models
- Adjustable speech parameters (speed, pitch, energy)
- Support for multiple speakers (LibriTTS pretrained model)
- Easy-to-use Colab interface with audio playback

## Prerequisites

- Google Colab (recommended) or Python 3.7+ environment
- NVIDIA GPU (for faster inference)
- Python packages (automatically installed in Colab):
  - torch
  - numpy
  - librosa
  - IPython
  - matplotlib
  - scipy

## Installation

1. Open the Colab notebook: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1uHNpmM30ZRjXtoljuDtNco_B02HIAg-P?usp=sharing)
2. Run all cells sequentially (Runtime -> Run all)
3. For voice cloning, upload a reference audio file when prompted

## Usage

### Basic Text-to-Speech

1. Enter your text in the provided text box
2. Select a speaker (for multispeaker model)
3. Adjust parameters (speed, pitch, energy) if desired
4. Click "Synthesize" to generate speech

### Voice Cloning

1. Upload a reference audio file (WAV format recommended, 5-10 seconds of clean speech)
2. Enter your text
3. Click "Synthesize" to generate speech in the reference voice

## Models Used

- Tacotron 2: Sequence-to-sequence model for generating mel spectrograms from text
- WaveGlow: Flow-based network for generating speech from mel spectrograms
- SV2TTS: Speaker encoder for voice cloning (optional)

## Examples

Try these sample texts:
- "Hello world, this is a test of text to speech synthesis."
- "The quick brown fox jumps over the lazy dog."
- "I am sorry, Dave. I'm afraid I can't do that."

## Limitations

- Voice cloning works best with high-quality reference audio
- Long sentences may be split into chunks
- Some artifacts may be present in generated speech
- English language only for pretrained models

## License

The code is provided for research purposes only. The pretrained models are subject to their respective licenses (NVIDIA Tacotron 2 and WaveGlow models are available under the NVIDIA Source Code License).

## References

- Tacotron 2: https://github.com/NVIDIA/tacotron2
- WaveGlow: https://github.com/NVIDIA/waveglow
- SV2TTS: https://github.com/CorentinJ/Real-Time-Voice-Cloning
- LibriTTS dataset: https://openslr.org/60/
