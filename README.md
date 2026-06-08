# Music Therapy Knowledge Database

This repository provides the public data tables, figure previews, and LLM-assisted extraction notebooks for a music therapy knowledge database project.

## Repository Contents

```text
.
├── code/
│   └── LLM_Extraction/        # Jupyter notebooks for LLM-assisted full-text extraction
├── data/                      # Public Excel tables derived from the knowledge database
├── figures/
│   ├── preview/               # PNG previews for GitHub display
│   └── high_resolution/       # High-resolution figure files that are small enough for normal GitHub upload
├── docs/
│   └── github_deployment.md   # Step-by-step GitHub upload notes
├── requirements.txt           # Python dependencies for the extraction notebooks
└── README.md
```

The original unstandardized master table `SummaryofKnowledgeBaseData.xlsx` is intentionally not included.

## Data Files

The `data/` folder contains the public structured tables:

- `1-Disease information.xlsx`
- `2-Study population characteristics.xlsx`
- `3-Reference information.xlsx`
- `4-Study design information.xlsx`
- `5-Music-baesd intervention design.xlsx`
- `6-Music therapy-based technologies.xlsx`
- `7-Session design.xlsx`
- `8-Intervention music design.xlsx`
- `SummaryofKnowledgeBaseData_standardized.xlsx`

## LLM-Assisted Extraction Code

The notebooks in `code/LLM_Extraction/` read a spreadsheet, locate PDFs by PMID, extract text from each PDF, send the text to an LLM with field-specific prompts, parse JSON output, and write extracted values back to Excel.

The notebooks are intended for first-pass assisted extraction only. Final database values should be checked manually against the original full texts.

Required user-filled settings inside each notebook:

- `OPENAI_BASE_URL`
- `OPENAI_API_KEY`
- `MODEL_NAME`
- `EXCEL_PATH`
- `OUTPUT_EXCEL_PATH`
- `PDF_DIR`
- `SHEET_NAME`

Install dependencies:

```bash
pip install -r requirements.txt
```

## Figure Preview

GitHub README pages reliably display PNG files. Therefore, Figure 4 to Figure 8 are included as PNG previews:

| Figure | Preview |
| --- | --- |
| Figure 4 | ![Figure 4](figures/preview/Figure4.PNG) |
| Figure 5 | ![Figure 5](figures/preview/Figure5.PNG) |
| Figure 6 | ![Figure 6](figures/preview/Figure6.PNG) |
| Figure 7 | ![Figure 7](figures/preview/Figure7.PNG) |
| Figure 8 | ![Figure 8](figures/preview/Figure8.PNG) |

`Figure4.tiff` is also included in `figures/high_resolution/` because it is small enough for standard GitHub upload. The original high-resolution TIFF files for Figure 5 to Figure 8 are larger than GitHub's normal 100 MB per-file limit and should be uploaded with Git LFS or attached as release assets if needed.

## Recommended Citation

Please cite the related manuscript when using this dataset or code. Update this section with the final paper citation after publication.

## License

This repository is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0), unless otherwise stated.

The data tables, figures, and accompanying extraction notebooks may be reused with appropriate attribution. See `LICENSE` for details.
