
# Crop Prediction Web Application

This is a simple web application that allows farmers to upload crop images and predict the **variety**, **disease**, or **age** using machine learning models. It has a user-friendly React frontend and a Flask backend with trained TensorFlow models.

---

## What You Need

### General Requirements
- **Python 3.10+**
- **Node.js (LTS version)**
- **Git (optional but helpful)**

---

## How to Set Up (for Non-IT Users)

### For Windows

1. **Install Python**
   - Download: https://www.python.org/downloads/windows/
   - During installation, **check** the box: **Add Python to PATH**
   - Open Command Prompt and run:
     ```bash
     python --version
     ```

2. **Install Node.js**
   - Download: https://nodejs.org
   - Choose the **LTS version**

3. **Install Git (optional)**
   - https://git-scm.com/download/win

---

### For macOS

1. **Install Python**
   - Open Terminal and run:
     ```bash
     brew install python
     ```

2. **Install Node.js**
   - Run:
     ```bash
     brew install node
     ```

3. **Install Git (optional)**
   - Run:
     ```bash
     brew install git
     ```

---

##  Folder Structure

```
Crop-Prediction-Application/
├── Crop-Prediction-Application-Front-end/   ← React + Vite frontend
└── Crop-Prediction-Application-Back-end/    ← Flask backend with models
```

---

Loading the Model from a Zip File
Because the model is large and exceeds GitHub’s file size limit, it is zipped and stored in the backend.

Steps to Use the Zipped Model:
Find the zip file

Location: Crop-Prediction-Application-Back-end/models/

Example file: variety_model.zip

Unzip the mode

In app.py, load the model path like this : MODEL_PATH = 'models/model/variety_model.keras'
##  How to Run the App

### 1. Run the Backend (Flask)

> Go to the backend folder.

```bash
cd Crop-Prediction-Application-Back-end
```

> Install required Python packages:

```bash
pip install flask tensorflow pillow
```

> Start the Flask server:

```bash
python app.py
```

> The server should run at `http://localhost:5000`

---

### 2. Run the Frontend (React + Vite)

> Open a second terminal and go to the frontend folder:

```bash
cd Crop-Prediction-Application-Front-end
```

> Install dependencies:

```bash
npm install
```

> Start the React app:

```bash
npm run dev
```

> The app should run at `http://localhost:5173`

---

##  Using the App

1. Open your browser and go to `http://localhost:5173`
2. Select a prediction task (Variety, Disease, or Age)
3. Upload a crop image (JPG or PNG)
4. Click **Upload & Predict**
5. The result will be shown below the image

---

##  Notes

- All models are pre-trained and saved as `.keras` files in the backend.
- Images are not stored in a database, only temporarily used for prediction.

---

##  Troubleshooting

- **If you get `'pip' is not recognized`**:
  - On Windows: Reinstall Python and check "Add to PATH"
- **If the frontend shows "Prediction failed"**:
  - Make sure Flask backend is running at `localhost:5000`
- **Need Help?**
  - Ask the project owner or search the error on Google/ChatGPT 😊

---

## Author
If you have questions, reach out to the developer of this app.
