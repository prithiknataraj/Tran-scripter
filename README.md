# Tran-scripter
## Video Transcription and Translation

This project is a web application that allows users to upload a video, extract and process the audio, transcribe the speech, and translate the transcript into a specified language. The application is built using Flask, OpenCV, MoviePy, and the Google Web Speech API.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Features

- Upload a video file through the web interface.
- Extract and process audio from the video.
- Transcribe speech to text using Google Web Speech API.
- Translate the transcript into a specified language using an external translation API.
- Display the translated transcript on the web page.

## Installation

### Prerequisites

- Python 3.x
- Virtual environment (optional but recommended)

### Steps

1. Clone the repository:

```sh
git clone https://github.com/yourusername/video-transcription-translation.git
cd video-transcription-translation
```

2. Create and activate a virtual environment:

```sh
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install the required packages:

```sh
pip install -r requirements.txt
```

## Usage

To run the web application:

```sh
python app.py
```

Navigate to `http://127.0.0.1:5000/` in your web browser to access the application.

### Uploading and Processing a Video

1. On the home page, upload a video file.
2. Select the language you want to translate the transcript into.
3. Click the upload button to process the video.
4. The translated transcript will be displayed on the page.

## Configuration

You can configure various aspects of the application by modifying the `app.py` file. For example, you can change the file paths, adjust the audio processing parameters, or update the API keys for translation.

### API Key for Translation

Make sure to update the `X-RapidAPI-Key` in the `video()` function with your own API key from RapidAPI:

```python
headers = {
    "X-RapidAPI-Key": "your_rapidapi_key_here",
    "X-RapidAPI-Host": "nlp-translation.p.rapidapi.com"
}
```

## Dependencies

- Flask
- OpenCV
- MoviePy
- Numpy
- SpeechRecognition
- Requests

Install these dependencies via:

```sh
pip install flask opencv-python moviepy numpy SpeechRecognition requests
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.
