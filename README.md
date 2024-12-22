# Diffusion-Based Generative Model for Synthetic Face Images

## Project Overview
This project focuses on developing a diffusion-based generative model to create synthetic face images. The dataset consists of facial images categorized into three demographic groups: Orientals, Indians, and White Europeans. The model generates images that blend features from these groups using a UNet-based architecture.

The main objective is to demonstrate the capability of diffusion-based models to generate diverse and realistic synthetic faces while maintaining demographic diversity.


## Features
- Data Preprocessing: Images are resized, normalized, and categorized by demographic group.
- Model Architecture: UNet-based encoder-decoder model optimized for image generation.
- Diffusion Process: Introduces and removes noise in a controlled manner to synthesize realistic images.
- Output: Generates images with combinations of features from multiple demographic groups.


## Dataset
The dataset was created using a combination of publicly available datasets and images collected via Google Image Search. Preprocessed images are labeled by race and gender.

Publicly available datasets considered:
- [UTKFace Dataset](https://susanqq.github.io/UTKFace/)
- [CelebA Dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
- [Labeled Faces in the Wild (LFW)](http://vis-www.cs.umass.edu/lfw/)


## Implementation Details
1. Data Preprocessing:
   - Images resized to 64x64 RGB.
   - Normalization applied to facilitate model training.

2. Model Training:
   - Gaussian noise was added at each step to simulate the diffusion process.
   - Loss function: Mean Squared Error (MSE).
   - Optimized using custom diffusion schedulers.

3. Evaluation:
   - Loss trends tracked over 100 epochs.
   - Generated images assessed for quality, diversity, and demographic representation.


## Results
- Loss Trends: Training and testing losses stabilized to near-zero (~0.005) by the 100th epoch, indicating effective learning.
- Generated Images: Synthetic images exhibit a realistic blending of features from the targeted demographic groups.
- Challenges: Minor artifacts and lack of sharp details in some outputs highlight areas for improvement.


## Future Work
- Enhance image clarity by fine-tuning the UNet architecture and hyperparameters.
- Increase dataset size and diversity to capture finer details.
- Experiment with advanced diffusion schedulers and longer training durations.
