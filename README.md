# screenshot-to-code

This app converts a screenshot to code (HTML/Tailwind CSS, React, Bootstrap, or Vue). It uses GPT‑4 Vision or Claude 3 to generate the code and can also generate similar-looking images. You can enter a URL to clone a live website.

## 🚀 Try It Out!

You can run it locally with your own OpenAI key (must have access to GPT‑4 Vision). See the instructions below.

## 🌟 Recent Updates

- Mar 8 – Video-to-app: turn videos/screen recordings into functional apps  
- Mar 5 – Added support for Claude Sonnet 3 (fast and capable)

## 🛠 Getting Started

The app has a React/Vite frontend and a FastAPI backend. You will need an OpenAI API key with access to the GPT‑4 Vision API.

Run the backend (using Poetry for package management):

```bash
cd backend
echo "OPENAI_API_KEY=sk-your-key" > .env
poetry install
poetry shell
poetry run uvicorn main:app --reload --port 7001
```

Run the frontend:

```bash
cd frontend
yarn
yarn dev
```

Open http://localhost:5173 to use the app.

If you prefer to run the backend on a different port, update `VITE_WS_BACKEND_URL` in `frontend/.env.local`.

For debugging, you can run the backend in mock mode (streams a pre-recorded response):

```bash
MOCK=true poetry run uvicorn main:app --reload --port 7001
```

## Video to App (experimental)

Record yourself using any website, app, or prototype, drag & drop in a video, and get a functional, similar-looking app.  
Requires an Anthropic API key.

## Configuration

- Configure the OpenAI base URL if you need to use a proxy: set `OPENAI_BASE_URL` in `backend/.env` or directly in the UI.

## Using Claude 3

Support for Claude 3 Sonnet is included.  
1. Add `ANTHROPIC_API_KEY` to `backend/.env` with your Anthropic key.  
2. Select "Claude 3 Sonnet" from the model dropdown in the frontend.

## Docker

If you have Docker installed:

```bash
echo "OPENAI_API_KEY=sk-your-key" > .env
docker-compose up -d --build
```

The app will be available at http://localhost:5173.  
Note: file changes won’t trigger rebuilds in this setup.

## 🙋 FAQs

- **Error setting up backend?** See open issues in the repo for fixes.  
- **How do I get an OpenAI API key?** Check the official OpenAI docs.  
- **Feedback or bug reports?** Open an issue in this repository.

## 📚 Examples

Examples include replicas of popular sites like NYTimes, Instagram, and Hacker News. See the repo for demo screenshots.

## 🌍 Hosted Version

You can also run the hosted version with your own OpenAI key (must have GPT‑4 Vision access).

---

## 🎨 Branding

This project is powered by **[brelinx.com](https://brelinx.com)** - Your trusted partner for innovative web solutions.

---

**GitHub Repository:** [https://github.com/Uwami-Mgxekwa/](https://github.com/Uwami-Mgxekwa/)
