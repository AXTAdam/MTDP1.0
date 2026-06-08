# LLM_Extraction

This folder contains five Jupyter notebooks for LLM-assisted extraction from full-text PDFs.

## Notebook List

- `01_extract_disease_and_study_design.ipynb`
- `02_extract_music_based_intervention_design.ipynb`
- `03_extract_session_delivery_design.ipynb`
- `04_extract_intervention_music_design.ipynb`
- `05_extract_music_therapy_technologies.ipynb`

## Workflow

1. Read the input Excel file.
2. Use the PMID column to locate the corresponding PDF.
3. Extract text from the PDF.
4. Send the text to an LLM with field-specific prompts.
5. Require JSON-only output.
6. Write the extracted values back to an output Excel file.

The notebooks contain empty placeholders for API settings and local paths. Fill these values before running:

- `OPENAI_BASE_URL`
- `OPENAI_API_KEY`
- `MODEL_NAME`
- `EXCEL_PATH`
- `OUTPUT_EXCEL_PATH`
- `PDF_DIR`
- `SHEET_NAME`

The LLM output should be treated as preliminary extraction and checked manually against the original full text before being used as final database content.
