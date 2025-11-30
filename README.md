# 🚀 Multimodal AI System  
*A browser-style interface for Image Captioning (BLIP) + Image Search (CLIP) using Django*

---

## 📌 Overview
Multimodal AI System is a modern, browser-like web interface that supports:

### ✅ **Image → Text (Captioning)**  
Upload an image and generate a natural language caption using:

- **BLIP – Salesforce/blip-image-captioning-base**

### ✅ **Text → Image (Search)**  
Enter a text prompt (e.g., “cat”, “sunset”, “dog running”), and the system returns the closest matching image from your dataset using:

- **CLIP – openai/clip-vit-base-patch32**

### 🎨 Modern UI  
Designed with a clean dark theme inspired by ChatGPT/Gemini:

- Center pill-shaped input bar  
- Floating upload button (`+`)  
- Browser-style search field  
- Smooth mode switching (Upload ↔ Search)  
- Results panel with shadows, animations

---

## 🧠 Features

### 1️⃣ **Image Captioning (Upload → Caption)**
- Upload any image
- Stored in `/media/`
- BLIP generates caption
- Result displayed with image preview + caption text

---

### 2️⃣ **Image Search (Text → Image)**
- Uses CLIP text embedding → image embedding similarity
- Searches in `/media/search_images/`
- Calculates cosine similarity
- Filters with threshold to avoid irrelevant matches
- Returns best photo and query

---

### 3️⃣ **Unified Django Backend**
Contains:
- BLIP processor + model
- CLIP processor + model
- Image management
- Cosine similarity search
- Claude API fallback (optional)
- Upload endpoint for search dataset

---

### 4️⃣ **Modern UI / UX**
- Upload popup that works in both modes
- Dark mode gradients
- Clean result cards
- Responsive layout for mobile/desktop
- ChatGPT-like rounded components

---

## 📂 Project Structure

project/
│── manage.py
│── media/
│ └── search_images/
│── app/
│ │── views.py
│ │── urls.py
│ │── templates/
│ │ └── index.html
│ └── static/
│
└── requirements.txt

yaml
Copy code

---

## ⚙️ Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/yourusername/multimodal-ai-system.git
cd multimodal-ai-system
2️⃣ Create virtual environment
bash
Copy code
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
3️⃣ Install dependencies
bash
Copy code
pip install -r requirements.txt
4️⃣ Run migrations
bash
Copy code
python manage.py migrate
5️⃣ Start server
bash
Copy code
python manage.py runserver
📦 Requirements
requirements.txt must include:

nginx
Copy code
django
torch
transformers
pillow
requests
(Optionally add gunicorn, whitenoise, etc. for production.)

📸 Usage Guide
Image Captioning
Click the + icon

Upload a picture

Click the ↓ button

BLIP caption appears in the results panel

Image Search
Switch to Search Images mode

Type text prompt

Click the ↓ button

CLIP returns best match from /media/search_images/

📁 Adding Search Images
Place your dataset images inside:

bash
Copy code
media/search_images/
Supported formats: .jpg, .jpeg, .png, .bmp, .gif

🔥 API Endpoints
/
Main UI + BLIP + CLIP integration

/api/upload_search_image/
Uploads a new image to search dataset

/api/unified_chat/
Claude / fallback model chat API (optional)

🧪 Tech Stack
Frontend: HTML, CSS, JavaScript

Backend: Django

AI Models:

BLIP (image captioning)

CLIP (image similarity search)

Storage: Local media/ folder

🧩 Future Enhancements (Optional)
Full chat interface with Claude / GPT

Live preview of embeddings

Batch captioning / search

Image-to-image search using CLIP

Browser-like History Panel

Mobile app version (Flutter)

📝 License
MIT License — free to use and modify.

✨ Author
Created by Gopija — Paday Thalapathi
Multimodal AI • Vision Models • Full-Stack Development

yaml
Copy code

---

If you want, I can also generate:

✔ `requirements.txt`  
✔ `urls.py`  
✔ Deploy-ready Dockerfile  
✔ A full GitHub project structure  

Just tell me!





