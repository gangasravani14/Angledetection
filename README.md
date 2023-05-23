# Angledetection
Title: Angle Detection Using Computer Vision and OpenCV

* **Introduction:**

This project focuses on developing a system for angle detection

using computer vision techniques and the OpenCV library. By

leveraging image processing algorithms and OpenCV's functionality,

the system aims to accurately detect angles in various applications,

such as robotics, object recognition, and image analysis.

* **Problem Statement:**

The project aims to address the challenge of accurately detecting

angles in images using computer vision techniques. This involves

identifying the presence of angles, determining their magnitude, and

visualizing the results for interpretation and analysis.

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

high degree of accuracy. Experimental evaluation and testing on

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
**Team members**
1. Ganga sravani
2. Almas bhanu
3. Akshay kumar
4. Mallikarjuna
5. Syra bhanu
6. Anitha rani
7. Chandralekha
