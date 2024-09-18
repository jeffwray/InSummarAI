# InSummarAI

InSummarAI (pronounced "In Summary"): Transcribe voice recordings (MP3, M4A) from iPhone and Android devices and generate comprehensive meeting minutes using AI assistance.

## Overview

InSummarAI is a tool that helps users transcribe voice recordings (MP3, M4A formats) from iPhone and Android devices and generate detailed meeting minutes with the aid of AI. While not fully automatic, it streamlines the process of converting audio to text and extracting key information from meetings.

## Features

- Transcribes audio files using OpenAI's Whisper API
- Generates an executive summary
- Extracts attendees list
- Identifies action items and follow-ups
- Creates a formatted Word document with meeting minutes
- Speaker diarization (currently commented out, work in progress)

## Note on Speaker Diarization

The speaker diarization feature is currently a work in progress and is commented out in the code. This feature aims to identify and separate different speakers in the audio. When implemented, it will enhance the meeting minutes by attributing speech to specific individuals. For now, the transcription is processed without speaker identification.

## Requirements

- Python 3.7+
- OpenAI API key
- HuggingFace API token
- Required Python packages (install via `pip install -r requirements.txt`)

## Setup

1. Clone the repository
2. Create a virtual environment (recommended)
3. Install dependencies: `pip install -r requirements.txt`
4. Set up environment variables:
   ```
   export OPENAI_API_KEY=your_openai_api_key
   export HUGGINGFACE_TOKEN=your_huggingface_token
   ```

## Usage

1. Ensure you're in the project's root directory.
2. Activate your virtual environment (if you're using one).
3. Run the script with the path to your audio file:

   ```bash
   python3 transcribe_meeting.py path/to/your/audio_file.mp3
   ```

   Replace `path/to/your/audio_file.mp3` with the actual path to your MP3 or M4A file.

4. The script will process the audio file and generate a Word document (`audio_file_meeting_minutes.docx`) in the same directory as the input audio file.

Note: The script supports audio formats including .mp3 and .m4a, which are common for voice recordings on mobile devices.

## License

MIT License with Attribution

Copyright (c) 2024 Jeffrey Wray, BIGDEALIO, LLC

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

Additionally, any use of this Software in a product or service must include 
clear and visible attribution to Jeffrey Wray, BIGDEALIO, LLC as the original creator.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.