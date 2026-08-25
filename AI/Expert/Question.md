## 🧠 Understanding the Architecture

A conversational voice pipeline operates in three smooth stages:
1. **Ear (STT):** Captures audio from your microphone and converts spoken words into a text string using models like OpenAI Whisper.
2. **Brain (LLM):** Takes the text string, processes the intent, and generates a smart response (via local Ollama or an API).
3. **Mouth (TTS):** Takes the text response and synthesizes it into a realistic human audio voice stream to play back to the user.

---

## 📝 The Task

### Objective
Build a Python script that records your voice, transcribes it, queries an AI model, and speaks the answer out loud using lightweight Python libraries (`SpeechRecognition`, `gTTS`, and `requests` or `ollama`).

### Requirements
1. **Audio Capture & Transcription:** Use the `speech_recognition` library to record audio from your computer's microphone and convert it to text.
2. **AI Response Generation:** Send the transcribed text to a local LLM (running via Ollama) or a cloud API to get a concise text reply.
3. **Voice Synthesis (TTS):** Use Google Text-to-Speech (`gTTS`) or `pyttsx3` to convert the AI's text response into an audio file and play it automatically.
4. **Interactive Loop:** Wrap it inside a continuous loop so you can have a back-and-forth conversation.

### Starter Template
```python
import speech_recognition as sr
from gtts import gTTS
import os
import subprocess

def speak(text):
    """Converts text to speech and plays it."""
    print(f"AI: {text}")
    tts = gTTS(text=text, lang='en')
    tts.save("response.mp3")
    # Play audio (works on Mac/Linux/Windows via cross-platform system calls)
    os.system("start response.mp3" if os.name == "nt" else "afplay response.mp3" if os.uname().sysname == "Darwin" else "mpg321 response.mp3")

def listen_and_transcribe():
    """Listens to microphone and converts audio to text."""
    r = sr.Recognizer()
    with sr.Microphone() as source:
        print("Listening for your command... (Speak now)")
        r.adjust_for_ambient_noise(source)
        audio = r.listen(source)
    
    try:
        text = r.recognize_google(audio)
        print(f"You said: {text}")
        return text
    except sr.UnknownValueError:
        print("Could not understand audio.")
        return None
    except sr.RequestError:
        print("Speech service error.")
        return None

# --- Main Interaction Loop ---
if __name__ == "__main__":
    user_input = listen_and_transcribe()
    if user_input:
        # Simulate LLM response (Replace this with an Ollama/OpenAI API call!)
        ai_reply = f"I heard you say: {user_input}. That sounds interesting!"
        speak(ai_reply)
```

# Resources
Videos : 
https://www.youtube.com/watch?v=Lp9Ftuq2sVI&t=1650s : How To Make Jarvis by Codewithharry

Documentation : https://archive.codewithharry.com/videos/python-tutorials-for-absolute-beginners-120/
