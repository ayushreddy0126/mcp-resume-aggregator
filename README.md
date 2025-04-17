



# 📄 AI Resume Summary Generator (Built on MCP)

🚀 An intelligent resume summarization tool that fetches your public profile data from multiple platforms and generates an ATS-friendly resume summary using OpenAI's GPT-3.5 — all orchestrated using the **Model-Compute-Platform (MCP)** architecture.

---

## 🧠 Features

- 🔗 Multi-source data fetching from:
  - ✅ GitHub
  - ✅ LinkedIn
  - ✅ Google Scholar
- 🧱 Built on modular MCP design: each data fetcher is pluggable
- ✨ AI-generated professional resume summary using LLMs (OpenAI)
- 🌗 Dark/Light mode UI (Streamlit frontend)
- 🖥️ Local frontend to test summary generation instantly

---

## 🧩 Architecture Diagram

![output](https://github.com/user-attachments/assets/351fdbab-e106-48d5-b3ab-2b3215343ee3)


---

## ⚙️ Tech Stack

| Layer       | Tools & Frameworks                     |
|-------------|----------------------------------------|
| Frontend    | Streamlit                              |
| Backend     | FastAPI (MCP Aggregator API)           |
| LLM Engine  | OpenAI GPT-3.5 via Python SDK          |
| Scraping    | `requests`, `BeautifulSoup`, `Selenium`|
| Integration | `.env` for secure API key management   |

---

## 📦 Project Structure

```
mcp-resume-aggregator/
├── app/                   # FastAPI backend
│   ├── main.py
│   ├── aggregator.py
│   └── fetchers/          # GitHub, Scholar, LinkedIn fetchers
├── llm/
│   └── llm_integration.py # LLM calling logic
├── frontend/
│   └── streamlit_app.py   # Streamlit UI
├── .env                   # API keys (not committed)
├── requirements.txt
└── README.md
```

---

## 🚀 Setup Instructions

1. **Clone the repo**
   ```bash
   git clone https://github.com/your-username/mcp-resume-aggregator.git
   cd mcp-resume-aggregator
   ```

2. **Create & activate virtual environment**
   ```bash
   python -m venv env
   source env/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create `.env` file**
   ```env
   OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxx
   ```

5. **Run FastAPI backend**
   ```bash
   uvicorn app.main:app --reload --port 8001
   ```

6. **Run Streamlit frontend**
   ```bash
   streamlit run frontend/streamlit_app.py
   ```

---

## 🧪 Example Input

```json
{
  "github": "ayushreddy0126",
  "linkedin": "ayushreddy0126",
  "scholar": "Ayush Reddy"
}
```

### 📝 Example Output

```text
Experienced professional with a strong background in engineering and technology. Skilled in project management, problem-solving, and communication...
```

---

## 🚧 Upcoming Features

- 🧾 Upload existing resume + paste job description
- 🧠 Tailor resume to match specific job posting (ATS optimization)
- 📥 Export to PDF / Markdown
- 🌐 Deploy as public demo

---

## 👨‍💻 Author

Built by **Ayush Reddy**  
Grad student, Computer Science 👨🏻‍💻 | Northeastern University 
[LinkedIn](https://www.linkedin.com/in/ayushreddy0126/) • [GitHub](https://github.com/ayushreddy0126)


