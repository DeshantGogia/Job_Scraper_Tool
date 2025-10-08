# Job Scraper Tool

A small Streamlit-based job scraping tool that scrapes job listings from multiple Indian job platforms (Internshala, Naukri, Indeed). The project includes a notebook for scraping experiments and a Streamlit app (`job_scraper.py`) for interactive use.

## Features

- Scrape job listings concurrently from multiple sources
- Display results in a Streamlit UI with filters and download option
- Export results to CSV

## Prerequisites

- Python 3.10+ recommended
- Ollama (optional): if you use the notebook LLM cleaning steps, run an Ollama server locally and pull the model:

```powershell
ollama pull llama2
```

## Install

Create a virtual environment and install dependencies:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r "c:\Users\desha\Data science\Gen_AI\job_searching_tool\requirements.txt"
```

## Run the Streamlit app

```powershell
streamlit run job_scraper.py
```

## Files

- `job_scraper.py` - Streamlit app entrypoint (main UI and scraping logic)
- `scraping.ipynb` - Notebook with scraping experiments and LLM-based cleaning
- `internshala_jobs.csv` / `internshala_jobs.json` - sample export files
- `requirements.txt` - Python dependencies

## GitHub

To publish this repo to GitHub (replace `<your-repo-url>` with the repository URL):

```powershell
git remote add origin <your-repo-url>
git branch -M main
git push -u origin main
```

Or, if you have the GitHub CLI (`gh`) installed, you can create and push in one step:

```powershell
cd "c:\Users\desha\Data science\Gen_AI\job_searching_tool"
gh repo create <repo-name> --public --source=. --remote=origin --push
```

## Notes

- Respect `robots.txt` and site terms when scraping.
- The notebook uses an Ollama LLM to clean job text; ensure Ollama is running and the model is pulled.

