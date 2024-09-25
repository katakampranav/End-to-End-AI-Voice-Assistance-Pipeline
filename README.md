# End-to-End AI Voice Assistance Pipeline

## Overview

The End-to-End AI Voice Assistance Pipeline is an integrated system that processes an audio file by converting speech to text, generating a response using the LLaMA2 language model, and then converting that response back into speech. This project leverages several advanced technologies, including OpenAI's Whisper for speech-to-text, LLaMA2 for text processing, and Edge TTS for text-to-speech conversion. The system is designed to be user-friendly, with a Gradio interface for easy interaction.

## Features

- **Speech-to-Text Conversion**: Uses Whisper to transcribe audio into text.
- **Voice Activity Detection (VAD)**: Filters out non-speech segments from the audio.
- **Text Processing**: Generates coherent responses using the LLaMA2 language model.
- **Text-to-Speech Conversion**: Converts the generated text response back into speech using Edge TTS.
- **Gradio Interface**: Provides an interactive web interface for user interaction.

## Installation

Follow these steps to set up the environment and install necessary dependencies:

1. **Clone the Repository**

   ```bash
   git clone https://github.com/katakampranav/End-to-End-AI-Voice-Assistance-Pipeline.git
   ```

2. **Install Dependencies**

   Run the following commands to install the required libraries:

   ```bash
   pip install librosa pydub webrtcvad
   pip install git+https://github.com/openai/whisper.git
   pip install langchain llama-cpp-python pypdf langchain_community
   pip install edge-tts asyncio
   pip install gradio
   ```

3. **Mount Google Drive**

   If using Google Colab, mount your Google Drive to access your LLaMA2 model:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

4. **Download the Model**

   Download the quantized LLaMA2 model and place it in your Google Drive. Update the model path in the code accordingly.
   [Download LLama model](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGUF/blob/main/llama-2-7b-chat.Q2_K.gguf)

## Usage

1. **Run the Notebook**

   Open the provided Jupyter notebook (`project.ipynb`) and run all cells sequentially. Ensure that you have updated paths for your audio files and LLaMA2 model.

2. **Upload an Audio File**

   Use the Gradio interface to upload an audio file in MP3 format. The pipeline will process the audio, generate a text response, and convert the response back into speech.

3. **Observe the Results**

   The Gradio interface will display the synthesized speech output. You can listen to the output directly or download it as an MP3 file.

## Instructions to Run the Demo

1. In this README.md file i provided a link to include the quantized LLaMA2 model to the project by adding it to your drive after downloading it, and recordings are given above which used for testing. Please use these when running the notebook (`project.ipynb`).
2. Install the necessary libraries by running the provided pip commands.
3. Run all cells from start to end for better functionality.
4. Upload an audio file using the Gradio interface.
5. Observe the transcription, text processing, and synthesized speech output.

## Code Implementation

For a detailed breakdown of the code implementation, refer to the `Code Implementation` section in the notebook. It covers:

- **Speech-to-Text Conversion**: Using Whisper to transcribe audio.
- **Voice Activity Detection (VAD)**: Filtering non-speech segments.
- **Audio Preprocessing and Saving**: Preparing audio for transcription.
- **Text Processing with LLaMA2**: Generating responses.
- **Text-to-Speech Conversion**: Using Edge TTS for speech synthesis.
- **Integration with Gradio**: Creating a user-friendly interface.

## Flowchart and Outputs

### Flowchart

![image](https://github.com/user-attachments/assets/25334094-693a-4261-b977-cd9697760506)

### Output Screens
![image](https://github.com/user-attachments/assets/ae0fddbd-b2fd-463d-bff4-de2cb85365b0)

![image](https://github.com/user-attachments/assets/b2946e74-0e92-49ab-a5df-6aaa3e77a0e8)


## Author

This Comment Toxicity Model was developed by :
-	[@katakampranav](https://github.com/katakampranav)
-	Repository : https://github.com/katakampranav/End-to-End-AI-Voice-Assistance-Pipeline

## Feedback

For any feedback or queries, please reach out to me at katakampranavshankar@gmail.com.
