# Computer_Vision-Virtual-Drag-and-Drop

This Python script uses OpenCV and Computer Vision Zone (cvzone) to create a real-time application where draggable rectangles can be controlled using hand gestures. The hand landmarks are detected using a hand tracking module, and the movement of the index finger is used to drag and move the rectangles.

## Prerequisites

Before running the script, ensure that you have the following dependencies installed:

- Python 3.x
- OpenCV (`cv2`)
- Computer Vision Zone (`cvzone`)
- NumPy (`numpy`)

You can install the required packages using pip:
pip install opencv-python cvzone numpy

Additionally, you need to have a webcam or camera connected to your system.

## Usage

1. Clone or download the repository containing the script and the `handTrackingModule.py` file.
2. Open a terminal or command prompt and navigate to the project directory.
3. Run the script with the following command:<br>
python main.py
4. The script will open a window displaying the camera feed.
5. Bring your hand into the camera's view, and the script will automatically detect and track your hand.
6. To drag a rectangle, move your index finger inside the rectangle's boundaries.
7. The rectangle will follow the movement of your index finger as long as it remains inside the rectangle.
8. Multiple rectangles can be dragged simultaneously by moving your index finger across different rectangles.
9. Press 'q' or close the window to exit the script.

## Code Overview

The code consists of the following main components:

1. **Importing necessary libraries**: OpenCV (`cv2`), hand tracking module (`handTrackingModule`), cvzone, and NumPy.
2. **Setting up the camera**: The script initializes the webcam and sets the desired resolution.
3. **Hand detection**: An instance of the hand detector class is created using the `handTrackingModule`.
4. **DragRect class**: This class represents a draggable rectangle. It has methods to initialize the rectangle's position and size, and update its position based on the cursor (index finger) location.
5. **Main loop**: The script enters a continuous loop where it reads frames from the camera, detects hand landmarks, and updates the positions of the rectangles based on the index finger's location.
6. **Drawing rectangles**: The script creates semi-transparent rectangles on a new image layer and blends it with the original camera feed using OpenCV's `addWeighted` function.
7. **Display and exit**: The final output is displayed in a window, and the script waits for the user to press 'q' or close the window to exit.

## Customization

You can customize various aspects of the script, such as the number of rectangles, their initial positions, sizes, colors, and transparency levels. Modify the values in the respective sections of the code to suit your preferences.

## Acknowledgments

This script utilizes the following libraries and modules:

- OpenCV (`cv2`): Open-Source Computer Vision Library
- Computer Vision Zone (`cvzone`): Computer Vision Utils
- NumPy (`numpy`): Numerical Python Library
- `handTrackingModule`: Custom hand tracking module
