---

# Centralized CCTV Surveillance System

## Overview

This project implements a centralized CCTV surveillance system designed for real-time video enhancement, monitoring, and detection of illegal activities and violence. The system provides advanced capabilities for alerting relevant authorities, ensuring enhanced security and timely responses.

## Features

- **Live Video Enhancement**: Improve video quality for better clarity and detail.
- **Real-Time Monitoring**: Continuously monitor live feeds from multiple cameras.
- **Illegal Movement Detection**: Identify and track unauthorized or suspicious movements.
- **Violence Detection**: Detect violent actions and behaviors in video streams.
- **Alert System**: Notify relevant authorities in case of detected threats or incidents.

## Technologies Used

- **Video Processing Libraries**: For enhancing and analyzing video feeds.
- **Machine Learning Models**: For detecting illegal movements and violence, including time series forecasting for predictive analytics.
- **Cloud Services**: For scalable storage and processing of video data.
- **API Integration**: For interfacing with external systems and alerting authorities.

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/centralized-cctv-surveillance.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd centralized-cctv-surveillance
   ```
3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Configure the System**:
   - Update configuration files with camera details and alert settings.
2. **Run the Application**:
   ```bash
   python main.py
   ```
3. **Monitor Outputs**:
   - Access the live video feeds through the provided interface.
   - Review alerts and notifications through the integrated alert system.

## Contributing

Contributions are welcome! Please follow these guidelines:

1. **Fork the Repository**.
2. **Create a Feature Branch**:
   ```bash
   git checkout -b test.py
   ```
3. **Commit Your Changes**:
   ```bash
   git commit -am 
   ```
4. **Push to the Branch**:
   ```bash
   git push origin test.py
   ```
5. **Create a Pull Request**.



Feel free to adjust the details to better fit your specific project and its requirements.# human-pose-estimation-opencv
Perform Human Pose Estimation in OpenCV Using OpenPose MobileNet

![OpenCV Using OpenPose MobileNet](output.JPG)


# How to use

- Test with webcam

```
python openpose.py
```

- Test with image
```
python openpose.py --input image.jpg
```

- Use `--thr` to increase confidence threshold

```
python openpose.py --input image.jpg --thr 0.5
```

# Notes:
- I modified the [OpenCV DNN Example](https://github.com/opencv/opencv/blob/master/samples/dnn/openpose.py) to use the `Tensorflow MobileNet Model`, which is provided by [ildoonet/tf-pose-estimation](https://github.com/ildoonet/tf-pose-estimation/tree/master/models/graph/mobilenet_thin), instead of `Caffe Model` from CMU OpenPose. The original `openpose.py` from `OpenCV example` only uses `Caffe Model` which is more than 200MB while the `Mobilenet` is only 7MB.
- Basically, we need to change the `cv.dnn.blobFromImage` and use `out = out[:, :19, :, :]` to get only the first 19 rows in the `out` variable.
