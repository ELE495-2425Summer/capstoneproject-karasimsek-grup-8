# 🚗 Voice-Controlled Autonomous Mini Vehicle (ELE 495 Capstone Project)

This project is a smart autonomous vehicle that can understand **Turkish natural language voice commands** and act accordingly using AI. The system interprets spoken commands, converts them into basic movement instructions, and controls a mobile robot accordingly — all while giving real-time voice feedback in Turkish.

---

## 🎯 Key Features

- Understands Turkish speech in natural language  
- Uses Google Gemini to extract intent from sentences  
- Sends motor commands in structured JSON format  
- Moves autonomously based on commands and obstacle feedback  
- Gives spoken responses using Text-to-Speech (TTS)  
- Real-time system monitoring through a web interface

---

## 🧠 System Flow

1. User gives a voice command via wireless microphone  
2. Raspberry Pi uses STT to convert speech to text  
3. GPT-4 processes the sentence and generates JSON control data  
4. Raspberry Pi parses JSON and moves the vehicle accordingly  
5. Ultrasonic sensors detect obstacles during movement  
6. Web interface shows current command, system status, and logs  

📌 See diagram below:
<p align="center">
  <img width="650" alt="Account ownership flow (1)" src="https://github.com/user-attachments/assets/c8504bc2-4d1d-4060-b34f-c7a87122165c" />
</p>


---

## 🖥 Web Interface

A Flask-based dashboard provides:

- Command logs  
- Current vehicle status (moving, stopped, turning, etc.)  
- JSON command preview  
- Live STT output  
- Error messages and feedback

**➡️ [Insert screenshot of the web UI here]**

---

## 🚘 Final Prototype Image

➡️
<p align="center">
  <img width="650" alt="Final Vehicle Image" src="https://github.com/user-attachments/assets/cad90b9d-c54d-490d-a50d-123af8b792b4"  />
</p>
</p>



---

## 🎬 Demo Video

**➡️ [Insert working video or YouTube link here]**

---

## 📁 Folder Structure

```bash
├── main.py                  # Core control loop
├── stt_module.py           # Speech-to-Text handling
├── llm_module.py           # GPT integration
├── tts_module.py           # Voice feedback
├── static/ and templates/  # Flask web files
├── commands.json           # Generated movement commands
├── status_logs.json        # Live logs for web UI
