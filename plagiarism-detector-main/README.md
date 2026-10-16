# Smart Plagiarism Detector

A Python-based text similarity application that compares documents using string-matching algorithms and displays matching passages and similarity scores.

## Features

- Upload text files or paste text for comparison
- Compare documents using KMP, Rabin–Karp, and LCS algorithms
- Calculate pairwise LCS similarity scores
- Highlight matching text spans
- Export analysis results
- Streamlit-based user interface
- Optional REST API for text analysis

*Confirm each feature works in your local setup before presenting it as functional.*

## Technology Stack

- **Language:** Python
- **Algorithms:** Knuth–Morris–Pratt (KMP), Rabin–Karp, Longest Common Subsequence (LCS)
- **Interface:** Streamlit
- **API:** FastAPI
- **Testing:** pytest
- **Deployment:** Docker and Streamlit Community Cloud

## Algorithms

- **KMP:** Uses a prefix table to find exact pattern matches efficiently.
- **Rabin–Karp:** Uses rolling hashes to locate matching substrings.
- **LCS:** Uses dynamic programming to measure the longest common subsequence between two texts.

The LCS similarity score is calculated as:

`Similarity = LCS length / maximum text length × 100`

## Getting Started

### Prerequisites

- Python 3.10 or later, subject to the project's dependencies
- pip

### Installation

Create and activate a virtual environment.

**Windows PowerShell:**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the application:

```bash
streamlit run app.py
```

Open `http://localhost:8501` in your browser.

## Running Tests

```bash
pytest -q
```

## Optional REST API

If the API dependencies and implementation are present, start the service with:

```bash
uvicorn api.main:app --host 127.0.0.1 --port 8000
```

The API provides text-analysis functionality through the `/api/analyze` endpoint.

## Privacy

The project is designed to process text in memory. Verify the implementation before making claims about data retention or privacy.

## Original Project and Attribution

This project is based on the original repository:

https://github.com/anshukashyap26/plagiarism-detector

The original source and applicable licence terms are acknowledged. Document additional modifications after implementing and testing them.

## My Contributions

Record your own verified improvements here as you implement them.

## License

Refer to the included `LICENSE` file for the applicable licence terms.
