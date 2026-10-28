PatentClass-HAT
A Section-Aware Hierarchical Transformer Framework for Explainable Multi-Label Patent Classification

Python 3.10+ PyTorch License: MIT

Overview
PatentClass-HAT is an AI system that predicts Cooperative Patent Classification (CPC) codes from patent documents. It handles long, section-structured patents using a hierarchical Transformer architecture with:

Section-Aware Attention — Learns the importance of title, abstract, claims, and description
Long-Document Chunking — Processes documents beyond the 512-token Transformer limit
Hierarchical CPC Prediction — Leverages the CPC tree structure for coarse-to-fine classification
Imbalance-Aware Learning — Handles rare CPC codes through focal loss and threshold tuning
Explainable Predictions — Provides evidence showing why a CPC code was predicted
Research Novelty
The main contribution is a section-aware hierarchical Transformer architecture that:

Encodes patent sections separately to preserve structural information
Uses learnable multi-head attention to weight section importance
Processes long documents through chunk-based encoding with attention aggregation
Predicts hierarchical CPC codes with parent-child consistency
Generates section-level, chunk-level, and token-level explanations
Datasets
Dataset	Role	Status
USPTO-3M	Main supervised training & testing	Pending (Phase 1)
HUPD	External evaluation & domain-shift analysis	Pending (Phase 1)
BIGPATENT	Optional domain-adaptive pretraining	Pending (Phase 1)
Quick Start
Prerequisites
Python 3.10 or 3.11
pip
(Optional) NVIDIA GPU with CUDA for accelerated training
Installation
# 1. Clone the repository
git clone https://github.com/your-username/PatentClass-HAT.git
cd PatentClass-HAT

# 2. Create a virtual environment
python -m venv .venv

# Windows
.venv\Scripts\activate

# Linux / macOS
source .venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Install the project in editable mode
pip install -e .

# 5. Copy and configure environment variables
copy .env.example .env   # Windows
cp .env.example .env     # Linux/macOS

# 6. Validate your environment
python scripts/validate_env.py

# 7. Run tests
pytest tests/ -v
Verify Installation
python -c "from src.utils import load_config, set_seed, PATHS; print('✓ All imports work')"
Project Structure
PatentClass-HAT/
│
├── README.md                      # This file
├── LICENSE                        # MIT License
├── requirements.txt               # Python dependencies
├── setup.py                       # Editable install
├── .gitignore                     # Git ignore rules
├── .env.example                   # Environment variable template
│
├── configs/                       # YAML configuration files
│   ├── base_config.yaml           #   Project, seed, device, logging
│   ├── data_config.yaml           #   Datasets, schema, preprocessing
│   ├── training_config.yaml       #   Optimizer, scheduler, checkpointing
│   └── model_config.yaml          #   Encoder, chunking, section attention
│
├── data/                          # Data directory (not committed)
│   ├── raw/                       #   Original datasets
│   ├── interim/                   #   Intermediate artifacts
│   ├── processed/                 #   Final processed data
│   └── label_maps/                #   CPC label mappings
│
├── src/                           # Source code
│   ├── data/                      #   Dataset loaders
│   ├── preprocessing/             #   Text cleaning, section extraction
│   ├── baselines/                 #   TF-IDF, SVM baselines
│   ├── models/                    #   PatentClass-HAT architecture
│   ├── training/                  #   Training loops
│   ├── evaluation/                #   Metrics and analysis
│   ├── explainability/            #   SHAP, attention visualization
│   ├── inference/                 #   Prediction pipeline
│   └── utils/                     #   Config, seed, paths, logging
│
├── api/                           # FastAPI inference service
├── frontend/                      # React demo interface
├── tests/                         # Pytest test suite
├── notebooks/                     # Jupyter notebooks
├── experiments/                   # Experiment results
├── outputs/                       # Models, predictions, plots
├── scripts/                       # Utility scripts
└── docs/                          # Documentation
Development Phases
Phase	Name	Status
0	Project Initialization	✅ Complete
1	Dataset Acquisition & Audit	⏳ Next
2	Data Preprocessing	Planned
3	ML Baselines (TF-IDF)	Planned
4	Transformer Baselines	Planned
5	Long-Document Processing	Planned
6	Section-Aware Attention	Planned
7	Hierarchical CPC Classification	Planned
8	Class Imbalance & Rare Labels	Planned
9	Explainable AI	Planned
10	External Dataset Evaluation	Planned
11	Full Model Integration	Planned
12	API Development	Planned
13	Frontend Development	Planned
14	Docker & Reproducibility	Planned
15	Research Paper Package	Planned
Configuration
All settings are managed through YAML files in configs/. Key settings:

# configs/base_config.yaml
seed: 42
device: "auto"  # "auto", "cuda", or "cpu"

# configs/model_config.yaml
encoder:
  name: "microsoft/deberta-v3-base"
section_attention:
  enabled: true
Environment variables (in .env) override config values:

PATENTCLASS_DEVICE — Force device selection
PATENTCLASS_SEED — Override random seed
HF_TOKEN — Hugging Face access token
Testing
# Run all tests
pytest tests/ -v

# Run with coverage
pytest tests/ --cov=src --cov-report=term-missing

# Run specific test file
pytest tests/test_config.py -v
Documentation
Architecture — System design and pipeline
Datasets — Dataset roles and schema
Methodology — Research approach
Experiments — Experiment plan and results
Limitations — Known constraints
Research Notes — Paper planning
Changelog — Version history
Technology Stack
Category	Technologies
Deep Learning	PyTorch, Hugging Face Transformers
NLP	BERT, DeBERTa, PatentBERT
Data	Pandas, NumPy, PyArrow, Hugging Face Datasets
ML Baselines	Scikit-learn (TF-IDF, SVM, Logistic Regression)
Explainability	Captum, SHAP
Tracking	MLflow, TensorBoard
API	FastAPI, Uvicorn
Frontend	React, Tailwind CSS
Testing	Pytest
DevOps	Docker, Docker Compose
License
This project is licensed under the MIT License — see LICENSE for details.

Citation
@software{patentclass_hat_2026,
    title     = {PatentClass-HAT: A Section-Aware Hierarchical Transformer
                 Framework for Explainable Multi-Label Patent Classification},
    author    = {PatentClass-HAT Authors},
    year      = {2026},
    url       = {https://github.com/your-username/PatentClass-HAT}
}
