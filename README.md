# Angledetection

This project was developed during a 24 hour hackathon at RGMCET conducted by BYTS INDIA(BYTS HACKLEAGUE 1.0)

 * **Title:**
Angle detection between two flat objects Using Computer Vision and OpenCV

* **Introduction:**

This project focuses on developing a system for angle detection using computer vision techniques and the OpenCV library. By
leveraging image processing algorithms and OpenCV's functionality,
the system aims to accurately detect angles in various applications,
such as robotics, object recognition, and image analysis.

* **Problem Statement:**

The project aims to address the challenge of accurately detecting
angles in images using computer vision techniques. This involves
identifying the presence of angles, determining their magnitude, and
visualizing the results for interpretation and analysis.

* **Installation**

1.Set up the Development Environment:

a. Install visual code editor. 
b. Install Python: Ensure that Python is installed on your system. You can download and install Python from the official Python website (https://www.python.org) based on your operating system.
c. Install OpenCV: Install the OpenCV library using pip, the Python package installer. Open a command prompt or terminal and run the following command: pip install opencv-python.


1.Download the Project Files:

 Obtain the project files containing the code and resources for the angle detection system. This could be from a Git repository or a provided project archive.

1.Install Required Dependencies:

a. Navigate to the project directory in the command prompt or terminal.
b.Install any additional dependencies or libraries required by the project. These dependencies may vary depending on the specific implementation. Typically, they can be installed using pip by running the command: pip install -r requirements.txt (if a requirements.txt file is provided).

1.Run the Angle Detection System:

a. Execute the main script or application to run the angle detection system. This could be a Python script (e.g., main.py) or an executable file, depending on the project structure.
b.If needed, pass any required arguments or parameters to the script, such as the input image or video source.

1.Interact with the Angle Detection System:

Once the angle detection system is running, interact with it based on its specific functionality and user interface. This could involve capturing images or video frames, processing them, and displaying the detected angles.


* **Methodology:**

The proposed methodology for angle detection involves the
following steps:

a. Image Acquisition: The system captures images using a camera
or webcam, utilizing OpenCV's video capturing capabilities.

b. Preprocessing: The acquired images undergo preprocessing
techniques to enhance quality and improve angle detection
accuracy. This includes resizing, denoising, and applying suitable
image filters like Gaussian or median filters.

c. Edge Detection: The Canny edge detection algorithm is applied to
the preprocessed images. This algorithm identifies significant
changes in pixel intensity, highlighting the edges.

d. Contour Extraction: OpenCV's contour detection algorithms are
utilized to extract contours from the edge-detected images.
Contours represent the boundary lines of objects within the image.

e. Line Fitting: The project employs the Hough Line Transform
algorithm provided by OpenCV to fit lines to the extracted contours.
This algorithm detects and parameterizes lines within the image,
enabling the identification of angular structures.

f. Angle Calculation: Using the parameters of the detected lines, the
system calculates the angles between them. This can be achieved
using trigonometric functions like atan2() or by leveraging
geometric properties of intersecting lines.

g. Visualization and Output: The detected angles are visualized by
overlaying them on the original image. This provides a clear
representation of the presence and magnitude of each angle, aiding
interpretation and analysis.

* **Results and Discussion:**

The system successfully detects angles in various images with a
high degree of accuracy. 

Experimental evaluation and testing on
different datasets show reliable angle detection performance. The
system is capable of handling real-time angle detection applications
and provides visually interpretable results for further analysis.

* **Conclusion:**

In conclusion, the developed system effectively detects angles in
images using computer vision techniques and the OpenCV library.

By leveraging edge detection, contour extraction, line fitting, and
angle calculation algorithms, the system achieves accurate angle
detection, making it a valuable tool for applications requiring angle
analysis and recognition.

* **Applications:**

1.Robotics
1.Manufacturing and Quality Control
1.Construction and Architecture
1.Image Analysis and Object Recognition
1.Geometric Measurements and Surveying
1.Augmented Reality and Virtual Reality
1.Medical Imaging

* **Future work**

some potential areas for future work. 
1.Improved Angle Calculation Methods
1.Calibration and Accuracy Enhancement
1.Real-time Performance Optimization
1.Angle Tracking and Dynamic Analysis
1.Integration with Robotics and Automation
1.Integration with Other Computer Vision Techniques

**Team members**
1. Ganga sravani
2. Almas bhanu
3. Akshay kumar
4. Mallikarjuna
5. Syra bhanu
6. Anitha rani
7. Chandralekha

*For any queries contact **gangasravani12@gmail.com**
