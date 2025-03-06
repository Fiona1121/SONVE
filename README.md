# SONVÉ 🎤✨

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Next.js](https://img.shields.io/badge/Next.js-12-blue)](https://nextjs.org/)

> **SONVÉ** transforms your voice into wearable art. By analyzing your speech with advanced signal processing and machine learning, SONVÉ creates unique accessory designs that reflect your emotions. Every design is as unique as your mood!

## 🚀 Features

- 🎙 **Voice-Activated Design** – Converts speech into dynamic accessory patterns.
- 🤖 **Emotion Detection** – Utilizes a CNN-LSTM model to classify your emotions from audio.
- 🔊 **Signal Processing** – Extracts dominant frequencies (via DTFT) and MFCC features from your voice.
- 🎨 **Design Mapping** – Maps detected emotions to design elements (like color and pattern).
- 💡 **Cost-Effective & Scalable** – Built on free-tier cloud services for effortless deployment.

## 🛠️ Tech Stack

- **Backend:** Python, FastAPI, TensorFlow/Keras, Librosa, Uvicorn
- **Frontend:** Next.js, React, Three.js (for visualizations)
- **Database:** PostgreSQL (via Supabase) or SQLite
- **Storage:** Cloudinary
- **Deployment:** Docker, Vercel, Render/Fly.io/Cloud Run

## 📥 Installation

### 1️⃣ Clone the Repository

```sh
git clone https://github.com/your-username/SONVE.git
cd SONVE
```

````

### 2️⃣ Backend Setup

- **Navigate to the backend directory:**

  ```sh
  cd backend
  ```

- **Create & activate a virtual environment:**

  ```sh
  python3 -m venv venv
  source venv/bin/activate  # On Windows: venv\Scripts\activate
  ```

- **Install dependencies:**

  ```sh
  pip install -r requirements.txt
  ```

- **Configure Environment Variables:**
  Create a `.env` file in the `backend` directory:

  ```ini
  API_HOST=0.0.0.0
  API_PORT=8000
  DATABASE_URL=<your_database_url>
  CLOUDINARY_CLOUD_NAME=<your_cloudinary_cloud_name>
  CLOUDINARY_API_KEY=<your_cloudinary_api_key>
  CLOUDINARY_API_SECRET=<your_cloudinary_api_secret>
  MODEL_PATH=./model.h5
  ```

- **Start the FastAPI Server:**

  ```sh
  uvicorn api.main:app --reload
  ```

### 3️⃣ Frontend Setup

- **Navigate to the frontend directory:**

  ```sh
  cd ../frontend
  ```

- **Install Node dependencies:**

  ```sh
  npm install
  ```

- **Create a `.env.local` file:**

  ```ini
  NEXT_PUBLIC_API_URL=http://localhost:8000
  ```

- **Start the Next.js Development Server:**

  ```sh
  npm run dev
  ```

- Open your browser at [http://localhost:3000](http://localhost:3000) to see the app.

## 📂 Project Structure

```plaintext
SONVE/
├── backend/
│   ├── audio_processing/
│   │   ├── record_audio.py       # Record or import audio
│   │   ├── preprocess.py         # Noise reduction & normalization
│   │   └── feature_extraction.py # MFCC & DTFT extraction functions
│   ├── ml_model/
│   │   ├── train_model.py        # CNN-LSTM model training script
│   │   └── predict_emotion.py    # Emotion prediction logic
│   ├── api/
│   │   ├── main.py               # FastAPI application entry point
│   │   └── routes/
│   │       ├── audio.py          # Audio processing endpoints
│   │       └── health.py         # Health check endpoint
│   ├── database/
│   │   ├── models.py             # Database schema models
│   │   └── crud.py               # CRUD operations
│   ├── requirements.txt          # Python dependencies
│   └── Dockerfile                # Docker configuration for backend
├── frontend/
│   ├── app/                      # Next.js App Directory
│   │   ├── layout.js             # Global layout component
│   │   └── page.js               # Main page with audio upload & preview UI
│   ├── components/
│   │   └── TwoDPattern.js        # 2D pattern visualization component
│   ├── services/
│   │   └── api.js                # API communication layer
│   ├── next.config.js            # Next.js configuration
│   ├── package.json              # Node dependencies
│   └── Dockerfile                # Docker configuration for frontend
└── deployment/
    ├── backend-deployment.yaml   # Kubernetes deployment for backend
    ├── frontend-deployment.yaml  # Kubernetes deployment for frontend
    └── ingress.yaml              # Ingress configuration for routing
```

## ⚙️ Usage

- **Local Development:**
  Use the UI to record or upload audio. The backend processes your voice, classifies your emotion, and generates a 2D design pattern that reflects your mood.

- **API Testing:**
  Visit [http://localhost:8000/docs](http://localhost:8000/docs) for interactive API documentation.

## 🚧 Roadmap

- [x] **Project Setup & Environment Configuration**
- [ ] **Audio Processing & Feature Extraction**
- [ ] **ML Model Development & Training**
- [ ] **Backend API Integration**
- [ ] **Frontend UI Development**
- [ ] **End-to-End Integration & Testing**
- [ ] **Deployment to Production**
- [ ] **Performance Optimization & Scaling**

_Transform your voice into art with SONVÉ!_
````
