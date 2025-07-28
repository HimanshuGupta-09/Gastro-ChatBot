# Gastro-ChatBot
# 🩺 Gastroenteritis Symptom Self-Assessment Chatbot

This is a local AI-powered chatbot designed for residents of **Halifax, Nova Scotia** to help them understand **gastroenteritis symptoms**, learn when to seek medical care, and get home-care guidance. The system uses **AnythingLLM** (RAG) with **Ollama** running a local LLM model.

---

## 🧠 Project Overview

This chatbot is part of an educational use case where a lightweight, locally deployed system helps users:

- Recognize gastroenteritis symptoms
- Understand warning signs of dehydration
- Get safe home-care recommendations
- Know when to consult a medical professional

Built using:

- ✅ AnythingLLM (Docker)
- ✅ Ollama (Local LLM Runner)
- ✅ Custom knowledge base (Nova Scotia & Canadian health sources)

---

## 📁 Project Structure

gastro-chatbot/
├── knowledge_base/
│ ├── knowledge_document_1.pdf
│ ├── knowledge_document_2.md
│ └── knowledge_document_3.txt
├── prompt/
│ └── system_prompt.txt
├── documentation/
│ ├── scenario_pack.md
│ └── use_case_description.md
├── demo/
│ ├── demo_video.mp4
│
└── README.md


---

## ⚙️ How to Run Locally

### 🐳 1. Install Docker

Download: https://www.docker.com/products/docker-desktop  
Ensure Docker is running on your system.

### 🤖 2. Run AnythingLLM via Docker

```bash
docker run -d --name anythingllm-container \
 -p 3001:3001 \
 -e STORAGE_DIR=/app/server/storage \
 -v anythingllm:/app/server/storage \
 mintplexlabs/anythingllm

Then visit:
#http://localhost:3001

Set Up Ollama
Download and install Ollama: https://ollama.com/download
ollama pull mistral
ollama run mistral

Demo Video
A 2:30 minute walkthrough showcasing chatbot responses to two core scenario questions:

“I’ve had watery diarrhea since last night — should I go see a doctor?”

“What should I eat or drink while I’m recovering from a stomach bug?”

#Location demo/demo_video.mp4

Disclaimer
This chatbot is for educational research only.
It does not provide medical diagnoses and is not a substitute for professional healthcare.
Please consult a licensed medical provider for any real health concerns.

Author
Himanshu Gupta
Master’s in Business Analytics
Sobey School of Business, Saint Mary's University
 July 2025
