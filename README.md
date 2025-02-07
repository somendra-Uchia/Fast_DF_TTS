Key Features:
Text-to-Speech Conversion

The generate_audio() function uses the StreamElements API to generate speech audio from a given text string.
It constructs a URL request with the selected voice and retrieves the generated speech audio.
Playing the Generated Audio

The speak() function calls generate_audio(), saves the audio file temporarily, plays it using the playsound module, and then deletes the file after playback.
Alternative Method using edge-tts (Commented Out)

Another implementation (commented out) uses Microsoft's Edge TTS for speech synthesis.
It generates an audio file using the edge-tts command-line tool and plays it using playsound in a separate thread.
Libraries Used:
requests: Fetches speech audio from the API.
playsound: Plays the generated audio file.
os: Handles file operations (saving and deleting temporary audio files).
subprocess: Runs system commands (used in the alternative method).
threading: Plays audio in a non-blocking way (used in the alternative method).
tempfile: Creates temporary files for speech output.
Usage:
The script enables speech output by converting text into audio and playing it instantly.
It provides flexibility by allowing different voices to be selected.
The commented-out alternative method shows how to use the edge-tts tool for TTS instead of an online API.
