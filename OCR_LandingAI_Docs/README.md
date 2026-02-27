# LandingAI ADE OCR Example

This repository contains a Jupyter notebook that demonstrates document parsing, classification, and data extraction using LandingAI Agentic Document Extraction (ADE). The workflow includes:

- Installing dependencies
- Loading environment variables for the ADE API key
- Parsing documents into structured chunks
- Classifying document type
- Extracting fields using document-specific schemas
- Visualizing extracted bounding boxes
- Summarizing results in a DataFrame

## Contents

- [LandingAi_example.ipynb](LandingAi_example.ipynb)
- [helper.py](helper.py)
- [input/](input/)

## Prerequisites

- Python 3.9+
- A LandingAI ADE API key

## Setup

1. Create an environment variable named `VISION_AGENT_API_KEY`.
   - On Windows PowerShell:
     ```powershell
     setx VISION_AGENT_API_KEY "<YOUR_API_KEY>"
     ```
2. Open the notebook and run the cells from top to bottom.

## Dependencies

The notebook installs the following packages:

- `pymupdf`
- `python-dotenv`
- `landingai-ade`
- `pandas`
- `Pillow`

## Notes

- The notebook uses `google.colab.userdata` for retrieving the API key in Colab. If running locally, set `VISION_AGENT_API_KEY` in your environment and skip the Colab-specific cell.
- Place your PDFs or images in [input/](input/) or update the notebook’s `input_folder` path to match your local directory.
- [helper.py](helper.py) contains visualization and utility helpers used by the notebook.

## Output

The notebook produces:

- Document type predictions
- Extracted fields per document
- Visual overlays of parsed chunks and extracted fields
- A summary DataFrame with extracted values
