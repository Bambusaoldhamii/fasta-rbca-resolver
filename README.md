# Rule-Based Country Assignment (RBCA) for Avian Influenza FASTA files

This repository contains the implementation of a rule-based pipeline for assigning standardized ISO 3166-1 country names to geographic metadata embedded in avian influenza FASTA headers. The main script is implemented in `Fasta RBCA R1.ipynb`.

## Overview

This study uses a deterministic string-matching strategy to resolve sampling locations from HA segment FASTA headers. Virus names are expected to follow the GISAID-recommended format:  
`A/host/location/isolate/year`.  

The third component (`location`) is extracted using regular expressions and matched to a standardized dictionary (`location_to_country_ISO_3166_1.json`) that maps known location strings to ISO 3166-1 short English country names. Unmatched locations are labeled as `Other`.

## Features

- Deterministic parsing using regular expressions
- ISO 3166-1-based country mapping (no AI inference)
- Robust handling of location extraction errors
- Export of location list and country sample counts
- Compatible with Jupyter Notebook and Python 3.12+

## Output

- `location_list.csv`: Extracted location names and frequencies
- `country_stat.csv`: Country-level sample count distribution

## Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

Or create a dedicated Conda environment:

```bash
conda create -n rbca-env python=3.12
conda activate rbca-env
pip install -r requirements.txt
```

## 🚀 How to Run

1. Launch Jupyter:

```bash
jupyter notebook
```

2. Open the file: `Fasta RBCA R1.ipynb`

3. Follow the notebook step-by-step.

📂 **Note**: Make sure your FASTA file is placed in the **same directory** as the notebook. The script automatically detects the latest `.fasta` file for processing.

## Citation

> He, Jie-Long. (2025). *Fasta RBCA R1: Rule-Based Country Assignment Pipeline for FASTA Metadata* (v1.0.0). Zenodo. https://doi.org/10.5281/zenodo.15341375

## License

MIT License
