# Microcysts Source Code

Source Code of the paper: 

P. L. Vidal, J. de Moura, J. Novo, M. Ortega, "Robust fully-automatic multi-stage learning for the intuitive representation of MME accumulations in OCT images", The Visual Computer, 2024 (pending acceptance).

## 1. Installation Guide

To replicate the experiments, you need the following dependencies and requirements. Ensure you have Python 3.8+ installed.

- Clone the repository:
  ```bash
  git clone https://github.com/PlacidoFranciscoLizancosVidal/Microcysts_paper_code.git
  cd Microcysts_paper_code

 # Install the required Python libraries:
 
pip install -r requirements.txt

## 2. Usage Guide

This section explains how to use the repository to replicate the experiments:

Data Preparation: Place your OCT image datasets in the data/ directory, following the same structure used in the experiments.
Training the Model: To train the model on your data, run:

python train.py --dataset data/dataset_name --epochs 100 --batch_size 16

Adjust parameters like epochs, batch_size, etc., as needed.

## 3. Algorithm Documentation

Preprocessing Stage: The preprocessing pipeline applies standardization techniques to normalize OCT images, removing artifacts and preparing data for robust model training. This involves histogram equalization and artifact cropping (details available in preprocessing.py).

Model Architecture: The core of the model is based on a Convolutional Neural Network (CNN) inspired by U-Net, optimized for segmenting microcyst regions in OCT images. The architecture includes an encoder-decoder structure, with skip connections allowing for the preservation of spatial context (explained in model.py).

Training and Loss Functions: We employed a multi-stage training approach, progressively fine-tuning the model using different datasets. A combination of Cross Entropy Loss and Dice Loss was utilized to improve pixel-wise accuracy (see train.py for implementation).

## 4. Permanent Links

To enhance reproducibility, the following resources have been archived using Zenodo for persistent access:

https://doi.org/10.5281/zenodo.14006681

## 5. Usage Disclaimer and Citation

This dataset is intended for statistical purposes only, and no private data or fees are required. If you use this image set in your work, please include the following reference:

P. L. Vidal, J. de Moura, J. Novo, M. Ortega, "Robust fully-automatic multi-stage learning for the intuitive representation of MME accumulations in OCT images", The Visual Computer, 2024 (pending acceptance).
