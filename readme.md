# Speech Transcription and Control

This repository contains a Python script that uses Azure Cognitive Services for real-time speech transcription and system volume control. The script listens for a hotkey (F2) to start or stop transcription and mutes/unmutes the system volume accordingly. The transcribed text is typed into the active window. I wrote this out of necessity for my own use, to minimise my typing load over hundreds of MS-Teams messages every day, but I hope it can be helpful to others as well. I understand there are built-in options, but I wanted to try this regardless. 

## Features

- Real-time speech transcription using Azure Cognitive Services.
- Mute/unmute system volume during transcription.
- Hotkey listener to start/stop transcription.

## Requirements

- Python 3.6+
- Azure Cognitive Services Speech SDK
- `python-dotenv`
- `keyboard`
- `pyautogui`
- `pycaw`
- `comtypes`

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/dan-hampton/azure-speech-transcribe.git
    cd azure-speech-transcribe
    ```

2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

3. Set up Azure Speech Service and obtain your API keys:
    - Go to the [Azure Portal](https://portal.azure.com/).
    - Create a new Speech service resource.
    - Navigate to the resource and copy the API key and region.

4. Create a `.env` file in the root directory and add your Azure Cognitive Services API key and region:
    ```env
    AZURE_SPEECH_KEY=your_speech_key
    AZURE_REGION=your_service_region
    ```

## Usage

1. Run the script:
    ```sh
    python speech.py
    ```

2. Choose the transcription mode:
    - Press `1` for continuous transcription.
    - Press `2` for one-shot transcription.

3. Follow the on-screen instructions:
    - For continuous transcription, press `F2` to start or stop transcription.
    - For one-shot transcription, press `F2` to start a one-shot transcription.

4. To exit the script, press `Ctrl+C`.

## Use Case

This script is particularly useful for individuals who need to transcribe spoken words into text in real-time, such as during meetings, lectures, or interviews. By muting the system volume during transcription, it ensures that background noise from the system does not interfere with the transcription process. The hotkey functionality allows for easy control over when transcription starts and stops, making it convenient to use in various scenarios.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Azure Cognitive Services](https://azure.microsoft.com/en-us/services/cognitive-services/)
- [pycaw](https://github.com/AndreMiras/pycaw)
- [pyautogui](https://pyautogui.readthedocs.io/en/latest/)
- [python-dotenv](https://github.com/theskumar/python-dotenv)