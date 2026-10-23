# Tri9T AI Engineering Internship Assignment

## Overview
This project is a Python-based backend application built with FastAPI to process medical-device PDF manuals, organize extracted content into a structured document hierarchy, manage document versions, generate QA test cases using Large Language Models (LLMs), and identify potentially outdated test cases when documentation changes.

## Features
- **PDF Parsing:** Extracts text from medical-device manuals using PyMuPDF.
- **Document Structure:** Organizes extracted content into a hierarchical document tree.
- **Version Management:** Supports tracking different versions of manuals.
- **AI-Based Test Generation:** Generates QA test cases using an LLM when configured, with a fallback method.
- **Stale Test Detection:** Identifies test cases that may need review after manual updates.
- **REST API:** Provides endpoints through FastAPI.
- **Testing:** Includes basic parser tests.

## Technology Stack
- Python
- FastAPI
- SQLAlchemy
- PyMuPDF
- Large Language Models (LLMs)
- Pytest

## Project Structure
```text
tri9t-ai-assignment/
├── app/
│   ├── main.py
│   ├── models.py
│   ├── parser.py
│   ├── generator.py
│   ├── store.py
│   ├── config.py
│   ├── database.py
│   └── schemas.py
├── tests/
├── requirements.txt
├── .env.example
├── APPROACH.md
└── README.md
```

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/vtu24815/tri9t-ai-assignment.git
cd tri9t-ai-assignment
```

### 2. Install Dependencies
```bash
python -m venv .venv
```

Activate the environment and install the packages:

```bash
pip install -r requirements.txt
```

### 3. Configure Environment
Use `.env.example` as a reference to configure the required environment variables. Add an LLM API key only if using an external LLM provider. Never commit secrets to GitHub.

### 4. Run the Application
```bash
uvicorn app.main:app --reload
```

### 5. Open API Documentation
Visit [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) to explore and test the available API endpoints.

## Testing
Run the tests using:

```bash
pytest
```

## Project Goal
The goal is to demonstrate how document parsing, version tracking, and AI-assisted QA test generation can support medical-device documentation analysis and help maintain test cases as manuals evolve.

## Note
Parsing accuracy and stale-test detection should be validated against the actual manual versions. OCR and complex table extraction may require additional implementation and testing.
