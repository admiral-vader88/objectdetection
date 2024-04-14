# Object Detection Using Python
Object Detection: Python script uses OpenCV and the Ultralytics YOLO (You Only Look Once) object detection model to perform real-time object detection using a webcam feed. Here's a breakdown of the key components and the functionality of the code:

1. **Imports and Setup**:
   - `cv2` for OpenCV functionalities, used for capturing video from the webcam and displaying the output.
   - `YOLO` from the `ultralytics` library, which is a pre-trained object detection model.
   - `math` for mathematical calculations, specifically used here to format the confidence score.

2. **Webcam Configuration**:
   - The script initializes the webcam and sets its resolution to 640x480 pixels.

3. **Load YOLO Model**:
   - The YOLO object detection model (`yolov8n.pt`) is loaded from a specified directory. This model can detect multiple object classes.

4. **Object Classes**:
   - A list of class names represents the types of objects the model can detect, ranging from people and vehicles to everyday items like food and furniture.

5. **Detection Loop**:
   - An infinite loop (`while True`) continuously captures frames from the webcam.
   - Each frame is processed by the YOLO model to detect objects. For each detected object, the model provides bounding boxes (coordinates), confidence scores, and class identifiers.
   - For each detected object:
     - The bounding box is drawn on the frame.
     - The confidence score (formatted to two decimal places) and the class name of the object are printed to the console and displayed on the frame using `cv2.putText`.

6. **Display and Exit**:
   - The processed frame (with bounding boxes and labels) is displayed in a window titled 'Webcam'.
   - The loop can be exited by pressing 'q', which also releases the webcam and closes all OpenCV windows.

Overall, this script is designed for real-time visualization and identification of objects using a webcam, utilizing the power of deep learning through YOLO for object detection.
