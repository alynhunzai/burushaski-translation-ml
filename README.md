# 🔤 Burushaski ↔ English Neural Machine Translation (NMT)

![License](https://img.shields.io/badge/license-MIT-green)
![Build](https://img.shields.io/badge/build-passing-brightgreen)
![Status](https://img.shields.io/badge/status-ongoing-blue)
![MLOps](https://img.shields.io/badge/MLOps-DVC%20%7C%20MLflow%20%7C%20Docker%20%7C%20CI--CD-orange)

## 🧠 Project Overview

This repository is going to host a complete **Neural Machine Translation (NMT)** pipeline for the **Burushaski ↔ English** language pair — a unique translation challenge involving a **language isolate** with low-resource status. The goal is to both preserve and promote Burushaski (Hunza & Nagar dialects) through modern NLP and MLOps techniques.

✅ The project is structured to include:
- End-to-end pipelines for **data collection, cleaning, training, evaluation, and deployment**
- Dual modeling approach: **from-scratch Seq2Seq** and **fine-tuned transformer-based models**
- Scalable, reproducible MLOps stack with **DVC, MLflow, GitHub Actions, Docker**, and (optionally) cloud integrations

---

## 🎯 Project Goals

| Goal | Description |
|------|-------------|
| 🗣️ Language Preservation | Digitize and translate Burushaski content to increase its global accessibility |
| 🤖 ML Exploration | Train both traditional and modern translation models to compare performance |
| ⚙️ MLOps Showcase | Demonstrate industry-level ML engineering workflows for portfolio |
| 🌍 Community Contribution | Contribute linguistic datasets and tools to support low-resource NLP research |

---

## 🧩 Project Structure

```bash
.
├── data/                    # Raw and processed Burushaski-English datasets
│   ├── hunza/
│   └── nagar/
├── notebooks/              # Jupyter notebooks for EDA, training, and eval
├── src/                    # Source code for data processing and modeling
│   ├── data_pipeline/
│   ├── models/
│   └── evaluation/
├── configs/                # YAML/JSON config files for experiments
├── dvc.yaml                # DVC pipeline stages
├── mlruns/                 # MLflow experiment tracking logs
├── requirements.txt
├── Dockerfile
├── .github/workflows/      # GitHub Actions for CI/CD
├── README.md
└── LICENSE
```

---

## 🛠️ Models Used

### 1. 🔧 From-Scratch Model (Baseline)
- Architecture: Encoder-Decoder with Attention
- Framework: PyTorch
- Tokenization: Word + BPE
- Evaluation: BLEU, TER

### 2. 🧠 Fine-Tuned Model (Transformer-Based)
- Base: `Helsinki-NLP/opus-mt-en-ROMANCE` and others
- Framework: Hugging Face Transformers
- Training: PyTorch Lightning or 🤗 Trainer
- Features: Transfer learning, early stopping, mixed precision

---

## 🧪 Reproducibility Stack

| Tool | Purpose |
|------|---------|
| ✅ **DVC** | Dataset and model versioning |
| ✅ **MLflow** | Experiment tracking and evaluation |
| ✅ **Docker** | Environment consistency |
| ✅ **GitHub Actions** | CI/CD for tests, linting, and deployment |
| ✅ **FastAPI** | Inference API for the translation model |

---

## 📦 Installation

```bash
# Clone repo and setup env
git clone https://github.com/alynhunzai/burushaski-translation-ml.git
cd burushaski-translation-ml
pip install -r requirements.txt

# Run a training pipeline (with DVC)
dvc repro

# Or launch the FastAPI server
uvicorn src.api.main:app --reload
```

---

## 📊 Evaluation Metrics

| Metric | Purpose |
|--------|---------|
| BLEU | Measures translation quality |
| ROUGE | Measures text overlap (optional) |
| TER | Measures edit distance from reference |
| Human Evaluation | Manual grading by native speakers |

---

## 🚀 Deployment

- 🐳 Docker-ready container with exposed `/translate` API endpoint
- Optionally deployable on:
  - 🌥️ AWS Lambda + API Gateway
  - 🚀 Hugging Face Spaces or Streamlit Sharing

---

## 🗂️ Dataset Details

| Source | Domain | Size |
|--------|--------|------|
| Manually curated (Hunza + Nagar dialects) | General domain | 1K–5K+ sentence pairs (growing) |
| Additional [community-contributed](https://github.com/alynhunzai/burushaski-ml-data-app) corpora | General domain | ✅ Open source under CC-BY-SA |

---

## 🧑‍💻 Contributors

- **Noor Ali** - ML/MLOps
- Open to contributors (especially native speakers, linguists, and ML engineers)

---

## 📜 License

MIT License © Noor Ali, 2025

---

## 📌 Acknowledgements

- Native Burushaski speakers and elders
- Hugging Face 🤗 for pre-trained models and tokenizers
- DeepLearning.AI and DataCamp for foundational knowledge

---

## 🌐 Connect

Feel free to connect with me on [LinkedIn](https://linkedin.com/in/alynhunz).
