# CUDAatScaleForTheEnterpriseCourseProjectTemplate
OVERVIEW
This assignment focuses on Image Processing, specifically using Median Filtering and Canny Edge Detection techniques. These methods are implemented using NVIDIA's NPP (NVIDIA Performance Primitives) library to harness GPU acceleration for efficient image processing.

Folder Structure:
medianFilterCannyEdgeNPP: This is the main directory containing the primary code file, medianFilterCannyEdgeNPP.cpp, which implements both algorithms, along with the Makefile.
cmu_face_images: This directory contains the original CMU FACE IMAGES dataset, organized into 20 subfolders, each with 32 images, representing 20 different individuals.
cmu_face_medianFilter: This is the output directory where the images processed with the Median Filter are stored.
cmu_face_cannyedge: This is the output directory where the images processed with Canny Edge Detection are stored.
run.sh: A script included in the folder to facilitate running the code.
This structure ensures clear organization and efficient processing of the image dataset using GPU-accelerated techniques.

Dataset
For the assignment I have used the CMU FACE IMAGES Dataset(https://www.cs.cmu.edu/afs/cs.cmu.edu/project/theo-8/faceimages/faces/). This is one of the datasets mentioned in the Instructions. The images in this dataset are in PGM format, which is similar to the format given in the NPP Box Filtering Laboratory.

Techniques Used
Median Filter: Reduces noise in images by replacing each pixel with the median value from a surrounding window of pixels. I have used this algorithm as it is one of the altenative methods to box filtering.
Canny Edge Detection: It identifies edges in images using a multi-stage algorithm involving noise reduction, gradient calculation, non-maximum suppression, and edge tracking by hysteresis. I have used this algorithm for finding edge detection in the input images.

Requirements
CUDA Toolkit
NPP Library
C++ Compiler
Makefile

Code Workflow
Following the NVIDIA documentation, the code starts by defining a function for Median Filtering, which blurs the images. Next, a function for Canny Edge Detection is written to identify the edges of faces and surrounding areas. These functions are invoked in the main function to process the images and generate the output folders. The file medianFilterCannyEdgeNPP.cpp includes comments explaining the code. To use a different dataset, simply update the input and output folder paths in medianFilterCannyEdgeNPP.cpp to obtain the desired results.

How to View the Results

You can view the output images by either install an application like Bitberry File Opener or simply viewing on some PGM file viewer website.
