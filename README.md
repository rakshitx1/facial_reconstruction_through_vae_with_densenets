# Facial Reconstruction through VAE with DenseNets

[![](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qjF3h6CBCCqq8J5Zv0OFjRs9iqJR81M5?usp=sharing)

This repository contains the implementation of our Project paper "Face Reconstruction with DenseNet-Enhanced Variational Autoencoders" which explores an enhanced approach to face reconstruction using variational autoencoders (VAEs) with DenseNet connectivity patterns and depthwise separable convolutions.

VAE architectures for face reconstruction by incorporating:
- **DenseNet connectivity patterns** for improved gradient flow and feature reuse
- **Depthwise separable convolutions** to reduce parameter count

Our approach achieves a 32.8% reduction in parameters (9.35M to 6.28M) compared to the baseline model while maintaining reasonable reconstruction quality. Interestingly, despite the parameter reduction, we observed an increased inference latency, highlighting the complex relationship between architectural design choices and computational performance.

## Key Features

- **Parameter Efficiency**: 32.8% reduction in model parameters
- **Latent Space Analysis**: Visualization and comparison of latent spaces
- **Attribute Manipulation**: Tools for manipulating facial attributes
- **Comparative Analysis**: Detailed comparison with baseline VAE model

## Results

Our experiments revealed several interesting findings:

1. **Parameter Reduction**: Successfully reduced parameters by 32.8% (9.35M to 6.28M)
2. **Inference Time**: Contrary to expectations, inference time increased from 1.77ms to 10.32ms per batch
3. **Reconstruction Quality**: Maintained reasonable reconstruction quality with slight reduction in fine details
4. **Latent Space Organization**: Modified VAE exhibits more clustered latent space organization compared to the original model's smoother distribution

## Usage

### Running the Notebook

The easiest way to explore our implementation is through Google Colab:

1. Click the "Open in Colab" badge at the top of this README
2. Run the cells in sequence to train models and visualize results

### Local Setup

To run the code locally:

```bash
# Clone the repository
git clone https://github.com/rakshitx1/facial_reconstruction_through_vae_with_densenets.git
cd facial_reconstruction_through_vae_with_densenets

# Install dependencies
pip install -r requirements.txt

# Open the notebook
jupyter notebook Face_Reconstruction_VAE_DenseNet.ipynb
```

## Dataset

We used the CelebA dataset, which contains 202,599 face images with 40 binary attributes. For computational efficiency, we trained on a subset of 20,000 images.

## Authors

- Rakshit Singhal
- Ram Prasad
- Palash Khatod

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
