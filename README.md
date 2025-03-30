# Road-link
This contains the code for accident free road 

# Road Link - Vehicle-to-Vehicle Communication System

## Project Overview
Road Link is an advanced real-time vehicle-to-vehicle (V2V) communication system that combines computer vision with Dedicated Short-Range Communications (DSRC) technology. The system provides:
- Proximity warnings between vehicles
- Directional intention alerts (turning left/right)
- AI-powered autonomous decision making for collision prevention
- Retrofit compatibility for both new and older heavy-duty vehicles

## Key Features
1. **Real-time Object Detection**: Uses YOLOv8 for identifying vehicles and obstacles
2. **Region of Interest (ROI) Monitoring**: Tracks objects in critical zones
3. **Adjustable Sensitivity**: Customizable detection thresholds
4. **Visual Alert System**: Color-coded warnings (red for danger, green for safe)
5. **Future DSRC Integration**: Designed for seamless V2V communication

## Code Files

### 1. `collision_warning_system.py`
This script implements a comprehensive collision prediction system using:
- YOLOv8 for object detection
- MiDaS for depth estimation
- Simple centroid tracking
- Distance and speed thresholding

Key functionalities:
- Cached detection for performance optimization
- Depth estimation scaled to real-world distances
- Speed calculation between frames
- Visual warnings for nearby objects

### 2. `roi_monitoring.py`
A simpler version focusing on Region of Interest monitoring:
- Diagonal ROI line definition
- Configurable sensitivity settings
- Visual feedback for objects entering danger zones
- Adjustable confidence and box area thresholds

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/road-link.git
cd road-link
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### For the full collision warning system:
```bash
python collision_warning_system.py
```

### For the ROI monitoring system:
```bash
python roi_monitoring.py
```

Use the trackbars in the "Sensitivity Settings" window to adjust:
- Confidence threshold (0-100%)
- Minimum detection box area (100-5000 pixels)

Press ESC to exit the application.

## System Requirements
- Python 3.7+
- Webcam or video input source
- NVIDIA GPU recommended for better performance (not required)

## Future Enhancements
1. **DSRC Integration**: Implement actual V2V communication
2. **Advanced Tracking**: Replace simple centroid with DeepSORT
3. **Vehicle-specific Detection**: Custom models for heavy-duty vehicles
4. **Directional Intention**: Detect turn signals and communicate intentions
5. **Multi-camera Support**: 360-degree coverage around the vehicle

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Ultralytics for YOLOv8
- Intel for MiDaS depth estimation
- OpenCV for computer vision components

---

This README provides comprehensive documentation for your GitHub repository. It includes:
1. Project overview and features
2. Code file descriptions
3. Installation and usage instructions
4. System requirements
5. Future enhancement plans
6. Licensing information

The structure is clean and professional, making it easy for users and contributors to understand your project. You may want to add:
- Screhots of the system in action
- A more detailed hardware requirements section if deploying to actual vehicles
- Contribution guidelines if opening the project to collaborators
