# dynamic-corpus-scraper

# Automated Web Scraping & Ingestion Pipeline for Unstructured Text Corpora

A Python-based data engineering tool utilizing Selenium and BeautifulSoup to build automated web scraping pipelines for dynamic, JavaScript-rendered web platforms.

---

## Project Overview
In modern Natural Language Processing (NLP) and Large Language Model (LLM) workflows, the biggest bottleneck is often constructing custom domain-specific datasets. 

This project simulates a high-scale data ingestion engine designed to overcome anti-scraping barriers and capture unstructured textual data (such as online user discourse and reviews) from dynamic platforms.

*   **Key Achievement**: Successfully engineered an end-to-end data pipeline that automates sequential link harvesting, handles infinite scrolling via background JavaScript execution, and transforms noisy web structures into refined training data.

---

## Tech Stack & Advanced Implementation

*   **Language**: Python 3.x
*   **Libraries**: Selenium WebDriver, BeautifulSoup 4, Requests, Time, Math
*   **Key Engineering Techniques**:
    *   *Headless Browser Automation*: Configured a decoupled, headless Chrome environment (`--headless`, `--no-sandbox`) optimized for cloud instances and Linux-based background data collection.
    *   *Dynamic Interaction & Infinite Scroll*: Injected customized JavaScript snippets (`window.scrollTo`) inside automated loop structures to dynamically trigger AJAX/lazy-loading requests.
    *   *Sequential URL Harvesting*: Built an agile indexer that crawls main query pages, extracts deep product/video hyperlinks, and dynamically maps a nested loop to scrape deeply embedded review data across different target layers.
    *   *Granular Data Extraction*: Leveraged CSS selectors to target specific data fields simultaneously (e.g., matching actual user commentary strings with corresponding engagement metrics like 'like counts').

---

## Pipeline Architecture & Workflow

1.  **Query Input**: Ingests user-defined search keywords to target domain-specific web zones.
2.  **Link Ingestion**: Automatically crawls index pages and compiles a list of deep target URLs.
3.  **Dynamic Rendering Execution**: Launches the headless Selenium engine, handles pop-ups, and triggers auto-scrolling loops to load hidden asynchronous components.
4.  **HTML Parsing**: Captures the state-rendered `page_source` and parses text with BeautifulSoup.
5.  **Output & Formatting**: Converts the unstructured raw strings into clean, aligned textual arrays ready for feature extraction.

---

## Acknowledgement & Academic Context
*   This data engineering project was developed during advanced laboratory sessions in language data science coursework at Sungkyunkwan University.
*   The system was benchmarked on live dynamic entertainment and e-commerce platforms (YouTube and Musinsa) to ensure robustness against production-level layout complexity.
