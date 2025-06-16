# LM-Net-crack: LM-Net but for Crack Detection
- This model is based on the architecture of LM_NET which was mainly used for medical images segmentation, i optimized it to be used for crack detection.

## Model Architecture

LM-Net is a novel architecture that combines:

- Multi-Branch Modules for efficient feature extraction
- Global Feature Transformer (GFT) for capturing long-range dependencies
- Neighborhood Attention Transformers (NAT) for local context modeling
- Skip connections with M2Skip and M3Skip modules for multi-scale feature fusion


- I am trying to implement a new FPN since the current FPN only has the top down path.
## Dataset

The model is trained on the UDTIRI-Crack dataset, which contains images of cracks in various surfaces with corresponding binary segmentation masks. This dataset was proposed on a recent paper, and comprises of multiple images from different publick crack datasets

## Requirements

- PyTorch
- torchvision
- NATTEN (Neighborhood Attention Extension)
- albumentations
- PIL
- numpy
- matplotlib
- tqdm

## Usage

The notebook demonstrates:
1. Model definition and architecture
2. Dataset loading and preprocessing
3. Training and validation loops
4. Metrics calculation (Dice coefficient and IoU)
5. Visualization of predictions

## Training

The model is trained using a combination of Cross-Entropy and Dice loss with the AdamW optimizer. Learning rate scheduling is implemented using ReduceLROnPlateau.

## Performance Metrics

The model's performance is evaluated using:
- Dice coefficient
- Intersection over Union (IoU)
- Visual comparison of predictions against ground truth
