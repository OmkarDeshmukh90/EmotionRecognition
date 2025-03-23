# Speech Emotion Recognition

## Overview
This repository contains a comprehensive implementation of a Speech Emotion Recognition (SER) system using various machine learning and deep learning techniques. The project utilizes audio datasets, specifically the Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS) and the Toronto Emotional Speech Set (TESS), to classify emotions from speech recordings.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Datasets](#datasets)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Multiple Algorithms**: Implementations of various algorithms including Support Vector Machine (SVM) and Multi-Layer Perceptron (MLP) for emotion classification.
- **Feature Extraction**: Utilizes Mel-frequency cepstral coefficients (MFCCs) and other audio features for effective emotion recognition.
- **Live Predictions**: A class for making real-time predictions using a pre-trained model.
- **Data Handling**: Scripts for creating and managing datasets, including saving features for quick access.

## Installation
To set up the project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. **Install Required Packages**:
   It is recommended to create a virtual environment. You can use `venv` or `conda` for this purpose. Then, install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

   The `requirements.txt` file includes:
   - librosa
   - numpy
   - pandas
   - scikit-learn
   - keras
   - soundfile
   - matplotlib

## Usage
### Data Preparation
Before running the models, ensure that the datasets are properly organized. The expected directory structure is as follows:
```
Datasets/
    ├── RAVDESS/
    └── TESS/
```

### Running the Models
1. **Feature Creation**:
   To create features from the audio files, run:
   ```bash
   python create_features.py
   ```

2. **Training the Model**:
   To train the model using SVM or MLP, execute the respective Jupyter notebooks:
   - For SVM: `Machine Learning Algorithm - SVM/SER_SVM.ipynb`
   - For MLP: `MLP classifier/MLP.ipynb`

3. **Making Predictions**:
   To make predictions on new audio files, use the `TestingLive.ipynb` notebook or the `livePredictions` class in the `Deep Learning` folder.

## Code Structure
The repository is organized as follows:

```
.
├── create_features.py          # Script for feature extraction
├── tess_pipeline.py            # Main pipeline for TESS dataset processing
├── Machine Learning Algorithm - SVM/
│   ├── SER_SVM.ipynb           # Jupyter notebook for SVM training
├── MLP classifier/
│   ├── MLP.ipynb               # Jupyter notebook for MLP training
├── Deep Learning/
│   ├── TestingLive.ipynb       # Jupyter notebook for live predictions
│   ├── SER(Deep_Learning).ipynb # Jupyter notebook for deep learning model training
└── requirements.txt             # List of required packages
```

## Datasets
This project uses the following datasets:
- **RAVDESS**: A dataset containing emotional speech and song recordings.
- **TESS**: A dataset with recordings of target words spoken in various emotions.

Ensure you have the datasets downloaded and placed in the appropriate directories as mentioned in the usage section.

## Contributing
Contributions are welcome! If you have suggestions for improvements or new features, please fork the repository and submit a pull request.
