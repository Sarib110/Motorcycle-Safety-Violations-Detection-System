# Motorcycle-Safety-Violations-Detection-System

This repository contains a Python-based application designed to detect and document traffic violations using machine learning models. The system processes video footage to identify various traffic violations involving motorcyclists, such as helmet usage, lane discipline, triple riding, mobile usage, and one-wheeling. It also extracts license plate numbers for further action.

## Features

- **Detection of Traffic Violations**:
  - Helmet usage
  - Lane discipline
  - Triple riding (more than two riders)
  - Mobile usage while riding
  - One-wheeling
- **License Plate Recognition**:
  - Extracts and validates license plate numbers using OCR.
- **Violation Documentation**:
  - Saves evidence images of violations with annotated detections.
  - Categorizes violations with timestamps and license plate numbers (if available).

## System Requirements

- Python 3.8 or later
- Required Libraries: 
  - `opencv-python`
  - `pillow`
  - `tqdm`
  - `python-decouple`
  - `requests`
  - `inference_sdk` (InferenceHTTPClient for machine learning models)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Sarib110/Motorcycle-Safety-Violations-Detection-System
   cd Motorcycle-Safety-Violations-Detection-System
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Configure environment variables:
   - Create a `.env` file in the project root.
   - Add the following keys with your credentials:
     ```env
     ROBOFLOW_API_KEY=your_roboflow_api_key
     OCR_SPACE_API=your_ocr_space_api_key
     ```

4. Place your input video in the project directory with the name `input3.mp4` (or update the code to use your video file).

## Usage

1. Run the application:
   ```bash
   python traffic_violation.py
   ```

2. The system processes the input video and saves the violation evidence in a folder named `Violations/<date>` and also print the violation.

## Folder Structure

- **Violations**: Contains subfolders for each violation date. 
  - Each violation folder includes:
    - Annotated motorcycle images
    - License plate images (if detected)
    - Text file with license plate numbers

## Models and APIs Used

- **Roboflow API**: For object detection models.
  - Helmet detection
  - Face detection
  - Lane detection
  - Mobile and one-wheeling detection
- **OCR Space API**: For extracting license plate numbers from images.

---

**Note:** Ensure compliance with local data privacy and traffic regulations before deploying this system.
```
