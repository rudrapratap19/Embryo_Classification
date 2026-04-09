# Embryo Classification

Classify embryo images into clinically relevant categories using deep learning.

## Overview
This repository contains code to train and evaluate an embryo image classification model. It includes utilities for:
- dataset loading and preprocessing
- model training
- evaluation (accuracy/F1/confusion matrix)
- inference on new images

> **Note:** Replace the placeholders in this README with the exact scripts/paths used in this repo.

## Project Structure
```text
.
├── data/                   # (optional) local dataset directory (usually not committed)
├── notebooks/              # Jupyter notebooks (if any)
├── src/                    # source code (if any)
├── models/                 # saved checkpoints / exported models (if any)
├── requirements.txt        # Python dependencies (or environment.yml)
└── (train/eval/infer).py   # main scripts (names may differ)
```

## Requirements
- Python 3.9+ (recommended)
- A GPU is optional but recommended for training

Install dependencies:
```bash
pip install -r requirements.txt
```

If you use Conda:
```bash
conda env create -f environment.yml
conda activate embryo-classification
```

## Data
### Expected dataset format
Put your dataset in a folder like:
```text
data/
  train/
    class_a/
    class_b/
  val/
    class_a/
    class_b/
  test/
    class_a/
    class_b/
```

### Classes
- `class_a`: <describe>
- `class_b`: <describe>
- ...

## Training
Run training (update to match your actual entrypoint):
```bash
python train.py --data_dir data --epochs 30 --batch_size 32 --lr 1e-3
```

Common options:
- `--img_size` (e.g., 224)
- `--model` (e.g., resnet18 / efficientnet)
- `--checkpoint_dir models/`

## Evaluation
```bash
python eval.py --data_dir data --checkpoint models/best.pt
```

Metrics typically reported:
- Accuracy
- Precision / Recall / F1-score
- Confusion matrix

## Inference
Classify a single image:
```bash
python infer.py --checkpoint models/best.pt --image path/to/image.jpg
```

Batch inference:
```bash
python infer.py --checkpoint models/best.pt --input_dir path/to/images --output predictions.csv
```

## Results
Add your best results here:
- Dataset: <name / description>
- Best model: <architecture>
- Accuracy: <value>
- F1 (macro): <value>

## Reproducibility
Example:
```bash
python train.py --seed 42
```

## Notes / Disclaimer
This project is for research/educational purposes. It is **not** a medical device and should not be used for clinical decision-making without appropriate validation and regulatory approval.

