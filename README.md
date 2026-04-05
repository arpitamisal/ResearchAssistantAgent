# 🔍 Research Assistant AI Agent

An AI-powered research assistant built using **LangChain**, **OpenAI**, and tool-calling agents that can search the web, fetch Wikipedia data, and save structured research outputs to a file.

## 🚀 Features

- 🌐 Web search using DuckDuckGo
- 📚 Wikipedia-based research
- 🧠 AI-generated structured responses
- 💾 Save research outputs to a `.txt` file
- 🛠️ Tool-calling agent using LangChain
- 📄 Structured output using Pydantic

---

## 🛠️ Tech Stack

- Python
- LangChain
- OpenAI (GPT-4o-mini)
- Pydantic
- DuckDuckGo Search
- Wikipedia API
- dotenv

---

## ⚙️ Setup Instructions

### 1. Clone the repo

```bash
git clone <your-repo-link>
cd ResearchAssistantAgent
```
### 2. Create virtual environment
```
python3 -m venv .venv
source .venv/bin/activate
```
### 3. Install dependencies
```
pip install -r requirements.txt
```
### 4. Add your API key

Create a .env file:
```
OPENAI_API_KEY=your_api_key_here
```
---

## ▶️ Usage

### Run the agent:
```
python main.py
```
#### Then enter a query like:

What is MCP server?
⚡ Example Output
```
{
  "topic": "MCP server",
  "summary": "An MCP server is a system that connects AI models to external tools and data...",
  "source": ["Wikipedia", "Web Search"],
  "tools_used": ["search", "wiki"]
}
```
---

## 🧠 How It Works

The agent uses multiple tools:

- search → Fetches real-time web results
- wiki → Retrieves summarized Wikipedia content
- save_text_to_file → Stores research output in a text file

### The AI agent:

- Understands the query
- Decides which tools to use
- Collects information
- Returns structured output
- Optionally saves results to a file

---
  
## 💾 Output Saving

All saved outputs are appended to:

research_output.txt

### Each entry includes:

- Timestamp
- Structured research data

---

## ⚠️ Notes
- .env is ignored for security
- Do not expose API keys
- DuckDuckGo search may fail on older Python SSL setups (use Python 3.11+)

---

## 🔮 Future Improvements
- Add PDF export
- Add streaming responses
- Improve error handling
- Add UI (Streamlit / React)
- Support multiple research topics at once
