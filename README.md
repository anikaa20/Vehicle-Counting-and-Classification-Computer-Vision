# Vehicle-Counting-and-Classification-Computer-Vision


This project uses YOLO object detection and tracking to count vehicles crossing a defined line in a video. It leverages the [Ultralytics YOLO](https://github.com/ultralytics/ultralytics) model and OpenCV for real-time video processing and visualization.

## Features

- Detects and tracks vehicles in a video using a YOLO model.
- Counts vehicles by class as they cross a specified line.
- Displays bounding boxes, class names, and unique IDs for each detected vehicle.
- Real-time visualization with OpenCV.

## Requirements

- Python 3.8+
- [Ultralytics YOLO](https://docs.ultralytics.com/)
- OpenCV (`opencv-python`)
- PyTorch (required by YOLO)

Install dependencies with:

```sh
pip install ultralytics opencv-python torch
```

## Usage

1. Place your YOLO model weights (e.g., yolo11l.pt) and video file (e.g., test_video.mp4) in the project directory.
2. Update the video path in Vehicle tracking and counting.py by replacing the line:
   ```python
   cap = cv2.VideoCapture(r" ")
   ```
   with:
   ```python
   cap = cv2.VideoCapture(r"test_video.mp4")
   ```
3. Run the script:
   ```sh
   python "Vehicle tracking and counting.py"
   ```
4. Press `q` to exit the video window.

## Customization

- **Model Weights:** Change the model file in `YOLO("yolo11l.pt")` to use a different YOLO weights file.
- **Classes:** The script tracks classes `[1,2,3,5,6,7]` by default. Adjust the `classes` parameter in `model.track()` as needed.
- **Line Position:** Modify `line_y_red` to change the counting line's vertical position.

## Output

- The script displays a video window with detected vehicles, their IDs, and a red counting line.
- Vehicle counts by class are stored in the `class_counts` dictionary.

## License

This project is for educational purposes. Refer to the YOLO and Ultralytics licenses for model and library usage.

