Here’s a complete `README.md` tailored for your **Docs to PPT (Flask)** project, ready to be published on GitHub:

---
# 📝 Docs2PPT - Convert PDF/DOCX to PowerPoint Slides (Flask + Gemini API)

This project allows users to upload **PDF or DOCX** files and generates AI-powered PowerPoint slides using **Gemini API**. Built with **Flask**, it includes cleanup of temporary files and supports deployment to platforms like **Render.com**.

---

## 🚀 Features

- 📄 Upload DOCX or PDF documents
- 🤖 Extract slide content using Gemini API
- 📊 Auto-generate PowerPoint presentations
- 🧹 Auto-cleanup of files older than 15 minutes
- 🌐 Web interface with upload and result screens
- 🛡️ Environment variable support via `.env`

---

## 🧱 Project Structure

```

version0/
├── app.py                 # Main Flask app
├── main.py                # Optional, includes Gemini logic
├── layout.py, style.py    # Slide layout and styles
├── pdf\_to\_json.py         # PDF to slide content extractor
├── templates/             # HTML templates (upload/result)
├── static/                # Static assets (if any)
├── uploads/               # Uploaded documents
├── output/                # Generated PPTX files
├── pdf\_images/            # Extracted images from PDFs
├── requirements.txt       # Project dependencies
├── runtime.txt            # Python runtime (e.g., python-3.11.2)
├── .env                   # Environment secrets (excluded from Git)
├── .gitignore             # Files to ignore in Git



---

## ⚙️ Setup Instructions (Local)

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/docs2ppt-flask.git
cd docs2ppt-flask/version0
````

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

Visit: `http://localhost:8080/`

---

## 🌐 Deployment (Render.com)

### 1. Push to GitHub

Make sure your project is in a Git repo and pushed to GitHub.

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/docs2ppt-flask.git
git push -u origin main
```

### 2. Deploy on Render

* Go to [https://render.com](https://render.com)
* New Web Service → Connect GitHub Repo
* Build Command:

  ```bash
  pip install -r requirements.txt
  ```
* Start Command:

  ```bash
  gunicorn app:app
  ```
* Add environment variable:
  `GEMINI_API_KEY=your_key`

---

## 📎 Example Output

* Input: `khushi.pdf`
* Output: `khushi.pptx`
* Stored temporarily in `/uploads` and `/output` with session-based folders

---

## 🧼 Auto Cleanup

A background thread removes uploaded/generated files every 15 minutes for security and storage control.

---

## 🛠️ Tech Stack

* Python 3.11.2
* Flask
* Gunicorn
* Gemini API (by Google)
* pdf2image, python-docx, python-pptx

---

## ❗ Disclaimer

This tool is an AI demonstration and **not for confidential or sensitive documents**.

---

## 📄 License

MIT License

```

---

Would you like me to:

- Turn this into a real `README.md` file for download?
- Include project badges (e.g., Build passing, Python version)?
- Auto-fill your GitHub username/repo name?
```
