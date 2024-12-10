# dip_project_sujanateam
"This project implements edge detection and object segmentation using Python and MATLAB."
Image Edge Detection and Object Segmentation Using Python and MATLAB
Table of Contents
Introduction
Dataset : https://www.kaggle.com/datasets/prasunroy/natural-images

Methodology
Python Implementation
MATLAB Implementation
Metrics and Results
Comparison Between Python and MATLAB
Challenges and Learnings
Conclusion and Future Work
How to Run the Code
Introduction
This project implements edge detection and object segmentation using two different platforms, Python and MATLAB, to analyze and compare their performance. The primary objective is to:

Detect edges in images using the Canny Edge Detection Algorithm.
Segment objects from edge-detected images using contours and connected regions.
Evaluate results using metrics such as Edge Density, Mean Gradient Magnitude, Number of Objects, and Average Object Size. The project showcases the advantages and limitations of Python and MATLAB for computer vision tasks, providing insights into their capabilities in handling edge detection and segmentation workflows.
Dataset
Name: Natural Images Dataset
Source: Public dataset repository.
Size: 6,899 images.
Categories: Airplanes, Cars, People, Flowers, and Buildings.
Preprocessing:
All images were converted to grayscale to standardize edge detection.
A subset of 5 images was used for testing and visualization.
Purpose: The dataset's diversity makes it ideal for evaluating edge detection and segmentation performance across different object types.
Methodology
Python Implementation
Edge Detection:
Used OpenCV’s cv2.Canny() for Canny Edge Detection.
Calculated metrics:
Edge Density: Ratio of edge pixels to total pixels.
Mean Gradient Magnitude: Computed using Sobel filters (cv2.Sobel()).
Object Segmentation:
Extracted contours using cv2.findContours().
Filtered small contours to remove noise.
Visualized segmented objects by overlaying green contours on the original images.
Metrics calculated:
Number of Objects.
Average Object Size.
MATLAB Implementation
Edge Detection:
Used the edge() function for Canny Edge Detection.
Calculated metrics:
Edge Density: Ratio of edge pixels.
Mean Gradient Magnitude: Computed using Sobel gradients (imgradientxy).
Object Segmentation:
Used bwconncomp() to identify connected components in edge-detected images.
Visualized segmented objects with green contours overlaid on the original images.
Metrics calculated:
Number of Objects.
Average Object Size.
Metrics and Results
Edge Detection Metrics:
Edge Density: Quantifies the prominence of edges.
Mean Gradient Magnitude: Measures average gradient intensity.
Segmentation Metrics:
Number of Objects: Total objects segmented.
Average Object Size: Mean area of segmented objects.
Sample Results (Python):

Image Name	Edge Density	Mean Gradient Magnitude	Number of Objects	Average Object Size
airplane_0000.jpg	0.0403	43.2911	54	324.40
airplane_0001.jpg	0.0385	44.5143	46	182.50
Sample Results (MATLAB):

Image Name	Edge Density	Mean Gradient Magnitude	Number of Objects	Average Object Size
airplane_0000.jpg	0.0398	42.8912	52	310.20
airplane_0001.jpg	0.0379	44.3215	45	178.90
Comparison Between Python and MATLAB
Aspect	Python	MATLAB
Edge Detection	Flexible, customizable thresholds and tuning.	Fast implementation with built-in functions.
Object Segmentation	Detected finer details with contour filtering.	Clean segmentation with built-in metrics.
Performance	Handles large datasets effectively.	Ideal for rapid prototyping.
Visualization	Requires additional libraries (e.g., Matplotlib).	Integrated visualization tools.
Challenges and Learnings
Challenges:
Handling large datasets in MATLAB Online due to storage limits.
Tuning thresholds for Canny Edge Detection to optimize results.
Filtering noise during object segmentation while preserving meaningful details.
Learnings:
Python offers high flexibility and scalability for custom workflows.
MATLAB simplifies implementation with robust pre-built functions.
Edge detection and segmentation heavily depend on preprocessing steps like grayscale conversion and noise removal.
Conclusion and Future Work
Conclusion:
The project successfully implemented and compared edge detection and object segmentation using Python and MATLAB.
Python provided flexibility for customizations, while MATLAB offered efficient built-in functions for rapid prototyping.
Metrics calculated validated the accuracy and efficiency of both implementations.
Future Work:
Extend the methodology to handle colored images and video streams.
Explore deep learning-based segmentation techniques, such as Mask R-CNN.
Optimize implementations for real-time applications.
How to Run the Code
