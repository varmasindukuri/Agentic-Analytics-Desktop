# Agentic-Analytics-Deskto

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![PySide6](https://img.shields.io/badge/UI-PySide6%20%28Qt6%29-green.svg)
![Build](https://img.shields.io/badge/Packaging-PyInstaller-orange.svg)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey.svg)

An AI-powered standalone desktop analytics application built with **PySide6 (Qt6)** and compiled into a native Windows executable (`.exe`). The application enables users to perform statistical data analysis, automated agentic reasoning, live web scraping, and natural language Q&A over CSV and Excel datasets via LLM integration.

---

## Features

- **Dataset Ingestion**: Import `.csv` and `.xlsx` (Excel) files with automated schema inspection and summary statistics.
- **Statistical Analytics Engine**: Automated calculation of descriptive statistics (mean, median, std, skewness, kurtosis), correlation matrices, and outlier detection flags.
- **Autonomous AI Agent**: Dedicated agentic pipeline that analyzes multi-step datasets, discovers insights, and surfaces key patterns.
- **Web Scraping Pipeline**: Scrapes unstructured data from web URLs using `BeautifulSoup4` and directly injects it into the analysis pipeline.
- **Natural Language Q&A**: LLM-driven query interface powered by Groq API for plain-English data analysis and insights.
- **Data Visualizations**: Built-in interactive charts (bar charts, line graphs, scatter plots, histograms) with export capabilities.
- **Standalone Executable**: Fully packaged with PyInstaller into a single Windows `.exe` with zero Python dependency requirements for end users.

---

## Architecture & Project Structure

```text
agentic-analytics-desktop/
│
├── charts/                   # Visualizations module (bar, line, scatter, histogram)
├── core/
│   ├── agent.py              # AI agent logic for autonomous dataset analysis
│   ├── analytics.py          # Core statistical calculation engine
│   ├── data_loader.py        # CSV & Excel (.xlsx) ingestion via pandas/openpyxl
│   ├── groq_client.py        # Groq LLM API integration wrapper
│   └── web_scraper.py        # Web scraping engine using BeautifulSoup4
├── gui/
│   └── main_window.py        # PySide6 Qt6 tabbed main interface & event handling
├── .env.example              # Sample environment configuration file
├── .gitignore                # Git exclusion list
├── main.py                   # Application entry point
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation
