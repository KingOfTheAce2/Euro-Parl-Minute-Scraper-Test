# European Parliament Minutes Scraper

This repository contains a simple Python script to scrape the Dutch minutes of the European Parliament and upload them to the Hugging Face Hub.

The crawler starts from the earliest available minutes page and walks forward using the "Volgende" link. Each minutes page is downloaded in XML format, cleaned, and pushed as a dataset.

## Requirements

- Python 3.8+
- See `requirements.txt` for the list of Python dependencies.

## Usage

1. Install the dependencies:

```bash
pip install -r requirements.txt
```

2. Set your Hugging Face credentials as environment variables:

```bash
export HF_USERNAME=<your_username>
export HF_TOKEN=<your_token>
```

3. Run the scraper:

```bash
python scraper.py
```

The dataset will be created or updated on the Hugging Face Hub under `<HF_USERNAME>/Dutch-European-Parliament-Minutes`.

## GitHub Actions

A workflow is included to run the scraper periodically. Provide the secrets `HF_USERNAME` and `HF_TOKEN` in your repository settings to enable automatic uploads.

