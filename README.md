# Image Colorization Using GANs

A deep learning-based image colorization system that automatically converts grayscale images into realistic color images using a **Conditional GAN (cGAN)** architecture. The model uses a **U-Net generator** with a **PatchGAN discriminator** and operates in the **L*a*b*** color space to predict color channels from grayscale inputs.

## Key Features

* **U-Net Generator** for pixel-level color prediction.
* **PatchGAN Discriminator** for learning realistic local color details.
* **L*a*b*** color space for separating luminance from color information.
* Combined **L1 + adversarial loss** for accurate and visually realistic outputs.
* **Pretrained ResNet18 backbone** used to initialize the U-Net generator.
* Two-stage training: **L1 pretraining followed by adversarial fine-tuning**.

## Dataset

The model is trained and validated on a subset of the **COCO dataset**, using 8,000 images for training and 2,000 for validation.

## Tech Stack

**Python · PyTorch · FastAI · NumPy · OpenCV/PIL · scikit-image · Matplotlib**

## Results

Pretraining the generator with L1 loss before adversarial training significantly improves colorization quality and reduces the training required compared with training the GAN from scratch.
