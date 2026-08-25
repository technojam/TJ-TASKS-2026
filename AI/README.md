# 🚀 Welcome to the AI/ML Fresher Track!
### *Where "Hello World" meets "Hello Neural Network"*

---

> **Disclaimer:** No prior knowledge of machine learning is required. Prior knowledge of coffee consumption is optional but recommended. ☕

You've just joined one of the most exciting fields in tech. This guide will walk you through **4 progressive tasks** each one building on the last so by the end, you'll go from writing `if-else` statements to building an AI that talks back to you. Yes, really.

Let's go. One step at a time. You've got this. 💪

---

## 📋 Task Overview

| Level | Task | Vibe |
|-------|------|-------|
|  Easy | Basic NLP with Stop Words & Decision Trees | "I can do this before lunch" |
|  Medium | Simulated Neural Network (Perceptron) | "Wait, this is actually cool" |
|  Hard | Convolutional Neural Network with PyTorch | "I need more coffee" |
| Expert | Real-Time Conversational Voice Agent | "Am I a wizard?" |

---

## 🟢 Level 1 — Basic NLP: Stop Words & Decision Trees

### What You're Building
A Python script that reads a customer message, strips out useless filler words (like "the", "is", "a"), and routes the message to the right department using simple `if-else` logic.

Think of it as building a tiny, very literal customer service agent. It won't win any awards, but it'll teach you how real NLP pipelines start.

### The Task
```python
# 1. Define common stop words to ignore
STOP_WORDS = ["the", "is", "at", "which", "and", "to", "a", "an", "for", "my", "i"]

def clean_and_tokenize(text):
    # TODO: Convert text to lowercase, split into words, and filter out stop words
    pass

def classify_message(text):
    # TODO: Get filtered keywords and use if-else logic to classify the message
    # "crash", "bug", "broken", "error"     -> "Technical Support"
    # "bill", "charged", "payment", "subscription" -> "Billing Support"
    # Otherwise                              -> "General Inquiry"
    pass

# Test your code
print(classify_message("the app crashes every time I open it"))
```

### Classification Rules
- Keywords `crash`, `bug`, `broken`, `error` → **Technical Support**
- Keywords `bill`, `charged`, `payment`, `subscription` → **Billing Support**
- Everything else → **General Inquiry**

### 📚 Resources to Solve This
| Resource | Link | Why It Helps |
|----------|------|--------------|
| Python `if-elif-else` | [docs.python.org/3/tutorial/controlflow](https://docs.python.org/3/tutorial/controlflow.html) | The backbone of your classifier |
| Python Lists & List Comprehensions | [w3schools.com/python/python_lists](https://www.w3schools.com/python/python_lists.asp) | For filtering stop words cleanly |
| String Methods (`lower()`, `split()`) | [docs.python.org/3/library/stdtypes.html#string-methods](https://docs.python.org/3/library/stdtypes.html#string-methods) | Step 1 of every NLP pipeline ever |
| Python for Beginners (Full Course) | [youtube.com/watch?v=eWRfhZUzrAc](https://www.youtube.com/watch?v=eWRfhZUzrAc) | freeCodeCamp's 4-hour Python crash course |

> 💡 **Hint:** A list comprehension like `[word for word in words if word not in STOP_WORDS]` will do the filtering in one line. You're welcome.

---

## 🟡 Level 2 — Simulated Neural Network (Perceptron)

### What You're Building
A single artificial neuron the fundamental building block of every neural network simulated entirely in pure Python. No libraries. No magic. Just math and `print()` statements.

You'll feed it two inputs (study hours + attendance), multiply by weights, add a bias, and watch it decide if a student passes or fails. It's basically a very opinionated calculator.

### The Math Behind It
```
weighted_sum = (study_hours × 3.5) + (attendance × 2.0) + (-3.0)
output = 1 if weighted_sum >= 0 else 0
```

### 📚 Resources to Solve This
| Resource | Link | Why It Helps |
|----------|------|--------------|
| Neural Networks from Scratch (Article) | [towardsdatascience.com](https://towardsdatascience.com/a-neural-network-in-11-lines-of-python-part-1-a0f36a0db09f) | Exactly what this task is about |
| 3Blue1Brown — Neural Networks (Visual) | [youtube.com/watch?v=aircAruvnKk](https://www.youtube.com/watch?v=aircAruvnKk) | The best visual explanation of neurons on the internet |
| Python f-strings | [docs.python.org/3/tutorial/inputoutput](https://docs.python.org/3/tutorial/inputoutput.html) | For the pretty print output |
| But What Is a Neural Network? | [youtube.com/watch?v=aircAruvnKk](https://www.youtube.com/watch?v=aircAruvnKk) | Watch this even if you think you understand it |

> 😅 **Fun Fact:** This single neuron is essentially how Rosenblatt's Perceptron worked in 1957. You just rebuilt a 60-year-old invention. Respect.

---

## 🔴 Level 3 — Convolutional Neural Network (CNN) with PyTorch

### What You're Building
A real CNN that learns to recognize handwritten digits (0–9) from the famous MNIST dataset. You'll write the model architecture, training loop, and evaluation the full pipeline.

This is where things get serious. But also seriously cool.

### The Task
```python
import torch
import torch.nn as nn
import torch.optim as optim
from torchvision import datasets, transforms
from torch.utils.data import DataLoader

transform = transforms.Compose([
    transforms.ToTensor(),
    transforms.Normalize((0.5,), (0.5,))
])
trainset = datasets.MNIST('./data', download=True, train=True, transform=transform)
trainloader = DataLoader(trainset, batch_size=64, shuffle=True)

class SimpleCNN(nn.Module):
    def __init__(self):
        super(SimpleCNN, self).__init__()
        self.conv1 = nn.Conv2d(1, 16, kernel_size=3, stride=1, padding=1)
        self.pool = nn.MaxPool2d(kernel_size=2, stride=2)
        self.fc1 = nn.Linear(16 * 14 * 14, 10)

    def forward(self, x):
        x = self.pool(torch.relu(self.conv1(x)))
        x = x.view(-1, 16 * 14 * 14)
        x = self.fc1(x)
        return x

model = SimpleCNN()
# TODO: Define loss function (CrossEntropyLoss) + optimizer (Adam)
# TODO: Write training loop for 1-3 epochs
# TODO: Evaluate on test set and print accuracy
```

### Architecture at a Glance
```
Input (28×28 image)
    ↓
Conv2D (16 filters, 3×3) + ReLU
    ↓
MaxPool2D (2×2) → 14×14
    ↓
Flatten → 3136 values
    ↓
Linear → 10 class scores
    ↓
Predicted Digit (0-9)
```

### 📚 Resources to Solve This
| Resource | Link | Why It Helps |
|----------|------|--------------|
| PyTorch Official Docs | [pytorch.org/docs/stable/index](https://pytorch.org/docs/stable/index.html) | The source of truth |
| PyTorch 60-Minute Blitz | [pytorch.org/tutorials/beginner/blitz](https://pytorch.org/tutorials/beginner/blitz/blitz_intro.html) | Perfect starting point, literally made for this |
| CNN Explained Visually | [youtube.com/watch?v=YRhxdVk_sIs](https://www.youtube.com/watch?v=YRhxdVk_sIs) | Andrej Karpathy's legendary CS231n lecture |
| Training a CNN in PyTorch (YouTube) | [youtube.com/watch?v=pDdP2sAxQ1M](https://www.youtube.com/watch?v=pDdP2sAxQ1M) | Full walkthrough with MNIST |
| `nn.CrossEntropyLoss` docs | [pytorch.org/docs/stable/generated/torch.nn.CrossEntropyLoss](https://pytorch.org/docs/stable/generated/torch.nn.CrossEntropyLoss.html) | You'll need this for the loss function |

> ⚠️ **Install First:**
> ```bash
> pip install torch torchvision
> ```
> If your laptop sounds like a jet engine after running this, that's normal. It's working. 🔥

---

## 🟣 Level 4 — Real-Time Conversational Voice Agent

### What You're Building
A full voice pipeline: your mic → speech-to-text → LLM → text-to-speech → speaker. An AI that listens and talks back. In Python. On your machine. Today.

If Level 1 was a calculator, this is Iron Man's JARVIS (budget edition).

### The Architecture
```
🎙️ Your Voice
    ↓  (speech_recognition)
📝 Transcribed Text
    ↓  (Ollama / API call)
🧠 AI Response Text
    ↓  (gTTS / pyttsx3)
🔊 Spoken Audio Output
```

### The Task
```python
import speech_recognition as sr
from gtts import gTTS
import os

def speak(text):
    print(f"AI: {text}")
    tts = gTTS(text=text, lang='en')
    tts.save("response.mp3")
    os.system("mpg321 response.mp3")  # Linux | use 'afplay' on Mac | 'start' on Windows

def listen_and_transcribe():
    r = sr.Recognizer()
    with sr.Microphone() as source:
        print("🎙️ Listening... (Speak now)")
        r.adjust_for_ambient_noise(source)
        audio = r.listen(source)
    try:
        text = r.recognize_google(audio)
        print(f"You said: {text}")
        return text
    except sr.UnknownValueError:
        return None

if __name__ == "__main__":
    user_input = listen_and_transcribe()
    if user_input:
        # Replace with Ollama or OpenAI API call for real AI responses
        ai_reply = f"You said: {user_input}. Interesting!"
        speak(ai_reply)
```

### 📚 Resources to Solve This
| Resource | Link | Why It Helps |
|----------|------|--------------|
| SpeechRecognition Library Docs | [pypi.org/project/SpeechRecognition](https://pypi.org/project/SpeechRecognition/) | Your "ear" component |
| gTTS (Google Text-to-Speech) | [pypi.org/project/gTTS](https://pypi.org/project/gTTS/) | Your "mouth" component |
| Ollama — Run LLMs Locally | [ollama.com](https://ollama.com) | Run Llama 3 / Mistral locally for free |
| Build a Voice Assistant in Python | [youtube.com/watch?v=x8xjj6cR9Nc](https://www.youtube.com/watch?v=x8xjj6cR9Nc) | Full tutorial walkthrough |
| OpenAI Whisper (Advanced STT) | [github.com/openai/whisper](https://github.com/openai/whisper) | Upgrade your transcription accuracy significantly |

> ⚠️ **Install First:**
> ```bash
> pip install SpeechRecognition gTTS pyaudio
> # On Linux you may also need:
> sudo apt-get install mpg321 portaudio19-dev
> ```

> 🤫 **Pro Tip:** If your roommate hears you saying "Hey Python, what is the meaning of life?" at 2am, just tell them you're doing "AI research." Which is true.

---

## 🗺️ Your Learning Path

```
Level 1 (NLP)          →  Python strings, lists, control flow
    ↓
Level 2 (Perceptron)   →  Math intuition, weighted sums, activation
    ↓
Level 3 (CNN)          →  PyTorch, real training loops, GPU compute
    ↓
Level 4 (Voice Agent)  →  Multimodal pipelines, APIs, system integration
```

Each level genuinely builds on the previous one. Don't skip ahead the foundations matter more than you think.

---

## 🛠️ General Setup Checklist

Before starting, make sure you have:

- [ ] Python 3.9+ installed → [python.org/downloads](https://www.python.org/downloads/)
- [ ] A code editor (VS Code recommended) → [code.visualstudio.com](https://code.visualstudio.com/)
- [ ] `pip` working in your terminal (`pip --version`)
- [ ] A GitHub account to submit your work
- [ ] Snacks. Seriously. Get snacks.

---

## 💬 Final Note

Every expert you look up to started exactly where you are right now confused, excited, and Googling "what is a list comprehension." The only difference between them and you is time spent writing code.

Break things. Fix them. Break them again. That's the job.

**Welcome to the team. Now go build something.** 🚀

---

*Made with ❤️ for the freshers cohort. You're going to do great.*

*TEAM TECHNOJAM*
