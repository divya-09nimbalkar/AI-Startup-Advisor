
```markdown
#  AI Meeting Assistant

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini-2.5--flash-blueviolet.svg)](https://aistudio.google.com/)
[![Whisper](https://img.shields.io/badge/Whisper-OpenAI-darkblue.svg)](https://openai.com/whisper)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production_Ready-brightgreen.svg)]()

>  Transform raw meeting voice recordings or conversational text scripts into concise business briefings, categorized task tracking logs, formatted Word document artifacts, and ready-to-send corporate follow-up emails instantly. Powered by **OpenAI Whisper ASR** models and **Google Gemini 2.5-Flash** structural processing containers.

---

##  Table of Contents
- [Overview](#overview)
- [System Architecture](#system-architecture)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Jupyter Cell Execution Pipeline](#jupyter-cell-execution-pipeline)
- [Installation & Environment Setup](#installation--environment-setup)
- [Project Directory Architecture](#project-directory-architecture)
- [License](#license)

---

##  Overview

The **AI Meeting Assistant** automates the tedious post-meeting documentation loop. Instead of manually re-listening to hours of audio or tracking down loose assignments, the application processes text files or audio tracks to extract executive metrics, assign owners, set deadlines, compile Word document reports, and draft follow-up communications in seconds.

---

##  System Architecture




Audio Media File / Raw Text Transcript Input
│
▼
┌────────────────────┐
│  Whisper ASR Model │ ← Multi-language Audio Translation Engine
└──────────┬─────────┘
│
▼
┌──────────────────────────────────────────────┐
│     Gemini 2.5-Flash Processing Layer        │
│  ┌────────────────────┐ ┌─────────────────┐  │
│  │ Summary Compiler   │ │ Task Extractor  │  │
│  └────────────────────┘ └─────────────────┘  │
│  ┌────────────────────┐ ┌─────────────────┐  │
│  │ Decision Matrix Log│ │ Email Drafter   │  │
│  └────────────────────┘ └─────────────────┘  │
└──────────────────┬───────────────────────────┘
│
▼
┌──────────────────────────────────────────────┐
│           Consolidated Data Deliverables     │
│  ┌────────────────────┐ ┌─────────────────┐  │
│  │ Markdown Note Docs │ │ DOCX Document   │  │
│  └────────────────────┘ └─────────────────┘  │
│  ┌────────────────────┐                      │
│  │ Email Draft Copy   │                      │
│  └────────────────────┘                      │
└──────────────────────────────────────────────┘

```

---

##  Key Features

* **Multi-Input Transcription Layer:** Flexible setup supporting direct `.mp3`/`.wav` processing via Whisper, as well as pass-through structures for live Zoom/Teams log data text.
* **Native JSON Schema Generation:** Implements strict JSON constraint arrays using Gemini API `response_mime_type` mechanics to prevent system formatting issues.
* **Owner & Task Mapping:** Intelligent matching logic that flags task context, assigns precise deadlines, and groups action items by priority level.
* **Automated Microsoft Word Exporter:** Generates stylized, production-ready `.docx` documentation directly out of meeting metrics.
* **Clean Markdown Exporter:** Automatically compiles structured meeting notes and logs them out directly into a clean markdown format file.

---

##  Tech Stack

* **AI Processing Engine:** Google Gemini 2.5-Flash (`google-generativeai`)
* **Audio Speech Recognition:** OpenAI Whisper ASR Core Models
* **Document Exporter Layer:** `python-docx` API core library
* **Data Presentation Format:** Rich CLI Layout Panels & Pandas Matrix DataFrames
* **Interface App Container:** Gradio Blocks Dashboard Grid (Gradio 6.0+ compatible)

---

##  Jupyter Cell Execution Pipeline

The `AI_Meeting_Assistant.ipynb` workspace features a clean, step-by-step layout:
1. **Cell 1 (Markdown):** Technical badge indexes, tool features summaries, and flow maps.
2. **Cell 2 (Code):** Package requirements installation scripts (`openai-whisper`, `google-generativeai`, `python-docx`).
3. **Cell 3 (Code):** Configuration maps, API connections, and core blueprints definitions (`ActionItem`, `MeetingRecord`).
4. **Cell 4 (Code):** Audio-to-text class logic frameworks under `MeetingTranscriber`.
5. **Cell 5 (Code):** Gemini JSON queries construction and analytical engine classes in `MeetingAnalyzer`.
6. **Cell 6 (Code):** Complete system pipeline validation, Markdown parsing, and `.docx` compilers under `AIMeetingAssistant`.
7. **Cell 7 (Code):** Live pipeline processing test run using a sample technical group transcript.
8. **Cell 8 (Code):** Gradio UI Web Dashboard implementation layout with native input tabs.

---

##  Installation & Environment Setup

### 1. Build Local Target Project Workspace
```bash
git clone [https://github.com/divya-09nimbalkar/AI_Meeting_Assistant.git](https://github.com/divya-09nimbalkar/AI_Meeting_Assistant.git)
cd AI_Meeting_Assistant
python -m venv venv
source venv/bin/activate # Windows Terminal: .\venv\Scripts\activate

```

### 2. Install Project Dependency Packages

```bash
pip install -r requirements.txt

```

### 3. Setup Gemini Access Token

Get a free endpoint token key from [Google AI Studio](https://aistudio.google.com/). Paste your secret key parameter directly inside **Cell 3** configuration assignments:

```python
os.environ["GEMINI_API_KEY"] = "AIzaSyYourSecretKeyStringHere"

```

---

##  Project Directory Architecture

```text
AI_Meeting_Assistant/
├── notebooks/
│   └── AI_Meeting_Assistant.ipynb  # Main interactive development notebook
├── output
├── .gitignore                      # Git configuration tracking filters
├── README.md                       # Comprehensive system documentation (This file)
└── requirements.txt                # Pinned application dependencies matrix

```



##  Author

**Divya** — AI/ML Developer | B.Tech Electronics & Telecom.
