# SAT Practice App (32Q) — Frontend + Node backend (AI)

## What this is
A SAT-style practice app:
- Login starts a fresh **32-question** session
- 32-question UI with option selection, flag + highlight, and wrong-answer explanations
- Second chance mode (regenerates a new set for missed skills)

Question generation can use a real AI backend (OpenAI) via `POST /api/questions`.

## Folder structure
- `index.html`, `styles.css`, `app.js` : frontend
- `server.js` : backend API

## Setup (local)
### 1) Install backend dependencies
In PowerShell:
```powershell
cd C:\Users\Aadith\Desktop\sat-practice-app
npm install
```

### 2) Configure API key
Copy `.env.example` → `.env`:
```powershell
copy .env.example .env
```
Edit `.env` and set:
- `OPENAI_API_KEY=...`

### 3) Start backend
```powershell
npm run dev
```
Backend runs on: `http://localhost:3000`

### 4) Open frontend
Open:
- `C:\Users\Aadith\Desktop\sat-practice-app\index.html`

> If your browser blocks direct API calls from `file://`, open the frontend via a local server too.
> Example:
> `python -m http.server 8000 --directory C:/Users/Aadith/Desktop/sat-practice-app`
> then open: `http://localhost:8000/`

## Run on GitHub
1. Create a repo on GitHub.
2. In this folder:
```powershell
git init
git add .
git commit -m "Initial SAT practice app"
git branch -M main
git remote add origin https://github.com/<USER>/<REPO>.git
git push -u origin main
```

## Note
Do not commit `.env` or your API key.
Add it to `.gitignore` if you want.

