# 🛍️ Amazon Product Review Analysis

This project collects reviews from an Amazon product page and performs sentiment analysis and summarization on the text. It leverages powerful pre-trained NLP models from Hugging Face to determine how users feel about a product, and finally gives a **verdict** on whether it's worth buying.

## 📌 Features

- Scrapes product reviews from an Amazon product page
- Analyzes each review using pre-trained sentiment models
- Summarizes the general sentiment across all reviews
- Computes an overall sentiment score
- Gives a final **verdict**: ✅ Buy or ❌ Don't Buy

## ⚙️ Technologies Used

- Python
- `requests`, `BeautifulSoup` for scraping
- `transformers`, `torch` for NLP tasks
- Pretrained Hugging Face models:
  - `cardiffnlp/twitter-roberta-base-sentiment`
  - `distilbert-base-uncased-finetuned-sst-2-english` (via `pipeline`)
  - `facebook/bart-large-cnn` or similar for summarization

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- pip (Python package installer)

### Installation

Install dependencies:

```bash
pip install requests beautifulsoup4 transformers torch
```

### Run the Script

Open and run the Jupyter Notebook:

```bash
jupyter notebook AmazonProductAnalysis.ipynb
```

Or run it in Google Colab for convenience.

You will be prompted to enter the URL of the **Amazon product's review page**.

## 📊 Output

- Displays top reviews from the page
- Predicts and prints sentiment per review (Positive, Negative, Neutral)
- Computes average sentiment score
- Summarizes all reviews into a concise paragraph
- **Final Verdict**: Based on overall sentiment

## ⚠️ Disclaimer: Bot Detection on Amazon

> **Warning:** Amazon actively detects and blocks scraping activity. If the code fails to retrieve reviews or returns empty results, it may be due to:
>
> - Amazon temporarily blocking automated traffic
> - Missing or insufficient request headers
> - Frequent access without delays
>
> You can try:
> - Using a VPN
> - Rotating User-Agents
> - Adding delays between requests
> - Scraping during off-peak hours

This project is for **educational purposes only**. Do not violate Amazon’s [robots.txt](https://www.amazon.com/robots.txt) or terms of service.
