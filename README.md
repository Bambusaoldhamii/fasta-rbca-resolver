# 🧬 Fasta RBCA R1: AI-Aided Resolution of Country Metadata in Avian Influenza FASTA Headers

This Jupyter Notebook (`Fasta RBCA R1.ipynb`) performs automated resolution of ambiguous or non-standard location metadata in H5 subtype avian influenza virus HA sequences using a hybrid pipeline: ISO 3166-1 rule-based matching followed by GPT-assisted inference.

The final output includes country-level classification for all records, accompanied by data tables and geographic visualizations.

---

## 📦 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

Or create a dedicated Conda environment:

```bash
conda create -n rbca-env python=3.12
conda activate rbca-env
pip install -r requirements.txt
```

---

## 🚀 How to Run

1. Launch Jupyter:

```bash
jupyter notebook
```

2. Open the file: `Fasta RBCA R1.ipynb`

3. Follow the notebook cells step-by-step. The pipeline includes:

- **2.1 Sequence Import and Metadata Extraction**
- **2.2 Rule-Based Country Mapping**
- **2.3 GPT-Aided Country Inference**
- **2.4 Final Country Resolution and Export**
- **2.5 Static & Interactive Visualizations**

---

## 🧪 Example Inputs and Outputs

- Input file: `examples/sequences.fasta`
- Output file: `results.csv`  
- Visualization example: `figures/result_map.png`

---

## 🗺️ Visualization Preview

Output includes:

- Cleaned country assignments in table form
- Static map (matplotlib)
- Interactive choropleth map (plotly)

---

## 📜 License

MIT License

---

## 📌 Citation

> He, Jie-Long. (2025). *Fasta RBCA R1: A Hybrid AI Pipeline for FASTA Metadata Refinement* (v1.0.0). Zenodo. https://doi.org/10.5281/zenodo.xxxxxxx
