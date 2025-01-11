# Live Object Detection Alert System

## Overview
This project demonstrates a **Live Object Detection Alert System** designed to detect and alert users of specific objects (e.g., humans or animals) in restricted areas. The system leverages the **YOLOv8 model** for real-time object detection and includes an email alert mechanism for notification. The core objective of this project is to provide a proof-of-concept for deploying a robust detection system in real-world scenarios.

> **Note**: This repository contains a **demo version** of the project. For demonstration purposes, we have used:
> - A smaller dataset (Where we made our own customed small dataset with help of the annotation tools e.g. roboflow, V7, Labelbox, Scale AI, SuperAnnotate, DataLoop, Playment, Supervise.ly, Hive Data, CVAT, LabelMe, Labelimg, VoTT, ImgLab)
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

## Visual Represation of Factors

![image](https://github.com/user-attachments/assets/6be9deb5-9504-4468-9924-70154ba3d9cc)

---
![image](https://github.com/user-attachments/assets/da20c38a-573c-4750-a618-9d283f7e7323)

---
![image](https://github.com/user-attachments/assets/2827deb8-ab53-4a9f-b04d-b81fec7bac8a)

---
![image](https://github.com/user-attachments/assets/c01562c9-bf7f-41ac-a531-8fc6d12f3f93)

---
![image](https://github.com/user-attachments/assets/ea9606b6-666a-4b52-902c-3d484fd9b7f7)

---
![image](https://github.com/user-attachments/assets/9a2e9815-2809-4239-8169-14702b5de51e)

---
![image](https://github.com/user-attachments/assets/92ba5e76-e7d9-4cb7-8942-33da100732b7)

---
![image](https://github.com/user-attachments/assets/65a73b27-681c-49da-ae93-373acc932be5)

---
![image](https://github.com/user-attachments/assets/fa67ba61-d9d5-4be7-9ddf-1716a4eab646)

---
![image](https://github.com/user-attachments/assets/f0a889f6-f6dd-4fc2-a076-b8d758653dd3)

---
![image](https://github.com/user-attachments/assets/00d721cf-386b-4895-8f43-525759cc7f52)

---
## Contact
If you have any questions or need further assistance, please feel free to contact:

- **Name**: Sarowar Alam
- **Email**: sarowaralam40@gmail.com
- **GitHub**: [https://github.com/SarowarAlam](https://github.com/SarowarAlam)



