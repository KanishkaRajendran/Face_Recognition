# Face and Body Detection with YOLOv5 and OpenCV

This project performs face and body detection on a given input video. It uses YOLOv5 for person detection, OpenCV's deep learning module for face detection (SSD model), and Haar Cascade for profile face detection. The detected faces and persons are highlighted with bounding boxes.

## Features

- **Person Detection**: Detects persons using the YOLOv5 model.
- **Face Detection**: Detects frontal and profile faces using OpenCV’s pre-trained Caffe model and Haar Cascade.
- **ID Tracking**: Tracks persons across frames and assigns unique IDs.
- **Benchmarking**: Measures FPS, CPU usage, and memory usage throughout the video processing.
- **Video Output**: Saves the processed video with detections in MP4 format.

## Requirements

1. Python 3.x
2. `torch` (PyTorch)
3. `opencv-python`
4. `numpy`
5. `psutil`
6. `google.colab`

To install dependencies, run:
```bash
pip install torch opencv-python numpy psutil
```

## Files

- `deploy.prototxt`: [GitHub Link](https://github.com/KanishkaRajendran/Face_Recognition/blob/main/deploy.prototxt)
- `res10_300x300_ssd_iter_140000.caffemodel`: [GitHub Link](https://github.com/KanishkaRajendran/Face_Recognition/blob/main/res10_300x300_ssd_iter_140000.caffemodel)

## Input Video

- [Download Input Video](https://drive.google.com/file/d/1d5vAR35Xx9bzTax4Lm9DelhDvTiNINNb/view?usp=drive_link)

## Demo Output

- [View Demo Output Video](https://drive.google.com/file/d/1zrXFVVAjnQDYgFcgKutTeAptSrlpe9eF/view?usp=drive_link)

## How It Works

1. **Load Models**:
   - YOLOv5 (for person detection)
   - OpenCV face detection using Caffe's SSD model
   - Profile face detection using Haar Cascade

2. **Video Processing**:
   - Read video frames using OpenCV.
   - Run YOLOv5 for person detection and draw bounding boxes.
   - Use Caffe model to detect frontal faces and Haar Cascade for profile faces.
   - Assign a unique ID to each person and track them across frames.

3. **Resource Usage Monitoring**:
   - Measure and print FPS, CPU usage, and memory usage during the video processing.

4. **Save Output**: 
   - Save the processed video with detected faces and persons into an output file.

## Benchmark Report

After processing, a benchmark report will be displayed with:
- Average FPS
- Minimum and Maximum FPS
- Standard Deviation of FPS
- Average CPU usage
- Average memory usage

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/face-body-detection.git
   cd face-body-detection
   ```

2. Download the required models and place them in the repository.
   - `deploy.prototxt`
   - `res10_300x300_ssd_iter_140000.caffemodel`

3. Run the Python script:
   ```bash
   python face_body_detection.py
   ```

4. Check the output video and benchmark report in the terminal.

## Notes

- The input video can be changed by updating the `input_video_path`.
- The output video will be saved as `output_faces_and_bodies.mp4`.
