# Analysis of the “Fast Robust Automated Brain Extraction” Algorithm

## Overview

This project provides a comprehensive analysis of the "Fast Robust Automated Brain Extraction" (BET) algorithm, developed at Oxford. The BET algorithm is designed to perform brain extraction from MRI images, a crucial step in neuroimaging analysis.

The algorithm operates through several key steps:
1. **Intensity Histogram Analysis**: Processes the intensity histogram of the input image to determine robust lower and upper intensity values, establishing a rough brain/non-brain threshold.
2. **Center of Gravity and Head Size Estimation**: Calculates the center of gravity of the head in the image and estimates the rough size of the head.
3. **Surface Initialization and Deformation**: Initializes a triangular tessellation of a sphere's surface within the brain and iteratively deforms this surface, vertex by vertex. The deformation is guided by forces that maintain surface spacing and smoothness, while progressing towards the brain's edge.
4. **Surface Refinement**: If the initial deformation does not yield a clean separation between brain and non-brain regions, the process is repeated with increased smoothness constraints.
5. **Optional Skull Surface Estimation**: The algorithm can also estimate the outer surface of the skull if needed.

The project dissects each step of the algorithm, analyzing its computational flow, implementation details, and effectiveness in brain extraction. It also provides suggestions for potential optimizations to improve performance, particularly for handling larger datasets or time-sensitive applications.

## Background

I was highly intrigued by the field of brain research, particularly in image processing. This fascination led me to further explore and analyze the techniques used in neuroimaging. Additionally, I sought to improve my programming skills in C and C++, honed during my university studies, by examining the BET algorithm's implementation. This project was a great opportunity to adopt better programming practices while gaining a deeper understanding of existing approaches in brain extraction.
