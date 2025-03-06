# SONVÉ

**SONVÉ** transforms your voice into wearable art. By harnessing advanced audio signal processing and machine learning, it analyzes the emotions in your speech and dynamically generates unique accessory designs. Each piece is a visual manifestation of your mood—personal, expressive, and one-of-a-kind.

---

## Overview

SONVÉ is an innovative project that bridges technology and art by turning your voice into personalized accessory designs. The system extracts sound features using DTFT for pattern generation and MFCC for emotion classification. The resulting emotion is mapped to design attributes like color and pattern, creating a truly unique piece of wearable art every time you speak.

---

## Features

- **Voice-Activated Design:** Convert speech into dynamic accessory patterns.
- **Emotion Detection:** Leverages a CNN-LSTM model to classify your emotions from audio.
- **Signal Processing:** Uses DTFT and MFCC to capture the essence of your voice.
- **Unique Aesthetics:** Each design is a visual representation of your mood.
- **Cost-Effective & Scalable:** Built on free-tier cloud services for easy deployment.

---

## Tech Stack

- **Backend:** Python, FastAPI, TensorFlow/Keras, Librosa
- **Frontend:** Next.js, React, Three.js
- **Database:** PostgreSQL (via Supabase) or SQLite
- **Storage:** Cloudinary
- **Deployment:** Docker, Vercel, Render/Fly.io/Cloud Run

---

## Installation

### Prerequisites

- Python 3.9+
- Node.js 18+
- Git

### Quick Start

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/<your-username>/SONVE.git
   cd SONVE
   ```

2. **Backend Setup:**

   - Navigate to the `backend` directory:
     ```bash
     cd backend
     python3 -m venv venv
     source venv/bin/activate
     ```
   - Install dependencies:
     ```bash
     pip install -r requirements.txt
     ```
   - Create a `.env` file with your environment variables.
   - Start the FastAPI server:
     ```bash
     uvicorn api.main:app --reload
     ```

3. **Frontend Setup:**
   - Navigate to the `frontend` directory:
     ```bash
     cd ../frontend
     ```
   - Install Node dependencies:
     ```bash
     npm install
     ```
   - Create a `.env.local` file with:
     ```env
     NEXT_PUBLIC_API_URL=http://localhost:8000
     ```
   - Run the development server:
     ```bash
     npm run dev
     ```

---

## Usage

- **Local Development:**  
  Use the web UI to upload or record audio. The backend processes your voice, classifies the emotion, and dynamically generates a 2D design pattern that visually reflects your mood.

- **API Testing:**  
  Check the FastAPI docs at [http://localhost:8000/docs](http://localhost:8000/docs) to explore available endpoints.

---

## Roadmap

- [x] Setup & Environment Configuration
- [ ] Backend Development: Audio processing, ML integration, Cloudinary storage.
- [ ] Frontend Development: Minimal UI, API integration, 3D visualization.
- [ ] Integration & Testing
- [ ] Deployment & Monitoring
- [ ] Optimization & Scaling

_Turn your voice into art with SONVÉ!_
