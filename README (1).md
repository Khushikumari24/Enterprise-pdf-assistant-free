# 🏢 Enterprise LLM PDF Assistant

> **100% Free** · No credit card · No paid API · Runs on Google Colab
> Powered by **Groq API** (free tier) + **Llama 3.3 70B**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO_NAME/blob/main/Enterprise_PDF_Assistant_FREE.ipynb)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Free API](https://img.shields.io/badge/API-Free%20Groq-brightgreen)](https://console.groq.com)
[![Model](https://img.shields.io/badge/Model-Llama%203.3%2070B-blue)](https://console.groq.com)

---

## ✨ Features

- 📄 Upload and analyze multiple PDFs at once
- 🤖 Multi-turn chat with your documents using Llama 3.3 70B
- 📋 One-click executive summaries
- 📊 Extract and format tables from PDFs
- 📅 Extract all dates, deadlines, and time references
- 🔢 Pull out financial figures and statistics
- ⚠️ Identify risks, warnings, and obligations
- ✅ List action items and requirements
- 🔍 Named entity extraction (people, orgs, locations)
- 📑 Compare multiple documents side by side
- 🌐 Gradio web UI with public share link
- 💾 Export conversation history as JSON

---

## 🚀 Quick Start

### Option 1 — Open directly in Google Colab (recommended)

Click the badge above ☝️ or this link:

```
https://colab.research.google.com/github/khushikumari24/Enterprise-pdf-assistant/blob/main/Enterprise_PDF_Assistant_FREE.ipynb
```

### Option 2 — Run locally

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set your free Groq API key
export GROQ_API_KEY=gsk_your_key_here

# 4. Open the notebook
jupyter notebook Enterprise_PDF_Assistant_FREE.ipynb
```

---

## 🔑 Getting Your Free API Key

No credit card required.

1. Go to **https://console.groq.com**
2. Sign up with email
3. Navigate to **API Keys** → **Create API Key**
4. Copy the key (starts with `gsk_...`)
5. Paste it into Step 2 of the notebook when prompted

---

## 📖 How to Use

### Step-by-step in Colab

| Step | What it does |
|------|-------------|
| Step 1 | Installs `groq`, `pymupdf`, `gradio` |
| Step 2 | Enter your free Groq API key (tested automatically) |
| Step 3 | PDF processing engine loads |
| Step 4 | Assistant initializes with Llama 3.3 70B |
| Step 5 | Upload PDF from computer, Google Drive, or URL |
| Step 6 | Run quick analysis tools |
| Step 7 | Interactive multi-turn chat |
| Step 8 | Launch full Gradio web UI |
| Step 9 | Export results |

### Uploading PDFs

**From your computer:**
```python
from google.colab import files
uploaded = files.upload()  # Opens file picker
```

**From Google Drive:**
```python
from google.colab import drive
drive.mount('/content/drive')
assistant.load_pdf("/content/drive/MyDrive/your_document.pdf")
```

**From a URL:**
```python
load_from_url("https://example.com/report.pdf")
```

### Quick Analysis

```python
# Executive summary
assistant.quick_summary()

# Extract tables
assistant.extract_tables()

# Extract specific info
assistant.extract_key_info("dates")     # all dates & deadlines
assistant.extract_key_info("numbers")   # financial figures
assistant.extract_key_info("risks")     # risks & warnings
assistant.extract_key_info("actions")   # action items
assistant.extract_key_info("entities")  # people, orgs, locations

# Compare multiple documents
assistant.compare_documents()
```

### Chat with your documents

```python
assistant.reset_conversation()
response = assistant.chat("What are the payment terms in this contract?")
print(response)
```

---

## 📊 Free Tier Limits (Groq)

| Limit | Value |
|-------|-------|
| Cost | **$0.00** |
| Credit card required | No |
| Requests per day | 14,400 |
| Tokens per minute | 500,000 |
| Tokens per request | 8,192 |
| Model | Llama 3.3 70B |

> Large PDFs (100+ pages) are automatically chunked to stay within the token limit.

---

## 🗂️ Project Structure

```
📦 enterprise-pdf-assistant
 ┣ 📓 Enterprise_PDF_Assistant_FREE.ipynb   ← Main notebook
 ┣ 📄 requirements.txt                       ← Python dependencies
 ┣ 📄 README.md                              ← This file
 ┣ 📄 LICENSE                                ← MIT license
 ┗ 📄 .gitignore                             ← Ignores secrets & cache
```

---

## 🔧 Tech Stack

| Component | Tool | Cost |
|-----------|------|------|
| LLM | Llama 3.3 70B via Groq | Free |
| PDF parsing | PyMuPDF | Free / Open source |
| Web UI | Gradio | Free / Open source |
| Runtime | Google Colab | Free |

---

## 💡 Tips for Best Results

- **Be specific** — "List all payment clauses on page 4" works better than "summarize"
- **Use quick actions** for structured extraction (tables, dates, numbers)
- **Reset conversation** before switching to a new topic
- **Multi-doc compare** works great for contracts vs amendments, or reports across quarters
- For **large PDFs**, ask page-specific questions like "What does page 12 say about pricing?"

---

## 📝 Example Use Cases

| Document type | Useful actions |
|---------------|---------------|
| Legal contracts | Extract parties, dates, obligations, risks |
| Financial reports | Extract numbers, compare periods |
| Research papers | Summarize, extract methodology & findings |
| Technical specs | Q&A, extract requirements |
| HR policies | Extract rules, action items, dates |

---

## 🤝 Contributing

Pull requests welcome! Please open an issue first to discuss any major changes.

---

## 📄 License

MIT — free to use, modify, and distribute.

---

*Built with Groq + Llama 3.3 70B. 100% free, no paid services required.*
