# Biomarker Discovery and Prediction for Gastrointestinal Cancer

An industry-grade deep learning and machine learning solution for:
1. **Tissue Phenotype Classification** from histopathology images
2. **Lymph Node Metastasis Prediction** from clinical data

## Project Structure

```
├── app/                    # Streamlit web application
├── config/                 # Configuration files
├── data/                   # Raw data (images + CSV)
├── src/
│   ├── data/              # Data loading and preprocessing
│   ├── models/            # Model architectures
│   └── utils/             # Helper functions
├── tests/                  # Unit tests
├── models/                 # Saved trained models
└── requirements.txt
```

## Quick Start

```bash
# Install dependencies
pip install -r requirements.txt

# Train Vision Model
python -m src.train_vision

# Train Clinical Model
python -m src.train_clinical

# Run Web App
streamlit run app/main.py
```

## Dataset

- **Images**: 31,096 H&E stained patches (8 tissue classes)
- **Clinical**: 300 patients with staging and biomarker data

## Models

### Vision Module
- Architecture: EfficientNet-B0 (pretrained)
- Task: 8-class tissue classification
- Classes: ADI, DEB, LYM, MUC, MUS, NOR, STR, TUM

### Clinical Module
- Algorithm: XGBoost
- Task: Binary classification (N0 vs N+)
- Features: Age, T-staging, histological type, etc.

## License
MIT License
