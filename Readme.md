# 🦺 HelmetAI — Real-Time Helmet Detection for Construction Site Safety

HelmetAI is an **AI-powered helmet detection system** designed to improve **construction site safety** by ensuring workers wear helmets at all times.  
Built with **YOLOv8** and a **FastAPI backend**, it detects helmets from **live camera feeds or uploaded images** in real-time.  
The system identifies workers without helmets and triggers instant alerts, helping supervisors enforce safety compliance and prevent workplace injuries.

---

## 🚀 Features

- 🎥 **Live Detection** — Detect helmets directly from your webcam feed  
- 🧠 **YOLOv8 Model** — Trained for construction site helmet detection  
- ⚡ **FastAPI Backend** — High-performance inference server  
- 🖼️ **Image Upload Detection** — Upload and test static images  
- 🔊 **Audio Alerts** — Instant beep for “no helmet” detections  
- 💡 **Interactive Frontend** — Built with React + Vite, with glassmorphism UI  
- 🌐 **Deployed on Render (backend)** and **Vercel (frontend)**  

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-------------|
| **Model** | YOLOv8 (Ultralytics) |
| **Backend** | FastAPI, Python |
| **Frontend** | React (Vite), Tailwind CSS, Framer Motion |
| **Deployment** | Render (API) + Vercel (UI) |
| **Alerts** | Howler.js for sound feedback |

---

## 📂 Project Structure

Helmet-Detection-YOLOv8/
│
├── app_fastapi.py # FastAPI app for YOLO inference
├── requirements.txt # Python dependencies
├── runs/
│ └── detect/train3/weights/best.pt # YOLOv8 trained weights
│
├── helmet-frontend/ # React Frontend
│ ├── src/
│ ├── package.json
│ ├── vite.config.js
│ └── ...


---

                                                                                        ## ⚙️ Setup Instructions (Local Development)

### 🔧 1. Clone this repository
```bash
git clone https://github.com/<your-username>/HelmetAI.git
cd HelmetAI
```


🧩 **2. Backend Setup (FastAPI + YOLOv8)**
    Step 1 — Create a virtual environment
            python -m venv venv
            venv\Scripts\activate   # (Windows)
# OR
source venv/bin/activate   # (Mac/Linux)

  Step 2 — Install dependencies
  pip install -r requirements.txt

  Step 3 — Verify YOLO model path

  Ensure your trained model is located at:
  runs/detect/train3/weights/best.pt

  Step 4 — Run the FastAPI server
  uvicorn app_fastapi:app --reload


💻** 3. Frontend Setup (React + Vite)**
Step 1 — Navigate to frontend
cd helmet-frontend

Step 2 — Install dependencies
npm install

Step 3 — Start development server
npm run dev


⚙️ 4. Connecting Frontend and Backend

**🧾 Requirements
Component	Requirements
Python	3.9 or above
Node.js	16 or above
YOLOv8	Ultralytics 8.x
Browser	Chrome / Edge (for webcam access)**


**🐍 Python Dependencies**
Listed in requirements.txt:

**📦 Node Dependencies (Frontend)**

Installed automatically via npm install:
react
vite
framer-motion
howler
axios
react-webcam
tailwindcss


🎯 Example Use Case

Construction site supervisor connects a CCTV or webcam to HelmetAI.
The system monitors workers in real time.
When a worker without a helmet is detected:

🔴 A red bounding box appears.

🔊 A warning beep is played.

🧠 Data can optionally be logged for safety reports.



**🧰 Future Improvements**

🧾 Automatic violation logging with timestamps

🛰️ Multi-camera monitoring dashboard

⚡ YOLOv8n quantization for faster inference

☁️ GPU-based inference using Google Cloud Run


🤝 Contributors

Ashutosh Dash


🧩 License

This project is licensed under the MIT License — feel free to use and modify with attribution.

🌟 Support

If you found this helpful, consider giving a ⭐ on GitHub!

                                                                              “A safer worksite is a smarter worksite — HelmetAI makes it happen.”

## 🧠 Next Step
After creating this `README.md`:
1. Save it in the root folder of your repo (`Helmet-Detection-YOLOv8/README.md`)
2. Commit & push:
   ```bash
   git add README.md
   git commit -m "Added detailed README documentation"
   git push
