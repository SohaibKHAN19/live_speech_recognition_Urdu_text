# 🎙 Live Urdu Speech Recognition

A real-time speech recognition application built with Python using the `SpeechRecognition` library and Google Speech Recognition API.

This project continuously listens through your microphone and converts spoken Urdu into text in real time using multithreading for smooth audio capture and processing.

---

## 🚀 Features

- Real-time speech recognition
- Urdu language support (`ur-PK`)
- Multithreaded architecture
- Queue-based audio processing
- Ambient noise adjustment
- Continuous microphone listening
- Graceful shutdown with `Ctrl+C`

---

## 🛠 Technologies Used

- Python
- SpeechRecognition
- Google Speech Recognition API
- PyAudio
- Threading
- Queue

---

## 📦 Requirements

- Python 3.9+
- Working microphone
- Internet connection

---

## 📥 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/live-urdu-speech-recognition.git
cd live-urdu-speech-recognition
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ⚠ PyAudio Installation

### Windows

If PyAudio installation fails:

```bash
pip install pipwin
pipwin install pyaudio
```

### Ubuntu / Debian

```bash
sudo apt install portaudio19-dev python3-pyaudio
```

### macOS

```bash
brew install portaudio
pip install pyaudio
```

---

## ▶ Usage

Run the application:

```bash
python main.py
```

You will see:

```text
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🎙 Live Speech Recognition
Language : ur-PK
Press Ctrl+C to stop
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

Start speaking into your microphone.

Example output:

```text
[12:42:10] السلام علیکم
[12:42:15] آپ کیسے ہیں
```

---

## ⚙ Configuration

You can modify these variables inside `main.py`:

```python
LANGUAGE = "ur-PK"
ENERGY_THRESHOLD = 300
PAUSE_THRESHOLD = 0.8
PHRASE_LIMIT = None
```

### Configuration Details

| Variable | Description |
|---|---|
| `LANGUAGE` | Recognition language |
| `ENERGY_THRESHOLD` | Microphone sensitivity |
| `PAUSE_THRESHOLD` | Silence duration before processing |
| `PHRASE_LIMIT` | Maximum phrase duration |

---

## 📁 Project Structure

```text
live-urdu-speech-recognition/
│
├── main.py
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 📄 requirements.txt

```txt
SpeechRecognition==3.10.4
PyAudio==0.2.14
```

---

## 🧠 How It Works

1. The microphone continuously captures audio.
2. Audio chunks are placed into a queue.
3. A separate thread processes the audio.
4. Google Speech Recognition converts speech into text.
5. Recognized text is printed with timestamps.

---

## 📌 Future Improvements

- GUI interface
- Offline speech recognition
- Save transcripts to file
- Multiple language support
- Voice activity detection

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

Developed with Python and Speech Recognition APIs.
