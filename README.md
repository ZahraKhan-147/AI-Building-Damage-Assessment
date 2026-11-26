# AI-Based Building Damage Assessment

An AI-based building damage assessment system that uses pre- and post-disaster satellite imagery to identify and classify building damage using deep learning.

## Project Overview

This project uses a Siamese U-Net architecture with a ResNet50 encoder to analyze satellite imagery before and after a disaster. The model performs pixel-level segmentation to identify building damage categories.

## Damage Classes

The model predicts five classes:

- Background
- No Damage
- Minor Damage
- Major Damage
- Destroyed

## Project Components

- **Model Training:** Training and evaluation performed in Google Colab using a GPU.
- **Deep Learning Model:** Siamese U-Net with ResNet50 encoder.
- **Interactive Application:** Streamlit application for analyzing satellite image pairs.
- **Sample Dataset:** Disaster-related satellite image pairs with ground-truth masks.

## Dataset

The project uses disaster-related satellite imagery containing pre-disaster and post-disaster image pairs, along with ground-truth damage annotations. The dataset is used for model training, validation, and evaluation.

## Model Results

The model was evaluated using F1-score metrics on the test dataset.

- Background F1-score: 0.9881
- No Damage F1-score: 0.5526
- Minor Damage F1-score: 0.0000
- Major Damage F1-score: 0.0000
- Destroyed F1-score: 0.4707
- Mean damage F1-score: 0.2558

The model performed better on some damage categories than others. Minor and major damage were not reliably detected in the current experiment.

## Streamlit Application

The application allows users to:

- Select sample disaster image pairs
- Upload their own pre- and post-disaster images
- Run damage assessment
- View segmentation predictions and overlays
- Compare predictions with ground-truth masks
- View predicted damage class percentages

## Repository Structure

```text
AI-Building-Damage-Assessment/
├── notebooks/
│   └── Building_Damage_Assessment.ipynb
├── streamlit_app/
│   ├── checkpoints/
│   ├── sample_images/
│   ├── app.py
│   ├── model_def.py
│   ├── requirements.txt
│   └── README.md
├── .gitattributes
└── .gitignore
```

## Limitations

This project is an experimental prototype trained on a relatively small pilot dataset. Its predictions may not generalize to all disaster types or geographic locations and should not be used as the sole basis for real-world emergency or disaster-response decisions.

## Technologies Used

- Python
- PyTorch
- ResNet50
- Siamese U-Net
- Streamlit
- Google Colab
- Git and GitHub

## Team

Add project team members and their contributions here.
