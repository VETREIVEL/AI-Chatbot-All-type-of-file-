# 📘 Document Q&A System (Claude 3 Haiku)

This is a Python-based document question answering system built with **Streamlit** and powered by **Anthropic's Claude 3 Haiku**. It allows users to upload and query a variety of document formats (PDF, DOCX, PPTX, CSV, XLSX, TXT, JSON, images with OCR, and even URLs embedded within text) with natural language questions.

---

## 🚀 Features

- Upload multiple document types (PDF, DOCX, PPTX, XLSX, CSV, TXT, JSON, PNG, JPG).
- Extracts and processes text using OCR and parsers.
- Integrates with Claude 3 Haiku via the Anthropic API.
- Intelligent chunking and scoring to find relevant document context.
- Simple Streamlit UI for chatting with your documents.

---

## 🧠 System Architecture

### `Pipeline Overview`

1. **Upload Files**:
   - Supports PDF, DOCX, PPTX, XLSX, CSV, TXT, JSON, PNG, JPG.
2. **Extract Text**:
   - Each format is parsed separately. Images are handled using Tesseract OCR.
   - Embedded URLs are fetched and parsed via BeautifulSoup.
3. **Chunk and Match**:
   - Text is split into overlapping chunks. Relevance is scored based on keyword overlap.
4. **Claude API Call**:
   - The most relevant chunk is used as context in a Claude 3 Haiku prompt.
