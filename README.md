# Face-Recognition-System-Using-OpenCV-and-Tkinter
Simple face recognition system built with OpenCV for face detection and recognition, and Tkinter for the graphical user interface (GUI). It detects and recognizes faces from a live camera feed or uploaded images, allowing users to train the system with new faces.

## Features
Detect and recognize faces from a live video feed.
Pre-trained on a set of known faces from image files.
Ability to add new faces to the system via image upload.
Display live camera feed in the GUI and highlight recognized faces.
Confidence level displayed alongside each recognized face.

## Prerequisites
Before running the program, make sure you have the following installed:
Python 3.x
OpenCV
NumPy
Pillow (PIL)
Scikit-learn (for normalization)
Tkinter (usually pre-installed with Python)
You can install the necessary dependencies using pip:

### pip install opencv-python numpy Pillow scikit-learn
# How to Use
1. Clone the Repository
First, clone the repository to your local machine:
### git clone https://github.com/your-username/face-recognition-system.git
### cd face-recognition-system
2. Prepare the Dataset
Place the images of the known faces inside the project folder. The images should be named r1.jpg, r2.jpg, etc. Ensure they are front-facing images with clear visibility of the face. These images will be used to train the face recognizer.

The corresponding labels (names) for these images are stored in the list mnx in the script. You can modify this list to reflect the actual names of the individuals in the images.

3. Running the Program
Run the Python script:

 ### python face_recognition.py
This will open up the GUI where you can:

Start Camera: Start the live camera feed for face recognition.
Stop Camera: Stop the camera feed.
Upload Image: Upload a new image to add to the system.
4. Upload New Faces
To upload a new image and add a new face to the recognition system:

Click the "Upload Image" button in the GUI.
Select an image from your local machine.
The system will detect faces in the image and add them to the training data.
5. Training Process
Once you upload new images or start the camera, the system will train the recognizer using the Local Binary Patterns Histograms (LBPH) method on the detected faces. The system will predict the face labels and display the corresponding name or "Not Matched" if the confidence level is too low.

## How It Works
Face Detection: The program uses OpenCV’s Haar Cascade Classifier to detect faces in the camera feed or uploaded images.
Face Recognition: After detecting faces, it uses the Local Binary Patterns Histograms (LBPH) algorithm for face recognition.
Adding New Faces: New faces can be uploaded and added to the training set, allowing the system to improve over time.
## Improvements
Adjust the confidence threshold in the code to tweak the stringency of recognition.
Add more images to the dataset for better accuracy.
Use more advanced face recognition models such as deep learning-based methods for improved performance.
