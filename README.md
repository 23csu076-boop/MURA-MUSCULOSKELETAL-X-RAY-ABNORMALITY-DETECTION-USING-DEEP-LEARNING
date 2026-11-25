# MURA-MUSCULOSKELETAL-X-RAY-ABNORMALITY-DETECTION-USING-DEEP-LEARNING


MURA is a deep learning research project that explores the classification of musculoskeletal X-ray images as normal or abnormal. The project compares traditional neural networks, convolutional neural networks (CNNs), transfer-learning architectures, and transformer-based models for medical image classification.

The project includes exploratory data analysis, image preprocessing, model implementation, training, and performance comparison.

## Project team

- Chander Mohan (`23CSU076`)
- Pranav (`23CSU243`), Project Partner

**Department of Computer Science & Engineering**  
The NorthCap University, Gurugram, Haryana, India

## Project contents

- `notebooks/` — Jupyter notebooks for data exploration, preprocessing, model implementation, training, and comparison.
- `MURA_Project_with_CNNs_and_Transformers(2).ipynb` — Main notebook containing CNN and transformer experiments.
- `MURA_Project_with_ViT_Swin_Comparison(1).ipynb` — Notebook exploring Vision Transformer and Swin-style transformer approaches.
- `MURA_Full_Major_Project_Report_with_Graphs.docx` — Major project report with dataset analysis, methodology, graphs, and results.
- `MURA_Major_Project_Presentation.pptx` — Project presentation.
- `MURA_Research_Paper_Formatted_Like_VoiceGuard.docx` — Research paper formatted in an academic paper style.

## Data

The project uses the **MURA v1.1 musculoskeletal X-ray dataset**, which contains radiographs labeled as normal or abnormal.

The dataset contains:

- **36,807** training images
- **3,197** validation images

The training labels are:

- `0` — Normal
- `1` — Abnormal

The dataset includes X-ray images from seven body-part categories:

- Wrist
- Shoulder
- Hand
- Finger
- Elbow
- Forearm
- Humerus

The project focuses on broad musculoskeletal X-ray abnormality classification. The abnormal label does not specifically indicate a bone fracture or provide a diagnosis for a particular condition.

The notebooks use a smaller randomly sampled subset of the dataset for some experiments to reduce computational requirements. These experiments should not be interpreted as a complete evaluation on the entire dataset.

## Models explored

The project explores multiple deep learning architectures:

- Artificial Neural Network (ANN)
- Basic Convolutional Neural Network (CNN)
- LeNet-inspired CNN
- AlexNet-inspired CNN
- VGG16
- VGG19
- GoogLeNet-inspired Inception v1
- InceptionV3
- ResNet50
- DenseNet121
- Vision Transformer (ViT)
- Simplified Swin-style Transformer

The models use different image sizes and preprocessing configurations depending on the architecture.

The ANN and basic CNN experiments use 64 × 64 grayscale images. Transfer-learning models use 224 × 224 RGB images, while the ViT and Swin-style experiments use 96 × 96 RGB images.

## Environment

The notebooks use Python, TensorFlow/Keras, and common data science and image-processing libraries.

Some models require substantial memory and may take longer to train on a CPU. GPU availability depends on the installed TensorFlow build and hardware configuration.

### Setup

Create and activate a Python virtual environment on Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

Upgrade pip:

```bash
python -m pip install --upgrade pip
```

Install the required packages:

```bash
python -m pip install tensorflow pandas numpy matplotlib seaborn scikit-learn pillow jupyter
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open the project notebooks and update the dataset path according to your local MURA dataset location.

## Reproducing the experiments

Begin with the main MURA notebook:

`MURA_Project_with_CNNs_and_Transformers(2).ipynb`

The notebook includes dataset preparation, image preprocessing, model construction, and experiments with CNN and transformer architectures.

Use the following notebook for the ViT and Swin-style comparison:

`MURA_Project_with_ViT_Swin_Comparison(1).ipynb`

The ANN and basic CNN experiments include saved training and validation results. The notebook also contains prediction visualizations and model comparison outputs.

Final evaluation metrics for every architecture were not preserved in the available notebook outputs. Therefore, a complete numerical ranking of all models cannot be reproduced from the saved results alone.

## Results and limitations

The saved ANN and basic CNN experiments were trained for one epoch on a sampled dataset.

The ANN achieved approximately:

- Training accuracy: 54.15%
- Validation accuracy: 52.20%

The basic CNN achieved approximately:

- Training accuracy: 57.70%
- Validation accuracy: 52.40%

These early results are exploratory and do not establish that one architecture is significantly better than the other.

The project is an academic research prototype. It has not been clinically validated and is not intended for medical diagnosis or clinical decision-making.

## Collaboration

Use a separate branch for new experiments and create a pull request before merging changes into the shared `main` branch.

Keep generated model weights, downloaded datasets, cached files, and temporary exports out of Git. Do not commit API tokens, private keys, or personal access credentials.

## Citation and reuse

Please cite the MURA dataset and the relevant research papers when using this project.

The project explores deep learning methods for musculoskeletal X-ray abnormality classification and should be used for academic and educational purposes.

No software license has been selected yet. Until a license is added, public repository visibility does not automatically grant permission to reuse the project's code or documents.
