
---
# 📝 Docs2PPT - Convert PDF/DOCX to PowerPoint Slides (Flask + Gemini API)

🚀 **Live Demo**: [https://version0docs2ppt.onrender.com/](https://version0docs2ppt.onrender.com/)

This project allows users to upload **PDF or DOCX** files and generates AI-powered PowerPoint slides using **Gemini API**. Built with **Flask**, it includes cleanup of temporary files and supports deployment to platforms like **Render.com**.

---

## 🚀 Features

* 📄 Upload DOCX or PDF documents
* 🤖 Extract slide content using Gemini API
* 📊 Auto-generate PowerPoint presentations
* 🧹 Auto-cleanup of files older than 15 minutes
* 🌐 Web interface with upload and result screens
* 🛡️ Environment variable support via `.env`

---

## 🧱 Project Structure

```
version0/
├── app.py                 # Main Flask app
├── main.py                # Gemini logic
├── layout.py, style.py    # Slide layout and styles
├── pdf_to_json.py         # PDF/DOCX to slide data extractor
├── templates/             # HTML templates (upload/result)
├── static/                # Static assets
├── uploads/               # Uploaded documents
├── output/                # Generated PPTX files
├── pdf_images/            # Extracted images from PDFs
├── requirements.txt       # Python dependencies
├── runtime.txt            # Python version info
├── .env                   # Environment variables (not tracked)
├── .gitignore             # Git ignore file
```

---

## ⚙️ Setup Instructions (Local)

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/docs2ppt-flask.git
cd docs2ppt-flask/version0
```

### 2. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate (Windows)
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Add `.env` File

Create a `.env` file in the `version0/` folder:

```
GEMINI_API_KEY=your_actual_key_here
```

### 5. Run the App Locally

```bash
python app.py
```

Visit: [http://localhost:8080/](http://localhost:8080/)

---

## 🌐 Deployment (Render.com)

### 1. Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/docs2ppt-flask.git
git push -u origin main
```

### 2. Deploy on Render

* Go to [https://render.com](https://render.com)

* New Web Service → Connect your GitHub repo

* Build Command:

  ```bash
  pip install -r requirements.txt
  ```

* Start Command:

  ```bash
  gunicorn app:app
  ```

* Add Environment Variable:

  ```
  GEMINI_API_KEY=your_key
  ```

---

## 📎 Example Output

* **Input**: `khushi.pdf`
* **Output**: `khushi.pptx`
* Stored temporarily in `/uploads` and `/output` using session folders

---

## 🧼 Auto Cleanup

A background thread runs and deletes uploaded/generated files every 15 minutes for better resource management and security.

---

## 🛠️ Tech Stack

* Python 3.11.2
* Flask
* Gunicorn
* Gemini API (Google Generative AI)
* PyMuPDF, python-docx, python-pptx

---

## ❗ Disclaimer

This tool is an AI-powered educational demo and **not intended for handling sensitive or confidential documents**.

---

## 📄 License

[MIT License](https://opensource.org/licenses/MIT)

---

Would you like me to:

* Convert this to an actual downloadable `README.md` file?
* Add GitHub project badges?
* Auto-insert your GitHub username if you provide it?
