# 🚀 Run DeepSeek Locally on Android (Termux Guide)

This guide shows how to run *DeepSeek AI locally on Android* using *Termux + llama.cpp*.

✔ No cloud  
✔ Works offline  
✔ Free  
✔ Stable (No Ollama issues)

This is the *most reliable method* for Android users.

---

## 📱 Requirements

### Device
- Android 8+
- Minimum *6 GB RAM* (8 GB recommended)
- At least *5 GB free storage*

### Apps (Install from F-Droid)
1. Termux  
2. Termux:API (Optional – for microphone)

---

## 📥 Step 1: Install Termux

Download from F-Droid:

https://f-droid.org/en/packages/com.termux/

Open Termux after installation.

---

## ⚙️ Step 2: Setup Environment

Run this in Termux:

```bash
pkg update && pkg upgrade -y
pkg install git cmake clang make wget python ffmpeg sox espeak termux-api -y
```
This installs all required tools.
