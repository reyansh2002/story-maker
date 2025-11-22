🎨 Image-to-Story Generator

A multimodal AI project using Azure Vision, Azure OpenAI, and Azure Speech Services

This project converts any uploaded image into a 200-word AI-generated story, with an optional AI narration (Text-to-Speech).
It uses Azure Cognitive Services to analyze the image, generate a story, and read it aloud — all inside an interactive Streamlit web interface.

🚀 Features
🔍 AI Vision

Extracts image captions using Azure AI Vision (Image Analysis API)

Uses both CAPTION and DENSE_CAPTIONS for richer context

✍️ AI Story Generation

Uses Azure OpenAI GPT models

Generates a 200-word story based on the image + chosen genre

Allows downloading the story as a text file

🔊 AI Narration (Text-to-Speech)

Converts the generated story into natural-sounding audio

Uses Azure Speech Services

Saves the audio file locally and plays it in the UI

🖥️ Interactive UI (Streamlit)

Upload image

Choose a genre

Generate story

Enable narration

Preview and download outputs

🛠 Tech Stack
Component	Technology
Backend	Python
Web UI	Streamlit
Image Captioning	Azure Vision API
Story Generation	Azure OpenAI (GPT model)
Narration	Azure Cognitive Speech Services
Environment	dotenv
File Handling	PIL
📂 Project Structure
📁 project/
│── images/                 # Stores uploaded images
│── Audio/                  # Stores generated narration
│── app.py (your main script)
│── .env (Azure credentials)
│── requirements.txt

🔧 Setup Instructions
1️⃣ Install Dependencies
pip install streamlit azure-ai-vision azure-cognitiveservices-speech openai python-dotenv pillow

2️⃣ Add Environment Variables

Create a .env file:

AI_SERVICE_ENDPOINT=your_azure_vision_endpoint
AI_SERVICE_KEY=your_azure_vision_key

AZURE_OAI_ENDPOINT=your_openai_endpoint
AZURE_OAI_KEY=your_openai_key
AZURE_OAI_DEPLOYMENT=your_gpt_deployment_name

SPEECH_KEY=your_speech_key
SPEECH_REGION=your_speech_region

3️⃣ Run the App
streamlit run app.py

🎯 How It Works (Pipeline)

User uploads an image

Azure Vision generates captions

Caption + genre → prompt for Azure OpenAI

GPT model writes 200-word story

(Optional) Azure Speech generates audio narration

User downloads story and audio files

📦 Requirements

Python 3.8+

Azure Subscription

Azure Vision + Azure OpenAI + Speech Services

Streamlit installed

🧠 Future Enhancements

Multi-language story + narration

Style-transfer stories (humor, thriller, kids, etc.)

UI theme customization

Save history of generated stories
