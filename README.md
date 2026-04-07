<div align="center">

# 🚀 SEO AI Generator

### *Turn any topic into a fully optimized, AI-crafted article — in seconds.*

> Powered by Groq AI · Fueled by SerpAPI · Built for scale

[![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-009688?style=flat-square&logo=fastapi)](https://fastapi.tiangolo.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)]()

</div>

---

## ✨ What is SEO AI Generator?

**SEO AI Generator** is a full-stack AI-powered SEO automation tool that researches, writes, and scores SEO-optimized content for any topic — all from a clean, intuitive web UI. Just enter a keyword, hit generate, and get a publication-ready article backed by real search data and competitor insights.

No manual keyword research. No guessing. Just results.

---

## 🚀 Features

- 🔍 **Smart Keyword Research** — Uses SerpAPI to fetch real-time keyword data, search volume trends, and top-ranking queries for your topic
- 🕵️ **Competitor Insights** *(optional)* — Scrapes top-ranking competitor pages using BeautifulSoup to extract key themes, headings, and content patterns
- 🧠 **AI Content Generation** — Generates high-quality, SEO-optimized articles using the blazing-fast **Groq API** (LLaMA 3 / Mixtral)
- 📊 **SEO Scoring Engine** — Rates generated content on keyword density, readability, meta structure, heading hierarchy, and more via custom scoring logic
- 🖥️ **Clean Web UI** — A responsive HTML/CSS/JS frontend served via FastAPI — no React, no bloat, just fast and clean
- ⚡ **FastAPI Backend** — Asynchronous, production-ready REST API that handles all processing in the background
- 🔐 **Secure API Key Management** — All secrets managed via `.env` file, never exposed to the frontend

---

## 🧠 Tech Stack

| Layer | Technology |
|-------|-----------|
| 🐍 Backend | **FastAPI** (Python) |
| 🎨 Frontend | **HTML5, CSS3, Vanilla JavaScript** |
| 🤖 AI Engine | **Groq API** (LLaMA 3 / Mixtral) |
| 🔎 Keyword Research | **SerpAPI** |
| 🕸️ Web Scraping | **BeautifulSoup4 + Requests** |
| 🔧 Environment | **python-dotenv** |
| 📦 Package Manager | **pip** |

---

## 📂 Project Structure

```
seo-ai-generator/
│
├── backend/
│   ├── main.py                  # FastAPI app entry point
│   ├── routes/
│   │   ├── generate.py          # /generate endpoint
│   │   └── keywords.py          # /keywords endpoint
│   ├── services/
│   │   ├── groq_service.py      # Groq API integration
│   │   ├── serp_service.py      # SerpAPI integration
│   │   ├── scraper.py           # Competitor scraping logic
│   │   └── seo_scorer.py        # Custom SEO scoring engine
│   └── utils/
│       └── helpers.py           # Utility functions
│
├── frontend/
│   ├── index.html               # Main UI page
│   ├── style.css                # Styling
│   └── script.js                # Frontend logic & API calls
│
├── .env.example                 # Environment variable template
├── requirements.txt             # Python dependencies
├── .gitignore
└── README.md
```

---

## ⚙️ Installation & Setup

Follow these steps to get the project running locally:

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/seo-ai-generator.git
cd seo-ai-generator
```

### 2. Create a Virtual Environment

```bash
python -m venv venv

# Activate it:
# On Windows:
venv\Scripts\activate

# On macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

```bash
cp .env.example .env
```

Then open `.env` and fill in your API keys (see [Environment Variables](#-environment-variables) below).

### 5. Run the Backend

```bash
cd backend
uvicorn main:app --reload
```

The API will be live at: `http://127.0.0.1:8000`

### 6. Open the Frontend

Open `frontend/index.html` directly in your browser, **or** serve it via FastAPI's static files (configured by default).

```
http://127.0.0.1:8000
```

---

## 🔑 Environment Variables

Create a `.env` file in the root directory with the following keys:

```env
# .env

# Groq API Key — https://console.groq.com
GROQ_API_KEY=your_groq_api_key_here

# SerpAPI Key — https://serpapi.com/manage-api-key
SERP_API_KEY=your_serpapi_key_here
```

> ⚠️ **Never commit your `.env` file to GitHub.** It's already listed in `.gitignore`.

---

## ▶️ Usage

Using SEO AI Generator is as simple as 1-2-3:

1. **Enter a Topic** — Type your target keyword or article topic in the search bar (e.g., *"best Python frameworks 2025"*)
2. **Click Generate** — Hit the **Generate** button and let the AI do its magic
3. **Review Your Results** — The tool will display:
   - 📝 Full AI-generated article
   - 🔑 Researched keywords with relevance scores
   - 📊 SEO score breakdown (readability, density, structure)
   - 🕵️ Competitor insights *(if enabled)*

That's it. Copy, edit, publish.

---

## 📸 Screenshots

> 🖼️ *Screenshots coming soon — the contributor will add UI previews here.*

| Home Screen | Results Page | SEO Score Panel |
|:-----------:|:------------:|:---------------:|
| *(coming soon)* | *(coming soon)* | *(coming soon)* |

---

## 💡 Future Improvements

Here's what's on the roadmap:

- [ ] 🎨 **Enhanced UI/UX** — Dark mode, animations, and a more polished design system
- [ ] 📈 **Advanced SEO Metrics** — Backlink analysis, Core Web Vitals hints, schema suggestions
- [ ] 🌐 **Auto Blog Publishing** — Direct integration with WordPress, Ghost, or Hashnode APIs
- [ ] 📊 **Analytics Dashboard** — Track content history, score trends, and keyword performance
- [ ] 🌍 **Multi-language Support** — Generate content in multiple languages
- [ ] 🔁 **Batch Generation** — Generate multiple articles from a keyword list at once
- [ ] 🔌 **Plugin System** — Allow custom SEO scoring rules and AI prompt templates

---

## 🤝 Contributing

Contributions are welcome and appreciated! 🙌

If you'd like to improve this project — whether it's fixing a bug, adding a feature, or improving documentation — feel free to:

1. Fork the repo
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add: your feature description'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

Please make sure your code is clean and well-commented.

---

## 📜 License

This project is licensed under the **MIT License** — you're free to use, modify, and distribute it.

See the [LICENSE](LICENSE) file for full details.

---

<div align="center">

**Built with 🧠 AI + ❤️ passion by [Kartvaya](https://github.com/Kartvaya2008)**

*If this project helped you, drop a ⭐ on GitHub — it means a lot!*

</div>
