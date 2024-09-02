### 1. Segmentation

Image segmentation breaks down an image into smaller regions to make analysis easier. A common method to achieve this is through the K-means clustering algorithm, which groups pixels with similar properties. In this context, if a pixel is closer to the center of a cluster (representing tumor areas), it may be classified as part of the tumor; otherwise, the comparison continues till a decision is reached. Additionally, the Watershed segmentation technique is mentioned, which helps group pixels based on similar intensity levels.
### 2. Feature Decomposition

To efficiently process large images, they are decomposed into smaller sections using the 2D Discrete Wavelet Transform (2D DWT). This method splits the image into four parts known as sub-bands, including approximations and detailed information. This approach simplifies subsequent processing and reduces computation time.

### 3. Feature Reduction - (improves efficiency)

To streamline the analysis, feature reduction is performed through a method called Principal Component Analysis (PCA). This technique reduces the number of features while retaining the most important information, thus speeding up processing and improving efficiency.

### 4. Texture Analysis

Texture analysis examines the detailed patterns within the images, specifically using techniques like the Gray Level Co-occurrence Matrix (GLCM). This method analyzes textural features that can help in distinguishing tumor types and consist of calculating various metrics that describe the image's texture.

### 5. Classification

Tumors are classified using an algorithm called Support Vector Machine (SVM). This method aims to find the best way to separate tumor types (either benign or malignant) using various mathematical functions called kernels (like linear, polynomial, and RBF). The effectiveness of the classifier can be measured through terms such as true positive (correctly identified tumor), false positive (normal tissue misclassified as tumor), and others.