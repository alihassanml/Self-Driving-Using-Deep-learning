# Self-Driving Car System Using Deep Learning

![Project Banner](https://your-image-url.com/banner.png)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Overview

This project implements a self-driving car system utilizing a Convolutional Neural Network (CNN) to predict steering angles based on input images from a front-facing camera. The system is designed to operate within the Udacity Self-Driving Car Simulator, enabling autonomous navigation in a simulated environment.

## Features

- **Real-time Processing**: Utilizes `socketio` and `eventlet` for efficient real-time communication between the simulator and the model.
- **Image Preprocessing**: Implements preprocessing techniques including region of interest selection, color space conversion, Gaussian blur, resizing, and normalization.
- **Model Integration**: Loads a pre-trained CNN model (`model2.h5`) for predicting steering angles.
- **Adaptive Throttle Control**: Adjusts the throttle based on current speed to maintain a predefined speed limit.

## Installation

To set up the project, follow these steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/alihassanml/Self-Driving-Using-Deep-learning.git
   ```

2. **Navigate to the Project Directory**:

   ```bash
   cd Self-Driving-Using-Deep-learning
   ```

3. **Install Required Dependencies**:

   Ensure you have Python installed. Then, install the necessary packages:

   ```bash
   pip install -r requirements.txt
   ```

   *Note: The `requirements.txt` file should list all necessary packages. If it's not present, install the following packages individually:*

   ```bash
   pip install eventlet socketio flask keras pillow opencv-python numpy
   ```

## Usage

To run the self-driving car system:

1. **Launch the Udacity Self-Driving Car Simulator**:

   - Select the autonomous mode.

2. **Start the Python Server**:

   Execute the provided Python script to start the server:

   ```bash
   python drive.py
   ```

   *Ensure that `drive.py` contains the provided code snippet and is located in the project directory.*

3. **Monitor the Output**:

   The server will display real-time predictions of steering angles, throttle values, and current speed.

   Example output:

   ```
   Connected
   Steering Angle: -0.045 Throttle: 0.9 Speed: 8.5
   ```

## Model Architecture

The CNN model (`model2.h5`) follows the architecture inspired by NVIDIA's End-to-End Learning for Self-Driving Cars. The architecture includes:

- **Convolutional Layers**: Extract spatial features from input images.
- **Activation Functions**: Introduce non-linearity using ReLU activations.
- **Fully Connected Layers**: Interpret features and predict the steering angle.

*Note: For detailed architecture and training procedures, refer to the model documentation or training script.*

## Dataset

The model was trained using a dataset collected from the Udacity Self-Driving Car Simulator, comprising images from the front-facing camera and corresponding steering angles.

## Results

The system successfully navigates the simulated environment, maintaining lane discipline and adapting to curves based on real-time predictions.

*Include visual results or performance metrics if available.*

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Make your changes and commit them:

   ```bash
   git commit -m "Add your message here"
   ```

4. Push to your branch:

   ```bash
   git push origin feature/your-feature-name
   ```

5. Open a pull request detailing your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgements

- [Udacity Self-Driving Car Simulator](https://github.com/udacity/self-driving-car-sim)
- NVIDIA's research on [End-to-End Learning for Self-Driving Cars](https://arxiv.org/abs/1604.07316)
- [eventlet](http://eventlet.net/)
- [socketio](https://python-socketio.readthedocs.io/en/latest/)
- [Keras](https://keras.io/)
- [OpenCV](https://opencv.org/)

```

**Notes**:

- Replace `https://your-image-url.com/banner.png` with the actual URL of your project banner image.
- Ensure that `requirements.txt` is present in your repository, listing all necessary dependencies. If not, consider creating one for ease of installation.
- Include any additional sections or details relevant to your project to enhance clarity and usability.
