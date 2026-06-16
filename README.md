# project-cnn-vs-transfer-learning
[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/Qoqokoi/project-cnn-vs-transfer-learning)

## About The Project

This repository provides a comparative analysis between training a Convolutional Neural Network (CNN) from scratch and using a transfer learning approach for binary image classification tasks. The project implements and evaluates two distinct models on two different datasets to highlight the trade-offs and performance differences between these two common deep learning strategies.

The entire workflow, from data preprocessing to model training and evaluation, is contained within a single Jupyter notebook.

## Experiments

This project conducts two separate image classification experiments:

### 1. CNN from Scratch on CIFAR-10
*   **Objective:** To build and train a custom CNN architecture to classify two categories from the CIFAR-10 dataset.
*   **Dataset:** A subset of [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html), specifically the 'airplane' and 'automobile' classes.
*   **Model:** A simple CNN with two convolutional layers, batch normalization, max-pooling, and a fully connected classifier with dropout.

### 2. Transfer Learning on Oxford-IIIT Pets
*   **Objective:** To adapt a pre-trained model for a binary classification task using transfer learning.
*   **Dataset:** A subset of the [Oxford-IIIT Pet Dataset](https://www.robots.ox.ac.uk/~vgg/data/pets/), specifically 500 images of cats and 500 images of dogs.
*   **Model:** A pre-trained MobileNetV2 model with its weights frozen. Only the final classifier layer is replaced and trained for the cat vs. dog classification task.

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You need Python 3.x and pip installed on your system.

### Installation

1.  Clone the repository:
    ```sh
    git clone https://github.com/qoqokoi/project-cnn-vs-transfer-learning.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd project-cnn-vs-transfer-learning
    ```
3.  Install the required Python packages:
    ```sh
    pip install -r requirements.txt
    ```

### Usage

All the code for data loading, model definition, training, and evaluation is in the `notebook/cnn_vs_transfer_learning.ipynb` Jupyter notebook.

Open and run the notebook using a compatible environment like Jupyter Lab, Jupyter Notebook, or Google Colab. The notebook will automatically download the datasets and the pre-trained model weights.

## Results

After running the notebook, the models are evaluated on their respective test sets.

### CNN From Scratch (Airplane vs. Automobile)
*   **Final Test Accuracy:** 95.67%
*   **Confusion Matrix:**
    ```
    [[882  43]
     [ 35 840]]
    ```

### Transfer Learning (Cat vs. Dog)
*   **Final Test Accuracy:** 93.33%
*   **Confusion Matrix:**
    ```
    [[68  3]
     [ 7 72]]
    ```

The notebook also generates plots comparing the training/validation accuracy and loss curves for both experiments.

## Repository Structure

```
.
├── notebook/
│   └── cnn_vs_transfer_learning.ipynb # Main Jupyter Notebook with all code
├── report/                            # Directory for project reports
├── datasets.txt                       # Links to the datasets used
└── requirements.txt                   # Project dependencies