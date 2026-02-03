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

---

## 🧠 Step 3: Install llama.cpp (AI Engine)
```bash
git clone https://github.com/ggerganov/llama.cpp
cd llama.cpp
mkdir build && cd build
cmake ..
make -j4
```
⏳ Takes 2–5 minutes.

---

## ✅ Verify Installation
```bash
./main --help
```
If help appears → Installation successful.

---

## 📦 Step 4: Download DeepSeek Model

Go back to main folder:
```bash
cd ..
mkdir models
cd models
```
Download recommended lightweight model:
```bash
wget https://huggingface.co/TheBloke/DeepSeek-R1-Distill-Qwen-1.5B-GGUF/resolve/main/deepseek-r1-distill-qwen-1.5b-q4_k_m.gguf
```
Size: ~1GB
Best for Android devices.

## Run the Server

```bash
ollama serve
```
Nnow open new session in the termux then run this command

```bash
initiate deepseek-r1-1.5b
```
So you have successfully running the your own offgrid llm, enjoy!

Its a resoning model so it won't be a super genius but you can ask ques like
```bash
summarise this email
```
like ques it will run fine in any phone!
