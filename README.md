# License Plate Recognition System

## Introduction
**License Plate Recognition System** is a Windows Forms application that automatically recognizes and manages vehicle information through surveillance cameras using state-of-the-art AI models.

### Purpose
- Automatically recognize license plates from RTSP/IP cameras
- Manage traffic surveillance camera systems  
- Analyze and generate traffic statistics
- Retrieve vehicle movement history

### Advantages
- Modern, user-friendly interface
- **98.92% accuracy** with YOLOv11 + Fast-Plate OCR
- Custom OCR optimized for Vietnamese license plates
- Support for multiple simultaneous cameras
- Visual data analysis with charts
- Detailed history storage and retrieval

## Key Features

### 1. Camera Management
- **Add/Edit/Delete Cameras** with RTSP URLs
- **Filter & Search** cameras by name, location, status  
- **Toggle Detection** per camera
- **Real-time Connection Testing**

### 2. Camera Monitoring
- **Live Multi-camera Viewing** with grid layout
- **Full-screen Mode** for detailed inspection
- **Real-time Detection Status** with FPS monitoring
- **Detection Toggle Controls**

### 3. Traffic Analysis
- **Density Charts** - Traffic volume by hour
- **Vehicle Type Analysis** - Distribution pie charts
- **Dashboard Metrics** - Key performance indicators
- **Time & Location Filtering**
- **Excel Report Export**

### 4 Vehicle Information Retrieval
- **License Plate Search** (full or partial)
- **Vehicle Type Filtering** (Motorcycle, Car, Bus, Truck, Other)
- **Time Range Filtering**
- **Detailed History View** with captured images

## Performance Benchmarks

### Research-Based Performance Metrics
Based on FPT University comparative study, our system implements the best-performing models:

#### Detection Performance (mAP@0.5)
| Model | Accuracy | Parameters | GFLOPs |
|-------|----------|------------|---------|
| **YOLOv11** | **99.4%** | 2.6M | 6.3 |
| YOLOv8 | 98.7% | 3.5M | 10.5 |
| YOLOv5 | 97.2% | 1.8M | 4.1 |

#### OCR Performance (Plate Accuracy)
| OCR Method | Accuracy | Key Features |
|------------|----------|--------------|
| **Fast-Plate OCR (CNN+CTC)** | **98.92%** | End-to-end, sequence recognition |
| YOLOv11 + CNN | 77.9% | Character segmentation + classification |
| Contours + CNN | 60.0% | Traditional computer vision |

### Real-world Performance
- **Detection Speed**: 25-30 FPS per camera (with GPU acceleration)
- **Accuracy**: 98.92% plate-level recognition rate
- **Robustness**: Handles motion blur, lighting variations, and partial occlusions
- **Character Set**: 32 Vietnamese alphanumeric symbols

## Installation

### Quick Setup
1. Run `Setup.exe` as Administrator
2. Follow installation wizard steps
3. Database auto-configures on first run
4. Add camera RTSP URLs in Camera Management
5. Test camera connections and enable detection

## User Guide

### Getting Started
1. **Add Cameras**: Enter RTSP URLs in Camera Management
2. **Enable Detection**: Toggle detection for each camera
3. **Monitor**: View live streams in monitoring section
4. **Analyze**: Generate traffic reports in Analysis section
5. **Search**: Find vehicle history in Search section

### Camera Setup
- **RTSP Format**: `rtsp://username:password@ip:port/stream`
- **Test Connection**: Use built-in connection tester
- **Detection**: Enable per camera for automatic plate recognition

### Traffic Analysis
- Select date range and location filters
- View dashboard with key metrics
- Export comprehensive Excel reports
- Analyze traffic patterns with interactive charts

### Vehicle Search
- Search by full or partial plate numbers
- Filter by vehicle type and time range
- View detailed records with captured images
- Track vehicle movement history

## 🔧 Technical Architecture

### Research-Based Implementation
Our system implements findings from FPT University benchmark study:

#### Detection Pipeline
```
Video Stream → YOLOv11 Detection → Plate Cropping → Fast-Plate OCR → Database Storage
```

#### Key Advantages
- **YOLOv11**: Superior small object detection with attention mechanisms
- **Fast-Plate OCR**: End-to-end recognition without character segmentation  
- **CTC Decoding**: Handles variable-length sequences effectively

### Dataset Validation
- **8,259+ detection images** used for training validation
- **3,763 OCR samples** with Vietnamese plate variations
- **Real-world conditions**: Motion blur, lighting changes, occlusions

## Performance Summary

### Key Research Findings
- **Best Detection**: YOLOv11 (99.4% mAP@0.5)
- **Best OCR**: Fast-Plate OCR (98.92% plate accuracy)
- **Optimal Combination**: YOLOv11 + Fast-Plate OCR
- **Real-time Capable**: 25-30 FPS with GPU acceleration

### Deployment Ready
- Validated on Vietnamese license plates
- Robust to real-world conditions  
- Production-ready accuracy metrics

---

*Performance: 98.92% Plate Recognition Accuracy*  
*System Version: 1.0*
---

## Support & Contact

**Technical Support:**
- Email: vohoanglam2211@gmail.com 

**Documentation:**
- Document: [Document]()
