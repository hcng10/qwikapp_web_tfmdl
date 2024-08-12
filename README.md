# Qwikapp_web_tfmdl: Tensorflow Model on Qwikapp web

## Overview
This project consists of two dockerize components: LFT Detect and LFT Classify. Together, they provide a complete solution for processing lateral flow test (LFT) images. The detection component identifies and crops regions of interest within an LFT image, while the classification component categorizes these regions as 'invalid', 'negative', or 'positive'.


## Project Structure

- **[`lft_detect/`](./lft_detect/)**: Contains the code and configurations for detecting regions of interest in LFT images.
- **[`lft_classify/`](./lft_classify/)**: Contains the code and configurations for classifying the cropped regions from the detection step.

### `lft_detect/`
This component uses a YOLOv8 model to detect specific areas in the LFT images, such as the cassette, test region, and test strip. It then crops the detected regions and saves them for further analysis.


**Key Features:**

- Object detection using a YOLOv8 model from KerasCV.
- Automatic cropping of detected regions based on the target class.
- Preprocessing with image resizing and padding to maintain aspect ratio.

### `lft_classify/`

This component uses a MobileNetV3 model to classify the cropped LFT regions into predefined categories: 'invalid', 'negative', and 'positive'. It includes preprocessing steps such as normalization and resizing to ensure consistent input to the model.

**Key Features:**

- Image classification using a Classifier model from KerasCV.
- Preprocessing with normalization and resizing.

## Getting Started

### Prerequisites

- Docker and Docker Compose installed on your machine.

### Setup

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/lft_detection_classification.git](https://github.com/hcng10/qwikapp_web_tfmdl.git
   cd lft_detect

2. **Set Up Environment Variables:**
3. **Running the Services:**
4.   
