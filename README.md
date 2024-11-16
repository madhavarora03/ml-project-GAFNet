# GAF-Net: Classifying Glioblastoma Histopathology Images Using an Attention-based Feature-aware Framework
# Overview

GAF-Net is an ensemble deep learning framework for the classification of glioblastoma (GBM) histopathology images. It integrates three state-of-the-art models—RDF-Net, GED-Net, and VCA-Net—using Convolutional Block Attention Modules (CBAM) for efficient feature extraction. The model aims to improve diagnostic accuracy for glioblastoma detection and classification by identifying distinct histological subregions within H&E-stained formalin-fixed paraffin-embedded (FFPE) tissue sections.

This project addresses the challenges of class imbalance and complex image features by applying data augmentation techniques and a composite loss function.

## Features

- Ensemble of three deep learning models: RDF-Net, GED-Net, and VCA-Net.
- Utilizes Convolutional Block Attention Modules (CBAM) to enhance feature extraction.
- Data augmentation techniques for improved model robustness and generalization.
- Soft voting ensemble technique for combining the predictions of multiple models.
- Custom composite loss function for balanced classification performance.

## Dataset

The model uses H&E-stained FFPE tissue sections from The Cancer Imaging Archive (TCGA), specifically the TCGA-GBM and TCGA-LGG collections. The images are classified into six categories based on histopathological features:
- Cellular Tumor (CT)
- Pseudopalisading Necrosis (PN)
- Microvascular Proliferation (MP)
- Geographic Necrosis (NC)
- Cortical Infiltration (IC)
- White Matter Penetration (WM)

## Model Architecture

GAF-Net integrates three distinct models:

- RDF-Net (Residual Dual Focus Network): Built on a ResNet backbone with dual attention mechanisms (channel and spatial attention).
- VCA-Net (VGG-based Convolutional Attention Network): A VGG-based model augmented with attention modules to focus on discriminative features.
- GED-Net (Generalizing Encoder-Decoder Network): A VGG19-based encoder-decoder model that learns both global and local features.

These models are combined into an ensemble using a soft voting technique.

## Results
On a validation set (20% of the training data), the following results were achieved:

- Accuracy: 0.9673
- F1-Score: 0.9634
- Precision: 0.9670
- Sensitivity (Recall): 0.9600
- Specificity: 0.9860
