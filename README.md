# License Plate Recognition System

## Table of Contents
- [Introduction](#introduction)
- [Key Features](#key-features)
- [System Requirements](#system-requirements)
- [Installation](#installation)
- [User Guide](#user-guide)
- [Configuration](#configuration)
- [Troubleshooting](#troubleshooting)

---

## Introduction

**License Plate Recognition System** is a Windows Forms application developed with C# .NET Framework, integrating AI/ML to automatically recognize and manage vehicle information through surveillance cameras.

### Purpose
- Automatically recognize license plates from RTSP/IP cameras
- Manage traffic surveillance camera systems
- Analyze and generate traffic statistics
- Retrieve vehicle movement history
- 
---

## Key Features

### 1. Camera Management

**Core Functions:**
- **Add Camera**: Add new cameras with RTSP URLs
- **Edit Camera**: Modify existing camera information
- **Delete Camera**: Remove cameras from system
- **Filter Cameras**: Filter by name, location, status
- **Search**: Find cameras by keywords
- **Toggle Detection**: Enable/disable detection per camera

**Supported Camera Types:**
- All cameras supporting RTSP protocol
- Hikvision, Dahua, Axis, and other major brands
- IP cameras with public/private network access

### 2. Camera Monitoring

**Live Monitoring Features:**
- **Real-time Viewing**: Display streams from multiple cameras
- **Full-screen Mode**: View camera in detailed full-screen mode
- **Camera Filtering**: Filter by camera selection and status
- **Detection Control**: Toggle license plate detection in real-time
- **Status Monitoring**: View detection running status
- **FPS Monitoring**: Monitor frames per second for each camera

**Display Layout:**
- Grid view showing all active cameras
- Individual camera cards with video preview
- Real-time detection status indicators
- Quick access controls for each camera

### 3. Traffic Analysis

**Analytical Features:**
- **Density Charts**: Track traffic volume by hour (Line Chart)
- **Vehicle Type Analysis**: Analyze vehicle type distribution (Pie Chart)
- **Dashboard Overview**: Key performance indicators display
- **Time-based Filtering**: Filter data by date range
- **Location Filtering**: Filter by camera location area
- **Report Export**: Export data to Excel format

**Dashboard Metrics:**
- Total vehicles detected
-  Peak traffic hours
-  Growth rate trends
-  Motorcycle ratio
-  Average vehicles per hour
-  Busiest detection days

### 4. Vehicle Information Retrieval

**Search & Filter Capabilities:**
- **License Plate Search**: Search by full or partial plate numbers
- **Vehicle Type Filtering**: Filter by vehicle category
- **Time Range Filtering**: Filter by date and time ranges
- **Detailed View**: View complete information and images
- **Movement History**: Track vehicle movement patterns

---

## System Requirements

### Minimum Hardware
- **CPU**: Intel Core i5 6th gen or higher / AMD Ryzen 5
- **RAM**: 8GB (16GB recommended)
- **GPU**: NVIDIA GTX 1050 or higher (recommended for YOLOv11)
- **Storage**: 10GB free space
- **Network**: Gigabit Ethernet (for camera streaming)

### Software Requirements
| Software | Version | Download Link |
|----------|-----------|----------|
| Windows | 10/11 64-bit | - |
| .NET Framework | 4.7.2+ | [Download](https://dotnet.microsoft.com/download/dotnet-framework) |
| SQL Server | 2019+ / Express | [Download](https://www.microsoft.com/sql-server/sql-server-downloads) |

---

## Installation

### Step 1: Run Installer
1. Download the latest setup file (`Setup.exe`)
2. Run as Administrator
3. Follow the installation wizard steps
4. Choose installation directory
5. Complete installation

### Step 2: Database Setup
1. **Install SQL Server 2019 Express** (if not already installed)
2. **Configure Database:**
   - Run the application
   - Database setup will auto-configure on first run
   - Or manually run `database_setup.sql` if needed

### Step 3: Initial Configuration
1. **Launch Application** from desktop shortcut or start menu
2. **Configure Camera Connections:**
   - Navigate to Camera Management
   - Add camera RTSP URLs
   - Test camera connections
3. **Verify Detection Models:**
   - Models are included in installation
   - Automatic model validation on startup

### Step 4: System Verification
1. **Check System Status** in main dashboard
2. **Test Camera Feeds** in monitoring section
3. **Verify Detection** by enabling plate recognition
4. **Confirm Database Connectivity**

---

## User Guide

### A. Camera Management

#### Adding New Cameras
1. Open **Camera Settings** from sidebar
2. Click **Add New Camera**
3. Fill in camera details:
   - **Camera Name**: Descriptive identifier
   - **RTSP URL**: Camera stream address (e.g., `rtsp://username:password@ip:port/stream`)
   - **Location**: Physical camera location
   - **Status**: Active/Inactive
4. Click **Add** to save

#### Testing Camera Connections
- Use **Test Connection** button
- Verify stream in preview window
- Check for common RTSP format issues

#### Enabling Plate Detection
- Toggle **"Enable Plate Detection"** in camera list
- Or enable from individual camera detail view
- Monitor detection status in real-time

### B. Live Monitoring

#### Viewing Camera Feeds
- Main dashboard shows all active cameras
- Each camera displays:
  - Live video stream
  - Camera name and location
  - FPS counter
  - Detection status indicator

#### Camera Controls
- **Full-screen View**: Double-click camera or use detail button
- **Detection Toggle**: Enable/disable recognition per camera
- **Stream Controls**: Play/pause individual streams

#### Filtering and Search
- **Camera Selection**: Choose specific cameras to display
- **Status Filter**: Show Active/Inactive cameras only
- **Search**: Find cameras by name or location

### C. Traffic Analysis

#### Setting Analysis Parameters
1. **Select Time Range:**
   - From Date: Start of analysis period
   - To Date: End of analysis period
2. **Choose Location:**
   - All locations: System-wide data
   - Specific area: Location-filtered data
3. **Apply Filters** and generate reports

#### Interpreting Dashboard
- **Total Vehicles**: Overall detection count
- **Peak Hours**: Time periods with highest traffic
- **Growth Trends**: Comparison with previous periods
- **Vehicle Distribution**: Percentage by vehicle type

#### Exporting Reports
- Click **Export to Excel**
- Choose save location
- Report includes:
  - Summary statistics
  - Detailed data sheets
  - Chart images

### D. Vehicle Information Search

#### Basic Search
1. Enter license plate number (full or partial)
2. Select vehicle type if needed
3. Set time range for search
4. Click **Search**

#### Advanced Filtering
- **Vehicle Type**: Motorcycle, Car, Bus, Truck, Other
- **Time Range**: Specific date and time periods
- **Location Filter**: Search by camera location

#### Viewing Results
- Results displayed in tabular format
- Double-click entries for detailed view
- Detailed view shows:
  - Captured plate image
  - Complete vehicle information
  - Detection timestamp and location
  - Confidence scores

---

## Troubleshooting

### Common Issues

#### Camera Connection Failures
**Symptoms:**
- Black screen in camera preview
- "Connection failed" messages

**Solutions:**
1. Verify RTSP URL format and credentials
2. Check network connectivity to camera
3. Test URL in VLC media player
4. Ensure camera supports RTSP protocol

#### Plate Detection Not Working
**Symptoms:**
- Detection enabled but no plates recognized
- No database entries being created

**Solutions:**
1. Verify camera stream quality and focus
2. Check detection model files are present
3. Ensure adequate lighting for camera
4. Adjust camera angle and distance

#### Application Performance Issues
**Symptoms:**
- Low FPS on camera streams
- UI lag or freezing
- High CPU/RAM usage

**Solutions:**
1. Reduce number of active detection cameras
2. Lower stream resolution
3. Enable GPU acceleration if available
4. Close other resource-intensive applications

#### Database Connection Problems
**Symptoms:**
- "Database connection failed" errors
- Missing historical data

**Solutions:**
1. Verify SQL Server is running
2. Check database connection settings
3. Ensure sufficient database permissions
4. Verify database file integrity

### System Logs
- Application logs located in `Logs` folder
- Detailed error information for troubleshooting
- Log rotation with date-based files

### Support Resources
- Check `Help > System Information` for detailed status
- Use `Help > Diagnostics` for automated troubleshooting
- Contact support with log files for complex issues

---

## Support & Contact

**Technical Support:**
- Email: vohoanglam2211@gmail.com 

**Documentation:**
- Document: [Document]()
