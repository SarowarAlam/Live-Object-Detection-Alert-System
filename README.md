# Live Object Detection Alert System

## Overview
This project demonstrates a **Live Object Detection Alert System** designed to detect and alert users of specific objects (e.g., humans or animals) in restricted areas. The system leverages the **YOLOv8 model** for real-time object detection and includes an email alert mechanism for notification. The core objective of this project is to provide a proof-of-concept for deploying a robust detection system in real-world scenarios.

> **Note**: This repository contains a **demo version** of the project. For demonstration purposes, we have used:
> - A smaller dataset
> - Fewer training epochs
> to ensure faster training and testing. The actual project can be scaled with larger datasets and additional training epochs for enhanced performance.

---

## Features

- **Object Detection**: Detects objects such as humans and animals in real-time.
- **Email Alerts**: Sends an email notification when specific objects are detected in the restricted area.
- **Webcam Integration**: Uses the webcam feed for live detection.
- **YOLOv8**: Implements the latest YOLOv8 model for state-of-the-art object detection.

---

## Project Structure

```
├── dataset
│   ├── train/           # Training images
│   ├── val/             # Validation images
│   └── data.yaml        # Dataset configuration file
├── runs
│   ├── train/           # Directory where training results are saved
├── model_training.ipynb # Notebook for training the YOLOv8 model
├── Live_Object_Detection_Alert_System.ipynb
│                        # Notebook for live object detection
├── README.md            # Project documentation
```

---

## Setup

### Prerequisites
- Python 3.9 or above
- Anaconda environment (recommended for managing dependencies)
- Webcam for real-time detection

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Live-Object-Detection-Alert-System.git
   cd Live-Object-Detection-Alert-System
   ```

2. Create a Conda environment and activate it:
   ```bash
   conda create -n yolo_env python=3.9 -y
   conda activate yolo_env
   ```

3. Install required dependencies:
   ```bash
   pip install ultralytics opencv-python torch torchvision smtplib
   ```

4. Verify installation:
   ```bash
   python -c "import ultralytics; print('Ultralytics installed successfully!')"
   ```

---

## Usage

### 1. Train the Model
- Open the `model_training.ipynb` notebook.
- Replace the dataset path in the `data_yaml_path` variable with the actual path to your dataset's `data.yaml` file.
- Run the notebook to train the YOLOv8 model.
- Trained weights will be saved in the `runs/train` directory.

### 2. Perform Live Detection
- Open the `Live_Object_Detection_Alert_System.ipynb` notebook.
- Replace the model path with the path to the trained weights (e.g., `runs/train/object_detection_model/weights/best.pt`).
- Configure the email sender and recipient details in the `send_email_alert` function.
- Run the notebook to start live object detection.

### 3. Email Alerts
- Ensure you provide valid credentials in the email configuration.
- The system will send alerts when specific objects (e.g., humans or animals) are detected.

---

## Notes on the Demo
- **Reduced Dataset**: The demo uses a smaller dataset to simplify the training process.
- **Lower Epochs**: Training is limited to 10 epochs in the demo to reduce runtime.
- **Performance**: The system is designed to work efficiently with larger datasets and more training epochs in real-world applications.

---

## Limitations
- **Real-Time Constraints**: Webcam detection may have delays depending on hardware capabilities.
- **Email Configuration**: Ensure correct email settings for the alert system to work.
- **Hardware Requirements**: GPU acceleration is recommended for faster training and detection.

---

## Future Work
- Enhance the dataset with more diverse examples.
- Increase training epochs for improved accuracy.
- Optimize the model for edge device deployment.
- Add support for SMS or push notifications.

---

## Contributing
We welcome contributions to enhance the project! Please submit a pull request or open an issue for suggestions.

---
## Contact
If you have any questions or need further assistance, please feel free to contact:

- **Name**: Sarowar Alam
- **Email**: sarowaralam40@gmail.com
- **GitHub**: [https://github.com/SarowarAlam](https://github.com/SarowarAlam)



