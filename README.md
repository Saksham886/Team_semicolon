# Melo - Your AI Friend for Mental Well-Being

Melo is a mental well-being app that tracks emotions based on audio conversations. It integrates with our proprietary emotion detection model, *Colon*, to analyze speech, detect emotions, and generate personalized AI-driven responses. Melo acts as your AI companion, offering emotional support and insights into your mental health trends.

## Features

- *Emotion Detection*: Analyzes speech patterns to understand emotions.
- *AI Conversations*: Engages in meaningful conversations based on detected emotions.
- *Emotion Insights*: Provides a pie chart visualization of past emotions to track emotional well-being over time.

## Testing the App

You can test the app through this Drive link:
https://drive.google.com/drive/folders/1wQ8tAipVWCv98bwTAIuMDelGI6KA2xz2?usp=sharing

## Tech Stack

- *Frontend*: Flutter
- *Backend*: FastAPI (or any API service used)
- *Emotion Detection Model*: Colon (our very own ML model)

## Contributing

We welcome contributions! If you’d like to improve Melo, feel free to open an issue or submit a pull request.

## License

Melo is open-source. Feel free to use and modify it as needed.

---

Built with ❤ to support mental well-being.


# Voice Emotion Detection API

## 📦 *Project Overview*
This project uses *FastAPI* to deploy a voice emotion detection model. The model is stored in a pickle file (best_rf_model.pkl) and is downloaded from *Hugging Face* if not found locally. It extracts audio features using *librosa* and predicts the mood.

## 🚀 *Setup Instructions*

### 1. *Clone the Repository*
bash
git clone https://github.com/your-repo/voice-emotion-api.git
cd voice-emotion-api


### 2. *Create a Virtual Environment*
bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


### 3. *Install Requirements*
Ensure you have a requirements.txt file with the following (or similar) dependencies:

fastapi
uvicorn
librosa
numpy
joblib
requests

bash
pip install -r requirements.txt


## 📤 *Running the API*

### 4. *Run Locally*
bash
uvicorn main:app --host 0.0.0.0 --port 8000


## 🔍 *Using the API*

### *Endpoint:*

POST /predict


### *Request Format:*
- Upload a .wav audio file.

### *Response Format:*
json
{
  "mood": "Predicted mood label"
}


## 📤 *Deployment (On Railway)*

1. *Login to Railway:*
   - Go to [Railway.app](https://railway.app/).
2. *Create a New Project:*
   - Connect your GitHub repository.
3. *Add Environment Variables (if needed):*
   - Example: PORT=8000
4. *Deploy the Project.*

## ⚠ *Common Issues*

- *Model Not Found:*
  - Ensure the correct Hugging Face username and repository.
- *Port Issues:*
  - Use os.environ.get("PORT", 8000) for dynamic port allocation.
- *Librosa Load Error:*
  - Verify audio file format and sampling rate.

## 📞 *Contact*
For any questions, feel free to reach out at *your.email@example.com*.
