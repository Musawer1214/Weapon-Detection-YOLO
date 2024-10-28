# Weapon Detection with YOLOv8

This repository contains YOLOv8 model weights and code for testing a weapon detection model. The YOLOv8 architecture is the latest evolution of the YOLO (You Only Look Once) family, designed for high-performance real-time object detection tasks. The included model is specifically trained to detect weapons such as guns, knives, and other potentially harmful objects, making it ideal for surveillance systems, safety monitoring, and threat detection in various environments.

## Features
- **YOLOv8 Model Weights**: Pre-trained YOLOv8 weights specifically optimized for weapon detection.
- **Weapon Detection Testing Script**: Python script to test the YOLOv8 model on custom images or video feeds.
- **High Accuracy and Speed**: YOLOv8 provides enhanced accuracy and real-time detection, making it suitable for safety-critical applications.
- **Simple to Use**: Easy-to-follow instructions to load the model and test its performance.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Model Weights](#model-weights)
- [Testing the Model](#testing-the-model)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Installation
To get started, follow the instructions below to set up the environment and download the required files.

1. **Clone the repository**:
    ```sh
    git clone https://github.com/YourUsername/Weapon-Detection-YOLOv8.git
    cd Weapon-Detection-YOLOv8
    ```

2. **Set up the environment**:
   It is recommended to create a virtual environment before installing the dependencies to avoid conflicts.
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   Install the required Python libraries listed in the `requirements.txt` file.
   ```sh
   pip install -r requirements.txt
   ```

4. **Download the YOLOv8 Model Weights**:
   - Download the YOLOv8 model weights from the release page or a provided link.
   - Save the weights file (e.g., `best (3).pt`) in the root directory of the repository.

## Usage
To test the YOLOv8 weapon detection model, you can use the provided script to run detections on images or video streams.

### Run the Testing Script
Use the following command to test the model on an image or a video file:
```sh
python weapon-detection.ipynb --source path/to/your/input --weights best (3).pt
```

- **`--source`**: Specify the path to the input file (image or video).
- **`--weights`**: Path to the YOLOv8 model weights file (`best (3).pt`).

### Example
Test the model on an image:
```sh
python weapon-detection.ipynb --source sample_image.jpg --weights best (3).pt
```

Test the model on a video file:
```sh
python weapon-detection.ipynb --source sample_video.mp4 --weights best (3).pt
```

### Output
The script will display the input image or video stream with bounding boxes drawn around detected weapons. The confidence score of each detection is also displayed for easy interpretation.

## Dependencies
The following libraries are used in this project:
- `torch`: PyTorch is required for loading and running the YOLOv8 model.
- `opencv-python`: Used for image and video processing.
- `ultralytics`: YOLOv8 is developed and maintained by Ultralytics, and this package provides an easy interface to use YOLO models.

You can install all dependencies by running:
```sh
pip install -r requirements.txt
```

## Model Weights
The YOLOv8 model weights (`best (3).pt`) have been trained specifically for weapon detection. These weights need to be downloaded separately and placed in the root directory of the project.

If you do not have the weights file, you can download it from the [releases page](https://github.com/YourUsername/Weapon-Detection-YOLOv8/releases) or by following the instructions provided in the repository.

## Testing the Model
The testing script (`weapon-detection.ipynb`) allows you to evaluate the YOLOv8 model on images or videos.

### Script Overview
- **Load the Model**: The script loads the YOLOv8 model with the provided weights.
- **Process the Input**: It takes an image or video as input and processes each frame to detect weapons.
- **Display Results**: The script outputs the image or video with detected weapons highlighted, including bounding boxes and confidence scores.

### Supported Input Types
- **Images**: Test the model on static images for quick evaluation.
- **Video Files**: Use pre-recorded video files to assess the model's detection performance in different scenarios.
- **Live Video Streams**: With modifications, the script can also be adapted for live video feeds from a webcam or surveillance camera.

## File Structure
```
weapon-detection-yolov8/
├── weapon-detection.ipynb       # Script to test the YOLOv8 model
├── best (3).pt       # YOLOv8 model weights (downloaded separately)
├── requirements.txt               # List of dependencies
└── README.md                      # Documentation (this file)
```
- **`weapon-detection.ipynb`**: Main testing script for the YOLOv8 weapon detection model.
- **`best (3).pt`**: Pre-trained weights for YOLOv8 specifically for weapon detection.
- **`requirements.txt`**: Lists all required dependencies.
- **`README.md`**: Documentation for using the repository.

## Contributing
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. **Fork the repository**: This will create a copy of the repository in your GitHub account.
2. **Create a new branch**: Create a feature branch to work on a new feature or address a bug (`git checkout -b feature-name`).
3. **Commit your changes**: Make changes and commit them with a meaningful commit message (`git commit -m 'Add feature'`).
4. **Push to the branch**: Push your changes to your forked repository (`git push origin feature-name`).
5. **Open a pull request**: Create a pull request to merge your changes into the main repository.

Before contributing, please make sure to check the existing issues and follow the coding guidelines to ensure consistency across the project. We appreciate your help in improving the Weapon Detection system.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. You are free to use, modify, and distribute this project under the terms of the MIT License.

## Acknowledgments
- **Ultralytics**: Thanks to Ultralytics for providing the YOLOv8 model and the accompanying library that makes it easy to deploy state-of-the-art object detection models.
- **PyTorch**: For providing a flexible and powerful framework for building and deploying deep learning models.
- **OpenCV Community**: For maintaining and supporting one of the most widely used computer vision libraries available.
