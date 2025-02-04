# Image Segmentation with U-Net

This project implements image segmentation using the U-Net architecture, a widely-used model for semantic segmentation tasks. The project is built using TensorFlow and Keras.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Model](#model)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview

Image segmentation is the process of partitioning an image into multiple segments to simplify its representation. U-Net is a convolutional neural network designed for fast and precise segmentation of images.

This notebook demonstrates how to implement U-Net for image segmentation using TensorFlow, handling a dataset of RGB images and their corresponding segmentation masks.

## Dataset

The dataset consists of RGB images and their corresponding segmentation masks. The images are loaded from a directory and preprocessed for training the U-Net model.

- **Images:** Color images from the `./data/CameraRGB/` directory.
- **Segmentation Masks:** Ground truth segmentation masks from the `./data/CameraMask/` directory.

## Model

The U-Net architecture is implemented using Keras. The key features of the model include:

- **Encoder:** Series of convolutional layers and max pooling.
- **Bottleneck:** A bridge between the encoder and decoder.
- **Decoder:** Series of transposed convolution layers for upsampling.
- **Skip Connections:** Used to combine feature maps from the encoder with the decoder to improve performance.

## Installation

To run the code in this notebook, follow these steps:

1. Clone the repository.
2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Ensure you have the dataset stored in the appropriate folder structure (`./data/CameraRGB/` and `./data/CameraMask/`).

## Usage

1. Load the dataset by modifying the `path` variable in the notebook to point to the dataset folder.
2. Train the model by running the notebook cells. The training configuration (epochs, batch size) can be modified within the notebook.
3. Visualize the segmentation results by running the `show_predictions()` function.

## Results

During training, the model's accuracy and loss metrics are plotted. The segmentation results can be visualized for a set of images by displaying the predicted masks alongside the original images.

## Contributing

Contributions to improve the project are welcome. Please feel free to submit a pull request.

## License

This project is licensed under the MIT License.
